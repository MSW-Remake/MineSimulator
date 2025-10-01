# UI System - In-Game UI - Outgame UI

## Overview
The Outgame UI is the UI system displayed when players are in the Town. It is primarily composed of OutgameGroup and DefaultGroup, providing interfaces for menu access, chat, emotions, various shops, and system access. In contrast to Ingame UI, it is activated in Town and deactivated in Mine.

## Outgame UI System Architecture

### System Architecture
```mermaid
graph TD
    A[Outgame UI System] --> B[OutgameUIManager<br/>Outgame UI Overall Management]
    A --> C[OutgameGroup<br/>Main Menu UI]
    A --> D[DefaultGroup<br/>Basic Always-On UI]
    
    B --> E[Activate in Town]
    B --> F[Deactivate in Mine]
    B --> G[Platform-Specific UI Handling]
    
    C --> H[Menu Buttons]
    C --> I[Notification Markers]
    C --> J[Exit Button]
    
    D --> K[Chat System]
    D --> L[Joystick (Mobile)]
    D --> M[Emotions]
    
    H --> N[MenuOpenButton_1]
    H --> O[MenuOpenButton_2]
    
    K --> P[UIChat Component]
    L --> Q[UIJoystick Component]
    M --> R[Emotion Slots]
    
    N --> S[Shop Access]
    O --> T[Inventory and Collection Access]
```

## Related File Paths

### UI Group Files
```
ui/
├── OutgameGroup.ui                     # Main outgame UI group
├── DefaultGroup.ui                     # Basic always-on UI group
├── ShopGroup.ui                        # Shop-related UI group
├── InventoryGroup.ui                   # Inventory UI group
├── CollectionGroup.ui                  # Collection UI group
├── EquipShopGroup.ui                   # Equipment shop UI group
├── GemShopGroup.ui                     # Gem shop UI group
├── PetShopGroup.ui                     # Pet shop UI group
├── ConstructionGroup.ui                # Construction UI group
├── AchievementGroup.ui                 # Achievement UI group
├── TitleStorageGroup.ui                # Title storage UI group
├── TeleportGroup.ui                    # Teleport UI group
└── HelpGuideGroup.ui                   # Help guide UI group
```

### UI Management Components
```
RootDesk/MyDesk/Components/UI/
├── OutgameUIManager.mlua               # Outgame UI overall manager
├── OutgameUIManager.codeblock          # Outgame UI management visual
├── ButtonUIOpen.mlua                   # UI open button component
├── ButtonUIOpen.codeblock              # UI open button visual
├── ExitButton.mlua                     # Exit button component
├── ExitButton.codeblock                # Exit button visual
├── UIButtonSound.mlua                  # UI button sound
├── UIButtonSound.codeblock             # UI button sound visual
├── UIHelpGuide.mlua                    # Help guide system
├── UIHelpGuide.codeblock               # Help guide visual
├── UIGuideNavigatorButton.mlua         # Guide navigation button
└── UIGuideNavigatorButton.codeblock    # Guide navigation visual
```

### Individual UI System Components
```
RootDesk/MyDesk/Components/Player/
├── PlayerData.mlua                     # Player basic data (menu info integration)
├── Inventory/                          # Inventory-related components
├── Collection/                         # Collection-related components
├── Equipment/                          # Equipment-related components
├── Pet/                               # Pet-related components
└── Construction/                       # Construction-related components
```

## OutgameUIManager - Outgame UI Overall Management

### Core Functions and Data Structure
```lua
@Component
script OutgameUIManager extends Component

    property boolean AutoEnableOnOutgame = false    -- Auto-enable when in outgame
```

### Map-based UI Activation Management
```lua
@EventSender("LocalPlayer")
handler HandleLocalPlayerMapEnterEvent(LocalPlayerMapEnterEvent event)
    local EnteredMapType = event.EnteredMapType
    
    if EnteredMapType == "Mine" then
        -- Mine entry: deactivate outgame UI
        self.Entity.Enable = false
        
    elseif EnteredMapType == "Town" and self.AutoEnableOnOutgame == true then
        -- Town entry: activate outgame UI
        self.Entity.Enable = true
        
        -- Platform-specific UI handling
        if (tostring(self.Entity.UITransformComponent.ActivePlatform) == "Mobile" and 
            Environment:IsMobilePlatform() == false) or
           (tostring(self.Entity.UITransformComponent.ActivePlatform) == "PC" and 
            Environment:IsPCPlatform() == false) then
            self.Entity.Enable = false
        else
            self.Entity.Enable = true
        end
    end
end
```

