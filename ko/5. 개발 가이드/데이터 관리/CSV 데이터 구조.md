# 개발 가이드 - 데이터 관리 - CSV 데이터 구조

## 개요
광부 시뮬레이터 프로젝트는 CSV 파일과 UserDataSet을 통해 게임 데이터를 관리합니다. 이 문서는 데이터 구조와 관리 방법에 대한 가이드입니다.

## 데이터 파일 구조

### CSV 파일들
```
RootDesk/MyDesk/DataSets/
├── Equipment.csv                    # 장비 데이터
├── Equipment.userdataset           # 장비 데이터셋
├── DropItem.csv                    # 드롭 아이템 데이터  
├── ConsumableItems.csv             # 소모품 데이터
├── Construction.csv                # 건설 데이터
├── Pet.csv                        # 펫 데이터
├── PlayerTitle.csv                # 칭호 데이터
├── Map_Mine.csv                   # 광산 맵 데이터
├── Map_Town.csv                   # 마을 맵 데이터
└── NPCTable.csv                   # NPC 데이터
```

### 데이터 접근 방법
```lua
-- 테이블 로드
local equipmentTable = _DataService:GetTable("Equipment")

-- 특정 셀 값 읽기
local itemName = equipmentTable:GetCell(1, "Name")
local itemPrice = tonumber(equipmentTable:GetCell(1, "Price"))

-- 전체 행 읽기  
local itemRow = equipmentTable:GetRow(1)
local name = itemRow:GetItem("Name")
local price = itemRow:GetItem("Price")

-- 컬럼 전체 읽기
local allNames = equipmentTable:GetColumn("Name")

-- 행 수 확인
local rowCount = equipmentTable:GetRowCount()
```

## 주요 데이터 구조

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

## 데이터 관리 패턴

### 동적 데이터 로딩
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

### 데이터 캐싱
```lua
-- 자주 사용되는 데이터 캐싱
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