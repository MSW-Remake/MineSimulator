# Development Guide - Data Management - CSV Data Structure

## Overview
The Miner Simulator project manages game data through CSV files and UserDataSet. This document provides a guide on data structure and management methods.

## Data File Structure

### CSV Files
```
RootDesk/MyDesk/DataSets/
├── Equipment.csv                    # Equipment data
├── Equipment.userdataset           # Equipment dataset
├── DropItem.csv                    # Drop item data  
├── ConsumableItems.csv             # Consumable item data
├── Construction.csv                # Construction data
├── Pet.csv                        # Pet data
├── PlayerTitle.csv                # Player title data
├── Map_Mine.csv                   # Mine map data
├── Map_Town.csv                   # Town map data
└── NPCTable.csv                   # NPC data
```

### Data Access Methods
```lua
-- Load table
local equipmentTable = _DataService:GetTable("Equipment")

-- Read specific cell value
local itemName = equipmentTable:GetCell(1, "Name")
local itemPrice = tonumber(equipmentTable:GetCell(1, "Price"))

-- Read entire row  
local itemRow = equipmentTable:GetRow(1)
local name = itemRow:GetItem("Name")
local price = itemRow:GetItem("Price")

-- Read entire column
local allNames = equipmentTable:GetColumn("Name")

-- Check row count
local rowCount = equipmentTable:GetRowCount()
```

## Main Data Structures

### Equipment.csv
```csv
Name,Type,Grade,Power,Price,IconRUID,Description
EquipmentName1,1,1,10,100,icon_uuid,Equipment description
EquipmentName2,1,2,20,200,icon_uuid,Equipment description
```

### DropItem.csv  
```csv
Name,Type,Grade,IconRUID,Description,DropRate
DropItemName1,1,1,icon_uuid,Item description,0.1
DropItemName2,2,2,icon_uuid,Item description,0.05
```

### Construction.csv
```csv
Name,IconRUID,UnlockCost,ConstructionCost,MaxLevel,Desc
ConstructionName1,icon_uuid,0,0,1,Construction description
ConstructionName2,icon_uuid,1,80,3,Construction description
```

## Data Management Patterns

### Dynamic Data Loading
```lua
method void LoadDynamicData()
    local dataTable = _DataService:GetTable("Equipment")
    
    for i=1, dataTable:GetRowCount() do
        local itemData = {
            name = _LocalizationService:GetText(dataTable:GetCell(i, "Name")),
            type = tonumber(dataTable:GetCell(i, "Type")),
            grade = tonumber(dataTable:GetCell(i, "Grade")),
            power = tonumber(dataTable:GetCell(i, "Power")),
            price = tonumber(dataTable:GetCell(i, "Price")),
            iconRUID = dataTable:GetCell(i, "IconRUID")
        }
        
        table.insert(self.itemDatabase, itemData)
    end
end
```

### Data Caching
```lua
-- Cache frequently used data
local equipmentCache = {}

method table GetEquipmentData(number equipmentId)
    if not equipmentCache[equipmentId] then
        local table = _DataService:GetTable("Equipment")
        equipmentCache[equipmentId] = {
            name = table:GetCell(equipmentId, "Name"),
            power = tonumber(table:GetCell(equipmentId, "Power")),
            grade = tonumber(table:GetCell(equipmentId, "Grade"))
        }
    end
    
    return equipmentCache[equipmentId]
end
```