## OutgameGroup - Main Menu UI

### UI Components

#### 1. Exit Button
```json
{
  "path": "/ui/OutgameGroup/ExitButton_back",
  "components": ["ButtonComponent", "OutgameUIManager"],
  "description": "Game exit or menu close button"
}
```

#### 2. Menu Open Button 1
```json
{
  "path": "/ui/OutgameGroup/MenuOpenButton_1",
  "components": ["ButtonComponent", "ButtonUIOpen", "OutgameUIManager", "UIButtonSound"],
  "children": [
    {
      "path": "/ui/OutgameGroup/MenuOpenButton_1/icon_menu",
      "components": ["SpriteGUIRenderer"],
      "description": "Menu icon"
    },
    {
      "path": "/ui/OutgameGroup/MenuOpenButton_1/AlarmMarker",
      "components": ["SpriteGUIRenderer"],
      "description": "Alarm marker (new content notification)"
    }
  ]
}
```

#### 3. Menu Open Button 2
```json
{
  "path": "/ui/OutgameGroup/MenuOpenButton_2",
  "components": ["ButtonComponent", "ButtonUIOpen", "OutgameUIManager", "UIButtonSound"],
  "children": [
    {
      "path": "/ui/OutgameGroup/MenuOpenButton_2/icon_menu",
      "components": ["SpriteGUIRenderer"],
      "description": "Different menu category icon"
    }
  ]
}
```

### Menu Button Functions
```lua
-- UI opening handling in ButtonUIOpen.mlua
@Component
script ButtonUIOpen extends Component

    property Entity targetUI = nil    -- Target UI to open

    @EventSender("Self")
    handler HandleButtonClickEvent(ButtonClickEvent event)
        if self.targetUI ~= nil then
            -- Activate target UI
            self.targetUI.Enable = true
        end
    end
```

### Alarm Marker System
```lua
-- Manage alarm marker show/hide
method void UpdateAlarmMarker(string markerType, boolean isVisible)
    local alarmMarker = _EntityService:GetEntityByPath("/ui/OutgameGroup/MenuOpenButton_1/AlarmMarker")
    
    if markerType == "quest" then
        -- Achievement/quest related notifications
        alarmMarker.Enable = isVisible
        if isVisible then
            alarmMarker.SpriteGUIRendererComponent.Color = Color.red
        end
    elseif markerType == "shop" then
        -- Shop related notifications (new items etc.)
        alarmMarker.Enable = isVisible
        if isVisible then
            alarmMarker.SpriteGUIRendererComponent.Color = Color.yellow
        end
    elseif markerType == "collection" then
        -- Collection related notifications
        alarmMarker.Enable = isVisible
        if isVisible then
            alarmMarker.SpriteGUIRendererComponent.Color = Color.blue
        end
    end
end
```

## DefaultGroup - Basic Always-On UI

### UI Components

#### 1. Chat System (UIChat)
```json
{
  "path": "/ui/DefaultGroup/UIChat",
  "components": ["ChatComponent"],
  "description": "Multiplayer chat system"
}
```

```lua
-- Chat system management
method void InitializeChatSystem()
    local chatComponent = _EntityService:GetEntityByPath("/ui/DefaultGroup/UIChat").ChatComponent
    
    -- Chat settings
    chatComponent.MaxMessageCount = 50  -- Maximum message count
    chatComponent.AutoScroll = true     -- Auto scroll
    chatComponent.ShowTimestamp = true  -- Show timestamp
    
    -- Chat filter settings
    chatComponent:AddMessageFilter("All")      -- All chat
    chatComponent:AddMessageFilter("System")   -- System messages
    chatComponent:AddMessageFilter("Guild")    -- Guild chat
end

-- Send chat message
method void SendChatMessage(string message, string channel)
    local chatComponent = _EntityService:GetEntityByPath("/ui/DefaultGroup/UIChat").ChatComponent
    chatComponent:SendMessage(message, channel, _UserService.LocalPlayer.PlayerName)
end
```

#### 2. Joystick (UIJoystick) - Mobile Only
```json
{
  "path": "/ui/DefaultGroup/UIJoystick",
  "components": ["JoystickComponent"],
  "description": "Mobile virtual joystick"
}
```

