# Development Guide - Debugging - Common Troubleshooting

## Overview
This guide covers frequently occurring problems during Miner Simulator development and their solutions.

## Script-related Issues

### 1. When Components Don't Work

**Problem**: Scripts are written but don't function
**Solution**:
```lua
-- Check if OnBeginPlay is called
method void OnBeginPlay()
    log("OnBeginPlay called")  -- Verify with log
    
    -- Check server/client
    if self:IsServer() then
        log("Running on server")
    elseif self:IsClient() then  
        log("Running on client")
    end
end
```

**Checklist**:
- [ ] Verify component is properly attached to entity
- [ ] Check if @Component annotation exists  
- [ ] Verify correct inheritance relationship (extends Component)
- [ ] Confirm ExecSpace is properly set

### 2. Synchronization Issues

**Problem**: Data not synchronized between server and client
**Solution**:
```lua
-- Check @Sync property
@Sync  
property number syncedValue = 0

-- Manual synchronization with SetTableClient
@ExecSpace("Server")
method void UpdateClientData()
    self:SetTableClient("playerData", 
        _UtilLogic:TableToString(self.playerData), 
        self.Entity.OwnerId)
end

-- Verify synchronization with OnSyncProperty
@ExecSpace("Client")
method void OnSyncProperty(string name, any value)
    log("Synchronized: " .. name .. " = " .. tostring(value))
end
```

## UI-related Issues

### 1. When UI Doesn't Display

**Checklist**:
- [ ] Verify UI group is activated
- [ ] Check if path is correct
- [ ] Confirm Enable status
- [ ] Check sorting layer

```lua
-- UI state debugging
method void DebugUI()
    local ui = _EntityService:GetEntityByPath("/ui/MenuGroup/Button")
    
    if ui then
        log("UI found: " .. ui.Path)
        log("Enable status: " .. tostring(ui.Enable))
        log("Sorting layer: " .. tostring(ui.SortingLayer))
    else
        log("UI not found")
    end
end
```

### 2. When Button Click Doesn't Work

```lua
-- Check button event binding
method void SetupButton()
    local button = _EntityService:GetEntityByPath("/ui/MenuGroup/Button")
    
    if button and button.ButtonComponent then
        button.ButtonComponent.OnClick:Connect(function()
            log("Button clicked")
        end)
    else
        log("ButtonComponent not found")
    end
end
```

## Data-related Issues

### 1. DataService Access Failure

```lua
-- Debug data table
method void DebugDataTable(string tableName)
    local table = _DataService:GetTable(tableName)
    
    if table then
        log("Table " .. tableName .. " loaded")
        log("Row count: " .. tostring(table:GetRowCount()))
        
        -- Output first row
        if table:GetRowCount() > 0 then
            local firstRow = table:GetRow(1)
            log("First row: " .. tostring(firstRow))
        end
    else
        log("Table " .. tableName .. " not found")
    end
end
```

## Event-related Issues

### 1. When Events Don't Occur

```lua
-- Debug event handler
@EventSender("Self")
handler HandleTriggerEnterEvent(TriggerEnterEvent event)
    log("TriggerEnterEvent occurred")
    log("Triggering entity: " .. tostring(event.TriggerBodyEntity.Name))
    
    -- Check entity tags
    if event.TriggerBodyEntity.TagComponent then
        log("Tag: " .. tostring(event.TriggerBodyEntity.TagComponent.Tags[1]))
    end
end
```

**Checklist**:
- [ ] Verify trigger collider is set
- [ ] Check if on appropriate layer
- [ ] Confirm event handler annotation is correct

## Logging Usage

### Effective Logging
```lua
-- Basic log
log("Basic message")

-- Include variable values
log("Player HP: " .. tostring(player.health))

-- Conditional logging
if DEBUG_MODE then
    log("Debug: " .. debugInfo)
end

-- Error log
if not success then
    log("ERROR: Operation failed - " .. errorMessage)
end
```

### Log Categorization
```lua
-- Category-based log functions
method void LogInfo(string message)
    log("[INFO] " .. message)
end

method void LogError(string message)
    log("[ERROR] " .. message)
end

method void LogDebug(string message)
    if self.debugMode then
        log("[DEBUG] " .. message)
    end
end
```

## Performance Issue Solutions

### 1. Frame Drop Issues

**Causes and Solutions**:
- **Excessive Update calls**: Update only when necessary
- **Unnecessary UI updates**: Update only when changes occur
- **Memory leaks**: Clean up unused objects

```lua
-- Optimized update
property boolean needsUpdate = false
property number lastUpdateTime = 0

method void OnUpdate(number deltaTime)
    local currentTime = _TimeService:GetTime()
    
    -- Update only every 0.1 seconds
    if self.needsUpdate and (currentTime - self.lastUpdateTime) > 0.1 then
        self:UpdateLogic()
        self.needsUpdate = false  
        self.lastUpdateTime = currentTime
    end
end

method void RequestUpdate()
    self.needsUpdate = true
end
```

### 2. Memory Management

```lua
-- Object pooling
local objectPool = {}

method Entity GetPooledObject(string objectType)
    if objectPool[objectType] == nil then
        objectPool[objectType] = {}
    end
    
    local pool = objectPool[objectType]
    if #pool > 0 then
        return table.remove(pool)
    else
        return self:CreateNewObject(objectType)
    end
end

method void ReturnToPool(Entity obj, string objectType)
    obj.Enable = false
    table.insert(objectPool[objectType], obj)
end
```

## Common Error Messages and Solutions

### "Accessing nil value" Error
```lua
-- Safe access method
if entity and entity.Component then
    entity.Component:DoSomething()
else
    log("Entity or Component is nil")
end

-- Use isvalid
if isvalid(entity) then
    entity:DoSomething()
end
```

### "Path not found" Error
```lua
-- Check path existence
local ui = _EntityService:GetEntityByPath("/ui/MenuGroup")
if ui then
    log("Path exists")
else
    log("Path does not exist: /ui/MenuGroup")
end
```

### Type Conversion Error  
```lua
-- Safe type conversion
local numValue = tonumber(stringValue)
if numValue then
    -- Conversion successful
    self.value = numValue
else
    log("Number conversion failed: " .. tostring(stringValue))
    self.value = 0  -- Set default value
end
```

## Debug Tool Utilization

### 1. In-game Debug UI
```lua
-- Debug information display UI
method void ShowDebugInfo()
    local debugUI = _EntityService:GetEntityByPath("/ui/DebugInfo")
    if debugUI then
        debugUI:GetChildByName("PlayerHP").TextComponent.Text = "HP: " .. tostring(self.health)
        debugUI:GetChildByName("PlayerMP").TextComponent.Text = "MP: " .. tostring(self.mana)
        debugUI:GetChildByName("Position").TextComponent.Text = "Pos: " .. tostring(self.Entity.Transform.Position)
    end
end
```

### 2. Conditional Debugging
```lua
-- Debug mode setting
property boolean isDebugMode = false

method void DebugLog(string message)
    if self.isDebugMode then
        log("[DEBUG] " .. message)
        
        -- Also display in in-game debug UI
        self:ShowDebugMessage(message)
    end
end
```

