GoldAppleAltarInteraction:GiveReward -- Provides one of gold, gem, or accessory rewards to the player based on probability
GoldAppleAltarInteraction:Sacrifice -- Processes player offering golden apples to the altar to receive rewards
GoldAppleAltarInteraction:OnBeginPlay -- On component initialization, sets guide image on server and initial state on client
GoldAppleAltarInteraction:SpawnReward -- Spawns corresponding visual reward box based on reward type
GoldAppleAltarInteraction:CheckGoldAppleCountInServer -- Checks and processes player's golden apple count on server
GoldAppleAltarInteraction:SetRewardCountInClient -- Sets reward count on client and updates altar state
GoldAppleAltarInteraction:ShowMessage -- Displays warning message when player has no golden apples
GoldAppleAltarInteraction:PlaySoundInClient -- Plays specified sound on client
GoldAppleAltarInteraction:HandleInteractionEnterEvent -- Displays guide key UI when player enters altar interaction range
GoldAppleAltarInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when player leaves altar interaction range
GoldAppleAltarInteraction:HandleInteractionEvent -- Checks golden apple count and executes offering when player interacts with altar
GoldAppleAltarInteraction:HandleSpriteAnimPlayerChangeFrameEvent -- Handles altar animation frame changes to spawn reward apples or close altar
GoldAppleAltarInteraction:HandleTriggerEnterEvent -- Destroys apple and provides reward when reward apple enters trigger
InteractionTemplePortal:OnBeginPlay -- Sets up portal configuration and initialization timer based on portal position during component initialization
InteractionTemplePortal:UsePortal -- Processes player using portal to travel to temple
InteractionTemplePortal:Init -- Initializes temple portal UI information according to player's floor level
InteractionTemplePortal:SetLoadingOn -- Activates loading UI and restricts player movement when traveling from town to temple
InteractionTemplePortal:HandleInteractionEnterEvent -- Displays entrance guide UI when player enters portal interaction range
InteractionTemplePortal:HandleInteractionLeaveEvent -- Hides guide UI when player leaves portal interaction range
InteractionTemplePortal:HandleInteractionEvent -- Executes temple travel when player interacts with portal
InteractionTemplePortal:HandleLocalPlayerChangedTempleStartingFloor -- Updates portal information when player's temple starting floor changes
JumpingMachine:ready -- Places player on jumping machine and sets to launch ready state
JumpingMachine:ChangeDirection -- Periodically changes jump direction arrow to allow direction selection
JumpingMachine:jumping -- Launches player with jump in set direction and force
JumpingMachine:OnBeginPlay -- Resets jumping machine to initial state on component start
JumpingMachine:reset -- Initializes all jumping machine states and hides arrows
JumpingMachine:OnUpdate -- Continuously rotates rotary-type jumping machines
JumpingMachine:HandleInteractionEvent -- Switches between ready or launch state when player interacts with jumping machine
JumpingMachine:HandleInteractionLeaveEvent -- Resets when player leaves jumping machine interaction range
JumpingMachine:HandleInteractionEnterEvent -- Displays guide UI when player enters jumping machine interaction range
KronosClockTowerUI:RefreshUI -- Updates Kronos clock tower UI information according to player construction level and floor count
KronosClockTowerUI:HandleButtonClickEvent -- Sets starting floor to highest constructible floor when maximum floor button is clicked
KronosClockTowerUI:HandleButtonClickEvent2 -- Sets starting floor to 1st floor when minimum floor button is clicked
KronosClockTowerUI:HandleButtonClickEvent3 -- Increases starting floor by 1 when floor increase button is clicked
KronosClockTowerUI:HandleButtonClickEvent4 -- Decreases starting floor by 1 when floor decrease button is clicked
LandscapeTriggerBox:HandleTriggerEnterEvent -- Disables diving state and sets central area state when player enters landscape trigger
LandscapeTriggerBox:HandleTriggerLeaveEvent -- Sets diving state and disables central area state when player leaves landscape trigger
MenuUI:SetMenuUI -- Sets activation state of menu buttons and panels according to currently selected menu state
MenuUI:HandleButtonClickEvent -- Displays menu 1 when menu button 1 is clicked
MenuUI:HandleButtonClickEvent2 -- Displays menu 2 when menu button 2 is clicked
MenuUI:HandleButtonClickEvent3 -- Displays menu 3 when menu button 3 is clicked
MenuUI:HandleButtonClickEvent4 -- Closes menu to initial state when exit button is clicked
MenuUI:HandleButtonClickEvent5 -- Closes menu to initial state when close button is clicked
MenuUI:HandleButtonClickEvent6 -- Closes menu to initial state when close button is clicked
MenuUI:HandleButtonClickEvent7 -- Closes menu to initial state when close button is clicked
MenuUI:HandleLocalPlayerMapEnterEvent -- Resets menu to initial state when player enters town map
NPCTempleSnake:CheckRelicCollectionAcheivement -- Checks if player has 100% relic collection achievement and grants temple access permission
NPCTempleSnake:HandleTriggerEnterEvent -- Checks relic collection achievement progress when player enters temple snake NPC trigger
simulateButton:HandleButtonClickEvent -- Executes corresponding simulation based on input value when cheat simulation button is clicked
SunWorship:OnUpdate -- Moves in circular orbit around sun and changes direction indicator based on position
SunWorship:OnBeginPlay -- Component initialization (currently no special initialization logic)
SunWorship:HandleTriggerLeaveEvent -- Destroys bullet when bullet leaves trigger
TableSync:SetTableClient -- Synchronizes entire table data sent from server on client
TableSync:SetTableElementClient -- Synchronizes specific index value of table from server to client
TableSync:ClearTableClient -- Fully initializes client table to default values
AchievementItemUI:OnBeginPlay -- Initializes and sets up UI component references
AchievementItemUI:Refresh -- Updates UI elements according to achievement data and sets appropriate buttons for state
AchievementItemUI:Clear -- Cleans up and initializes UI elements (currently no special cleanup work)
AchievementRewardClaimButtonUI:HandleButtonClickEvent -- Provides achievement reward and disables button when achievement reward claim button is clicked
AchievementUI:OnBeginPlay -- Sets up grid view and loads data table during achievement UI initialization
AchievementUI:OnRefresh -- Callback function called when refreshing each item in grid view
AchievementUI:OnClear -- Callback function called when cleaning up each item in grid view
AchievementUI:InitAchievementDataTable -- Initializes achievement data table and constructs item table with player progress
AchievementUI:LoadAchievementDataTable -- Loads player's latest achievement progress and completion status to update item table
AchievementUI:RefreshUI -- Sets flag to refresh UI
AchievementUI:LoadAchivementRUIDDataTable -- Loads and maps achievement type and reward item image RUID information from table
AchievementUI:OnUpdate -- Updates achievement list if refresh flag is set
AchievementUI:HandleKeyDownEvent -- Closes achievement UI when ESC key is pressed
PlayerAchievementComponent:OnBeginPlay -- Sets up achievement progress and completion status tables during component initialization
PlayerAchievementComponent:GetProgress -- Increases achievement progress and processes completion when completion conditions are met
PlayerAchievementComponent:PopupCompleteUI -- Displays completion UI with fade effect when achievement is completed
PlayerAchievementComponent:SetTableClient -- Synchronizes table data sent from server on client
PlayerAchievementComponent:SetTableElementClient -- Synchronizes specific index value of table from server to client
PlayerAchievementComponent:ClearTableClient -- Fully initializes client table to default values
PlayerAchievementComponent:ChangedTable -- Refreshes UI and sets alarm marker when achievement table is changed
PlayerAchievementComponent:ClearAllProperty -- Initializes all achievement progress and completion status
PlayerAchievementComponent:LoadedUserData -- Loads saved achievement data to restore progress and completion status
PlayerAchievementComponent:OnMapEnter -- Increases corresponding achievement progress when entering specific map
PlayerAchievementComponent:GiveReward -- Code that gives achievement rewards to player.
PlayerAchievementComponent:SetAlarmMarker -- Activates marker if at least one achievement reward can be claimed, otherwise deactivates
CheatButton:HandleButtonClickEvent -- Executes corresponding cheat type on server when cheat button is clicked
CheatManager:OnBeginPlay -- Initializes administrator account list at game start
CheatManager:UseCheatOnServer -- Verifies administrator privileges and executes various cheat commands
CheatManager:IsAdmin -- Checks if given PPSN has administrator privileges
CheatManager:InitPPSN -- Initializes PPSN list of accounts with administrator privileges
CheatManager:GiveReward -- Determines relic drop status and provides rewards in ruins mining cheat
CheatManager:SetUI_RelicBoxResult -- Displays relic box opening result in UI
CheatManager:SetCheatUIEnableOnServer -- Activates cheat UI after verifying administrator status
CheatManager:SetCheatUIEnableOnClient -- Activates cheat UI group on client
CheatManager:UseCheatForTest0314 -- Test cheat that provides all items and progress to player
CheatManager:ResetDB -- Resets all player data to initial state
CheatManager:HandleKeyDownEvent -- Keyboard input processing to activate cheat with spacebar and number key combinations
CheatManager:HandleKeyUpEvent -- Processes key release to disable cheat input state
CheatManager:HandleButtonClickEvent -- Executes cheat that provides all items and progress when test button is clicked
GuideMessageTrigger:OnBeginPlay -- Guide message trigger initialization
GuideMessageTrigger:HandleTriggerEnterEvent -- Displays guide message when player enters trigger
IcicleSellNPCInteraction:OnBeginPlay -- Icicle sell NPC interaction initialization
IcicleSellNPCInteraction:OnInteractionEvent -- Processes selling all icicle materials
IcicleSellNPCInteraction:HandleInteractionEvent -- Handles NPC interaction event
IcicleSellNPCInteraction:HandleInteractionEnterEvent -- Displays guide UI when approaching NPC
IcicleSellNPCInteraction:HandleInteractionLeaveEvent -- Deactivates guide UI when moving away from NPC
InventoryButtonUI:OnUpdate -- Processes inventory UI refresh requests
InventoryButtonUI:RefreshUI_Inner -- Reflects inventory capacity information in UI
InventoryButtonUI:RefreshUI -- Schedules inventory UI refresh
InventoryUISlotButton_RelicBox:HandleButtonClickEvent -- Inventory relic box slot button click event
OutGameUIButtonEnabler:HandleLocalPlayerMapEnterEvent -- Handles UI button activation/deactivation based on map movement
RopeCorrection:OnBeginPlay -- Corrects rope collision box size
TrapManager:OnBeginPlay -- Temple trap manager initialization
TrapManager:Init -- Sets temple trap damage based on player abilities
LocalizationNPC:OnBeginPlay -- Initializes NPC name and chat balloon localization
LocalizationNPC:SetLocalization -- Sets NPC name and chat balloon text localization (legacy version)
LocalizationNPC:Localize -- Retrieves NPC name and chat balloon text from data table for localization setup
LocalizationUIModel:OnBeginPlay -- UI model text localization initialization
LocalizationUIModel:Localize -- Sets UI model text to localized data
DeadZone:HandleTriggerEnterEvent -- Handles player death when entering dead zone
DroppedChair:SetSpriteRUID -- Sets sprite of dropped chair
DroppedChair:OnBeginPlay -- Dropped chair follows player and auto-pickup
DroppedChair:SetItemProperty -- Sets index of dropped chair
DroppedGoldBox:OnBeginPlay -- Dropped gold box follows player and auto-pickup
DroppedItem:SetSpriteRUID -- Sets sprite of dropped item
DroppedItem:OnBeginPlay -- Dropped item follows player and auto-pickup
DroppedItem:SetItemProperty -- Sets properties of dropped item
DroppedMaterial:OnBeginPlay -- Dropped material item follows player and auto-pickup
DroppedRelicBox:OnBeginPlay -- Dropped relic box follows player and auto-pickup
ExplorerBoxInteraction:SetTravelerBoxResultUI -- Displays explorer box opening result UI
ExplorerBoxInteraction:OnBeginPlay -- Explorer box interaction initialization
ExplorerBoxInteraction:OnInteractionEvent -- Provides items when interacting with explorer box
ExplorerBoxInteraction:HandleInteractionEvent -- Handles explorer box interaction event
ExplorerBoxInteraction:HandleInteractionEnterEvent -- Displays guide UI when approaching explorer box
ExplorerBoxInteraction:HandleInteractionLeaveEvent -- Deactivates guide UI when moving away from explorer box
GameResultUI:OnBeginPlay -- Game result UI initialization and item slot creation
GameResultUI:HandleKeyDownEvent -- Move to town with E key/ESC key from game result screen
MiningGame:OnBeginPlay -- Mining minigame component initialization
MiningGame:InitMinningGame -- Initial setup and UI configuration of mining minigame
MiningGame:StartMinningGame -- Mining minigame start processing
MiningGame:OnUpdate -- Mining minigame timing arrow movement processing
MiningGame:Hit -- Mining timing result processing and damage calculation
MiningGame:SetTimingBarToRandomPos -- Sets mining game timing bar position randomly
MiningGame:FinishGame -- Mining minigame end and reward provision processing
MiningGame:GiveReward -- Reward provision request when mining succeeds
MiningGame:ExitGame -- Mining minigame forced exit processing
MiningGame:SetBonusGame -- Sets bonus game mode and UI configuration
MiningGame:HandleButtonClickEvent -- Mining minigame start button click event
MiningGame:HandleKeyDownEvent -- E key input for mining game start/timing event
MiningGame:HandleKeyDownEvent2 -- ESC key input for mining game cancel event
MiningTargetManager:SpawnRandomMiningTarget -- Spawns mining targets at random locations on map
MiningTargetManager:OnBeginPlay -- Mining target manager initialization
MiningTargetObject:OnBeginPlay -- Mining target object initialization and setup
MiningTargetObject:SetActivateEntity -- Sets mining target entity activation/deactivation
MiningTargetObject:SetSpriteRUID -- Sets mining target sprite and rendering layer
MiningTargetObject:GiveReward -- Processes reward provision to player when mining succeeds
MiningTargetObject:DropItem -- Processes basic mineral item drop during mining
MiningTargetObject:DropJewerly -- Processes jewelry item drop as bonus reward
MiningTargetObject:DropFossilBox -- Processes fossil item drop as bonus reward
MiningTargetObject:DropMoneyBox -- Processes gold box drop as bonus reward
MiningTargetObject:DropRelicBox -- Processes relic box drop as bonus reward
MiningTargetObject:SetUI_KeyboxSuccess -- Displays result UI when keybox succeeds
MiningTargetObject:DropMaterial -- Processes special material item drop
MiningTargetObject:DropChair -- Processes chair item drop as bonus reward
MiningTargetObject:SetPanel -- Sets interaction panel UI of mining target object
MiningTargetObject:OnInteractionEvent -- Handles when player interacts with mining target
MiningTargetObject:OnInteractionEventOnClient -- Handles mining minigame start on client
MiningTargetObject:RemoveVisitRecord -- Removes player's mining target visit record
MiningTargetObject:SetUI_GoldBoxResult -- Displays gold box opening result UI
MiningTargetObject:SetUI_RelicBoxResult -- Displays relic box opening result UI
MiningTargetObject:Init -- Mining target object initialization (used in inspector)
MiningTargetObject:HandleInteractionEvent -- Handles mining target interaction event
MiningTargetObject:HandleInteractionEnterEvent -- Displays guide UI when approaching mining target
MiningTargetObject:HandleInteractionLeaveEvent -- Deactivates guide UI when moving away from mining target
LightComponent:OnBeginPlay -- Light component initialization - loads user light data and disables interaction
LightComponent:TurnOn -- Turn on light - changes state and saves data
LightComponent:makeTriggerEnable -- Activates/deactivates trigger component based on light state
LightComponent:SaveLightOnData -- Asynchronously saves light on/off data to user data storage
LightComponent:LoadLightOnData -- Asynchronously loads light on/off data from user data storage
LightComponent:OnSyncProperty -- Updates trigger component state when turnedOn property is synchronized
LightInteraction:OnInteraction -- Executes light turn on when interacting with light
LightInteraction:HandleInteractionEnterEvent -- Creates and displays guide key UI when entering interaction
LightInteraction:HandleInteractionLeaveEvent -- Deactivates guide key UI when leaving interaction
ExtendPlayerControllerComponent:ActionDownJump -- Disables down jump usage (legacy or representative)
ExtendPlayerControllerComponent:ActionSit -- Uses chair function while sitting (only available in town)
ExtendPlayerControllerComponent:ActionDash -- Executes dash skill - MP consumption, cooldown, void item effect processing
ExtendPlayerControllerComponent:SitOnChair -- Sits on chair - disables gravity and adjusts position
ExtendPlayerControllerComponent:SitOnChair_Server -- Disables jump when sitting on chair on server
ExtendPlayerControllerComponent:OnBeginPlay -- Checks state and sets default values during component initialization
ExtendPlayerControllerComponent:Skill_Run -- Pet 2's running skill - duration and cooldown based on level
ExtendPlayerControllerComponent:OnUpdate -- Updates pet skill UI and processes various skill sustained effects every frame
ExtendPlayerControllerComponent:Skill_Superjump -- Pet 3's running jump skill - jump power proportional to gauge charge
ExtendPlayerControllerComponent:Skill_Flashjump -- Pet 4's air dash skill - MP consumption reduction based on level
ExtendPlayerControllerComponent:Skill_AirJump -- Pet 6's air jump skill - jumps upward while maintaining current Y velocity
ExtendPlayerControllerComponent:Skill_FastFall -- Pet 7's fast fall skill - fall speed proportional to level
ExtendPlayerControllerComponent:Skill_SlowFall -- Does not activate if mana is low
ExtendPlayerControllerComponent:ActionJump -- Temporarily disables gliding state then performs basic jump during basic jump
ExtendPlayerControllerComponent:HandleKeyDownEvent -- Executes various pet skills when key pressed (Shift: dash/air dash, Space: air jump, S: fast fall)
ExtendPlayerControllerComponent:HandleKeyDownEvent2 -- Second key press handler - running and running jump charging effects
ExtendPlayerControllerComponent:HandleKeyHoldEvent -- When holding key - running jump charging, acceleration, gliding skill processing
ExtendPlayerControllerComponent:HandleKeyUpEvent -- When releasing key - executes running jump, ends acceleration, ends gliding
ExtendPlayerControllerComponent:HandleFootholdCollisionEvent -- Resets air skill states when colliding with terrain (no reset for ladders or vertical surfaces)
ExtendPlayerControllerComponent:HandleStateChangeEvent -- Resets air skills when state change occurs in special available state
ExtendPlayerControllerComponent:HandleFootholdLeaveEvent -- Event generated when falling from terrain (currently empty)
PlayerConstruction:OnBeginPlay -- Construction component initialization - table list and type setup
PlayerConstruction:SetTableClient -- Full synchronization of table data from server to client
PlayerConstruction:SetTableElementClient -- Synchronizes specific index value of table from server to client
PlayerConstruction:ClearTableClient -- Resets all client table to default values
PlayerConstruction:ChangedTable -- Refreshes construction shop UI and sends construction event when table changes
PlayerConstruction:LoadedData -- Loads construction data from database and handles achievements
PlayerConstruction:UnlockConstruction -- Construction unlock - pays cost then unlocks and handles achievements
PlayerConstruction:BuyConstruction -- Construction purchase (level up) - pays cost then increases level and handles achievements
PlayerConstruction:PlayPurchaseDirection -- Plays purchase/unlock effect - unlock or expectation effect based on type
PlayerData:OnBeginPlay -- Player data component initialization and data loading from server
PlayerData:OnSyncProperty -- Refreshes related UI when synchronized properties change
PlayerData:OnEndPlay -- Saves player data when game ends
PlayerData:OnUpdate -- Saves data every 3-5 minutes
PlayerData:LoadData -- Loads player data from database and retries on failure
PlayerData:SaveData -- Does not save data if exiting due to data load failure
PlayerData:SellAllItems -- Sells all items in player bag and calculates bonus
PlayerData:UseMoney -- Deducts player money
PlayerData:GetMoney -- Provides money to player and plays sound
PlayerData:AddEquipment -- Purchases equipment and adds to inventory
PlayerData:ChangeEquipment -- Changes equipped equipment and synchronizes to client
PlayerData:ApplyPlayerStatus -- Does not execute if data has not been loaded yet
PlayerData:ChangeTownProgress -- Changes specific town progress to completed state
PlayerData:PurchaseTownAdmission -- Checks possession status
PlayerData:ChangeEquipmentAvatarOnServer -- Changes character appearance based on equipped equipment
PlayerData:AddPetEgg -- Increases pet egg count by 1
PlayerData:SetStatusUI -- Displays player stats in UI and updates mining power HUD
PlayerData:Reborn -- Condition validation
PlayerData:PlayRebornDirection -- Plays rebirth effect UI
PlayerData:SetTableClient -- Applies table data received from server on client
PlayerData:SetTableElementClient -- Applies specific index value of table received from server on client
PlayerData:ClearTableClient -- Resets all client table to default values
PlayerData:ChangedTable -- Refreshes related UI and states when table changes
PlayerData:ClearAllProperty -- Initializes all equipment and town progress during rebirth (except town 1)
PlayerData:LoadedUserData -- Synchronizes all table data to client after data loading is complete
PlayerData:OnMapEnter -- Updates ruins visit record and plays guide when entering map
PlayerData:RefreshUIHUDMoney -- Refreshes money display in HUD to current held amount
PlayerData:RefreshUIShop -- Refreshes shop UI only for local player
PlayerData:SetUIEquipmentPurchaseChecking -- Shows confirmation popup and effect after equipment purchase completion
PlayerData:PurchaseEquipmentBundle -- Processes bundle purchase of selected equipment at once
PlayerData:PlayDirection_EquipmentBundlePurchase -- Plays equipment bundle purchase completion effect
PlayerData:UseCharonsBoat -- Uses Charon's Boat - cheat function that consumes pet eggs to unlock all towns and equipment
PlayerIngameData:OnMapEnter -- Map type-specific initialization, UI update, and temple floor management when entering map
PlayerIngameData:InitIngamePropertiesOnClient -- Client state initialization and UI activation when starting in-game
PlayerIngameData:InitIngamePropertiesOnServer -- Function executed after loading ends when entering dungeon
PlayerIngameData:CleanupIngameProperties -- Function executed in town when respawning after death or first entering game
PlayerIngameData:OnUpdate -- Processes MP recovery, HP reduction, depth measurement, cave visibility calculation every frame
PlayerIngameData:OnSyncProperty -- Updates related UI and states when synchronized properties change
PlayerIngameData:SetHPStausAtMine -- Processes HP reduction in mines (exceptions for admin and Hades temple)
PlayerIngameData:SetHPandMPUI -- Updates HP, MP UI and shield icon to match current values
PlayerIngameData:Die -- Makes player entity die
PlayerIngameData:SetActivationIngameUI -- Activates/deactivates vision darkness effect and record UI based on in-game state
PlayerIngameData:SetResultUI -- Sets result window UI on death or escape (displays records and item information)
PlayerIngameData:SetRecordUI -- Updates survival time and depth (or floor) information displayed at top during in-game
PlayerIngameData:SetBlindRatio -- Sets screen darkness level based on light intensity in cave
PlayerIngameData:Hit -- Uses shield and processes health reduction when taking damage
PlayerIngameData:FinishAdventure -- Deactivates in-game state and control when adventure ends
PlayerIngameData:SetNearBonfire -- Sets whether near bonfire (health recovery near bonfire)
PlayerIngameData:UpdateDepthRecord -- Calculates exploration depth using current position and updates record
PlayerIngameData:UnprotectedHit -- Use this function for damage that doesn't apply shield (poison damage, etc.)
PlayerIngameData:PopupMapEnteringUI -- Displays map name and description with fade in/out animation when entering map
PlayerIngameData:SetWarningUI -- Shows/hides warning UI when health is 25% or below
PlayerIngameData:UseMP -- Function called when using MP for dash, etc.
PlayerIngameData:GetProtector -- Increases shield count by 1
PlayerIngameData:SetHPUseAmount -- Sets HP reduction per second for current mine/temple
PlayerIngameData:CleanupIngamePropertiesOnServer -- Cleans up in-game state on server (currently empty)
PlayerIngameData:SetChairBuffIdx -- Sets chair crowd buff index
PlayerIngameData:InitTempleTable -- Initializes temple list and selects random temple excluding recently visited temple
PlayerIngameData:GetTempleTable -- Selects and returns randomly from remaining temple list
PlayerIngameData:RecoverHP -- Recovers HP by specified amount (prevents exceeding maximum)
PlayerIngameData:AddCurrentTempleFloor -- Advances to upper floor in temple or performs floor reset
PlayerIngameData:resetPlayerSpeed -- Restores player movement speed in Hades temple, etc.
PlayerIngameData:HandleTriggerStayEvent -- Handles light brightness/health recovery when touching lighting object and bonfire
PlayerInstallationObject:OnBeginPlay -- Sets all exploration tool counts to 0 during component initialization
PlayerInstallationObject:RefreshNumUI -- Refreshes exploration tool UI icons and count display on PC and mobile
PlayerInstallationObject:UseObject -- Decreases specified exploration tool count by 1 and refreshes UI
PlayerInstallationObject:AddObject -- Recovers mana instead of torch if pet 1 is owned + skill in use
PlayerInstallationObject:SpawnRope -- Installs rope - lasts 10 seconds at position 3 units below player position
PlayerInstallationObject:SpawnTrampoline -- Installs trampoline - lasts 10 seconds at position 1 unit above player position
PlayerInstallationObject:UseTorch -- Removes already spawned torch if exists and removes reserved timer
PlayerInstallationObject:UsePotion -- Uses health recovery potion - recovers 15% of maximum health
PlayerInstallationObject:DisacardAllItems -- Discards all exploration tools (called when moving to town)
PlayerInstallationObject:SetTorchBrightnessInit -- Initializes brightness value of corresponding lighting object when torch is deleted
PlayerInstallationObject:OnMapEnter -- Initializes exploration tools and torch state when entering map
PlayerInstallationObject:UseTorchPet -- Pet 1's torch skill on/off toggle (continuously consumes MP)
PlayerInstallationObject:OnUpdate -- Consumes MP every frame when using pet torch (decreases based on level)
PlayerInstallationObject:SpawnTorchByPetSkill -- Handles torch creation/removal by pet skill
PlayerInstallationObject:HandleKeyUpEvent -- Uses various exploration tools with number keys (1-4 keys)
PlayerStateAtStage:OnMapEnter -- Sets stage-specific debuff UI and environment initialization when entering map
PlayerStateAtStage:OnUpdate -- Updates player status effects and environmental debuffs every frame
PlayerStateAtStage:GetMaterial -- Add count
PlayerStateAtStage:SellAllMaterial -- Check held quantity
PlayerStateAtStage:LoseMaterial -- Consumes held materials (icicles, star fragments, cloud fragments, golden apples)
PlayerStateAtStage:Poisoned -- Makes poisoned state and sets duration
PlayerStateAtStage:FreezePlayer -- Freezes player for 2 seconds making movement impossible when 10 cold stacks are achieved
PlayerStateAtStage:ElectricDamage -- Increases damage based on stack and changes appearance when taking electric damage
PlayerStateAtStage:StartExitedMode -- Activates 'Excited!' mode when obtaining 10 star fragments in stage 6, allowing dash without MP consumption for 15 seconds
PlayerStateAtStage:StartExitedModeOnServer -- Sets 'Excited!' mode MP consumption to 0 on server and restores after duration
PlayerStateAtStage:RemoveThirstyStack -- Removes thirst stack by drinking water from puddle in stage 8
PlayerStateAtStage:GetBurnStack -- Adds burn stack in stage 5 - damage increases by stages, offset by moisture stack
PlayerStateAtStage:GetWetStack -- Removes all burn stacks and adds moisture shield when touching water in stage 5
PlayerStateAtStage:GetCurseStack -- Adds curse stack every 30 seconds in stage 9 (ruins) - increases health consumption by 10% each
PlayerStateAtStage:InitAllState -- Initializes all debuffs and status effects and removes related effects and UI
PlayerStateAtStage:GetThirstyStack -- Adds thirst stack every 5 seconds in stage 8 - reduces movement speed
PlayerStateAtStage:SetUI_HavingMaterialNum -- Updates stage-specific material holding amount in UI
PlayerStateAtStage:OnBeginPlay -- Sets basic configuration values during component initialization
PlayerStateAtStage:HitBySquid -- Screen effects and control restrictions when hit by squid ink in stage 5
PlayerStateAtStage:GetRotationShield -- Creates rotation shield obtained with 10 cloud fragments in stage 7 (maximum 6)
PlayerStateAtStage:RemoveRotationShield -- Removes rotation shield at specified index
PlayerStateAtStage:Enchanted -- Aphrodite charm effect in stage 6 - reverses left/right control keys
PlayerStateAtStage:GetSnownStack -- Becomes snowman when frozen in Demeter temple and escapes by rapidly pressing left/right buttons
PlayerStateAtStage:Diving -- Creates oxygen gauge and bubbles when diving in stage 2 sea
PlayerStateAtStage:OnMapLeave -- Initializes temple-specific settings when leaving map
PlayerStateAtStage:HandleKeyReleaseEvent -- Removes arrow effect when releasing key in charmed state
PlayerStateAtStage:HandleKeyDownEvent -- Handles key input in charmed state or snowman state
PlayerStateAtStage:HandleBodyActionStateChangeEvent -- Additional processing based on player action state changes
StatusListUI:RefreshUI -- Refreshes stats list UI - displays base values, bonuses, and total stats
StatusListUI:HandleKeyDownEvent -- Closes stats list UI when ESC key is pressed
AccessoryLogic:GetAccessoryInfo -- Receives accessory information stored in string format and returns in table format.
AccessoryLogic:WrapAccessoryInfoToString -- Receives accessory information used in actual calculations and returns in string format.
AccessoryLogic:SetStatus -- Stat values are determined within 80% to 120% range.
AccessoryMergeShopUI:RefreshMainPanel -- Refreshes main panel - updates material slots, result grade, and synthesis button state
AccessoryMergeShopUI:ShowMaterialListPanel -- Shows material selection panel - creates list of items available for synthesis
AccessoryMergeShopUI:RegistMaterial -- Registers material to waiting slot and updates main panel
AccessoryMergeShopUI:InitAllSetting -- Initializes all settings - resets material slots, grade, and waiting index
AccessoryMergeShopUI:PlayDirection_Merge -- Plays accessory synthesis effect - effects, sound, result window display
AccessoryMergeShopUI:HandleButtonClickEvent -- First material slot click - opens material selection list and sets to waiting state
AccessoryMergeShopUI:HandleButtonClickEvent2 -- Second material slot click - opens material selection list and sets to waiting state
AccessoryMergeShopUI:HandleButtonClickEvent3 -- Synthesis button click - verifies material readiness then executes accessory synthesis
AccessoryMergeShopUI:HandleButtonClickEvent4 -- Reset button click - initializes all settings then refreshes main panel
AccessoryMergeShopUI:HandleKeyDownEvent -- Closes material selection panel or shop when ESC key is pressed
AccessoryMergeShopUI_SelectMaterialSlotButton:HandleButtonClickEvent -- Selects corresponding material and registers it in synthesis window when material slot button is clicked
PlayerAccessory:OnBeginPlay -- Accessory component initialization - table list and type setup
PlayerAccessory:SetTableClient -- Full synchronization of table data from server to client
PlayerAccessory:SetTableElementClient -- Synchronizes specific index value of table from server to client
PlayerAccessory:ClearTableClient -- Resets all client table to default values
PlayerAccessory:ChangedTable -- Refreshes equipment storage UI when table changes
PlayerAccessory:LoadedData -- Loads accessory data from database then sets complete state, equipped index, and proficiency
PlayerAccessory:GetItems -- Obtains accessories - sorts and inserts by part/grade/set/stats order
PlayerAccessory:EquipItem -- Equips/unequips accessory - applies stats and synchronizes to client
PlayerAccessory:UpgradeProficiency -- Upgrades accessory proficiency - uses 3 rare grade or higher accessories
PlayerAccessory:PlayUpgradeProficiencyDirection -- Plays proficiency upgrade effect
PlayerAccessory:OpenAccessoryBox -- Opens accessory box - generates random part/grade/set
PlayerAccessory:PlayDirection_AccessoryBoxOpen -- Plays accessory box opening effect
PlayerAccessory:MergeItems -- Accessory synthesis - creates accessory 1 grade higher from 2 materials (below rare)
PlayerAccessory:PlayMergeDirection -- Plays accessory synthesis effect
ChairBuffNova:OnBeginPlay -- Chair buff nova start - plays effect and auto-deletes after 0.5 seconds
ChairBuffNova:HandleTriggerEnterEvent -- Applies chair buff when player touches buff nova (excluding original owner)
ChairStorageUI:OnBeginPlay -- Chair storage UI initialization - duplicates chair slots to create list
ChairStorageUI:RefreshUI -- Full UI refresh - updates equipped chair, held list, stats, collection count
ChairStorageUI:ShowDetailInfoPopup -- Shows chair detail information popup - displays name, description, stats, buffs
ChairStorageUI:HandleButtonClickEvent -- Close/cancel button click - resets selection index and refreshes UI
ChairStorageUI:HandleButtonClickEvent2 -- Equip button click - changes equip target to selected chair
ChairStorageUI:HandleButtonClickEvent3 -- Probably detail popup close button - resets selection index and refreshes UI
ChairStorageUI:HandleKeyDownEvent -- Closes chair storage UI when ESC key is pressed
ChairStorageUI_EquipButton:HandleButtonClickEvent -- Changes equip target to corresponding chair when chair equip button is clicked
ChairStorageUI_SlotButton:HandleButtonClickEvent -- Shows detail information popup for corresponding chair when chair slot button is clicked
PlayerChair:OnBeginPlay -- Chair component initialization and basic chair entity creation
PlayerChair:OnSyncProperty -- Updates entity and UI when equipped chair index changes
PlayerChair:SetSitEnable -- Sets chair sitting enabled/disabled - disables gravity, shows sprite
PlayerChair:AddItem -- Obtains chair - gem reward for duplicate acquisition, log output, stat application
PlayerChair:ChangeEquipedItem -- Changes equipped chair - verifies possession then updates equipped index
PlayerChair:ApplyEquipedChairEntity -- Applies equipped chair to actual entity - sprite and position settings
PlayerChair:SetSortingOrder -- Sets rendering order for chair parts - distinguishes front and back layers
PlayerChair:OnUpdate -- Measures time sitting in chair and triggers buff every 30 seconds
PlayerChair:GenerateChairBuff -- Creates chair crowd buff nova - buff effect and nova creation after sitting for 30 seconds
PlayerChair:SetTableClient -- Full synchronization of table data from server to client
PlayerChair:SetTableElementClient -- Synchronizes specific index value of table from server to client
PlayerChair:ClearTableClient -- Resets all client table to default values
PlayerChair:ChangedTable -- Refreshes related UI when table changes
PlayerChair:ClearAllProperty -- Initializes all chair data on entry/rebirth
PlayerChair:LoadedUserData -- Loads chair data from database then synchronizes to client
PlayerChair:HandleChangedLookAtEvent -- Adjusts chair position and direction when player's look direction changes
PlayerChair:HandleOrderInLayerChangedEvent -- Updates chair rendering order when rendering order changes (currently disabled)
PlayerChair:HandleSortingLayerChangedEvent -- Updates chair rendering layer when rendering layer changes (currently disabled)
PlayerChair:HandleKeyDownEvent -- Gets up from chair and activates gravity when movement key is pressed
CollectionOpenButton:HandleButtonClickEvent -- Handles collection UI open button click
CollectionSlotButton:HandleButtonClickEvent -- Handles showing item detail information when collection slot is clicked
CollectionUI:OnBeginPlay -- Collection UI initial setup (creates item slots)
CollectionUI:OnUpdate -- Checks and processes UI refresh request flag
CollectionUI:RefreshUI -- Sets UI refresh flag
CollectionUI:RefreshUI_Inner -- Full collection UI refresh (drop item list)
CollectionUI:RefreshDescUI -- Initializes collection description panel
CollectionUI:SetDescUI -- Displays detailed information of selected item in description panel
CollectionUI:HandleKeyDownEvent -- Handles closing collection UI when ESC key is pressed
PlayerCollection:OnBeginPlay -- Collection component initialization and drop item initial setup
PlayerCollection:RecordData -- Records drop item acquisition data and synchronizes to client
PlayerCollection:SetTableClient -- Synchronizes table data sent from server to client
PlayerCollection:SetTableElementClient -- Synchronizes specific table element sent from server to client
PlayerCollection:ClearTableClient -- Initializes client table to set all values to defaults
PlayerCollection:ChangedTable -- Handles related UI refresh when table changes
PlayerCollection:ClearAllProperty -- Initializes all drop item collection data
PlayerCollection:LoadedUserData -- Loads saved user data to restore collection state
ConstructionObject:OnBeginPlay -- Construction object initialization and display setup
ConstructionObject:RefreshEntityEnable -- Updates object activation state based on construction level
ConstructionObject:SetNametagLocalization -- Sets construction object name tag localization
ConstructionObject:HandleLocalPlayerConstructed -- Updates object state when receiving player construction completion event
ConstructionShopUI:RefreshUI -- Full construction shop UI refresh (currency, list, state, etc.)
ConstructionShopUI:SetBuyCheckPopup -- Sets construction/level up confirmation popup UI
ConstructionShopUI:SetUnlockCheckPopup -- Sets construction facility unlock confirmation popup UI
ConstructionShopUI:PlayUnlockDirection -- Construction facility unlock success effect and toast message display
ConstructionShopUI:PlayPurchaseDireciton -- Construction/level up success effect and toast message display
ConstructionShopUI:HandleButtonClickEvent3 -- Handles actual purchase when construction/level up confirmation button is clicked
ConstructionShopUI:HandleButtonClickEvent5 -- Handles actual unlock when unlock confirmation button is clicked
ConstructionShopUI:HandleKeyDownEvent -- Handles closing shop UI when ESC key is pressed
ConstructionShopUI_BuyButton:HandleButtonClickEvent -- Handles showing confirmation popup when construction/level up button is clicked
ConstructionShopUI_UnlockButton:HandleButtonClickEvent -- Handles showing confirmation popup when construction facility unlock button is clicked
DailyRewardReceiveButton:HandleButtonClickEvent -- Handles daily reward receive button click
DailyRewardUI:RefreshUI -- Full daily reward UI refresh (progress, button state, etc.)
DailyRewardUI:OnUpdate -- Real-time calculation and display of remaining time until next reward
DailyRewardUI:HandleButtonClickEvent -- Handles reward description panel toggle button click
DailyRewardUI:HandleKeyDownEvent -- Handles closing daily reward UI when ESC key is pressed
PlayerDailyRewardComponent:OnBeginPlay -- Daily reward component initialization and table setup
PlayerDailyRewardComponent:ClearAllProperty -- Initializes all daily reward receive states
PlayerDailyRewardComponent:SetTableClient -- Synchronizes table data sent from server to client
PlayerDailyRewardComponent:SetTableElementClient -- Synchronizes specific table element sent from server to client
PlayerDailyRewardComponent:ChangedTable -- Handles related UI refresh when table changes
PlayerDailyRewardComponent:LoadedUserData -- Loads saved user data to restore daily reward state
PlayerDailyRewardComponent:RefreshDailyRewardTime -- Updates daily reward progress based on current date
PlayerDailyRewardComponent:GiveReward -- Provides daily reward for corresponding date to player
PlayerDailyRewardComponent:OnSyncProperty -- Handles UI refresh when synchronized properties change
PlayerDailyRewardComponent:DateToNumber -- Converts year/month/day to number for date calculations
PlayerDailyRewardComponent:RefreshDailyRewardTimeOnCheat -- Updates daily reward progress by manipulating date with cheat function
EmblemStorageUI:RefreshUI -- Full emblem storage UI refresh (list, RP, ranking, title)
EmblemStorageUI:HandleButtonClickEvent -- Handles emblem storage refresh button click
EmblemStorageUI:HandleKeyDownEvent -- Handles closing emblem storage UI when ESC key is pressed
PlayerEmblem:OnBeginPlay -- Emblem component initialization and ranking title entity creation
PlayerEmblem:SetTableClient -- Synchronizes table data sent from server to client
PlayerEmblem:SetTableElementClient -- Synchronizes specific table element sent from server to client
PlayerEmblem:ClearTableClient -- Initializes client table to set all values to defaults
PlayerEmblem:ChangedTable -- Handles related UI refresh when table changes
PlayerEmblem:LoadedData -- Loads saved user data to restore emblem state
PlayerEmblem:AddItems -- Adds specified emblem to inventory and calculates RP
PlayerEmblem:CalculateRP -- Calculates sum of owned emblem levels to determine RP
PlayerEmblem:GetRank -- Queries leaderboard to determine own ranking position
PlayerEmblem:SetRankTitleEntity -- Sets and displays title entity based on ranking
PlayerEmblem:PurchaseWithLegacyCoins -- Purchases random emblem using legacy coins
PlayerEmblem:PlayExchangeDirection -- Plays legacy coin exchange result UI effect
PlayerEmblem:OnSyncProperty -- Handles UI refresh when synchronized properties change
EmoticonPlayButton:HandleButtonClickEvent -- Handles equipped emoticon play button click
EmoticonShopUI:OnUpdate -- Checks and processes UI refresh request flag
EmoticonShopUI:RefreshUI -- Sets UI refresh flag
EmoticonShopUI:RefreshUI_Inner -- Full emoticon shop UI refresh (tokens, button state)
EmoticonShopUI:SetGachaResultUI -- Sets and displays gacha result UI
EmoticonShopUI:OnBeginPlay -- Emoticon shop UI initialization
EmoticonShopUI:HandleButtonClickEvent -- Handles emoticon purchase button click (condition verification and new emoticon acquisition)
EmoticonShopUI:HandleKeyDownEvent -- Handles closing shop UI when ESC key is pressed
EmoticonStorageChangeEquipedSlotButton:HandleButtonClickEvent -- Handles emoticon equipment slot change button click
EmoticonStorageSlotButton:HandleButtonClickEvent -- Handles emoticon storage slot selection button click
EmoticonStorageUI:OnBeginPlay -- Emoticon storage UI initial setup (creates storage/equipment slots)
EmoticonStorageUI:OnUpdate -- Checks and processes UI refresh request flag
EmoticonStorageUI:RefreshUI -- Sets UI refresh flag
EmoticonStorageUI:RefreshUI_Inner -- Full emoticon storage UI refresh (storage/equipment list)
EmoticonStorageUI:SelectStorageSlot -- Handles selected emoticon slot in storage
EmoticonStorageUI:ChangeEquipedSlot -- Changes selected emoticon to specified equipment slot
EmoticonStorageUI:HandleKeyDownEvent -- Handles closing storage UI when ESC key is pressed
PlayerEmoticon:OnBeginPlay -- Emoticon component initialization and server/client-specific setup
PlayerEmoticon:PlayEmoticon -- Displays equipped emoticon on screen with fade in/out animation
PlayerEmoticon:SetEmoticonUI -- Reflects equipped emoticon information to UI for screen refresh
PlayerEmoticon:ChangeEquipedSlot -- Equips owned emoticon to specified slot
PlayerEmoticon:GetNewEmot -- Acquires new emoticon using emote token
PlayerEmoticon:UseEmotToken -- Processes emote token consumption
PlayerEmoticon:SetTableClient -- Synchronizes table data sent from server to client
PlayerEmoticon:SetTableElementClient -- Synchronizes specific table element sent from server to client
PlayerEmoticon:ClearTableClient -- Initializes client table to set all values to defaults
PlayerEmoticon:ChangedTable -- Handles related UI refresh when table changes
PlayerEmoticon:ClearAllProperty -- Initializes all emoticon-related properties
PlayerEmoticon:LoadedUserData -- Loads saved user data to restore emoticon state
PlayerEmoticon:OnSyncProperty -- Handles UI refresh when synchronized properties change
PlayerEmoticon:SetUIGachaResult -- Displays gacha result UI for newly acquired emoticon
EquipmentStorageUI:OnBeginPlay -- Equipment storage UI initialization
EquipmentStorageUI:RefreshUI -- Refreshes equipment storage UI to match current state
EquipmentStorageUI:Refresh_Normal -- Refreshes normal equipment tab UI
EquipmentStorageUI:Refresh_Mythic -- Refreshes mythic equipment tab UI
EquipmentStorageUI:Refresh_Accessory -- Refreshes accessory tab UI
EquipmentStorageUI:ShowNormalEquipmentDetailInfo -- Shows normal equipment detail information popup
EquipmentStorageUI:ShowBeadsDetailInfo -- Shows mythic equipment bead detail information popup
EquipmentStorageUI:ApplyAvatarInfo -- Applies avatar appearance based on currently equipped equipment
EquipmentStorageUI:SetFilterIdx -- Sets equipment storage filter index to change tab
EquipmentStorageUI:SetSecondFilterIdx -- Sets equipment storage second filter index to change sub-category
EquipmentStorageUI:ShowAccessoryDetailInfo -- Shows accessory detail information popup
EquipmentStorageUI:RefreshAccessoryGradeupPanel -- Refreshes accessory proficiency upgrade panel
EquipmentStorageUI:SelectAccessoryGradeupMaterial -- Selects material to use for accessory proficiency upgrade
EquipmentStorageUI:PlayAccessoryGradeupDirection -- Plays accessory proficiency upgrade effect
EquipmentStorageUI:HandleButtonClickEvent -- Handles normal equipment filter button click event
EquipmentStorageUI:HandleButtonClickEvent2 -- Handles mythic equipment filter button click event
EquipmentStorageUI:HandleButtonClickEvent5 -- Handles accessory filter button click event
EquipmentStorageUI:HandleButtonClickEvent6 -- Handles bead detail information button click event
EquipmentStorageUI:HandleButtonClickEvent7 -- Handles normal equipment filter button click event (duplicate)
EquipmentStorageUI:HandleButtonClickEvent8 -- Handles equipment equip button click event
EquipmentStorageUI:HandleButtonClickEvent9 -- Handles equipment unequip button click event
EquipmentStorageUI:HandleButtonClickEvent3 -- Handles accessory equip button click event
EquipmentStorageUI:HandleButtonClickEvent4 -- Handles accessory unequip button click event
EquipmentStorageUI:HandleButtonClickEvent10 -- Handles accessory proficiency upgrade material reset button click event
EquipmentStorageUI:HandleButtonClickEvent11 -- Handles accessory proficiency upgrade material slot 1 select button click event
EquipmentStorageUI:HandleButtonClickEvent12 -- Handles accessory proficiency upgrade material slot 2 select button click event
EquipmentStorageUI:HandleButtonClickEvent13 -- Handles accessory proficiency upgrade material slot 3 select button click event
EquipmentStorageUI:HandleButtonClickEvent14 -- Handles accessory proficiency upgrade execute button click event
EquipmentStorageUI:HandleButtonClickEvent15 -- Handles accessory proficiency upgrade confirm button click event
EquipmentStorageUI:HandleButtonClickEvent16 -- Handles accessory proficiency upgrade cancel button click event
EquipmentStorageUI:HandleKeyDownEvent -- Handles closing equipment storage UI when ESC key is pressed
EquipmentStorageUI_AccessoryProficiencyUp_SlotSelectButton:HandleButtonClickEvent -- Handles accessory proficiency upgrade material selection button click event
EquipmentStorageUI_AccessorySlotButton:HandleButtonClickEvent -- Handles showing detail information when accessory slot button is clicked
EquipmentStorageUI_MythicItemMouseHover:SetHoverUI -- Sets tooltip UI display when mouse hovers over mythic equipment item
EquipmentStorageUI_MythicItemMouseHover:HandleButtonStateChangeEvent -- Handles hover UI display when mythic equipment item button state changes
EquipmentStorageUI_SecondFilterButton:HandleButtonClickEvent -- Handles equipment storage second filter button click event
PlayerMythicEquipment:OnBeginPlay -- Sets table list and type information during component initialization to prepare client synchronization
PlayerMythicEquipment:SetTableClient -- Synchronizes table data received from server on client side and refreshes UI
PlayerMythicEquipment:SetTableElementClient -- Updates specific index element of table on client and parses according to type
PlayerMythicEquipment:ClearTableClient -- Clears entire table to initial values on client side and refreshes UI
PlayerMythicEquipment:ChangedTable -- Refreshes corresponding UI component when table data changes
PlayerMythicEquipment:LoadedData -- Loads saved user data to restore mythic equipment level and element information and synchronizes to client
PlayerMythicEquipment:PurchaseMythicEquipment -- Upgrades specified mythic equipment level, deducts cost, acquires elements, and plays effect
PlayerMythicEquipment:PlayPurchaseDirection -- Plays upgrade effect on client after equipment purchase completion
PlayerMythicEquipment:RedistributionPowerOfGod -- Randomly redistributes selected divine stones to change equipment's element composition
PlayerMythicEquipment:PlayRedistributionDirection -- Plays divine stone redistribution effect on client and temporarily disables UI buttons
PlayerMythicEquipment:RedistributionDirection_Inner -- Internal function that handles individual divine stone redistribution animation
PlayerMythicEquipment:UnlockUpgradeLimit -- Uses golden key to unlock mythic equipment upgrade level limit
PlayerMythicEquipment:PlayUnlockDirection -- Plays unlock effect on client after level limit release completion
PlayerMythicEquipment:ResetPropertiesByReborn -- Initializes all mythic equipment levels and element information during rebirth and synchronizes to client
InfiniteQuestUI:OnBeginPlay -- Infinite quest UI initialization and basic setup
InfiniteQuestUI:FoldUI -- Handles infinite quest UI fold/unfold toggle
InfiniteQuestUI:HandleKeyDownEvent -- Handles quest reward claim and UI folding with Tab key input
InfiniteQuestUI:HandleButtonClickEvent2 -- Handles new quest start button click event
PlayerInfiniteQuest:GetNewQuest -- Creates and sets new infinite quest appropriate for player level
PlayerInfiniteQuest:GetReward -- Provides reward when quest completes and starts new quest
PlayerInfiniteQuest:GetScore -- Adds quest progress score
PlayerInfiniteQuest:UpdateQuestUI -- Updates UI according to quest progress
PlayerInfiniteQuest:NewQuestAlert -- Plays notification effect when new quest starts
PlayerInfiniteQuest:OnSyncProperty -- Handles UI update when quest-related properties are synchronized
PlayerInfiniteQuest:PlayRewardDirection -- Plays effect when quest reward is acquired
PlayerInfiniteQuest:OnMapEnter -- Adjusts quest UI position when entering map
EquipmentStorageUI_NormalSlotButton:HandleButtonClickEvent -- Handles showing detail information when normal equipment slot button is clicked
InventoryEquipedSlotButton:HandleButtonClickEvent -- Handles showing detail information when inventory equipped slot button is clicked
InventorySlotButton:HandleButtonClickEvent -- Handles showing detail information when inventory slot button is clicked
InventoryUI:OnBeginPlay -- Inventory UI initialization and slot creation
InventoryUI:OnUpdate -- Checks UI refresh every frame
InventoryUI:RefreshUI -- Requests inventory UI refresh
InventoryUI:RefreshUI_Inner -- Handles actual inventory UI refresh processing
InventoryUI:SetFilterIdx -- Sets inventory filter index to change tab
InventoryUI:SetDetailInfoUI -- Sets UI that displays detailed information of selected slot
InventoryUI:RefreshStatusInfoUI -- Displays player status information in UI
InventoryUI:SetFilterButtonEnable -- Sets filter button activation state based on current map
InventoryUI:SetDetailInfoUI_RelicBox -- Sets UI that displays detailed information of relic box
InventoryUI:HandleKeyDownEvent -- Handles keyboard input events (I key to open/close inventory, ESC key to close popup)
InventoryUI:HandleButtonClickEvent2 -- Handles mineral filter button click event
InventoryUI:HandleButtonClickEvent3 -- Handles equipment filter button click event
InventoryUI:HandleButtonClickEvent4 -- Handles chair filter button click event
InventoryUI:HandleButtonClickEvent5 -- Handles pet filter button click event
PlayerBackpack:AddItem -- Adds items to player considering backpack capacity and luck stats
PlayerBackpack:DiscardAllItem -- Discards all items in backpack and empties storage
PlayerBackpack:OnSyncProperty -- Refreshes corresponding UI components when backpack-related properties are synchronized
PlayerBackpack:OnBeginPlay -- Performs table setup and clears all items during backpack component initialization
PlayerBackpack:SetTableClient -- Sets table data received from server on client and applies related table changes
PlayerBackpack:SetTableElementClient -- Updates specific index element of table on client, parses type, and applies changes
PlayerBackpack:ClearTableClient -- Clears table to initial values on client and applies changes
PlayerBackpack:ChangedTable -- Refreshes related UI components when backpack table data changes
PlayerBackpack:ClearAllProperty -- Initializes all item storage information on server and synchronizes to client
PlayerBackpack:PlayAttackMotion -- Plays player attack motion and outputs different effects and sounds based on success/failure
PlayerBackpack:OnMapEnter -- Initializes visit records of mining targets on that map when player enters mine map
PlayerStorage:OnBeginPlay -- Player storage component initialization with table setup and consumable duration data preparation
PlayerStorage:SetTableClient -- Synchronizes table data received from server to client and refreshes related UI
PlayerStorage:SetTableElementClient -- Updates specific index element of table on client, parses type, and refreshes UI
PlayerStorage:ClearTableClient -- Clears entire table to initial values on client side and refreshes related UI
PlayerStorage:ChangedTable -- Refreshes all related UI components when table data changes
PlayerStorage:LoadedUserData -- Loads saved user data to restore consumable, currency, and start time information and synchronizes to client
PlayerStorage:AddCurrencyItems -- Adds specified currency items to player and determines special effect playback
PlayerStorage:PlayGainGemsDirection -- Plays visual effect on client when gems are acquired to display acquisition amount
PlayerStorage:AddConsumableItems -- Adds consumable items to player and outputs log message
PlayerStorage:UseCurrencyItems -- Consumes player's currency items and saves data with client synchronization
PlayerStorage:UseConsumableItem -- Handles consumable item usage: executes type-specific logic for contracts, sprinkles, accessory boxes, etc.
PlayerStorage:GetConvertedTimeFromUTC -- Converts UTC time to accumulated time in seconds for consumable duration calculations
PlayerStorage:OnUpdate -- Checks consumable duration every frame and updates state every second
PlayerStorage:RefreshConsumableItemAbility -- Checks consumable duration to manage buff state and display buff icons in UI
PlayerStorage:ApplySprinkleItem -- Applies effect to all clients when sprinkle item is used and records start time
StorageUI:OnBeginPlay -- Performs component initialization on client
StorageUI:RefreshUI -- Refreshes entire storage UI to update filter, currency, and item information
StorageUI:Refresh_ConsumableItems -- Refreshes consumable item list and updates UI based on held quantities
StorageUI:Refresh_Minerals -- Refreshes mineral item list and updates UI based on held quantities
StorageUI:Refresh_Relics -- Refreshes relic item list to display purified/unpurified relics
StorageUI:ShowDetailPopup -- Opens detailed information popup for selected item and displays appropriate information based on filter
StorageUI:UseConsumableItem -- Uses selected consumable item or opens relic box to process result
StorageUI:PlayAccessoryBoxOpenDirection -- Executes accessory box opening effect with slot machine effect and result display
StorageUI:HandleButtonClickEvent -- Switches to consumable filter when first filter button is clicked
StorageUI:HandleButtonClickEvent2 -- Switches to mineral filter when second filter button is clicked
StorageUI:HandleButtonClickEvent3 -- Switches to relic filter when third filter button is clicked
StorageUI:HandleButtonClickEvent4 -- Initializes to consumable filter and refreshes every time storage UI is newly opened
StorageUI:HandleButtonClickEvent5 -- Handles using selected consumable when consumable use button is clicked
StorageUI:HandleKeyDownEvent -- Handles keyboard input: I key to open/close inventory, ESC key to close
StorageUI:HandleButtonClickEvent6 -- Handles UI open/close toggle when inventory shortcut button is clicked
StorageUI_SlotButton:HandleButtonClickEvent -- Handles showing detail information popup when warehouse slot button is clicked
PetComponent:OnBeginPlay -- Sets up animation and state system during pet component initialization
PetComponent:ChangeState -- Changes pet state to play appropriate animation
PetComponent:ChangePos -- Moves pet position based on player's look direction and plays animation
PetComponent:ChangeClimb -- Handles pet position and effects based on player's climbing or ladder climbing state
PetShopUI:OnBeginPlay -- Pet shop UI initialization and localization setup
PetShopUI:OnUpdate -- Checks UI refresh flag status and handles delayed update processing
PetShopUI:RefreshUI -- Activates UI refresh flag
PetShopUI:RefreshUI_Inner -- Displays player's pet egg holdings and updates UI state based on total pet ownership
PetShopUI:SetWarningPopup -- Activates popup that displays warning message
PetShopUI:ButtonEnable -- Sets activation state of pet egg open button
PetShopUI:SetUIGettingNewPet -- Displays pet image, grade, and description in new pet acquisition result UI and plays sound
PetShopUI:HandleButtonClickEvent2 -- Requests new pet acquisition after condition check when pet egg open button is clicked
PetShopUI:HandleKeyDownEvent -- Handles closing pet shop UI and all popups when ESC key is pressed
PetStorageUI:OnBeginPlay -- Slot duplication and basic data setup during pet storage UI initialization
PetStorageUI:OnUpdate -- Checks UI refresh flag status and handles delayed update processing
PetStorageUI:RefreshUI -- Activates UI refresh flag
PetStorageUI:RefreshUI_Inner -- Gathers all UI elements of pet storage and updates according to level, abilities, and equipment status
PetStorageUI:ChangeEquipedPet -- Equips pet at specified index and updates equipment button state in UI
PetStorageUI:ShowDetailInfo -- Shows detailed information popup for specified pet and updates level, abilities, skill information
PetStorageUI:HandleButtonClickEvent -- Handles pet detail information popup close button click event
PetStorageUI:HandleKeyDownEvent -- Handles closing popup or entire pet storage when ESC key is pressed
PetStorageUI_EquipButton:HandleButtonClickEvent -- Requests equipping pet at corresponding slot index when pet equip button is clicked
PetStorageUI_SlotInfoPopup:HandleButtonClickEvent -- Requests showing detailed information for corresponding slot when pet info popup button is clicked
PetStorageUI_UseSkillButton:PlayUseSkillButtonAnim -- Animation and visual update according to pet skill use button ON/OFF state
PetStorageUI_UseSkillButton:OnBeginPlay -- Sets circular image entity reference during skill button initialization
PetStorageUI_UseSkillButton:HandleButtonClickEvent -- Requests skill use state toggle when pet skill use button is clicked
PlayerPet:OnBeginPlay -- Player pet system initialization and pet entity creation
PlayerPet:OnSyncProperty -- Sets pet entity and updates UI when equipped pet index is synchronized
PlayerPet:ChangePetEntityParameter -- Sets pet entity appearance and animation according to equipped pet index
PlayerPet:EnablePetEntity -- Sets pet entity activation state to control show/hide
PlayerPet:ChangeEquipedPet -- Equips pet at specified index and applies stats
PlayerPet:GetNewPet -- Consumes pet egg to acquire random new pet and displays result UI
PlayerPet:SetTableClient -- Full table data synchronization from server to client
PlayerPet:SetTableElementClient -- Synchronizes only specific elements of table from server to client
PlayerPet:ClearTableClient -- Initializes all client table to default values
PlayerPet:ChangedTable -- Updates related UI and applies stats when table changes
PlayerPet:ClearAllProperty -- Resets all pet-related properties to initial values
PlayerPet:LoadedUserData -- Loads pet-related information from user data and applies to properties
PlayerPet:SetGettingNewPetResultUI -- Shows appropriate UI popup according to pet acquisition result type
PlayerPet:ChangePetSkillUseState -- Changes specified pet's skill use state and synchronizes to client
PlayerPet:HandleChangedLookAtEvent -- Adjusts pet position when player look direction changes
PlayerPet:HandleStateChangeEvent -- Adjusts pet's corresponding state and animation when player state changes
PlayerRelic:OnBeginPlay -- Player relic system initialization and table setup
PlayerRelic:AddRelic -- Adds relic to player and applies bonus probability
PlayerRelic:Purifying -- Purifies dirty relic to convert to usable relic
PlayerRelic:RegisterToBook -- Registers relic to relic book and consumes necessary materials
PlayerRelic:ClearDirtyItems -- Function executed when player dies.
PlayerRelic:SetTableClient -- Full table data synchronization from server to client
PlayerRelic:SetTableElementClient -- Synchronizes only specific elements of table from server to client
PlayerRelic:ClearTableClient -- Initializes all client table to default values
PlayerRelic:ChangedTable -- Refreshes related UI to update screen when table changes
PlayerRelic:ClearAllProperty -- Resets all relic-related properties to initial values
PlayerRelic:LoadedUserData -- Updates relic possession information
PlayerRelic:SyncDirtyItem -- Synchronizes dirty relic data with client
PlayerRelic:OnMapEnter -- Performs automatic relic purification in town areas when entering map
PlayerRelic:BuyRelicBox -- Purchases relic box and adds to inventory
PlayerRelic:OnSyncProperty -- Updates relic box factory UI when properties are synchronized
PlayerRelic:OpenRelicBox -- Condition verification
PlayerRelic:SetUI_RelicBoxOpenResult -- Shows relic box opening result in UI and sets popup
PlayerRelic:GetRelicBox -- Directly adds relic box at specified index to inventory
PlayerRelic:Merge -- Quantity verification
PlayerRelic:SetMergeResultPopup -- Shows relic synthesis result in popup UI and sets style according to grade
PlayerRelic:RecycleToLegacyCoin -- Converts all owned relics to legacy coins by calculating grade-based scores
PlayerRelic:SetRecycleResultUI -- Shows relic recycling result in UI and activates popup
PlayerRelic:IsPossibleRegistToBook -- Checks whether specified relic can be registered in relic book
PlayerRelic:AutoMerge -- grade: Grade of material to consume. Normal(1), Advanced(2), Rare(3), Legendary(4) as parameter
PlayerRelic:SetAutoMergeResultUI -- Delivers auto synthesis result to relic synthesis shop UI to show result popup
RelicBookUI:OnBeginPlay -- Relic book UI initial setup and localization text application
RelicBookUI:OnUpdate -- Handles UI refresh flag processing and delayed update processing
RelicBookUI:RefreshUI -- Sets UI refresh flag
RelicBookUI:RefreshStatusUI -- Sets status UI refresh flag
RelicBookUI:RefreshUI_Inner -- Refreshes entire relic book UI and updates visual state according to registration information
RelicBookUI:ShowRegistrationPopup -- slotIdx: Display order index on current page
RelicBookUI:SetFilterIdx -- Sets relic grade filter index and initializes page
RelicBookUI:RefreshStatusUI_Inner -- Calculates total stats according to relic registration status and displays achievement rate
RelicBookUI:SetPageNavInfo -- Sets page navigation information according to current filter and registration availability
RelicBookUI:RefreshUI_Inner_FilteredByRegistable -- Filters and displays only registerable relics in UI
RelicBookUI:HandleButtonClickEvent -- Handles relic book page navigation button click event
RelicBookUI:HandleKeyDownEvent -- Handles closing relic book popup when ESC key is pressed
RelicBookUI:HandleButtonClickEvent2 -- Handles relic grade filter 1(normal) button click event
RelicBookUI:HandleButtonClickEvent3 -- Handles relic grade filter 2(advanced) button click event
RelicBookUI:HandleButtonClickEvent4 -- Handles relic grade filter 3(rare) button click event
RelicBookUI:HandleButtonClickEvent5 -- Handles relic grade filter 4(legendary) button click event
RelicBookUI:HandleButtonClickEvent6 -- Handles relic book next page navigation button click event
RelicBookUI:HandleButtonClickEvent7 -- Handles relic book previous page navigation button click event
RelicBookUI:HandleButtonClickEvent8 -- Handles registerable relics only view filter toggle button click event
RelicBookUI:HandleButtonClickEvent9 -- Handles relic book reset button click event (removes filter and resets to grade 1)
RelicShowRegistPopupButton:HandleButtonClickEvent -- Delivers corresponding slot and material index to show registration popup when relic registration popup button is clicked
PlayerTitle:OnBeginPlay -- Player title system initialization and title entity creation
PlayerTitle:OnSyncProperty -- Sets title entity and updates UI when equipped title index is synchronized
PlayerTitle:ChangeEquipedItem -- Equips title at specified index and verifies possession
PlayerTitle:GetNewItem -- Acquires new title and adds after checking if already owned
PlayerTitle:SpawnTitleEntity -- Creates title display entity and sets sorting and layer
PlayerTitle:SetTitleEntity -- Sets title entity appearance and color according to equipped title
PlayerTitle:SetTitleEntityOnClient -- Sets localized text and RUID of title entity on client
PlayerTitle:OnMapEnter -- Sets title entity on client when entering map (currently disabled)
PlayerTitle:SetTableClient -- Full table data synchronization from server to client
PlayerTitle:SetTableElementClient -- Synchronizes only specific elements of table from server to client
PlayerTitle:ClearTableClient -- Initializes all client table to default values
PlayerTitle:ChangedTable -- Updates related UI and applies stats when table changes
PlayerTitle:ClearAllProperty -- Resets all title-related properties to initial values
PlayerTitle:LoadedUserData -- Loads title-related information from user data and applies to properties
TitleEquipButton:HandleButtonClickEvent -- Requests equipping title at corresponding index when title equip button is clicked
TitleStorageUI:OnBeginPlay -- Localization and slot duplication setup during title storage UI initialization
TitleStorageUI:InitUI -- Initializes title list and stat list of title storage and sets basic data
TitleStorageUI:OnUpdate -- Checks UI refresh flag status and handles delayed update processing
TitleStorageUI:RefreshUI -- Activates UI refresh flag
TitleStorageUI:RefreshUI_Inner -- Updates UI according to title possession and equipment status and calculates and displays cumulative stats
TitleStorageUI:ChangeEquipedTitle -- Equips title at specified index and applies stats
TitleStorageUI:HandleKeyDownEvent -- Handles closing title storage UI when ESC key is pressed
PlayerVoidItem:OnBeginPlay -- Void item system initialization and table setup
PlayerVoidItem:LoadedData -- Loads void item possession information and random list from user data
PlayerVoidItem:SetTableClient -- Full table data synchronization from server to client
PlayerVoidItem:SetTableElementClient -- Synchronizes only specific elements of table from server to client
PlayerVoidItem:ChangedTable -- Refreshes related UI when table changes
PlayerVoidItem:GetItem -- Obtains void item at specified index, levels up, and applies stats
PlayerVoidItem:PurchaseItem -- Purchases selected void item from random list, consumes currency, and handles achievements
PlayerVoidItem:SetPurchaseResultPopup -- Shows void item purchase result popup in UI
PlayerVoidItem:SetRandomList -- Creates list of 3 random void items to display in shop
VoidItemShopUI:ShowSelectItemPopup -- Shows void item selection popup and updates 3 random option list and selection state
VoidItemShopUI:PlaySelectItemPopupDirection -- Plays animation effects of item selection popup sequentially
VoidItemShopUI:SetPurchaseResultPopup -- Sets purchase result popup and plays item information and effect animation
VoidItemShopUI:RefreshUI -- Updates purchase cost and held coin information in UI and handles purchase availability
VoidItemShopUI:OnUpdate -- Manages icon random change time and handles periodic icon random change effect
VoidItemShopUI:OnBeginPlay -- Loads icon RUID list during void item shop initialization
VoidItemShopUI:HandleButtonClickEvent -- Checks coin sufficiency when purchase button is clicked and activates purchase confirmation popup
VoidItemShopUI:HandleButtonClickEvent2 -- Initializes selection and shows popup when void item selection popup button is clicked
VoidItemShopUI:HandleButtonClickEvent3 -- Sets selection index to 1 and updates UI when first void item is selected
VoidItemShopUI:HandleButtonClickEvent4 -- Sets selection index to 2 and updates UI when second void item is selected
VoidItemShopUI:HandleButtonClickEvent5 -- Sets selection index to 3 and updates UI when third void item is selected
VoidItemShopUI:HandleButtonClickEvent6 -- Handles actual purchase and disables button when void item purchase confirmation button is clicked
VoidItemShopUI:HandleKeyDownEvent -- Handles closing void item shop when ESC key is pressed
VoidItemStorageUI:RefreshUI -- Refreshes entire void item storage UI and initializes selection state
VoidItemStorageUI:ShowSelectedItem -- Shows detailed information of selected void item in description panel and updates UI
VoidItemStorageUI:HandleButtonClickEvent -- Handles void item storage refresh button click event
VoidItemStorageUI:HandleKeyDownEvent -- Handles closing void item storage UI when ESC key is pressed
VoidItemStorageUI_SlotButton:HandleButtonClickEvent -- Requests showing detailed information for corresponding item when void item slot button is clicked
PortalFromMineToMineInteraction:OnBeginPlay -- Sets portal guide UI for going to next stage mine within mine
PortalFromMineToMineInteraction:OnInteractionEvent -- Handles teleport to next stage mine
PortalFromMineToMineInteraction:HandleInteractionEvent -- Portal interaction event handler (move to next stage mine)
PortalFromMineToMineInteraction:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
PortalFromMineToMineInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
PortalToHistoricSiteInteraction:HandleInteractionEvent -- Handles portal interaction to move to historic site
PortalToMineInteraction:OnBeginPlay -- Sets portal guide UI for going from town to mine
PortalToMineInteraction:SetLoadingUIOn -- Shows loading UI and disables player movement when entering mine
PortalToMineInteraction:EnterToMine -- Teleports to specified mine and sets loading UI
PortalToMineInteraction:HandleInteractionEvent -- Mine entry interaction event handler
PortalToMineInteraction:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
PortalToMineInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
PortalToNextHistoricSiteInteraction:HandleInteractionEvent -- Portal interaction to move to next historic site (currently commented out)
PortalToTownInteraction:OnBeginPlay -- Sets interaction guide hiding at game start
PortalToTownInteraction:OnInteractionEvent -- Handles interaction to return from mine to town
PortalToTownInteraction:HandleButtonClickEvent -- Handles return to town button click in result UI
PortalToTownInteraction:HandleButtonClickEvent2 -- Handles second return to town button click in result UI
PortalToTownInteraction:HandleInteractionEvent -- Interaction event handler (town return processing)
PortalToTownInteraction:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
PortalToTownInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
Portal_TownToTownInteraction:OnBeginPlay -- Sets portal guide UI for town-to-town movement
Portal_TownToTownInteraction:OnInteractionEventOnClient -- Executes town-to-town teleport on client
Portal_TownToTownInteraction:OnInteractionEvent -- Checks town entry permission on server then allows teleport
Portal_TownToTownInteraction:HandleInteractionEvent -- Town portal interaction event handler
Portal_TownToTownInteraction:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
Portal_TownToTownInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
TeleportNpcComponent:RenewUI -- Updates teleport UI according to town information (cost and town name)
TeleportNpcComponent:OnInteractionEvent -- Handles opening town admission purchase UI when interacting with NPC
TeleportNpcComponent:OnBeginPlay -- Sets NPC sprite layer
TeleportNpcComponent:HandleInteractionEvent -- NPC interaction event handler
TeleportNpcComponent:HandleButtonClickEvent -- Handles town admission purchase UI close button
TeleportNpcComponent:HandleButtonClickEvent2 -- Handles town admission purchase button click (verifies currency then purchases)
TeleportNpcComponent:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
TeleportNpcComponent:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
TeleportTownController:OnBeginPlay -- Teleport town controller initialization and UI setup
TeleportTownController:OnUpdate -- Update method executed when UI refresh is needed
TeleportTownController:RenewUI -- Sets flag for UI refresh
TeleportTownController:RenewUI_Inner -- Updates teleport button state for each town
TeleportTownController:HandleButtonClickEvent -- Handles first town (Town) teleport button click
TeleportTownController:HandleButtonClickEvent2 -- Handles second town (Town2) teleport button click
TeleportTownController:HandleButtonClickEvent3 -- Handles third town (Town3) teleport button click
TeleportTownController:HandleButtonClickEvent4 -- Handles fourth town (Town4) teleport button click
TeleportTownController:HandleButtonClickEvent5 -- Handles fifth town (Town5) teleport button click
TeleportTownController:HandleButtonClickEvent6 -- Handles sixth town (Town6) teleport button click
TeleportTownController:HandleButtonClickEvent7 -- Handles seventh town (Town7) teleport button click
TeleportTownController:HandleButtonClickEvent8 -- Handles eighth town (Town8) teleport button click
TeleportTownController:HandleButtonClickEvent9 -- Handles ninth town (Town9) teleport button click
TeleportTownController:HandleButtonClickEvent10 -- Handles tenth town (Town10 - temple) teleport button click
TeleportTownController:HandleKeyDownEvent -- Closes teleport UI when ESC key is pressed
CharonBoatUI_UseButton:HandleButtonClickEvent -- Handles Charon's Boat use button click (rebirth time reduction item)
LeaderBoardUI:OnUpdate -- Update method that auto-refreshes leaderboard UI every 60 seconds
LeaderBoardUI:RefreshUI -- Refreshes leaderboard ranking information and player ranking information
LegacycoinToEmblemUI:RefreshUI -- Refreshes UI information for exchanging legacy coins to emblem points
LegacycoinToEmblemUI:HandleButtonClickEvent -- Handles legacy coin to emblem point exchange button click
LegacycoinToEmblemUI:HandleKeyDownEvent -- Closes legacy coin exchange UI when ESC key is pressed
NPCInteraction:RefreshTargetUI -- Handles customized UI refresh according to target UI type
NPCInteraction:OnInteractionEvent -- Opens UI and sets state when interacting with NPC
NPCInteraction:OnBeginPlay -- Automatically sets NPC sprite layer
NPCInteraction:HandleInteractionEvent -- Interaction event handler (NPC interaction)
NPCInteraction:HandleInteractionEnterEvent -- Shows guide key UI when entering interaction area
NPCInteraction:HandleInteractionLeaveEvent -- Hides guide key UI when leaving interaction area
RebornUI:RefreshUI -- Refreshes rebirth UI information (rebirth count, temple records, rewards, etc.)
RebornUI:PlayRebornDirection -- Plays rebirth effect animation (background and text effects)
RebornUI:HandleButtonClickEvent -- Handles rebirth execute button click
RebornUI:HandleKeyDownEvent -- Closes rebirth UI when ESC key is pressed (if not during effect)
RelicBinUI:RefreshUI -- Refreshes relic recycling UI information (converts owned relics to legacy coins)
RelicBinUI:HandleButtonClickEvent -- Handles relic recycling button click (converts to legacy coins)
RelicBinUI:HandleKeyDownEvent -- Closes relic bin UI when ESC key is pressed
RelicGachaShopUI:RefreshUI -- Refreshes relic gacha shop UI information (price and purchase button state)
RelicGachaShopUI:HandleButtonClickEvent -- Handles relic gacha box purchase button click
RelicGachaShopUI:HandleKeyDownEvent -- Closes relic gacha shop UI when ESC key is pressed
ShopUI:OnBeginPlay -- Shop UI initial setup and inventory slot creation
ShopUI:RefreshUI -- Refreshes shop UI based on backpack item list
ShopUI:HandleButtonClickEvent -- Handles sell all button click
ShopUI:HandleKeyDownEvent -- Closes shop UI when ESC key is pressed
ShopUI:HandleKeyDownEvent2 -- Executes sell all function when E key is pressed
SprinkleItem:OnBeginPlay -- Creates sprinkle item and initializes server/client separately
SprinkleItem:HandleTriggerEnterEvent -- Handles item application when player touches sprinkle item
EquipmentShopBundleSlotButton:HandleButtonClickEvent -- Toggles checkbox state when equipment shop bundle purchase slot button is clicked
EquipmentShopSlotButton:HandleButtonClickEvent -- Shows detail information popup when equipment shop item slot button is clicked
EquipmentShopUI:OnBeginPlay -- Localization (text)
EquipmentShopUI:OnUpdate -- Executes every frame when UI refresh is needed
EquipmentShopUI:RefreshUI -- Sets UI refresh flag to process in next frame
EquipmentShopUI:RefreshUI_Inner -- Actual refresh processing of equipment shop UI (amount, item list update)
EquipmentShopUI:ChangeFilter -- Changes equipment type filter and initializes bundle purchase check state
EquipmentShopUI:ShowDetailPopup -- Shows detailed information popup for selected equipment item
EquipmentShopUI:SetPurchaseCheckUI -- Sets popup that displays stat increase information when equipment purchase is completed
EquipmentShopUI:PlayPurchaseDirection -- Plays animation effect when equipment purchase is completed
EquipmentShopUI:RefreshBundlePurchasePopup -- Updates bundle purchase popup content and reflects check state
EquipmentShopUI:Oneshot_CheckboxButtonClicked -- Toggles selection state when checkbox is clicked in bundle purchase
EquipmentShopUI:PlayPurchaseBundleDirection -- Animation effect and result display when bundle purchase is completed
EquipmentShopUI:HandleKeyDownEvent -- Closes popup or UI step by step when ESC key is pressed
EquipmentShopUI:HandleButtonClickEvent -- Switches to corresponding equipment type when filter button 1 (weapon) is clicked
EquipmentShopUI:HandleButtonClickEvent2 -- Switches to corresponding equipment type when filter button 2 (armor) is clicked
EquipmentShopUI:HandleButtonClickEvent3 -- Switches to corresponding equipment type when filter button 3 (accessory) is clicked
EquipmentShopUI:HandleButtonClickEvent4 -- Switches to corresponding equipment type when filter button 4 (skins) is clicked
EquipmentShopUI:HandleButtonClickEvent5 -- Handles when purchase button is clicked in equipment detail information popup
EquipmentShopUI:HandleButtonClickEvent6 -- Initializes check state and shows popup when bundle purchase button is clicked
EquipmentShopUI:HandleButtonClickEvent11 -- Handles actual purchase when purchase confirmation button is clicked in bundle purchase popup
EquipmentShopUI:HandleButtonClickEvent12 -- Removes all slots created in purchase result window
EquipmentShopUI:HandleButtonClickEvent7 -- Closes bundle purchase when shop is closed.
MythicEquipmentShopUI:OnBeginPlay -- Sets all redistribution check states to false when mythic equipment UI is initialized
MythicEquipmentShopUI:RefreshUI -- Turn off other popups
MythicEquipmentShopUI:SetUpgradeCheckPopup -- Sets and shows mythic equipment upgrade confirmation popup
MythicEquipmentShopUI:PlayUpgradeDirection -- Plays effect when mythic equipment upgrade is completed
MythicEquipmentShopUI:SetUnlockCheckPopup -- Sets and shows mythic equipment level limit unlock confirmation popup
MythicEquipmentShopUI:OpenRedistributionPopup -- Opens divine stone redistribution popup and initializes check state
MythicEquipmentShopUI:PlayUnlockDirection -- Plays key and lock animation when level limit unlock is completed
MythicEquipmentShopUI:RefreshRedistributionInfoPanel -- Updates divine stone redistribution popup content and reflects check state
MythicEquipmentShopUI:RefreshDevineStonesInfoPanel -- Opens divine stone detail information panel and updates information according to damage set
MythicEquipmentShopUI:HandleButtonClickEvent -- Shows upgrade check popup when level up button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent2 -- Executes mythic equipment purchase when upgrade confirmation button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent3 -- Switches to corresponding equipment when filter button 1 is clicked
MythicEquipmentShopUI:HandleButtonClickEvent4 -- Switches to corresponding equipment when filter button 2 is clicked
MythicEquipmentShopUI:HandleButtonClickEvent5 -- Switches to corresponding equipment when filter button 3 is clicked
MythicEquipmentShopUI:HandleButtonClickEvent6 -- Switches to corresponding equipment when filter button 4 is clicked
MythicEquipmentShopUI:HandleButtonClickEvent7 -- Shows level limit unlock popup when unlock button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent8 -- Shows divine stone redistribution popup when redistribution button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent9 -- Handles divine stone redistribution when redistribution execute button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent10 -- Attempts unlock.
MythicEquipmentShopUI:HandleButtonClickEvent11 -- Refreshes UI when close button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent12 -- Shows damage set information when divine stone detail information button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent13 -- Shows damage set information when divine stone detail information button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent14 -- Increases upgrade level by 1 step when level up button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent15 -- Sets upgrade to maximum available level when maximum level button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent16 -- Decreases upgrade level by 1 step when level down button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent17 -- Resets upgrade level to 1 when minimum level button is clicked
MythicEquipmentShopUI:HandleButtonClickEvent18 -- Refreshes UI when close button is clicked
MythicEquipmentShopUI:HandleKeyDownEvent -- Closes detail information panel or UI when ESC key is pressed
MythicEquipmentShopUI_RedistributionCheckPopup_CheckButton:HandleButtonClickEvent -- Toggles check state and refreshes UI when divine stone redistribution check button is clicked
GemShopLogic:BuyItem -- Handles item purchase in gem shop (consumables, additional items, special items)
GemShopLogic:GetNewChair -- Randomly acquires new chair or provides relic box instead if all are owned
GemShopUI:OnBeginPlay -- Creates and sets product list during gem shop UI initialization
GemShopUI:RefreshUI -- Refreshes gem shop UI (filter, selection, currency holdings, detailed information)
GemShopUI:ShowDetailInfo -- Shows detailed information popup for selected item and refreshes UI
GemShopUI:SetPurchaseCheckPopup -- Sets item purchase confirmation popup and displays cost information
GemShopUI:RefreshDetailInfoPanel -- Refreshes detailed information panel for selected item and sets purchase button state
GemShopUI:SetFilterIdx -- Changes product filter, closes popup, and refreshes UI
GemShopUI:HandleButtonClickEvent -- Switches to corresponding filter when filter button 1 (box) is clicked
GemShopUI:HandleButtonClickEvent2 -- Switches to corresponding filter when filter button 2 (tools) is clicked
GemShopUI:HandleButtonClickEvent3 -- Switches to corresponding filter when filter button 3 (misc) is clicked
GemShopUI:HandleButtonClickEvent4 -- Switches to corresponding filter when filter button 4 (event) is clicked
GemShopUI:HandleButtonClickEvent5 -- Handles when purchase button is clicked in detail information panel
GemShopUI:HandleButtonClickEvent6 -- Initializes filter and plays BGM when shop close button is clicked
GemShopUI:HandleButtonClickEvent7 -- Handles when purchase confirmation button is clicked in purchase confirmation popup
GemShopUI:HandleButtonClickEvent8 -- Initializes selection state when detail information panel close button is clicked
GemShopUI:HandleButtonClickEvent9 -- Initializes selection state and restores BGM when purchase confirmation popup cancel button is clicked
GemShopUI:HandleKeyDownEvent -- Closes purchase confirmation popup or UI when ESC key is pressed
GemShopUI_SlotButton:HandleButtonClickEvent -- Shows detailed information when gem shop item slot button is clicked
RebornShopUI:OnBeginPlay -- Rebirth shop UI initialization and localization
RebornShopUI:RefreshList -- Refreshes rebirth shop list (currently empty)
RelicMergeShopUI:PlayMergeDirection -- Animation effect and result display when relic synthesis is completed
RelicMergeShopUI:RefreshMainPanel -- Updates main panel relic material count, result count, and selection state
RelicMergeShopUI:IsPossibleRegistToBook -- Checks whether corresponding relic can be registered in collection
RelicMergeShopUI:SelectGrade -- Sets selected grade in auto synthesis and updates main panel
RelicMergeShopUI:SetResultPopup -- Sets popup showing relic synthesis result and updates list
RelicMergeShopUI:HandleButtonClickEvent -- Executes auto synthesis when synthesis button is clicked
RelicMergeShopUI:HandleKeyDownEvent -- Closes UI when ESC key is pressed if not during effect
RelicMergeShopUI:HandleButtonClickEvent2 -- Toggles selection state when grade 1 relic selection button is clicked
RelicMergeShopUI:HandleButtonClickEvent3 -- Toggles selection state when grade 2 relic selection button is clicked
RelicMergeShopUI:HandleButtonClickEvent4 -- Toggles selection state when grade 3 relic selection button is clicked
RelicMergeShopUI:HandleButtonClickEvent6 -- Toggles selection state when grade 4 relic selection button is clicked
RelicMergeShopUI_MaterialButton:HandleButtonClickEvent -- Handles registering corresponding material when relic synthesis material selection button is clicked
RelicMergeShopUI_MaterialSlotButton:HandleButtonClickEvent -- Sets waiting index and shows material selection panel when relic synthesis material slot button is clicked
DynamicFootholdManager:HandleInteractionEvent -- Activates foothold and plays sound when interacting with dynamic foothold
Trap:OnBeginPlay -- Sets to hittable state when trap is initialized
Trap:MakeCanHit -- Sets trap's hittable state externally
Trap:HandleTriggerEnterEvent -- Handles damage, effect, poison, knockback when colliding with player
TrapBullet:OnUpdate -- Trap bullet moves at constant speed and removes when survival time exceeded
TrapBullet:HandleTriggerEnterEvent -- Handles effect according to snowball/normal bullet type when colliding with player
TrapBulletShooter:Fire -- Creates projectile, launches at set angle, and plays effect
TrapBulletShooter:OnBeginPlay -- Sets cooldown and starts recursive function when trap bullet shooter is initialized
TrapBulletShooter:RecursiveFunc -- Recursive function that decreases cooldown at intervals and fires when it reaches 0
TrapContinuous:OnUpdate -- Checks cooldown and executes hit for continuous damage trap
TrapContinuous:Hit -- Continuously applies damage, sound, effect to player
TrapContinuous:HandleTriggerEnterEvent -- Starts hitting when player enters continuous damage range
TrapContinuous:HandleTriggerLeaveEvent -- Stops hitting when player leaves continuous damage range
TrapGuardian:SpawnAttack -- Creates guardian attack missile and sets properties
TrapGuardian:GetAttackModelId -- Returns attack model ID according to guardian type
TrapGuardian:OnUpdate -- Executes attack after checking cooldown when player is detected
TrapGuardian:OnBeginPlay -- Sets cooldown when guardian is initialized
TrapGuardian:HandleTriggerStayEvent -- Sets to detected state when player stays within range
TrapGuardian:HandleTriggerLeaveEvent -- Cancels detection when player leaves range
TrapGuardianBullet:OnUpdate -- Chases player and removes after checking survival time
TrapGuardianBullet:ChasePlayer -- Moves toward player direction and updates rotation
TrapGuardianBullet:HandleTriggerEnterEvent -- Handles electric damage, effect, sound when colliding with player then removes
TrapGuardianBullet:HandleTriggerLeaveEvent -- Removes entity when leaving range
TrapJump:HandleTriggerEnterEvent -- Provides upward jump force when player collides with jump pad
TrapProjectile:DestroySelf -- Removes projectile entity
TrapProjectile:SetParameter -- Sets projectile's angle, distance, speed for launch
TrapProjectile:HandleTriggerEnterEvent -- Handles damage and plays effect when colliding with player
TrapRotating:OnUpdate -- Rotates clockwise/counterclockwise and changes direction every 20 seconds
TrapRotating:ChangeClockwise -- Switches between clockwise and counterclockwise rotation
TrapRotating:OnBeginPlay -- Initializes rotation direction change timer
TrapShowHitRange:OnBeginPlay -- Creates objects that visually display trap's attack range
TrapTest:OnBeginPlay -- Sets target to local player and initializes lifetime
TrapTest:OnUpdate -- Tracks and moves toward player when lifetime ends
TrapTest:ChasePlayer -- Player tracking logic (not implemented)
TrapTriggerStay:OnUpdate -- Updates hit cooldown time
TrapTriggerStay:HandleTriggerStayEvent -- Continuously damages player when they stay in trap
TrapUprisingSpearSensor:SpawnUprisingSpearTrap -- Creates rising spear trap and removes after 0.5 seconds
TrapUprisingSpearSensor:OnUpdate -- Updates detection cooldown time
TrapUprisingSpearSensor:OnBeginPlay -- Initializes detection cooldown
TrapUprisingSpearSensor:HandleTriggerStayEvent -- Plays sound when detecting player then summons spear trap 1 second later
TrapDayOrNight:OnUpdate -- Switches day and night background every 30 seconds
TrapMonster:Sturn -- Stuns monster or recovers from stun
TrapThrownRock:OnUpdate -- Removes rock object after 3 seconds
TrapThrownRock:HandleTriggerEnterEvent -- Applies stun effect and plays effect when colliding with monster
ButtonDeselect:HandleButtonClickEvent -- Deselects parent selection state when button is clicked
ButtonSelect:Select -- Sets button's selection state and displays visually
ButtonSelect:OnBeginPlay -- Initializes selectability and selection state
ButtonSelect:HandleButtonClickEvent -- Changes button to selected state when selectable
ButtonUIOpen:HandleButtonClickEvent -- Activates specified target UI
DisableWhenESCKeyInputed:HandleButtonClickEvent -- Button click event handler (empty implementation)
DisableWhenESCKeyInputed:HandleKeyDownEvent -- Deactivates UI with ESC key or mouse click
DisableWhenESCKeyInputed:HandleScreenTouchEvent -- Deactivates UI with screen touch
ExitButton:HandleButtonClickEvent -- Deactivates specified UI or parent UI and enables player movement
IngameUIManager:OnBeginPlay -- Applies UI localization text (currently commented out)
IngameUIManager:HandleLocalPlayerMapEnterEvent -- Sets UI activation state according to map type when entering map
LoadingManager:SetLoadingUIOn -- Sets loading UI activation state and controls player movement
LoadingManager:UpdateTipMessage -- Generates random tip message and displays in UI
LoadingManager:OnUpdate -- Updates tip message every 4 seconds while loading
LoadingManager:SetPlayerMovement -- Sets player movement component activation state
LoadingManager:OnBeginPlay -- Initializes loading state at game start and activates adventure start button
LoadingManager:HandleButtonClickEvent -- Initializes game data and displays map entry UI when adventure start button is clicked
LoadingManager:HandleKeyDownEvent -- Handles starting adventure with E key input
OutgameUIManager:HandleLocalPlayerMapEnterEvent -- Sets outgame UI state according to map type when entering map
RainbowSprite:OnUpdate -- Cyclically changes sprite color to rainbow colors
RainbowText:OnUpdate -- Cyclically changes text color to rainbow colors
UIButtonSound:HandleButtonClickEvent -- Plays different sound according to sound type when button is clicked
UIFlickering:OnUpdate -- Updates UI flickering effect with 1 second cycle
UIGuideAndButtonInteraction:PlayButtonClickDirection -- Plays animation effect with delay on guide text and button icon when button is clicked
UIGuideAndButtonInteraction:HandleButtonClickEvent -- Handles interaction button click event to perform various object interactions
UIGuideNavigatorButton:HandleButtonClickEvent -- Activates target page and deactivates others when guide navigation button is clicked
UIHelpGuide:ChangePage -- Changes help guide page and updates corresponding button state
UIHelpGuide:OnBeginPlay -- Help guide UI initialization and localization setup
UIHelpGuide:HandleKeyDownEvent -- Handles closing help window when ESC key is pressed
UIHelpGuideNavButton:HandleButtonClickEvent -- Changes to corresponding page when help guide navigation button is clicked
UIMouseHover:SetHoverUI -- Shows or hides mouse hover tooltip according to specified UI type
UIMouseHover:OnBeginPlay -- Loads item/relic data tables and sets localization during component initialization
UIMouseHover:HandleButtonStateChangeEvent -- Handles showing/hiding hover UI by platform when button state changes
UISeekerComponent:OnUpdate -- Calculates position and speed of UI element moving toward target every frame
UISeekerComponent:Guide -- Determines movement direction by calculating unit vector toward target position
UISeekerComponent:OnBeginPlay -- Sets UI transform component reference during component initialization
UIWorldIngressLoading:OnUpdate -- Checks local player's map entry state every frame to deactivate loading UI
UIWorldIngressLoading:OnBeginPlay -- Shows appropriate logo according to language setting and activates loading UI
UIWorldIngressLoading:SetLoadingUIOff -- Gradually deactivates loading UI with fade-out effect
UIWorldIngressLoading:SetLoadingUIOn -- Immediately activates and displays loading UI
WarningFlickeringUI:OnUpdate -- Updates warning UI's cyclic flickering effect with set period
UIInventory:OnBeginPlay -- Inventory UI initialization and inventory button connection setup
UIInventory:HandleInventoryItemInitEvent -- Handles inventory item initialization event to create all item slots
UIInventory:HandleInventoryItemAddedEvent -- Creates slot when new item is added to inventory
UIInventory:HandleInventoryItemRemovedEvent -- Deletes corresponding slot when item is removed from inventory
UIInventory:HandleInventoryItemModifiedEvent -- Updates corresponding slot data when inventory item changes
UIItemSlot:SetData -- Sets item data in item slot and updates UI
UIItemSlot:HandleButtonClickEvent -- Handles item slot click event (currently empty)
UIMyInfoSimple:OnBeginPlay -- Sets my info UI reference during component initialization
UIMyInfoSimple:OnUpdate -- Updates local player's nickname and HP in UI every frame
ChasePlayer:OnUpdate -- Calculates distance to player to determine chase mode transition
ChasePlayer:ChasePlayer -- Chases player or returns to origin according to chase mode
ChasePlayer:OnBeginPlay -- Saves initial spawn position as origin
ChasePlayer:FlipX -- Controls sprite horizontal flip according to movement direction
Gimmick_PlayerJumping:HandleTriggerEnterEvent -- Launches player with specified force and plays effect when player touches jump gimmick
GraveStone:OnUpdate -- Counts down spawn timer when ghost doesn't exist
GraveStone:OnBeginPlay -- Gravestone initialization and spawn timer setup
GraveStone:SpawnGhost -- Creates ghost entity from gravestone and resets timer
GraveStone:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Creates ghost and returns to original sprite when spawn animation completes
PlanetMovement:OnUpdate -- Updates planet orbital motion every frame
PlanetMovement:Rotation -- Circular orbital motion around sun with specified radius and speed
PlanetMovement:OnBeginPlay -- Planet initialization and force setting for collision
PlanetMovement:HandleTriggerEnterEvent -- Applies force in orbital direction when player collides with planet
RotationShield:OnUpdate -- Updates rotation shield rotation operation every frame
RotationShield:Rotation -- Rotates in circular path at constant radius around player
RotationShield:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Removes shield and plays effect when destruction animation completes
TestCode230116:OnBeginPlay -- Sets player left/right movement key inversion (for testing)
TrapSpawnManager:SpawnRandomMiningTarget -- Activates specified number of child trap entities randomly and deactivates the rest
TrapSpawnManager:OnBeginPlay -- Trap spawn manager initialization and automatic trap activation execution
Trap_InkBullet:OnBeginPlay -- Sets ink projectile lifespan timer
Trap_InkBullet:OnUpdate -- Moves every frame in specified direction vector
Trap_InkBullet:HandleTriggerEnterEvent -- Applies damage when ink projectile hits player then self-destructs
Trap_InkBullet:HandleFootholdCollisionEvent -- Automatically removes ink projectile 2 seconds after collision with ground or obstacles
Trap_JuniorGhost:Destroy -- Switches junior ghost to death state to execute death animation
Trap_JuniorGhost:OnBeginPlay -- Junior ghost initialization (currently disabled)
Trap_JuniorGhost:OnUpdate -- Continuously moves to the left when not dead
Trap_JuniorGhost:HandleTriggerEnterEvent -- Handles game over when player contacts junior ghost
Trap_JuniorGhost:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Deletes entity when death animation completes
Trap_PillarManager:OnBeginPlay -- Fire pillar manager initialization and automatic attack start setup
Trap_PillarManager:PlayAttack -- Controls sequential activation of fire pillar attacks
Trap_PillarOfFire:Attack -- Starts fire pillar attack animation
Trap_PillarOfFire:OnBeginPlay -- Fire pillar initialization and original sprite storage
Trap_PillarOfFire:HandleTriggerEnterEvent -- Handles burn damage when player enters fire pillar combustion area
Trap_PillarOfFire:HandleTriggerStayEvent -- Handles burn damage when player stays in fire pillar combustion area
Trap_PillarOfFire:HandleSpriteAnimPlayerEndFrameEvent -- Returns to original sprite when attack animation ends and reserves next attack
Trap_PillarOfFire:HandleSpriteAnimPlayerChangeFrameEvent -- Tracks attack animation frame progression
Trap_SeaOfPoseidon:InToTheWater -- Starts penalty when entering water
Trap_SeaOfPoseidon:SpawnBubble -- Creates bubble at player location to execute rising animation
Trap_SeaOfPoseidon:HandleTriggerEnterEvent -- Switches to diving state when player enters Poseidon's sea trap area
Trap_SeaOfPoseidon:HandleTriggerLeaveEvent -- Handles when bubble or player leaves sea trap area
Trap_SeaOfPoseidon:HandleTriggerStayEvent -- Adjusts rendering layer and gravity when player stays underwater
Trap_Snow:HandleTriggerEnterEvent -- Adds freeze stack when player contacts snow if not in snowman state
Trap_SnowShooter:OnBeginPlay -- Snowball shooter initialization and periodic attack timer setup
Trap_SnowShooter:Throwing -- Starts snowball shooting animation and activates attack state
Trap_SnowShooter:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Creates snowball projectile according to attack animation frame and switches sprite
Trap_SnowShooter:HandleSpriteAnimPlayerEndFrameEvent -- Handles animation end (currently disabled)
Trap_SpawnSnow:OnBeginPlay -- Snow generator initialization and periodic snow creation timer setup
Trap_SpawnSnow:SpawnSnow -- Creates random number of snow entities at random positions within specified range
Trap_Squid:OnBeginPlay -- Squid trap initialization and attack timer setup
Trap_Squid:ReadyShot -- Executes squid color change animation according to attack readiness state
Trap_Squid:ShotInk -- Fires ink in 360-degree omnidirectional pattern to deliver damage
Trap_Squid:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Controls attack timing when squid animation frame changes
Trap_ThunderCloud:OnBeginPlay -- Thunder cloud initialization and periodic lightning attack timer setup
Trap_ThunderCloud:Lightning -- Creates thunder cloud sprite flicker then lightning attack at random position
Trap_ThunderCloud:SpawnBullet -- Creates electric projectile for lightning left-right spread
Trap_ThunderMonster:OnBeginPlay -- Lightning monster initialization and periodic lightning attack timer setup
Trap_ThunderMonster:Lightning -- Creates lightning projectiles that spread left and right
Trap_ThunderMonster:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Creates projectile according to lightning animation frame and switches sprite
Trap_ThunderMonsterBullet:OnUpdate -- Moves left and right after initialization and automatically destructs when falling to ground
Trap_ThunderMonsterBullet:OnBeginPlay -- Lightning projectile initialization and movement start setup after 1.5 seconds
Trap_ThunderMonsterBullet:HandleTriggerEnterEvent -- Plays electric effect and sound on player collision then removes entity
Trap_ThunderPriest:OnBeginPlay -- Stores original sprite and activates range display during component initialization
Trap_ThunderPriest:Lightning -- Executes lightning attack when player is within range and starts repeated attacks
Trap_ThunderPriest:RepeatLightning -- Sets timer for repeating lightning attacks at cooldown intervals
Trap_ThunderPriest:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- Handles lightning restoration and projectile creation when sprite animation frame changes
Trap_ThunderPriest:HandleTriggerEnterEvent -- Starts lightning attack when player enters trigger range
Trap_ThunderPriest:HandleTriggerLeaveEvent -- Stops lightning attack when player leaves trigger range
Trap_Torpedo:Explosion -- Executes explosion effect and applies knockback when player touches torpedo
Trap_Torpedo:OnBeginPlay -- Sets knockback power during torpedo trap initialization
Trap_Torpedo:HandleTriggerEnterEvent -- Changes to explosion state when player enters trigger and executes explosion
Trap_Torpedo:HandleSpriteAnimPlayerChangeFrameEvent -- Deactivates entity when explosion animation ends
GoldApple:OnUpdate -- Gold apple moves toward target position at specified speed
GoldApple:OnBeginPlay -- Sets timer to automatically remove gold apple after 3 seconds when created
GoldAppleReward:HandleFootholdCollisionEvent -- Gradually becomes transparent and disappears when gold apple collides with ground
Trap_Cupid:OnBeginPlay -- Cupid trap initialization and periodic attack timer setup
Trap_Cupid:SpawnArrow -- Creates cupid arrow and sets properties, manages lifecycle
Trap_Cupid:HandleSpriteAnimPlayerEndFrameEvent -- Restores sprite to original state when attack animation ends and creates arrow
Trap_CupidArrow:OnUpdate -- Moves arrow according to direction and acceleration after initialization is complete
Trap_CupidArrow:Init -- Initializes cupid arrow's direction, velocity, rotation, and flip state
Trap_CupidArrow:HandleTriggerEnterEvent -- Applies magic effect on collision with player and removes arrow
Trap_DevilBullet:OnUpdate -- Moves devil bullet according to direction and acceleration after initialization is complete
Trap_DevilBullet:Init -- Initializes devil bullet's direction, velocity, size, rotation, and flip state
Trap_DevilBullet:HandleTriggerEnterEvent -- Applies magic dispel effect on collision with player and removes bullet
Trap_HeartBullet:OnUpdate -- Heart bullet movement - advances then quickly returns in reverse direction
Trap_HeartBullet:OnBeginPlay -- Sets timer to switch to reverse direction at half of lifespan when heart bullet is created
Trap_HeartBullet:HandleTriggerEnterEvent -- Disappears when reaching spawn point, applies magic effect and damage on player collision
Trap_LittleDevil:OnBeginPlay -- Devil gimmick should only be placed left/right (diagonal placement causes spawn logic issues)
Trap_LittleDevil:SpawnArrow -- Sets devil arrow creation position and fires according to left/right direction
Trap_LovePoison:HandleTriggerEnterEvent -- Plays sound and applies magic effect when player contacts love poison
Trap_LoveStatus:OnBeginPlay -- Love status trap initialization, periodically fires heart bullets after warning effect
Trap_LoveStatus:Shot -- Fires 5-8 heart bullets in 360-degree circular pattern
TempleApollonManager:OnBeginPlay -- Apollo temple manager initialization, creates worship objects at specified times
Trap_Sun:FireCircle -- Fires bullets in circular pattern from sun trap (currently commented out)
Trap_Sun:OnBeginPlay -- Sun trap initialization and repeated firing pattern setup (currently commented out)
Trap_Sun:HandleTriggerEnterEvent -- Applies instant death damage when player contacts sun trap
Trap_SunBullet:OnUpdate -- Sun bullet directional movement and rotation effect
Trap_SunBullet:OnBeginPlay -- Sets lifespan timer for automatic destruction when sun bullet is created
Trap_SunBullet:HandleTriggerEnterEvent -- Applies burn stack and damage on player collision then destroys bullet
RotateDegree180:OnUpdate -- Continuously rotates clockwise/counterclockwise within 180-degree range
RotateDegree180:OnBeginPlay -- Initializes rotation state and sets sprite transparency
RotateDegree180:HandleTriggerEnterEvent -- Applies pushing force according to rotation direction on player contact and changes state
Trap_Arrow:OnUpdate -- Arrow trap moves according to direction and velocity
Trap_Arrow:HandleTriggerEnterEvent -- Applies pushback and destroys arrow on player collision (currently commented out)
Trap_ArrowShooter:OnBeginPlay -- Arrow shooter initialization and periodic firing timer setup
Trap_ArrowShooter:Shot -- Shows arrow firing preparation effect then creates and fires arrow after set time
DemeterTempleManager:Rebirth -- Rebirths player with spring theme to change map environment and disable traps
DemeterTempleManager:SetColorAlpha -- Adjusts masking UI alpha value for screen transition effect to execute fade in/out animation
DemeterTempleManager:OnBeginPlay -- Sets player movement drag when entering Demeter temple
DemeterTempleManager:HandleInteractionEvent -- Executes spring magic effect to transform temple when interacting with altar
DemeterTempleManager:HandleInteractionEnterEvent -- Shows guide key UI when entering near altar
DemeterTempleManager:HandleInteractionLeaveEvent -- Hides guide key UI when moving away from altar
SnowMan:destroy -- Plays snowman destruction animation quickly and executes destruction sound and effect
SnowMan:HandleSpriteAnimPlayerEndFrameEvent -- Restores player to original state when destruction animation ends and removes snowman entity
HadesWaterBuff:Use -- Uses Hades water to increase player movement speed then lowers transparency to indicate usage completion
HadesWaterBuff:HandleInteractionEnterEvent -- Shows usage guide when player enters near Hades water
HadesWaterBuff:HandleInteractionLeaveEvent -- Hides guide UI when player moves away from Hades water
HadesWaterBuff:HandleInteractionEvent -- Applies speed buff and removes guide UI when player interacts with Hades water
SpawnThroneManager:SpawnRandomMiningTarget -- Activates specified number of random throne traps and sets damage
SpawnThroneManager:OnBeginPlay -- Randomly spawns throne traps targeting local player during initialization
TempleHadesManager:OnBeginPlay -- Performs initialization to set game environment when entering Hades temple
TempleHadesManager:StartGame -- Starts grim reaper chase game and activates game state after 3 seconds
TempleHadesManager:SetHadesPlay -- Sets Hades temple game mode and initializes player state
TempleHadesManager:HandleButtonClickEvent -- Starts game and closes UI when entry confirmation button is clicked
TempleHadesManager:HandleKeyDownEvent -- Performs same function as entry confirmation button click when E key is pressed
Trap_ChaseSasin:OnUpdate -- Grim reaper chases player when Hades game starts and increases speed multiplier on game over
Trap_ChaseSasin:Chase -- Chases player and executes attack when within certain distance then handles game over
Trap_ChaseSasin:OnBeginPlay -- Stores original speed during initialization for later speed increase processing
Trap_GhostSpawner:OnBeginPlay -- Repeatedly creates ghosts according to set cooldown when Hades game starts
Trap_Hades_Throne:HandleTriggerEnterEvent -- Switches to game over state and executes success effect when player touches Hades throne
Trap_StoneFish:OnUpdate -- Manages stone fish left/right movement and attack state while periodically dealing damage
Trap_StoneFish:OnBeginPlay -- Activates attack range and sets cooldown during initialization
Trap_StoneFish:HandleTriggerEnterEvent -- Activates attack effect when player enters stone fish attack range
Trap_StoneFish:HandleTriggerLeaveEvent2 -- Deactivates attack effect and resets cooldown when player leaves attack range
Trap_StoneFishRangeCheck:HandleTriggerLeaveEvent -- Deactivates attack mode when player leaves stone fish attack range
Trap_StoneFishRangeCheck:HandleTriggerStayEvent -- Activates attack mode when player stays in stone fish attack range
sampleBullet:OnUpdate -- Moves bullet in straight line with set direction and velocity
sampleBullet:HandleTriggerEnterEvent -- Increases burn stack on player collision and destroys bullet
Trap_RotateShooter:Shooter -- Executes trap system that rotates and fires bullets in all directions
Trap_RotateShooter:OnUpdate -- Continuously rotates bullet firing point to attack in various directions
Trap_RotateShooter:OnBeginPlay -- Stores original color during initialization and starts repeated firing with set cooldown
CloudLightningTriggerCheck:HandleTriggerStayEvent -- Executes electric damage when player is in lightning attack area and attack selection state
ElectricWarpInteraction:teleport -- Executes electric warp in specified direction to move player
ElectricWarpInteraction:reset -- Resets all directional arrows and guide UI after warp usage
ElectricWarpInteraction:destroyGuideKey -- Removes warp usage guide key UI
ElectricWarpInteraction:OnBeginPlay -- Sets portal usability state to false during component initialization
ElectricWarpInteraction:HandleKeyDownEvent -- Receives directional key input to execute electric warp in corresponding direction
ElectricWarpInteraction:HandleInteractionEvent -- Shows available directions and activates warp mode when player interacts with warp pad
ElectricWarpInteraction:HandleInteractionEnterEvent -- Shows usage guide UI when player enters near warp pad
ElectricWarpInteraction:HandleInteractionLeaveEvent -- Removes guide UI when player moves away from warp pad
ElectricWarpSwitchInteraction:Switch -- Switches electric warp switch from off to on to activate warp line
ElectricWarpSwitchInteraction:destoryGuideKey -- Deactivates and hides usage guide UI
ElectricWarpSwitchInteraction:OnBeginPlay -- Sets guide image reference on server
ElectricWarpSwitchInteraction:HandleInteractionEvent -- Switches switch to on when interacting to activate warp
ElectricWarpSwitchInteraction:HandleInteractionEnterEvent -- Shows guide UI when entering near switch and informs usage method
ElectricWarpSwitchInteraction:HandleInteractionLeaveEvent -- Hides guide UI and shows default image when moving away from switch
TrapRotatingForward:OnUpdate -- Continuously rotates entity at set rotation speed
Trap_DeathLightning:OnBeginPlay -- Sets lightning transparent during initialization and enables activation after 2.5 seconds
Trap_DeathLightning:Init -- Switches to electric damage activation ready state by clearing initialization tag
Trap_DeathLightning:HandleTriggerStayEvent -- Applies electric damage when player stays in activation range and makes lightning fully visible
Trap_DeathLightning:HandleTriggerLeaveEvent -- Sets lightning transparent again when player leaves activation range
AbilityIcon:GetAbilityIconRUID -- Returns RUID of corresponding ability icon based on ability name
AbilityIcon:GetAbilityIconRUIDByIndex -- Returns ability icon RUID based on index
AbilityIcon:GetAbilityNameByIndex -- Returns ability name based on index
CustomLocalizationLogic:OnBeginPlay -- Loads multilingual table at client start and applies multilingual text to UI elements
CustomLocalizationLogic:ApplyLocalizeOfCommonWordOnUI -- Manually applies multilingual localization to commonly used UI elements (buttons, messages, etc.)
CustomLocalizationLogic:SendLocalizedToastMessageFromServer -- Shows multilingual toast message with message key received from server
CustomLocalizationLogic:SendLocalizedFormattedToastMessageFromServer -- Shows formatted multilingual toast message with message key and arguments received from server
CustomLocalizationLogic:SetInstallationObjectsNametag -- Sets multilingual nametag including owner and item type for installation entities
LeaderBoard:SaveData -- Saves player's ranking score (RP) and nickname to database
LeaderBoard:LoadData -- Loads ranking data from server in descending order and updates rankings of connected users
LeaderBoard:OnUpdate -- Automatically updates ranking data at the top of each hour
LeaderBoard:OnBeginPlay -- Loads initial ranking data at server start
ParsingLogic:ParseByType -- Converts string value to specified type (string, number, boolean) and returns
ParsingLogic:GetInitValueByType -- Returns default initial value for specified type (string:"", number:0, boolean:false)
ThousandsSeparator:Separate -- Converts numbers to easy-to-understand format by separating with commas (,) every 3 digits
ThousandsSeparator:ConvertToMetricPrefixString -- Converts large numbers to abbreviated format (wan, eok, K, M, etc.) according to regional settings
ThousandsSeparator:Round -- Rounds numbers to specified unit (significance) for accurate values
ThousandsSeparator:OldConvertToMetricPrefixString -- Previous version of abbreviated string conversion method (supports regional units)
TutorialGuide:PlayGuide -- Plays tutorial guide at specific index and displays on screen
TutorialGuide:ShowNextMessage -- Gets next message from queue and outputs on screen with animation
TutorialGuide:OnBeginPlay -- Initializes tutorial data at client start and loads saved data
TutorialGuide:LoadData -- Loads user's tutorial progress state and condition data from server
TutorialGuide:SaveData -- Saves user's tutorial progress state and condition data to server
TutorialGuide:OnTableChanged -- Applies table data received from server to corresponding client table
TutorialGuide:AddCondition -- Adds specific tutorial condition and plays guide when condition is satisfied
TutorialGuide:HandleButtonClickEvent -- Shows next tutorial message when next message button is clicked
TutorialGuide:HandleButtonClickEvent2 -- Ends tutorial and opens corresponding UI when exit button is clicked
TutorialGuide:HandleLocalPlayerMapEnterEvent -- Plays corresponding tutorial according to conditions when player enters map
UIAlarmMarker:SetEnableMarker -- Activates/deactivates alarm marker corresponding to specified UI and manages menu button marker
UIAlarmMarker:HandleButtonClickEvent -- Deactivates corresponding alarm marker when title system button is clicked
UIAlarmMarker:HandleButtonClickEvent2 -- Deactivates corresponding alarm marker when emoticon system button is clicked
UIAlarmMarker:HandleButtonClickEvent3 -- Deactivates corresponding alarm marker when relic book system button is clicked
UIAlarmMarker:HandleButtonClickEvent4 -- Deactivates corresponding alarm marker when chair system button is clicked
UIAlarmMarker:HandleButtonClickEvent5 -- Deactivates corresponding alarm marker when pet system button is clicked
UIAlarmMarker:HandleButtonClickEvent6 -- Deactivates corresponding alarm marker when void item system button is clicked
UIGetLog:AddLog -- Adds item acquisition log to message queue and displays on screen with animation
UIGetLog:PrintVoidItemLog -- Creates and displays void item acquisition log on screen with animation
UIGetLog:AddLog_Accessory -- Displays accessory acquisition log with special color and style
UIGetLog:PrintLuckAbilityLog -- Displays luck ability activation log on screen with special effects
UIGetLog:OnBeginPlay -- Initializes log display entities at client start and sets to standby state
UIGetLog:OnUpdate -- Updates log message times every frame and handles fade-out animation
UIPopup:Open -- Opens popup dialog with message and callback function and starts appearance animation
UIPopup:OnClickOk -- Executes OK callback after OK button click then closes popup
UIPopup:OnClickCancel -- Executes Cancel callback after cancel button click then closes popup
UIPopup:Close -- Closes popup dialog while disconnecting events and starting disappearance animation
UIPopup:StartTween -- Handles popup appearance/disappearance animation with timer for smooth execution
UIToast:ShowMessage -- Shows toast message for default 2 seconds and starts animation
UIToast:StartTween -- Handles toast message appearance/disappearance animation for specified duration
UIToast:ShowMessageDuration -- Shows toast message for user-specified duration and starts animation
TempleExplorerBox:SetTravelerBoxResultUI -- Sets explorer box interaction result UI and displays obtained item information
TempleExplorerBox:OnBeginPlay -- Initializes interactable guide image at server start
TempleExplorerBox:OnInteractionEvent -- Plays sound and provides random exploration tool with UI display on explorer box interaction
TempleExplorerBox:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleExplorerBox:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleExplorerBox:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleFountain:SetTravelerBoxResultUI -- Sets potion generator interaction result UI and displays obtained potion information
TempleFountain:OnBeginPlay -- Initializes interactable guide image at server start
TempleFountain:OnInteractionEvent -- Plays sound and provides fixed potion with UI display on potion maker interaction
TempleFountain:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleFountain:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleFountain:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleGemBox:OnBeginPlay -- Initializes interactable guide image at server start
TempleGemBox:OnInteractionEvent -- Plays sound and calls server logic with UI display on Hades treasure box interaction
TempleGemBox:OnInteractionEventOnServer -- Handles treasure box interaction on server: checks cooldown then provides gems according to construction level
TempleGemBox:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleGemBox:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleGemBox:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleGoldstatus:OnBeginPlay -- Initializes interactable guide image at server start
TempleGoldstatus:OnInteractionEvent -- Plays sound and calls server logic on Plutus golden staff interaction
TempleGoldstatus:OnInteractionEventOnServer -- Handles golden staff interaction on server: confirms cooldown, provides gold, updates UI
TempleGoldstatus:SetGoldRewardUI -- Sets golden staff interaction result UI and deactivates after set time
TempleGoldstatus:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleGoldstatus:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleGoldstatus:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleHarp:OnBeginPlay -- Initializes interactable guide image at server start
TempleHarp:OnInteractionEvent -- Plays sound and recovers stamina with UI display on Apollo harp interaction
TempleHarp:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleHarp:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleHarp:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleMinerva:SetTravelerBoxResultUI -- Sets Minerva's wisdom interaction result UI and displays obtained potion information
TempleMinerva:OnBeginPlay -- Initializes interactable guide image at server start
TempleMinerva:OnInteractionEvent -- Plays sound and provides 2-3 potions with UI display on Minerva's wisdom interaction
TempleMinerva:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleMinerva:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleMinerva:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TemplePegasus:OnBeginPlay -- Initializes interactable guide image at server start
TemplePegasus:OnInteractionEvent -- Checks inventory items and processes server logic on Pegasus interaction
TemplePegasus:OnInteractionEventOnServer -- Handles Pegasus interaction on server: checks cooldown and usage count then sells items
TemplePegasus:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TemplePegasus:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TemplePegasus:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
TempleSiren:OnBeginPlay -- Initializes interactable guide image at server start
TempleSiren:OnInteractionEvent -- Plays sound and recovers stamina with UI display on Siren interaction
TempleSiren:HandleInteractionEvent -- Entity interaction event handler: calls OnInteractionEvent method
TempleSiren:HandleInteractionEnterEvent -- Creates and shows E key guide UI when entering interaction area
TempleSiren:HandleInteractionLeaveEvent -- Deactivates E key guide UI and shows default guide image when leaving interaction area
PortalToSpawnInteraction:HandleInteractionEvent -- Teleports to current map's spawn point when player interacts with portal
StarMovement:OnBeginPlay -- Sets star's initial movement direction randomly
StarMovement:OnUpdate -- Continuously moves star within specified area and changes direction at boundaries
StarMovement:HandleInteractionEvent -- Handles star collection when player interacts with star
StarMovementManager:OnBeginPlay -- Sets random colors and positions for child stars to manage within map
SwitchButtonUI:HandleButtonClickEvent -- Toggles target UI's activation/deactivation state when button is clicked
TrapBallonRope:OnBeginPlay -- Stores rope's original position to use as restoration reference point
TrapBallonRope:OnUpdate -- Processes rope movement up and down according to number of hanging players
TrapBallonRope:HandleTriggerEnterEvent -- Counts hanging personnel when player enters target area while riding rope
TrapBallonRope:HandleTriggerLeaveEvent -- Dedicated handling when player leaves rope area (currently empty)
TrapBigRock:OnUpdate -- Continuously rotates rock and plays sound at regular intervals
TrapBigRock:OnBeginPlay -- Rock trap initialization and cooldown setup
TrapBigRock:HandleTriggerEnterEvent -- Applies damage and provides pushback velocity when player contacts rock
TrapBlinkFoothold:OnUpdate -- Provides warning effect by making foothold blink when player steps on it
TrapBlinkFoothold:OnBeginPlay -- Initializes foothold deactivation timer at game start
TrapBlinkFoothold:HandleTriggerLeaveEvent -- Cancels blinking state when player leaves foothold
TrapBlinkFoothold:HandleTriggerEnterEvent -- Briefly increases gravity then schedules foothold deactivation when player steps on foothold
TrapBlinkFoothold:HandleTriggerStayEvent -- Maintains continuous interaction state while player is on foothold
TrapBlinkRope:OnUpdate -- Provides warning effect by making rope blink when player climbs on it
TrapBlinkRope:HandleTriggerLeaveEvent -- Cancels blinking state when player leaves rope
TrapBlinkRope:HandleTriggerEnterEvent -- Greatly increases gravity then schedules rope deactivation when player climbs on rope
TrapBlinkRope:HandleTriggerStayEvent -- Maintains continuous interaction state while player is on rope
TrapCactus:OnUpdate -- Handles cooldown for cactus spawn reservation after set time
TrapCactus:SpawnCactus -- Creates cactus spawn and processes automatic removal after set time
TrapChaseMobController:OnBeginPlay -- Controller initialization and signal button UI setup
TrapChaseMobController:SetUsed -- Synchronizes controller's usage state from server
TrapChaseMobController:HandleButtonClickEvent -- Switches between alpha/beta signals by clicking signal button
TrapChaseMobController:HandleButtonClickEvent2 -- Sends signal to robot and closes UI by clicking send button
TrapChaseMobController:HandleInteractionEvent -- Opens control UI when player interacts with controller
TrapChaseMonster:OnBeginPlay -- Randomly sets to alpha or beta signal at game start
TrapChaseMonster:Destroy -- Stops robot or attacks player according to transmitted signal
TrapChaseMonster:SendMessage -- Sends message to specific player and plays sound
TrapChaseMonster:OnUpdate -- Shows and updates repair time while robot is stopped
TrapChaseMonster:HandleTriggerEnterEvent -- Applies damage and cooldown when player approaches robot
TrapControllerLava:OnBeginPlay -- Sets fire hydrant name and lava solidification visual effect initialization
TrapControllerLava:OnInteractionEvent -- Temporarily solidifies lava and applies cooldown when operating fire hydrant
TrapControllerLava:HandleInteractionEvent -- Receives interaction event and calls fire hydrant operation method
TrapControllerLava:HandleInteractionEnterEvent -- Creates or activates guide UI when approaching fire hydrant
TrapControllerLava:HandleInteractionLeaveEvent -- Deactivates guide UI when moving away from fire hydrant
TrapDirShooter:OnUpdate -- Handles trap that rotates in 4 directions at regular intervals and fires lightning projectiles
TrapFillWater:HandleTriggerEnterEvent -- Removes fire state or applies regional special effects when player enters water
TrapFillWater:HandleTriggerLeaveEvent -- Clears existing timers and initializes state when player leaves water
TrapFireParabola:OnBeginPlay -- Initializes filter effects and sound ID
TrapFireParabola:HandleTriggerEnterEvent -- Applies damage and effects when player touches flame projectile then destroys projectile
TrapFireParabola:HandleFootholdCollisionEvent -- Immediately destroys projectile when it hits ground or other objects
TrapGasLava:OnUpdate -- Processes cycle that repeats 2 seconds gas emission followed by 2 seconds rest
TrapGasLava:HandleTriggerEnterEvent -- Applies damage and pushback effect when player touches gas lava if in attackable state
TrapGreatRock:ControlAngle -- Adjusts firing angle left and right and limits range
TrapGreatRock:Shoot -- Fires rock projectile at currently set angle
TrapGreatRock:Shift -- Switches UI and firing direction according to player's facing direction
TrapGreatRock:HandleKeyDownEvent -- Handles firing angle adjustment and firing with keyboard input
TrapGreatRock:HandleKeyHoldEvent -- Continuously adjusts angle while holding key
TrapGreatRock:HandleChangedLookAtEvent -- Synchronizes UI when player's facing direction changes
TrapGreatRock:HandleTriggerEnterEvent -- Activates control mode when player approaches cannon
TrapGreatRockUI:HandleKeyDownEvent -- Handler for keyboard input (currently not implemented)
TrapGuidedMissile:OnBeginPlay -- Sets guided missile target to local player
TrapGuidedMissile:OnUpdate -- Calculates distance to target and performs guided movement if within range
TrapIceFall:OnUpdate -- Executes falling logic every frame when in falling state
TrapIceFall:Falling -- Drops icicle downward and destroys after 5 seconds
TrapIceFallSensor:OnUpdate -- Decreases timer and creates icicle warning model when reaching 0
TrapIceFallSensor:SpawnCautionModel -- Creates warning model in icicle drop area and plays positional sound
TrapInteractionRock:ControlAngle -- Controls rock firing angle and updates UI arrow direction
TrapInteractionRock:Shoot -- Fires rock at set angle and direction then restores player control
TrapLava:OnUpdate -- Manages lava projectile to fire lava balls every 3 seconds if it's a lava shooter
TrapLava:HandleTriggerEnterEvent -- Initially applies burn stack when entering lava and starts continuous damage timer
TrapLava:HandleTriggerLeaveEvent -- Stops all running continuous damage timers when leaving lava
TrapLavaProjectile:MoveUp -- Fires lava ball upward in parabolic trajectory and deactivates after set time
TrapLavaProjectile:OnBeginPlay -- Damage increase adjustment only in ruins (commented out state)
TrapMagnetFieldMaker:Attack -- Executes magnetic field attack with effects and sound, applies damage and knockback to player
TrapMagnetFieldMaker:OnBeginPlay -- Initializes cooldown and starts attack at game start
TrapMagnetFieldMaker:Start -- Starts cooldown timer and repeatedly performs attack warning and execution
TrapMagnetFieldMaker:OnSyncProperty -- Updates countdown text UI when cooldown time is synchronized
TrapMagnetFieldMaker:HandleTriggerLeaveEvent -- Releases trigger state when player leaves collision area
TrapMagnetFieldMaker:HandleTriggerEnterEvent -- Activates trigger state when player enters collision area
TrapMagneticField:OnUpdate -- Manages magnetic field trap cooldown state and switches range/warning/attack UI
TrapMagneticField:Attack -- Applies electric damage and knockback when player is within magnetic field
TrapMagneticField:HandleTriggerStayEvent -- Maintains trigger state while player stays within magnetic field
TrapMagneticField:HandleTriggerLeaveEvent -- Releases trigger state when player leaves magnetic field area
TrapPoison:OnUpdate -- Continuously applies poison damage while inside poison trap
TrapRotateBar:OnUpdate -- Update logic that reciprocally rotates rotating bar angle at constant speed
TrapRotateBar:HandleTriggerEnterEvent -- Applies damage and burn stack to player and interrupts ladder/rope state
Trap_Electric:OnUpdate -- Updates attack cooldown to prevent falling below 0