```lua
-- Joystick system initialization
method void InitializeJoystick()
    local joystick = _EntityService:GetEntityByPath("/ui/DefaultGroup/UIJoystick").JoystickComponent
    
    if Environment:IsMobilePlatform() then
        joystick.Enable = true
        
        -- Joystick settings
        joystick.MovementRange = 100        -- Movement range
        joystick.ReturnToCenter = true      -- Auto return to center
        joystick.Sensitivity = 1.5          -- Sensitivity
        
        -- Joystick event handling
        joystick.OnValueChanged:Connect(self.OnJoystickValueChanged)
    else
        joystick.Enable = false
    end
end

method void OnJoystickValueChanged(Vector2 joystickValue)
    -- Player movement handling
    local player = _UserService.LocalPlayer
    local moveDirection = Vector3(joystickValue.x, 0, joystickValue.y)
    
    player.PlayerMovement:SetMoveDirection(moveDirection)
end
```

#### 3. Emotion System (Emoticon)
```json
{
  "path": "/ui/DefaultGroup/Emoticon",
  "components": ["ScrollLayoutGroupComponent"],
  "children": [
    {
      "path": "/ui/DefaultGroup/Emoticon/Slot",
      "components": ["ButtonComponent", "EmoticonPlayButton"],
      "children": [
        {
          "path": "/ui/DefaultGroup/Emoticon/Slot/icon_emoticon",
          "components": ["SpriteGUIRenderer"]
        },
        {
          "path": "/ui/DefaultGroup/Emoticon/Slot/Thumbnail",
          "components": ["SpriteGUIRenderer"]
        }
      ]
    }
  ]
}
```

```lua
-- Emotion system initialization
method void InitializeEmoticonSystem()
    local emoticonPanel = _EntityService:GetEntityByPath("/ui/DefaultGroup/Emoticon")
    local emoticonSlot = _EntityService:GetEntityByPath("/ui/DefaultGroup/Emoticon/Slot")
    
    -- Load player's owned emotions
    local playerEmoticons = _UserService.LocalPlayer.PlayerEmoticon
    local emoticonTable = _DataService:GetTable("Emoticon")
    
    -- Create slots for owned emotions
    for i=1, emoticonTable:GetRowCount() do
        if playerEmoticons.haveEmoticon[i] == true then
            local newSlot = emoticonSlot:Clone("EmoticonSlot_"..i)
            
            -- Set emotion icon
            local iconRUID = emoticonTable:GetCell(i, "IconRUID")
            newSlot:GetChildByName("icon_emoticon").SpriteGUIRendererComponent.ImageRUID = iconRUID
            newSlot:GetChildByName("Thumbnail").SpriteGUIRendererComponent.ImageRUID = iconRUID
            
            -- Set click event
            newSlot.EmoticonPlayButton.emoticonIndex = i
        end
    end
end

-- Play emotion in EmoticonPlayButton.mlua
@Component
script EmoticonPlayButton extends Component

    property number emoticonIndex = 0

    @EventSender("Self")
    handler HandleButtonClickEvent(ButtonClickEvent event)
        if self.emoticonIndex > 0 then
            -- Display emotion above player
            _UserService.LocalPlayer.PlayerEmoticon:PlayEmoticon(self.emoticonIndex)
        end
    end
```

## UI Navigation System

### Menu Hierarchy Structure
```lua
-- Menu system hierarchy definition
local menuHierarchy = {
    ["MainMenu"] = {
        ["Shop"] = {
            ["Equipment Shop"] = "EquipShopGroup",
            ["Gem Shop"] = "GemShopGroup", 
            ["Pet Shop"] = "PetShopGroup"
        },
        ["Management"] = {
            ["Inventory"] = "InventoryGroup",
            ["Collection"] = "CollectionGroup",
            ["Title"] = "TitleStorageGroup"
        },
        ["System"] = {
            ["Construction"] = "ConstructionGroup",
            ["Achievement"] = "AchievementGroup",
            ["Teleport"] = "TeleportGroup"
        }
    }
}

-- Menu navigation
method void NavigateToMenu(string menuPath)
    local pathParts = string.split(menuPath, "/")
    local targetUIGroup = self:ResolveMenuPath(pathParts)
    
    if targetUIGroup then
        -- Close existing open UIs
        self:CloseAllMenuUIs()
        
        -- Open target UI
        local targetUI = _EntityService:GetEntityByPath("/ui/"..targetUIGroup)
        targetUI.Enable = true
        
        -- Add to back navigation stack
        self:PushToNavigationStack(targetUIGroup)
    end
end
```

