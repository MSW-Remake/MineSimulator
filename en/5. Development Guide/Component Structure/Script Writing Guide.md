# Development Guide - Component Structure - Script Writing Guide

## Overview
This document provides a guide on how to write mlua scripts and component structure in the Miner Simulator project. mlua is a scripting language for the MOD engine, a game development-specific language based on Lua.

## mlua Basic Structure

### Component Declaration
```lua
@Component
script ComponentName extends BaseComponent

    -- Property declaration
    property type propertyName = defaultValue
    
    -- Synchronized property
    @Sync
    property type syncPropertyName = defaultValue
    
    -- Method declaration
    method void MethodName(parameters)
        -- Method content
    end
    
    -- Event handler
    @EventSender("Target")
    handler HandleEventName(EventType event)
        -- Event processing logic
    end
```

### Execution Space Specification
```lua
-- Execute only on server
@ExecSpace("Server")
method void ServerOnlyMethod()
    -- Server logic
end

-- Execute only on client
@ExecSpace("Client")
method void ClientOnlyMethod()
    -- Client logic
end

-- Execute on both server and client
@ExecSpace("ServerAndClient")
method void SharedMethod()
    -- Shared logic
end
```

## Best Practices

### 1. Naming Conventions
- **Components**: PascalCase (e.g. PlayerData, InventoryUI)
- **Methods**: PascalCase (e.g. AddItem, RefreshUI)
- **Properties**: camelCase (e.g. maxHealth, isActive)
- **Event Handlers**: Handle + EventName + Event (e.g. HandleButtonClickEvent)

### 2. Code Structure
```lua
@Component
script ExampleComponent extends Component

    -- Constant declarations
    local MAX_ITEMS = 180
    local DEFAULT_HEALTH = 100
    
    -- Properties grouped by category
    -- Basic properties
    property number health = DEFAULT_HEALTH
    property boolean isActive = true
    
    -- Synchronized properties
    @Sync
    property number playerId = 0
    @Sync
    property string playerName = ""
    
    -- Table properties
    property SyncTable<number> itemList
    property SyncTable<boolean> flagList
    
    -- Lifecycle methods
    method void OnBeginPlay()
        if self:IsServer() then
            self:InitializeServer()
        elseif self:IsClient() then
            self:InitializeClient()
        end
    end
    
    -- Server methods
    @ExecSpace("Server")
    method void InitializeServer()
        log("Server initialization")
    end
    
    -- Client methods
    @ExecSpace("Client")
    method void InitializeClient()
        log("Client initialization")
    end
    
    -- Event handlers
    @EventSender("Self")
    handler HandleTriggerEnterEvent(TriggerEnterEvent event)
        -- Event processing
    end
```

### 3. Data Management
```lua
-- Using DataService
local itemTable = _DataService:GetTable("ItemData")
local itemName = itemTable:GetCell(1, "Name")
local itemRow = itemTable:GetRow(1)

-- Using SyncTable
property SyncTable<number> playerStats

method void InitializeStats()
    for i=1, 10 do
        self.playerStats[i] = 0
    end
end

-- Client synchronization
@ExecSpace("Server")
method void UpdateClientData()
    self:SetTableClient("playerStats", 
        _UtilLogic:TableToString(self.playerStats), 
        self.Entity.OwnerId)
end
```

### 4. UI Interaction
```lua
-- UI entity access
local buttonUI = _EntityService:GetEntityByPath("/ui/MenuGroup/Button")
buttonUI.ButtonComponent.OnClick:Connect(function()
    self:OnButtonClicked()
end)

-- UI refresh
method void RefreshUI()
    local healthBar = _EntityService:GetEntityByPath("/ui/HealthBar/Fill")
    healthBar.UITransformComponent.RectSize = 
        Vector2(200 * (self.health / 100), healthBar.UITransformComponent.RectSize.y)
end
```

### 5. Timer Usage
```lua
-- One-time timer
_TimerService:SetTimerOnce(function()
    log("Execute after 3 seconds")
end, 3.0)

-- Repeating timer
local repeatTimer = function()
    log("Execute every second")
    _TimerService:SetTimerOnce(repeatTimer, 1.0)
end
repeatTimer()
```
