# Development Guide - Asset Management - Model and Image Management

## Overview
This guide covers asset management for 3D models, images, and atlases in the Miner Simulator project.

## Asset Folder Structure

### Model Files
```
RootDesk/MyDesk/Models/
├── Guide_Key/              # Guide key models
├── Items/                  # Item models
├── Mine/                   # Mine object models
├── NPCs/                   # NPC models
├── Players/                # Player models
├── Traps/                  # Trap models
└── MapObjects/             # Map objects
```

### Image Files
```
RootDesk/MyDesk/Images/
├── UI/                     # UI images
├── Equipment/              # Equipment icons
│   ├── Bags/               # Bag icons
│   ├── Weapons/            # Weapon icons  
│   ├── Shoes/              # Shoe icons
│   └── Clothes/            # Clothing icons
├── Ore Veins/              # Ore vein images
└── Chair Resources/        # Chair images
```

### Atlas Files
```
RootDesk/MyDesk/Atlas/
├── common.blueprintatlas        # Common atlas
├── common2.blueprintatlas       # Common atlas 2
├── icon.blueprintatlas          # Icon atlas
└── ui.blueprintatlas           # UI atlas
```

## Asset Usage Methods

### Model Spawning
```lua
-- Spawn model
local spawnPos = Vector3(0, 1, 0)
local spawnedModel = _SpawnService:SpawnByModelId(
    "model://model_uuid_here", 
    "SpawnedObjectName", 
    spawnPos, 
    parentEntity)
```

### Image Setup
```lua
-- Set image to SpriteGUIRenderer
local imageComponent = entity.SpriteGUIRendererComponent
imageComponent.ImageRUID = "image_uuid_here"

-- Use image from atlas
local atlasSprite = entity.AtlasSpriteComponent
atlasSprite.AtlasRUID = "atlas_uuid_here"
atlasSprite.SpriteName = "sprite_name_in_atlas"
```

### Dynamic Asset Loading
```lua
method void LoadAssetDynamically(string assetType, number itemId)
    local assetTable = _DataService:GetTable(assetType)
    local assetRUID = assetTable:GetCell(itemId, "AssetRUID")
    
    if assetRUID and assetRUID ~= "" then
        -- For images
        if assetType == "ItemIcon" then
            self.Entity.SpriteGUIRendererComponent.ImageRUID = assetRUID
        -- For models  
        elseif assetType == "ItemModel" then
            local model = _SpawnService:SpawnByModelId(
                "model://" .. assetRUID, 
                "DynamicModel", 
                self.Entity.Transform.Position)
        end
    end
end
```

## Asset Optimization

### Memory Management
```lua
-- Unload unused assets
method void UnloadUnusedAssets()
    local unusedModels = self:GetUnusedModels()
    
    for _, model in ipairs(unusedModels) do
        model:Destroy()
    end
    
    -- Clear texture cache
    _ResourceManager:ClearTextureCache()
end
```

### LOD (Level of Detail)
```lua
-- Adjust model quality based on distance
method void UpdateModelLOD(Entity model, number distance)
    if distance > 50 then
        model.ModelComponent:SetLODLevel(0)  -- Low quality
    elseif distance > 20 then
        model.ModelComponent:SetLODLevel(1)  -- Medium quality  
    else
        model.ModelComponent:SetLODLevel(2)  -- High quality
    end
end
```