### Back Navigation System
```lua
-- UI navigation stack management
property table navigationStack = {}

method void PushToNavigationStack(string uiGroup)
    table.insert(self.navigationStack, uiGroup)
end

method void GoBack()
    if #self.navigationStack > 1 then
        -- Remove current UI
        table.remove(self.navigationStack)
        
        -- Return to previous UI
        local previousUI = self.navigationStack[#self.navigationStack]
        self:NavigateToMenu(previousUI)
    else
        -- Return to main menu if stack is empty
        self:CloseAllMenuUIs()
    end
end

method void CloseAllMenuUIs()
    local menuUIGroups = {
        "EquipShopGroup", "GemShopGroup", "PetShopGroup",
        "InventoryGroup", "CollectionGroup", "TitleStorageGroup",
        "ConstructionGroup", "AchievementGroup", "TeleportGroup"
    }
    
    for _, uiGroup in ipairs(menuUIGroups) do
        local ui = _EntityService:GetEntityByPath("/ui/"..uiGroup)
        ui.Enable = false
    end
    
    -- Reset navigation stack
    self.navigationStack = {}
end
```

## Help Guide System

### Guide Display and Navigation
```lua
-- Help system management in UIHelpGuide.mlua
@Component
script UIHelpGuide extends Component

    property table guidePages = {}      -- Guide pages
    property number currentPage = 1     -- Current page

    method void InitializeGuideSystem()
        -- Load guide page data
        local guideTable = _DataService:GetTable("HelpGuide")
        
        for i=1, guideTable:GetRowCount() do
            local pageData = {
                title = _LocalizationService:GetText(guideTable:GetCell(i, "Title")),
                content = _LocalizationService:GetText(guideTable:GetCell(i, "Content")),
                imageRUID = guideTable:GetCell(i, "ImageRUID")
            }
            table.insert(self.guidePages, pageData)
        end
    end
    
    method void ShowGuidePage(number pageIndex)
        if pageIndex < 1 or pageIndex > #self.guidePages then
            return
        end
        
        self.currentPage = pageIndex
        local pageData = self.guidePages[pageIndex]
        
        -- Update guide UI
        local guideUI = _EntityService:GetEntityByPath("/ui/HelpGuideGroup/HelpGuide")
        guideUI:GetChildByName("Title").TextComponent.Text = pageData.title
        guideUI:GetChildByName("Content").TextComponent.Text = pageData.content
        guideUI:GetChildByName("Image").SpriteGUIRendererComponent.ImageRUID = pageData.imageRUID
        
        -- Update navigation button state
        self:UpdateNavigationButtons()
    end
    
    method void UpdateNavigationButtons()
        local prevButton = _EntityService:GetEntityByPath("/ui/HelpGuideGroup/HelpGuide/PrevButton")
        local nextButton = _EntityService:GetEntityByPath("/ui/HelpGuideGroup/HelpGuide/NextButton")
        local pageInfo = _EntityService:GetEntityByPath("/ui/HelpGuideGroup/HelpGuide/PageInfo")
        
        -- Enable state of prev/next buttons
        prevButton.ButtonComponent.Enable = (self.currentPage > 1)
        nextButton.ButtonComponent.Enable = (self.currentPage < #self.guidePages)
        
        -- Display page information
        pageInfo.TextComponent.Text = string.format("%d / %d", self.currentPage, #self.guidePages)
    end
```

## Platform-Specific UI Adaptation

### Mobile Optimization
```lua
method void OptimizeForMobile()
    if Environment:IsMobilePlatform() then
        -- Activate joystick
        local joystick = _EntityService:GetEntityByPath("/ui/DefaultGroup/UIJoystick")
        joystick.Enable = true
        
        -- Enlarge button size
        local menuButtons = {
            "/ui/OutgameGroup/MenuOpenButton_1",
            "/ui/OutgameGroup/MenuOpenButton_2"
        }
        
        for _, buttonPath in ipairs(menuButtons) do
            local button = _EntityService:GetEntityByPath(buttonPath)
            button.UITransformComponent.LocalScale = Vector3(1.2, 1.2, 1)
        end
        
        -- Adjust emotion UI size
        local emoticonPanel = _EntityService:GetEntityByPath("/ui/DefaultGroup/Emoticon")
        emoticonPanel.UITransformComponent.LocalScale = Vector3(1.1, 1.1, 1)
    else
        -- Deactivate joystick on PC
        local joystick = _EntityService:GetEntityByPath("/ui/DefaultGroup/UIJoystick")
        joystick.Enable = false
    end
end
```

