# Mine Simulator Project Overview

## Game Introduction
Mine Simulator is a mining simulation game where players mine resources in various mines, upgrade equipment, and explore diverse temples. Players can explore mines to collect resources, which they can then use to purchase or enhance more powerful equipment, allowing them to progress to deeper mines.

## Core Gameplay Loop
1. **Mine Exploration**: Explore various mine maps from Mine1_1 to Mine9_5
2. **Resource Mining**: Collect various minerals and gems from mining veins
3. **Equipment Enhancement**: Purchase/upgrade weapons and armor using collected resources
4. **Temple Challenges**: Challenge special temple maps with Greek mythology themes
5. **Collection**: Collect rare items and achieve accomplishments

## Major Systems

### Player System
- **Equipment System**: Weapons, armor, bags, shoes
- **Inventory**: Item storage and management
- **Collection System**: Management of various collectibles
- **Pet System**: Summoning and managing helper pets
- **Construction System**: Building structures

### Shop System
- **Equipment Shop**: Purchase/sell weapons and armor
- **Gem Shop**: Purchase premium items
- **Relic Synthesis**: Combine and enhance relics

### Map System
- **Mine Maps**: Mine1_1 ~ Mine9_5 (25 maps)
- **Temple Maps**: 8 temples including Zeus, Poseidon, Apollon
- **Town Maps**: Town ~ Town10 (11 town maps)

## Folder Structure

### Core Folders
```
MineSimulator/
├── RootDesk/MyDesk/          # Game logic and components
│   ├── Components/           # Game mechanism scripts
│   ├── Achievement/          # Achievement system
│   ├── DataSets/            # Game data (CSV)
│   └── Images/              # Game image resources
├── map/                     # Map files
├── ui/                      # UI group definitions
└── docs/                    # Project documentation
```

### Excluded Folders from Analysis
- `Environment/`: NativeScript commonly used across all MSW games
- `Global/`: Global configuration files

## Related File Paths

### Core Configuration Files
- `rule_planner.txt`: Project analysis and documentation guide

### Map Files
- `map/Mine1_1.map ~ map/Mine9_5.map`: Mine maps
- `map/Temple_Zeus_1.map ~ map/Temple_Hades_8.map`: Temple maps  
- `map/Town.map ~ map/Town10.map`: Town maps

### UI Groups
- `ui/IngameGroup.ui`: In-game UI
- `ui/InventoryGroup.ui`: Inventory UI
- `ui/ShopGroup.ui`: Shop UI
- `ui/AchievementGroup.ui`: Achievement UI

### Game Logic Scripts
- `RootDesk/MyDesk/Components/Player/`: Player-related components
- `RootDesk/MyDesk/Components/Mine/`: Mine-related mechanisms
- `RootDesk/MyDesk/Components/Town/`: Town shop systems
- `RootDesk/MyDesk/Components/Traps/`: Trap systems

## Beginner Developer Getting Started Guide

1. **Understanding Project Structure**: Learn the overall structure through this document
2. **Learning Core Systems**: Refer to player, UI, and map system documentation
3. **Understanding Component Structure**: Reference script writing methods in the development guide
4. **Understanding Data Structure**: Reference CSV data structure documentation
5. **Practice**: Try modifying or extending existing components

