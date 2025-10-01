# Core Architecture - Game System - Player System

## Overview
The Player System is the core system of Mine Simulator that manages the player character's state, equipment, inventory, and progress. This system consists of multiple sub-systems, each operating independently while being organically interconnected.

## Player System Structure

### Main Components
- **Equipment System**: Weapon, armor, accessory management
- **Inventory System**: Item storage and management
- **Collection System**: Collectibles and collection book management  
- **Pet System**: Companion pet management
- **Construction System**: Structure building and placement
- **Title System**: Player title management
- **Emblem System**: Emblem attachment and effects
- **Emoticon System**: Emotion expression system

## Related File Paths

### Player Component Scripts
```
RootDesk/MyDesk/Components/Player/
├── Equipment/
│   ├── EquipmentUI.mlua                    # Equipment UI management
│   ├── EquipmentUISlotButton.mlua          # Equipment slot button
│   ├── EquipmentStorage.mlua               # Equipment storage
│   └── PlayerEquipmentManager.mlua         # Equipment manager
├── Inventory/
│   ├── InventoryUI.mlua                    # Inventory UI
│   ├── InventoryUISlotButton.mlua          # Inventory slot
│   ├── InventoryManager.mlua               # Inventory manager
│   └── ItemDragDropHandler.mlua            # Item drag and drop
├── Collection/
│   ├── CollectionUI.mlua                   # Collection UI
│   ├── CollectionManager.mlua              # Collection manager
│   └── CollectionProgressTracker.mlua      # Collection progress tracker
├── Pet/
│   ├── PetUI.mlua                          # Pet UI
│   ├── PetManager.mlua                     # Pet manager
│   ├── PetAI.mlua                          # Pet AI behavior
│   └── PetSummonSystem.mlua                # Pet summoning system
├── Construction/
│   ├── ConstructionUI.mlua                 # Construction UI
│   ├── ConstructionManager.mlua            # Construction manager
│   └── BuildingPlacer.mlua                 # Building placement
└── Title/
    ├── TitleUI.mlua                        # Title UI
    └── TitleManager.mlua                   # Title manager
```

### UI Group Files
- `ui/InventoryGroup.ui`: Inventory UI group
- `ui/EquipmentStorageGroup.ui`: Equipment storage UI group
- `ui/CollectionGroup.ui`: Collection UI group
- `ui/ConstructionGroup.ui`: Construction UI group
- `ui/TitleStorageGroup.ui`: Title storage UI group
- `ui/EmblemGroup.ui`: Emblem UI group
- `ui/EmoticonGroup.ui`: Emoticon UI group

### Data Files
```
RootDesk/MyDesk/DataSets/
├── EquipmentData.csv                       # Equipment basic data
├── ItemData.csv                            # Item basic information
├── PetData.csv                             # Pet basic data
├── TitleData.csv                           # Title data
├── CollectionData.csv                      # Collection data
├── ConstructionData.csv                    # Construction data
├── EmblemData.csv                          # Emblem data
└── EmoticonData.csv                        # Emoticon data
```

## Inter-System Interactions

### Equipment System and Inventory Integration
```lua
-- Remove from inventory when equipping
Equipment:EquipItem(itemId) -> Inventory:RemoveItem(itemId)

-- Move to inventory when unequipping  
Equipment:UnequipItem(slot) -> Inventory:AddItem(item)
```

### Collection System and Achievement Integration
- Notify achievement system when acquiring new collectibles
- Unlock titles based on collection completion

### Pet System and Gameplay Integration
- Pet's automatic collection function
- Pet's combat support ability
- Stat improvement when pet levels up

## Data Flow

### Player Data Saving
1. Collect state information from each system
2. Data synchronization through TableSync
3. Save player progress to server

### Player Data Loading
1. Load player data from server
2. Restore data to each system
3. Update UI state

## Expansion Guide

### Adding New Equipment Type
1. Add new equipment information to `EquipmentData.csv`
2. Add new equipment type handling logic to `EquipmentManager.mlua`
3. Add new equipment slot to UI

### Adding New Collection Category  
1. Add new category to `CollectionData.csv`
2. Implement category-specific handling logic in `CollectionManager.mlua`
3. Add new category tab to `CollectionUI.mlua`