### UI Adjustment by Resolution
```lua
method void AdjustUIForResolution()
    local screenWidth = Screen.width
    local screenHeight = Screen.height
    
    -- UI anchor adjustment
    local menuButton1 = _EntityService:GetEntityByPath("/ui/OutgameGroup/MenuOpenButton_1")
    local menuButton2 = _EntityService:GetEntityByPath("/ui/OutgameGroup/MenuOpenButton_2")
    
    if screenWidth > 1920 then
        -- UI position adjustment for high resolution
        menuButton1.UITransformComponent.AnchoredPosition = Vector2(-100, -100)
        menuButton2.UITransformComponent.AnchoredPosition = Vector2(-200, -100)
    else
        -- Standard resolution position
        menuButton1.UITransformComponent.AnchoredPosition = Vector2(-80, -80)
        menuButton2.UITransformComponent.AnchoredPosition = Vector2(-160, -80)
    end
end
```

## Accessibility and Usability Features

### Keyboard Shortcuts
```lua
-- Keyboard shortcut system
method void HandleKeyboardInput()
    if Input:GetKeyDown(KeyCode.I) then
        -- I key to open inventory
        self:NavigateToMenu("Management/Inventory")
    elseif Input:GetKeyDown(KeyCode.C) then
        -- C key to open collection
        self:NavigateToMenu("Management/Collection")
    elseif Input:GetKeyDown(KeyCode.B) then
        -- B key to open construction menu
        self:NavigateToMenu("System/Construction")
    elseif Input:GetKeyDown(KeyCode.Escape) then
        -- ESC key to go back or close menu
        self:GoBack()
    end
end
```

### Tooltip System
```lua
-- Display tooltips for UI elements
@Component
script UITooltip extends Component

    property string tooltipText = ""
    property Entity tooltipPanel = nil

    method void OnMouseEnter()
        if self.tooltipText ~= "" then
            self:ShowTooltip()
        end
    end
    
    method void OnMouseExit()
        self:HideTooltip()
    end
    
    method void ShowTooltip()
        if self.tooltipPanel == nil then
            self.tooltipPanel = _EntityService:GetEntityByPath("/ui/TooltipPanel")
        end
        
        self.tooltipPanel.Enable = true
        self.tooltipPanel:GetChildByName("Text").TextComponent.Text = 
            _LocalizationService:GetText(self.tooltipText)
        
        -- Display tooltip at mouse position
        local mousePos = Input.mousePosition
        self.tooltipPanel.UITransformComponent.Position = 
            Vector3(mousePos.x + 10, mousePos.y + 10, 0)
    end
    
    method void HideTooltip()
        if self.tooltipPanel ~= nil then
            self.tooltipPanel.Enable = false
        end
    end
```

## Performance Optimization

### UI Visibility Management
```lua
-- Deactivate UI elements outside screen
method void UpdateUIVisibility()
    local activeUIGroups = self:GetActiveUIGroups()
    
    for uiGroupName, uiGroup in pairs(allUIGroups) do
        if not table.contains(activeUIGroups, uiGroupName) then
            -- Completely deactivate inactive UI groups
            uiGroup.Enable = false
        end
    end
end

-- UI animation optimization
method void OptimizeAnimations()
    local frameRate = Application.targetFrameRate
    
    if frameRate < 30 then
        -- Simplify animations at low frame rates
        self:SimplifyAnimations()
    end
end
```

### Memory Management
```lua
-- Release unused UI resources
method void CleanupUnusedResources()
    -- Unload UI groups not used for a long time
    for uiGroupName, lastUsedTime in pairs(uiUsageTracker) do
        if (_TimeService:GetTime() - lastUsedTime) > 300 then  -- 5 minutes
            local uiGroup = _EntityService:GetEntityByPath("/ui/"..uiGroupName)
            uiGroup:UnloadResources()
        end
    end
end
```

## Common Troubleshooting

### When UI Doesn't Display
1. Check `OutgameUIManager` activation state
2. Verify map type is "Town"
3. Check `AutoEnableOnOutgame` setting

### When Buttons Don't Work
1. Check `ButtonUIOpen.targetUI` setting
2. Check target UI's Enable state
3. Verify button component activation state

### Platform-Specific UI Issues
1. Check `UITransformComponent.ActivePlatform` setting
2. Verify joystick activation conditions
3. Check resolution-based UI scaling application
