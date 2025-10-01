# Feature Guide - Player Management - Equipment System

## Overview
The Equipment System is a core system where players can equip weapons, armor, accessories, and other items to enhance their stats. Each equipment piece has unique stats and special effects that directly impact the player's combat power and survivability.

## Equipment Types

### Weapons
- **Pickaxe**: Improves mining efficiency
- **Sword**: Increases combat attack power
- **Staff**: Enhances magical abilities
- **Bow**: Provides ranged attack capabilities

### Armor
- **Helmet**: Head protection, increases defense
- **Chest Armor**: Torso protection, increases health  
- **Leggings**: Leg protection, improves movement speed
- **Gloves**: Hand protection, increases mining speed

### Accessories
- **Necklace**: Grants special abilities
- **Ring**: Provides stat bonuses
- **Earrings**: Increases experience gain

### Other Equipment
- **Backpack**: Expands inventory slots
- **Boots**: Improves movement speed and jump power

## Related File Paths

### Equipment System Scripts
```
RootDesk/MyDesk/Components/Player/Equipment/
├── EquipmentUI.mlua                        # Equipment window UI management
├── EquipmentUI.codeblock                   # Equipment UI visual scripting
├── EquipmentUISlotButton.mlua              # Equipment slot button handling
├── EquipmentUISlotButton.codeblock         # Equipment slot visual
├── PlayerEquipmentManager.mlua             # Player equipment state management
└── PlayerEquipmentManager.codeblock        # Equipment manager visual
```

### Equipment Image Resources
```
RootDesk/MyDesk/Images/장비/
├── 무기/                                   # Weapon sprites
│   ├── 곡괭이_1티어.sprite
│   ├── 곡괭이_2티어.sprite
│   └── ... (40 weapon sprites)
├── 옷/                                     # Armor sprites  
│   ├── 상의_1티어.sprite
│   ├── 상의_2티어.sprite
│   └── ... (40 armor sprites)
├── 신발/                                   # Boot sprites
│   └── ... (40 boot sprites)
└── 가방/                                   # Backpack sprites
    └── ... (40 backpack sprites)
```

### Equipment Data Files
```
RootDesk/MyDesk/DataSets/
├── EquipmentData.csv                       # Equipment basic information
├── EquipmentData.userdataset              # Equipment dataset
├── WeaponData.csv                         # Weapon detailed data
├── ArmorData.csv                          # Armor detailed data
└── AccessoryData.csv                      # Accessory detailed data
```

### UI Group Files
- `ui/EquipmentStorageGroup.ui`: Equipment storage UI group

## Equipment System Implementation Details

### Equipment Equip/Unequip Logic
```lua
-- Core logic implemented in EquipmentUI.mlua

method void EquipItem(string itemId)
    -- 1. Check currently equipped item
    local currentEquip = self:GetEquippedItem(slot)
    
    -- 2. Move current equipment to inventory if exists
    if currentEquip then
        InventoryManager:AddItem(currentEquip)
    end
    
    -- 3. Equip new item
    self:SetEquippedItem(slot, itemId)
    
    -- 4. Recalculate stats
    self:RecalculateStats()
    
    -- 5. Update UI
    self:UpdateEquipmentUI()
end
```

### Stat Calculation
```lua
-- Stat calculation in PlayerEquipmentManager.mlua

method table CalculateTotalStats()
    local totalStats = {}
    
    -- Iterate through each equipment slot
    for slotType, equipment in pairs(self.equippedItems) do
        local equipStats = EquipmentData:GetStats(equipment.id)
        
        -- Sum up stats
        for statName, value in pairs(equipStats) do
            totalStats[statName] = (totalStats[statName] or 0) + value
        end
    end
    
    return totalStats
end
```

### Equipment Enhancement System
```lua
-- Stat increase based on equipment enhancement level

method number GetEnhancedStatValue(number baseValue, number enhanceLevel)
    local multiplier = 1 + (enhanceLevel * 0.1) -- 10% increase per level
    return math.floor(baseValue * multiplier)
end
```

## Equipment Grade System

### Grade-based Properties
1. **Common**: White, base stats
2. **Uncommon**: Green, +20% stats
3. **Rare**: Blue, +50% stats, 1 special option
4. **Epic**: Purple, +100% stats, 2 special options  
5. **Legendary**: Orange, +200% stats, 3 special options

### Grade Color Handling
```
RootDesk/MyDesk/Material/GradeColor/
├── grade_common.material                   # Common grade color
├── grade_uncommon.material                 # Uncommon grade color
├── grade_rare.material                     # Rare grade color
└── grade_legendary.material                # Legendary grade color
```

## Equipment Acquisition Methods

### Shop Purchase
- Purchase from equipment shop with gold
- Purchase from gem shop with premium currency

### Drop Acquisition  
- Drops from monster kills during mine exploration
- Acquired from treasure boxes
- Special event rewards

### Crafting System
- Craft by combining material items
- Random options applied during crafting

## Storage and Synchronization

### Equipment Data Storage Structure
```lua
PlayerEquipmentData = {
    equipped = {
        weapon = { id = "sword_001", enhanceLevel = 5 },
        armor = { id = "plate_001", enhanceLevel = 3 },
        accessory = { id = "ring_001", enhanceLevel = 1 }
    },
    storage = {
        -- List of stored equipment
    }
}
```

### Synchronization Through TableSync
- Synchronize equipment state with server through `TableSync.mlua`
- Real-time reflection of equipment changes

## Extension Methods

### Adding New Equipment Types
1. Add new equipment information to `EquipmentData.csv`
2. Add corresponding equipment sprites
3. Add new slot handling logic to `EquipmentUI.mlua`
4. Add new slots to UI

### Adding Equipment Set System
1. Define equipment set data
2. Implement set effect calculation logic
3. Add set effect display feature to UI
