GoldAppleAltarInteraction:GiveReward -- 확률에 따라 골드, 젬, 또는 장신구 중 하나의 보상을 플레이어에게 지급
GoldAppleAltarInteraction:Sacrifice -- 플레이어가 황금사과를 제단에 바쳐 보상을 받는 처리
GoldAppleAltarInteraction:OnBeginPlay -- 컴포넌트 초기화 시 서버에서는 가이드 이미지를 설정하고 클라이언트에서는 초기 상태를 설정
GoldAppleAltarInteraction:SpawnReward -- 보상 타입에 따라 해당하는 시각적 보상 박스를 소환
GoldAppleAltarInteraction:CheckGoldAppleCountInServer -- 서버에서 플레이어의 황금사과 보유량을 확인하고 처리
GoldAppleAltarInteraction:SetRewardCountInClient -- 클라이언트에서 보상 개수를 설정하고 제단 상태를 업데이트
GoldAppleAltarInteraction:ShowMessage -- 황금사과가 없을 때 경고 메시지를 표시
GoldAppleAltarInteraction:PlaySoundInClient -- 클라이언트에서 지정된 사운드를 재생
GoldAppleAltarInteraction:HandleInteractionEnterEvent -- 플레이어가 제단 상호작용 범위에 들어왔을 때 가이드 키 UI를 표시
GoldAppleAltarInteraction:HandleInteractionLeaveEvent -- 플레이어가 제단 상호작용 범위를 벗어났을 때 가이드 키 UI를 숨김
GoldAppleAltarInteraction:HandleInteractionEvent -- 플레이어가 제단과 상호작용했을 때 황금사과 개수를 확인하고 제물 바치기 실행
GoldAppleAltarInteraction:HandleSpriteAnimPlayerChangeFrameEvent -- 제단 애니메이션 프레임 변화를 처리하여 보상 사과를 소환하거나 제단을 닫음
GoldAppleAltarInteraction:HandleTriggerEnterEvent -- 보상 사과가 트리거에 들어왔을 때 사과를 파괴하고 보상을 지급
InteractionTemplePortal:OnBeginPlay -- 컴포넌트 초기화 시 포털 위치에 따른 설정과 초기화 타이머 설정
InteractionTemplePortal:UsePortal -- 플레이어가 포털을 사용하여 신전으로 이동하는 처리
InteractionTemplePortal:Init -- 신전 포털의 UI 정보를 플레이어 층수에 맞게 초기화
InteractionTemplePortal:SetLoadingOn -- 마을에서 신전 이동 시 로딩 UI를 활성화하고 플레이어 움직임을 제한
InteractionTemplePortal:HandleInteractionEnterEvent -- 플레이어가 포털 상호작용 범위에 들어왔을 때 입장 가이드 UI를 표시
InteractionTemplePortal:HandleInteractionLeaveEvent -- 플레이어가 포털 상호작용 범위를 벗어났을 때 가이드 UI를 숨김
InteractionTemplePortal:HandleInteractionEvent -- 플레이어가 포털과 상호작용했을 때 신전으로 이동 실행
InteractionTemplePortal:HandleLocalPlayerChangedTempleStartingFloor -- 플레이어의 신전 시작층이 변경되었을 때 포털 정보를 갱신
JumpingMachine:ready -- 플레이어를 점프 머신에 올려놓고 발사 준비 상태로 설정
JumpingMachine:ChangeDirection -- 점프 방향 화살표를 주기적으로 변경하여 방향을 선택할 수 있게 함
JumpingMachine:jumping -- 설정된 방향과 힘으로 플레이어를 점프시켜 발사
JumpingMachine:OnBeginPlay -- 컴포넌트 시작 시 점프 머신을 초기 상태로 리셋
JumpingMachine:reset -- 점프 머신의 모든 상태를 초기화하고 화살표를 숨김
JumpingMachine:OnUpdate -- 회전형 점프 머신의 경우 지속적으로 회전시킴
JumpingMachine:HandleInteractionEvent -- 플레이어가 점프 머신과 상호작용할 때 준비 또는 발사 상태 전환
JumpingMachine:HandleInteractionLeaveEvent -- 플레이어가 점프 머신 상호작용 범위를 벗어났을 때 리셋
JumpingMachine:HandleInteractionEnterEvent -- 플레이어가 점프 머신 상호작용 범위에 들어왔을 때 가이드 UI 표시
KronosClockTowerUI:RefreshUI -- 크로노스 시계탑의 UI 정보를 플레이어 건설 레벨과 층수에 맞게 갱신
KronosClockTowerUI:HandleButtonClickEvent -- 최대 층수 버튼 클릭 시 건설 가능한 최고층으로 시작층을 설정
KronosClockTowerUI:HandleButtonClickEvent2 -- 최소 층수 버튼 클릭 시 시작층을 1층으로 설정
KronosClockTowerUI:HandleButtonClickEvent3 -- 층수 증가 버튼 클릭 시 시작층을 1층씩 증가
KronosClockTowerUI:HandleButtonClickEvent4 -- 층수 감소 버튼 클릭 시 시작층을 1층씩 감소
LandscapeTriggerBox:HandleTriggerEnterEvent -- 플레이어가 지형 트리거에 들어왔을 때 잠수 상태를 해제하고 중앙 공간 상태로 설정
LandscapeTriggerBox:HandleTriggerLeaveEvent -- 플레이어가 지형 트리거를 벗어났을 때 잠수 상태로 설정하고 중앙 공간 상태를 해제
MenuUI:SetMenuUI -- 현재 선택된 메뉴 상태에 따라 메뉴 버튼들과 메뉴 패널들의 활성화 상태를 설정
MenuUI:HandleButtonClickEvent -- 메뉴 1번 버튼 클릭 시 1번 메뉴를 표시
MenuUI:HandleButtonClickEvent2 -- 메뉴 2번 버튼 클릭 시 2번 메뉴를 표시
MenuUI:HandleButtonClickEvent3 -- 메뉴 3번 버튼 클릭 시 3번 메뉴를 표시
MenuUI:HandleButtonClickEvent4 -- 종료 버튼 클릭 시 메뉴를 닫아 초기 상태로 변경
MenuUI:HandleButtonClickEvent5 -- 닫기 버튼 클릭 시 메뉴를 닫아 초기 상태로 변경
MenuUI:HandleButtonClickEvent6 -- 닫기 버튼 클릭 시 메뉴를 닫아 초기 상태로 변경
MenuUI:HandleButtonClickEvent7 -- 닫기 버튼 클릭 시 메뉴를 닫아 초기 상태로 변경
MenuUI:HandleLocalPlayerMapEnterEvent -- 플레이어가 마을 맵에 입장했을 때 메뉴를 초기 상태로 리셋
NPCTempleSnake:CheckRelicCollectionAcheivement -- 플레이어의 유물 도감 100% 달성 여부를 확인하고 신전 입장 권한을 부여
NPCTempleSnake:HandleTriggerEnterEvent -- 플레이어가 신전 뱀 NPC 트리거에 들어왔을 때 유물 도감 달성도를 확인
simulateButton:HandleButtonClickEvent -- 치트 시뮬레이션 버튼 클릭 시 입력된 값에 따라 해당하는 시뮬레이션을 실행
SunWorship:OnUpdate -- 태양을 중심으로 원형 궤도를 그리며 움직이고 위치에 따라 방향 표시를 변경
SunWorship:OnBeginPlay -- 컴포넌트 초기화 (현재는 특별한 초기화 로직 없음)
SunWorship:HandleTriggerLeaveEvent -- 총알이 트리거를 벗어났을 때 해당 총알을 파괴
TableSync:SetTableClient -- 서버에서 전송된 전체 테이블 데이터를 클라이언트에서 동기화
TableSync:SetTableElementClient -- 테이블의 특정 인덱스 값을 서버에서 클라이언트로 동기화
TableSync:ClearTableClient -- 클라이언트의 테이블을 초기값으로 전체 초기화
AchievementItemUI:OnBeginPlay -- UI 컴포넌트들의 참조를 초기화하고 설정
AchievementItemUI:Refresh -- 업적 데이터에 따라 UI 요소들을 갱신하고 상태에 맞는 버튼을 설정
AchievementItemUI:Clear -- UI 요소들을 정리하고 초기화 (현재는 특별한 정리 작업 없음)
AchievementRewardClaimButtonUI:HandleButtonClickEvent -- 업적 보상 받기 버튼 클릭 시 해당 업적의 보상을 지급하고 버튼을 비활성화
AchievementUI:OnBeginPlay -- 업적 UI 초기화 시 그리드뷰 설정과 데이터 테이블을 로드
AchievementUI:OnRefresh -- 그리드뷰의 각 아이템을 갱신할 때 호출되는 콜백 함수
AchievementUI:OnClear -- 그리드뷰의 각 아이템을 정리할 때 호출되는 콜백 함수
AchievementUI:InitAchievementDataTable -- 업적 데이터 테이블을 초기화하고 플레이어 진행상황과 함께 아이템 테이블을 구성
AchievementUI:LoadAchievementDataTable -- 플레이어의 최신 업적 진행도와 완료 상태를 불러와서 아이템 테이블을 갱신
AchievementUI:RefreshUI -- UI를 새로고침하도록 플래그를 설정
AchievementUI:LoadAchivementRUIDDataTable -- 업적 타입과 보상 아이템의 이미지 RUID 정보를 테이블에서 불러와 매핑
AchievementUI:OnUpdate -- 새로고침 플래그가 설정되어 있으면 업적 리스트를 갱신
AchievementUI:HandleKeyDownEvent -- ESC 키 입력 시 업적 UI를 닫음
PlayerAchievementComponent:OnBeginPlay -- 컴포넌트 초기화 시 업적 진행도와 완료 상태 테이블을 설정
PlayerAchievementComponent:GetProgress -- 업적 진행도를 증가시키고 완료 조건 달성 시 완료 처리
PlayerAchievementComponent:PopupCompleteUI -- 업적 완료 시 페이드 효과가 있는 완료 UI를 표시
PlayerAchievementComponent:SetTableClient -- 서버에서 전송된 테이블 데이터를 클라이언트에서 동기화
PlayerAchievementComponent:SetTableElementClient -- 테이블의 특정 인덱스 값을 서버에서 클라이언트로 동기화
PlayerAchievementComponent:ClearTableClient -- 클라이언트의 테이블을 초기값으로 전체 초기화
PlayerAchievementComponent:ChangedTable -- 업적 테이블이 변경되었을 때 UI를 갱신하고 알람 마커를 설정
PlayerAchievementComponent:ClearAllProperty -- 모든 업적 진행도와 완료 상태를 초기화
PlayerAchievementComponent:LoadedUserData -- 저장된 업적 데이터를 불러와 진행도와 완료 상태를 복원
PlayerAchievementComponent:OnMapEnter -- 특정 맵에 입장했을 때 해당하는 업적 진행도를 증가시킴
PlayerAchievementComponent:GiveReward -- 플레이어에게 업적 보상을 주는 코드입니다.
PlayerAchievementComponent:SetAlarmMarker -- 보상 수령이 가능한 업적이 1개라도 있으면 마커를 활성화하고, 아니면 비활성화
CheatButton:HandleButtonClickEvent -- 치트 버튼 클릭 시 해당하는 치트 타입을 서버에서 실행
CheatManager:OnBeginPlay -- 게임 시작 시 관리자 계정 목록을 초기화
CheatManager:UseCheatOnServer -- 관리자 권한을 확인하고 다양한 치트 명령을 실행
CheatManager:IsAdmin -- 주어진 PPSN이 관리자 권한을 가지고 있는지 확인
CheatManager:InitPPSN -- 관리자 권한을 가진 계정들의 PPSN 목록을 초기화
CheatManager:GiveReward -- 유적지 채굴 치트에서 유물 드롭 여부를 결정하고 보상을 지급
CheatManager:SetUI_RelicBoxResult -- 유물상자 개봉 결과를 UI로 표시
CheatManager:SetCheatUIEnableOnServer -- 관리자인지 확인 후 치트 UI를 활성화
CheatManager:SetCheatUIEnableOnClient -- 클라이언트에서 치트 UI 그룹을 활성화
CheatManager:UseCheatForTest0314 -- 테스트용 치트로 모든 아이템과 진행사항을 플레이어에게 지급
CheatManager:ResetDB -- 플레이어의 모든 데이터를 초기 상태로 리셋
CheatManager:HandleKeyDownEvent -- 키보드 입력 처리로 스페이스키와 숫자키 조합으로 치트 활성화
CheatManager:HandleKeyUpEvent -- 키보드 키를 뗄 때 처리하여 치트 입력 상태를 해제
CheatManager:HandleButtonClickEvent -- 테스트 버튼 클릭 시 모든 아이템과 진행사항을 지급하는 치트 실행
GuideMessageTrigger:OnBeginPlay -- 가이드 메시지 트리거 초기화
GuideMessageTrigger:HandleTriggerEnterEvent -- 플레이어가 트리거에 진입하면 가이드 메시지 표시
IcicleSellNPCInteraction:OnBeginPlay -- 고드름 판매 NPC 상호작용 초기화
IcicleSellNPCInteraction:OnInteractionEvent -- 고드름 재료를 모두 판매하는 처리
IcicleSellNPCInteraction:HandleInteractionEvent -- NPC와 상호작용 이벤트 처리
IcicleSellNPCInteraction:HandleInteractionEnterEvent -- NPC에 근접 시 가이드 UI 표시
IcicleSellNPCInteraction:HandleInteractionLeaveEvent -- NPC에서 먀어질 때 가이드 UI 비활성화
InventoryButtonUI:OnUpdate -- 인벤토리 UI 새로고침 요청 처리
InventoryButtonUI:RefreshUI_Inner -- 인벤토리 용량 정보를 UI에 반영
InventoryButtonUI:RefreshUI -- 인벤토리 UI 새로고침 예약
InventoryUISlotButton_RelicBox:HandleButtonClickEvent -- 인벤토리 유물박스 슬롯 버튼 클릭 이벤트
OutGameUIButtonEnabler:HandleLocalPlayerMapEnterEvent -- 맵 이동에 따른 UI 버튼 활성화/비활성화 처리
RopeCorrection:OnBeginPlay -- 로프 충돌 박스 크기 보정
TrapManager:OnBeginPlay -- 신전 트랩 매니저 초기화
TrapManager:Init -- 플레이어 능력에 따른 신전 트랩 데미지 설정
LocalizationNPC:OnBeginPlay -- NPC 이름과 채팅밌룬 지역화 초기화
LocalizationNPC:SetLocalization -- NPC의 이름과 채팅밌룬 텍스트 지역화 설정 (구 버전)
LocalizationNPC:Localize -- NPC 이름과 채팅밌룬 텍스트를 데이터 테이블에서 가져와 지역화 설정
LocalizationUIModel:OnBeginPlay -- UI 모델 텍스트 지역화 초기화
LocalizationUIModel:Localize -- UI 모델의 텍스트를 지역화 데이터로 설정
DeadZone:HandleTriggerEnterEvent -- 플레이어가 데드존에 진입 시 사망 처리
DroppedChair:SetSpriteRUID -- 드롭된 의자의 스프라이트 설정
DroppedChair:OnBeginPlay -- 드롭된 의자가 플레이어를 따라가고 자동 픽업
DroppedChair:SetItemProperty -- 드롭된 의자의 인덱스 설정
DroppedGoldBox:OnBeginPlay -- 드롭된 골드박스가 플레이어를 따라가고 자동 픽업
DroppedItem:SetSpriteRUID -- 드롭된 아이템의 스프라이트 설정
DroppedItem:OnBeginPlay -- 드롭된 아이템이 플레이어를 따라가고 자동 픽업
DroppedItem:SetItemProperty -- 드롭된 아이템의 속성 설정
DroppedMaterial:OnBeginPlay -- 드롭된 재료 아이템이 플레이어를 따라가고 자동 픽업
DroppedRelicBox:OnBeginPlay -- 드롭된 유물박스가 플레이어를 따라가고 자동 픽업
ExplorerBoxInteraction:SetTravelerBoxResultUI -- 탐험가 상자 개봉 결과 UI 표시
ExplorerBoxInteraction:OnBeginPlay -- 탐험가 상자 상호작용 초기화
ExplorerBoxInteraction:OnInteractionEvent -- 탐험가 상자 상호작용 시 아이템 지급
ExplorerBoxInteraction:HandleInteractionEvent -- 탐험가 상자 상호작용 이벤트 처리
ExplorerBoxInteraction:HandleInteractionEnterEvent -- 탐험가 상자에 근접 시 가이드 UI 표시
ExplorerBoxInteraction:HandleInteractionLeaveEvent -- 탐험가 상자에서 멀어질 때 가이드 UI 비활성화
GameResultUI:OnBeginPlay -- 게임 결과 UI 초기화 및 아이템 슬롯 생성
GameResultUI:HandleKeyDownEvent -- 게임 결과화면에서 E키/ESC키로 마을로 이동
MiningGame:OnBeginPlay -- 채광 미니게임 컴포넌트 초기화
MiningGame:InitMinningGame -- 채광 미니게임의 초기 설정 및 UI 구성
MiningGame:StartMinningGame -- 채광 미니게임 시작 처리
MiningGame:OnUpdate -- 채광 미니게임 타이밍 화살표 이동 처리
MiningGame:Hit -- 채광 타이밍 결과 처리 및 데미지 계산
MiningGame:SetTimingBarToRandomPos -- 채광 게임의 타이밍바 위치를 랜덤 설정
MiningGame:FinishGame -- 채광 미니게임 종료 및 보상 지급 처리
MiningGame:GiveReward -- 채광 성공 시 보상 지급 요청
MiningGame:ExitGame -- 채광 미니게임 강제 종료 처리
MiningGame:SetBonusGame -- 보너스 게임 모드 설정 및 UI 구성
MiningGame:HandleButtonClickEvent -- 채광 미니게임 시작 버튼 클릭 이벤트
MiningGame:HandleKeyDownEvent -- E키 입력으로 채광 게임 시작/타이밍 이벤트
MiningGame:HandleKeyDownEvent2 -- ESC키 입력으로 채광 게임 취소 이벤트
MiningTargetManager:SpawnRandomMiningTarget -- 맵에서 랜덤한 위치에 채광 대상들을 스폰
MiningTargetManager:OnBeginPlay -- 채광 대상 매니저 초기화
MiningTargetObject:OnBeginPlay -- 채광 대상 오브젝트 초기화 및 설정
MiningTargetObject:SetActivateEntity -- 채광 대상 엔티티의 활성화/비활성화 설정
MiningTargetObject:SetSpriteRUID -- 채광 대상의 스프라이트와 렌더링 레이어 설정
MiningTargetObject:GiveReward -- 채광 성공 시 플레이어에게 보상 지급 처리
MiningTargetObject:DropItem -- 채광 시 기본 광물 아이템 드롭 처리
MiningTargetObject:DropJewerly -- 보너스 보상으로 보석류 아이템 드롭 처리
MiningTargetObject:DropFossilBox -- 보너스 보상으로 화석 아이템 드롭 처리
MiningTargetObject:DropMoneyBox -- 보너스 보상으로 골드박스 드롭 처리
MiningTargetObject:DropRelicBox -- 보너스 보상으로 유물박스 드롭 처리
MiningTargetObject:SetUI_KeyboxSuccess -- 열쇠박스 성공 시 결과 UI 표시
MiningTargetObject:DropMaterial -- 특수 재료 아이템 드롭 처리
MiningTargetObject:DropChair -- 보너스 보상으로 의자 아이템 드롭 처리
MiningTargetObject:SetPanel -- 채광 대상 오브젝트의 인터랙션 패널 UI 설정
MiningTargetObject:OnInteractionEvent -- 플레이어가 채광 대상과 상호작용 시 처리
MiningTargetObject:OnInteractionEventOnClient -- 클라이언트에서 채광 미니게임 시작 처리
MiningTargetObject:RemoveVisitRecord -- 플레이어의 채광 대상 방문 기록 제거
MiningTargetObject:SetUI_GoldBoxResult -- 골드박스 개봉 결과 UI 표시
MiningTargetObject:SetUI_RelicBoxResult -- 유물박스 개봉 결과 UI 표시
MiningTargetObject:Init -- 채광 대상 오브젝트 초기화 (인스펙터에서 사용)
MiningTargetObject:HandleInteractionEvent -- 채광 대상과 상호작용 이벤트 처리
MiningTargetObject:HandleInteractionEnterEvent -- 채광 대상에 근접 시 가이드 UI 표시
MiningTargetObject:HandleInteractionLeaveEvent -- 채광 대상에서 멀어질 때 가이드 UI 비활성화
LightComponent:OnBeginPlay -- 라이트 컴포넌트 초기화 - 사용자 라이트 데이터 로드 및 상호작용 비활성화
LightComponent:TurnOn -- 라이트 켜기 - 상태 변경 및 데이터 저장
LightComponent:makeTriggerEnable -- 라이트 상태에 따라 트리거 컴포넌트 활성화/비활성화
LightComponent:SaveLightOnData -- 라이트 on/off 데이터를 사용자 데이터 저장소에 비동기 저장
LightComponent:LoadLightOnData -- 사용자 데이터 저장소에서 라이트 on/off 데이터를 비동기 로드
LightComponent:OnSyncProperty -- turnedOn 속성 동기화 시 트리거 컴포넌트 상태 업데이트
LightInteraction:OnInteraction -- 라이트 상호작용 시 라이트 켜기 실행
LightInteraction:HandleInteractionEnterEvent -- 상호작용 진입 시 가이드 키 UI 생성 및 표시
LightInteraction:HandleInteractionLeaveEvent -- 상호작용 진출 시 가이드 키 UI 비활성화
ExtendPlayerControllerComponent:ActionDownJump -- 아래 점프 사용 비활성화 (기존 또는 대의성)
ExtendPlayerControllerComponent:ActionSit -- 앉아서 의자 기능 사용 (마을에서만 사용 가능)
ExtendPlayerControllerComponent:ActionDash -- 대쉬 스킬 실행 - MP 소모, 쿨다운, 공허 아이템 효과 처리
ExtendPlayerControllerComponent:SitOnChair -- 의자에 앉기 - 중력 비활성화 및 위치 조정
ExtendPlayerControllerComponent:SitOnChair_Server -- 서버에서 의자에 앉아벤그상 점프 비활성화
ExtendPlayerControllerComponent:OnBeginPlay -- 컴포넌트 초기화 시 상태 체크 및 기본 값 설정
ExtendPlayerControllerComponent:Skill_Run -- 2번 펫의 달리기 스킬 - 레벨에 따른 지속시간과 쿨다운
ExtendPlayerControllerComponent:OnUpdate -- 매 프레임마다 펫 스킬 UI 업데이트 및 각종 스킬 지속 효과 처리
ExtendPlayerControllerComponent:Skill_Superjump -- 3번 펫의 도움닫기 점프 스킬 - 게이지 충전량에 비례한 점프력
ExtendPlayerControllerComponent:Skill_Flashjump -- 4번 펫의 공중 대쉬 스킬 - 레벨에 따른 MP 소모량 감소
ExtendPlayerControllerComponent:Skill_AirJump -- 6번 펫의 공중점프 스킬 - 현재 Y 속도 유지하며 위로 점프
ExtendPlayerControllerComponent:Skill_FastFall -- 7번 펫의 고속 낙하 스킬 - 레벨에 비례한 낙하 속도
ExtendPlayerControllerComponent:Skill_SlowFall -- 마나가 적으면 발동 안함
ExtendPlayerControllerComponent:ActionJump -- 기본 점프 시 활강 상태 일시 비활성화 뒤 기본 점프 수행
ExtendPlayerControllerComponent:HandleKeyDownEvent -- 키 눌렀을 때 각종 펫 스킬 실행 (Shift: 대쉬/공중대쉬, Space: 공중점프, S: 고속냙하)
ExtendPlayerControllerComponent:HandleKeyDownEvent2 -- 두 번째 키 눌렀 핸들러 - 달리기와 도움닫기 차징 효과
ExtendPlayerControllerComponent:HandleKeyHoldEvent -- 키 계속 누르고 있을 때 - 도움닫기 차징, 가속, 활강 스킬 처리
ExtendPlayerControllerComponent:HandleKeyUpEvent -- 키에서 손 떼을 때 - 도움닫기 점프 실행, 가속 종료, 활강 종료
ExtendPlayerControllerComponent:HandleFootholdCollisionEvent -- 지형과 충돌했을 때 공중 스킬 상태 리셋 (사다리나 버티컬 면에는 리셋 안됨)
ExtendPlayerControllerComponent:HandleStateChangeEvent -- 상태 변경시 특대 가능 상태에서 공중 스킬들 리셋
ExtendPlayerControllerComponent:HandleFootholdLeaveEvent -- 지형에서 떨어졌을 때 생성되는 이벤트 (현재 비어있음)
PlayerConstruction:OnBeginPlay -- 건설 컴포넌트 초기화 - 테이블 리스트와 타입 설정
PlayerConstruction:SetTableClient -- 서버에서 클라이언트로 테이블 데이터 전체 동기화
PlayerConstruction:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 인덱스 값 동기화
PlayerConstruction:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 리셋
PlayerConstruction:ChangedTable -- 테이블 변경 시 건설 샵 UI 새로고침 및 건설 이벤트 전송
PlayerConstruction:LoadedData -- 데이터베이스에서 건설물 데이터 로드 후 업적 처리
PlayerConstruction:UnlockConstruction -- 건설물 해금 - 비용지불 후 해금 및 업적 처리
PlayerConstruction:BuyConstruction -- 건설물 구매(레벨업) - 비용지불 후 레벨 상승 및 업적 처리
PlayerConstruction:PlayPurchaseDirection -- 구매/해금 연출 재생 - 타입에 따라 해금 또는 기대 연출
PlayerData:OnBeginPlay -- 플레이어 데이터 컴포넌트 초기화 및 서버에서 데이터 로드
PlayerData:OnSyncProperty -- 동기화 속성이 변경될 때 관련 UI를 새로고침
PlayerData:OnEndPlay -- 게임 종료시 플레이어 데이터를 저장
PlayerData:OnUpdate -- 3~5분마다 데이터 저장
PlayerData:LoadData -- 데이터베이스에서 플레이어 데이터를 로드하고 실패시 재시도
PlayerData:SaveData -- 데이터 로드에 실패해서 퇴장하는 상황의 경우 데이터를 저장하지 않음
PlayerData:SellAllItems -- 플레이어 가방의 모든 아이템을 판매하고 보너스 계산
PlayerData:UseMoney -- 플레이어 돈을 차감
PlayerData:GetMoney -- 플레이어에게 돈을 지급하고 사운드 재생
PlayerData:AddEquipment -- 장비를 구매하여 인벤토리에 추가
PlayerData:ChangeEquipment -- 장착 장비를 변경하고 클라이언트에 동기화
PlayerData:ApplyPlayerStatus -- 데이터가 로드되기 전이라면 실행하지 않음
PlayerData:ChangeTownProgress -- 특정 마을의 진행도를 완료 상태로 변경
PlayerData:PurchaseTownAdmission -- 보유 여부 체크
PlayerData:ChangeEquipmentAvatarOnServer -- 장착중인 장비에 따라 캐릭터 외형을 변경
PlayerData:AddPetEgg -- 펫 알 개수를 1개 증가시킴
PlayerData:SetStatusUI -- 플레이어 능력치를 UI에 표시하고 채광력 HUD 업데이트
PlayerData:Reborn -- 조건 검증
PlayerData:PlayRebornDirection -- 환생 연출 UI를 재생
PlayerData:SetTableClient -- 서버에서 전달받은 테이블 데이터를 클라이언트에서 적용
PlayerData:SetTableElementClient -- 서버에서 전달받은 테이블의 특정 인덱스 값을 클라이언트에서 적용
PlayerData:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 리셋
PlayerData:ChangedTable -- 테이블이 변경될 때 관련 UI와 상태를 새로고침
PlayerData:ClearAllProperty -- 환생 시 모든 장비와 마을 진행도를 초기화 (마을1 제외)
PlayerData:LoadedUserData -- 데이터 로드 완료 후 클라이언트에 모든 테이블 데이터 동기화
PlayerData:OnMapEnter -- 맵 입장시 유적 방문 기록 갱신 및 가이드 재생
PlayerData:RefreshUIHUDMoney -- HUD의 돈 표시를 현재 보유 금액으로 새로고침
PlayerData:RefreshUIShop -- 로컬 플레이어인 경우에만 상점 UI 새로고침
PlayerData:SetUIEquipmentPurchaseChecking -- 장비 구매 완료 후 확인 팝업과 연출을 표시
PlayerData:PurchaseEquipmentBundle -- 선택된 장비들을 한번에 번들 구매 처리
PlayerData:PlayDirection_EquipmentBundlePurchase -- 장비 번들 구매 완료 연출을 재생
PlayerData:UseCharonsBoat -- 카론의 배 사용 - 펫 알을 소모해 모든 마을과 장비를 해금하는 치트 기능
PlayerIngameData:OnMapEnter -- 맵 입장시 맵 유형별 초기화와 UI 업데이트, 신전 층수 관리
PlayerIngameData:InitIngamePropertiesOnClient -- 인게임 시작 시 클라이언트 상태 초기화 및 UI 활성화
PlayerIngameData:InitIngamePropertiesOnServer -- 던전에 진입하면 로딩이 끝난 후 실행하는 함수
PlayerIngameData:CleanupIngameProperties -- 사망 후 부활하거나 게임을 처음 진입하면 마을에서 실행하는 함수
PlayerIngameData:OnUpdate -- 매 프레임마다 MP 회복, HP 감소, 깊이 측정, 동굴 시야 캘기 처리
PlayerIngameData:OnSyncProperty -- 동기화 속성 변경시 관련 UI와 상태 업데이트
PlayerIngameData:SetHPStausAtMine -- 광산에서의 체력 감소 처리 (관리자와 하데스 신전에서는 예외)
PlayerIngameData:SetHPandMPUI -- HP, MP UI와 보호막 아이콘을 현재 수치에 맞게 업데이트
PlayerIngameData:Die -- 플레이어 엔티티를 죽게 만듦
PlayerIngameData:SetActivationIngameUI -- 인게임 상태에 따라 시야 어둠운 효과와 기록 UI 활성화/비활성화
PlayerIngameData:SetResultUI -- 사망 또는 탈출 시 결과창 UI 설정 (기록, 아이템 정보 표시)
PlayerIngameData:SetRecordUI -- 인게임 중 상단에 표시되는 생존 시간과 깊이(또는 층수) 정보 업데이트
PlayerIngameData:SetBlindRatio -- 동굴 내 빛 세기에 따른 화면 어두운 정도 설정
PlayerIngameData:Hit -- 피해를 입을 때 보호막 사용 및 체력 감소 처리
PlayerIngameData:FinishAdventure -- 모험 종료 시 인게임 상태와 컴트롤 비활성화
PlayerIngameData:SetNearBonfire -- 모닥불 근처 여부 설정 (모닥불 근처에서는 체력 회복)
PlayerIngameData:UpdateDepthRecord -- 현재 위치를 이용해 침탐 깊이를 계산하고 기록 업데이트
PlayerIngameData:UnprotectedHit -- 보호막을 적용하지 않는 데미지일 경우 이 함수 사용 (중독 데미지 등)
PlayerIngameData:PopupMapEnteringUI -- 맵 입장시 맵 이름과 설명을 페이드 인/아웃 애니메이션과 함께 표시
PlayerIngameData:SetWarningUI -- 체력이 25% 이하일 때 경고 UI 표시/비표시
PlayerIngameData:UseMP -- 대쉬 등에서 MP 사용시 호출되는 함수
PlayerIngameData:GetProtector -- 보호막 개수를 1개 증가
PlayerIngameData:SetHPUseAmount -- 현재 광산/신전의 초당 HP 감소량 설정
PlayerIngameData:CleanupIngamePropertiesOnServer -- 서버에서 인게임 상태 정리 (현재 비어있음)
PlayerIngameData:SetChairBuffIdx -- 의자 군중버프 인덱스 설정
PlayerIngameData:InitTempleTable -- 신전 목록 초기화 및 최근 방문 신전을 제외한 랜덤 신전 선택
PlayerIngameData:GetTempleTable -- 남은 신전 목록에서 랜덤으로 선택하여 반환
PlayerIngameData:RecoverHP -- HP를 지정된 양만큼 회복 (최대치 초과 방지)
PlayerIngameData:AddCurrentTempleFloor -- 신전 에서 상위 층으로 나아갈 때 또는 층수 리셋 수행
PlayerIngameData:resetPlayerSpeed -- 하데스 신전 등에서 플레이어 이동 속도 원복
PlayerIngameData:HandleTriggerStayEvent -- 조명 오브젝트와 모닥불에 닿았을 때 빛 밝기/체력 회복 처리
PlayerInstallationObject:OnBeginPlay -- 컴포넌트 초기화 시 모든 탐험도구 개수를 0으로 설정
PlayerInstallationObject:RefreshNumUI -- PC와 모바일에서 탐험도구 UI 아이콘과 개수 표시 새로고침
PlayerInstallationObject:UseObject -- 지정된 탐험도구 개수를 1 감소시키고 UI 새로고침
PlayerInstallationObject:AddObject -- 1번 펫 보유중+스킬 사용중인 경우, 횃불 대신 마나 회복
PlayerInstallationObject:SpawnRope -- 배충 설치 - 플레이어 위치에서 아래 3만큼 떨어진 곳에 10초간 지속
PlayerInstallationObject:SpawnTrampoline -- 트램펄린 설치 - 플레이어 위치에서 위 1만큼 올라간 곳에 10초간 지속
PlayerInstallationObject:UseTorch -- 이미 스폰된 횃불이 있다면 제거하고, 예약된 타이머도 제거함
PlayerInstallationObject:UsePotion -- 체력 회복 물약 사용 - 최대 체력의 15% 회복
PlayerInstallationObject:DisacardAllItems -- 모든 탐험도구 버리기 (마을 이동 시 호출)
PlayerInstallationObject:SetTorchBrightnessInit -- 횟불 삭제 시 해당 조명 객체의 밝기값 초기화
PlayerInstallationObject:OnMapEnter -- 맵 입장 시 탐험도구 및 횟불 상태 초기화
PlayerInstallationObject:UseTorchPet -- 1번 펫의 횟불 스킬 온/오프 토글 (지속적으로 MP 소모)
PlayerInstallationObject:OnUpdate -- 펫 횟불 사용 중일 때 매 프레임마다 MP 소모 (레벨에 따라 감소)
PlayerInstallationObject:SpawnTorchByPetSkill -- 펫 스킬로 횟불 생성/제거 처리
PlayerInstallationObject:HandleKeyUpEvent -- 숫자 키 누려서 각종 탐험도구 사용 (1-4번 키)
PlayerStateAtStage:OnMapEnter -- 맵 입장 시 스테이지별 디버프 UI 설정 및 환경 초기화
PlayerStateAtStage:OnUpdate -- 매 프레임마다 플레이어의 상태이상과 환경적 디버프를 업데이트
PlayerStateAtStage:GetMaterial -- 개수 추가
PlayerStateAtStage:SellAllMaterial -- 보유 수량 체크
PlayerStateAtStage:LoseMaterial -- 보유 재료(고드름, 별 조각, 구름 조각, 황금 사과) 소모
PlayerStateAtStage:Poisoned -- 중독 상태로 만들고 지속시간 설정
PlayerStateAtStage:FreezePlayer -- 추위 스택 10개 달성 시 플레이어를 빙결시켜 2초간 이동 불가
PlayerStateAtStage:ElectricDamage -- 감전 피해를 입을 때 스택에 따라 피해량 증가 및 외모 변경
PlayerStateAtStage:StartExitedMode -- 6스테이지에서 별 조각 10개 획득시 '신난다!' 모드 활성으로 15초간 MP 소모 없이 대쉬 가능
PlayerStateAtStage:StartExitedModeOnServer -- 서버에서 '신난다!' 모드의 MP 소모량 0으로 설정 및 지속시간 후 원복
PlayerStateAtStage:RemoveThirstyStack -- 8스테이지 물웅덩이에서 물를 마셔 목마름 스택 제거
PlayerStateAtStage:GetBurnStack -- 5스테이지 화상 스택 추가 - 단계별로 피해량 증가, 수분 스택으로 상쇄
PlayerStateAtStage:GetWetStack -- 5스테이지에서 물에 닿았을 때 전체 화상 스택 제거 및 수분 보호막 추가
PlayerStateAtStage:GetCurseStack -- 9스테이지(유적)에서 30초마다 저주 스택 추가 - 체력 소모량 10%씩 증가
PlayerStateAtStage:InitAllState -- 모든 디버프와 상태이상을 초기화하고 관련 이펙트와 UI 제거
PlayerStateAtStage:GetThirstyStack -- 8스테이지에서 5초마다 목마름 스택 추가 - 이동속도 저하
PlayerStateAtStage:SetUI_HavingMaterialNum -- 스테이지별 재료 보유량을 UI에 업데이트
PlayerStateAtStage:OnBeginPlay -- 컴포넌트 초기화 시 기본 설정값들을 설정
PlayerStateAtStage:HitBySquid -- 5스테이지 오징어의 먹물에 맞았을 때 화면 효과와 통제 제약
PlayerStateAtStage:GetRotationShield -- 7스테이지 구름 조각 10개로 획득하는 회전 보호막 생성 (최대 6개)
PlayerStateAtStage:RemoveRotationShield -- 지정된 인덱스의 회전 보호막을 제거
PlayerStateAtStage:Enchanted -- 6스테이지 아프로디테 매혹 효과 - 좌우 조작키 반전
PlayerStateAtStage:GetSnownStack -- 데메테르 신전에서 빙결시 눈사람이 되어 좌우 버튼 연타로 탈출
PlayerStateAtStage:Diving -- 2스테이지 바다에 다이빙할 때 산소 게이지와 버블 생성
PlayerStateAtStage:OnMapLeave -- 맵 퇴장시 신전별 설정 초기화
PlayerStateAtStage:HandleKeyReleaseEvent -- 매혹 상태에서 키 떼 때 화살표 이팩트 제거
PlayerStateAtStage:HandleKeyDownEvent -- 매혹 상태나 눈사람 상태에서의 키 입력 처리
PlayerStateAtStage:HandleBodyActionStateChangeEvent -- 플레이어 액션 상태 변경에 따른 추가 처리
StatusListUI:RefreshUI -- 능력치 리스트 UI 새로고침 - 기본값, 보너스, 총합 능력치 표시
StatusListUI:HandleKeyDownEvent -- ESC 키 입력 시 능력치 리스트 UI 닫기
AccessoryLogic:GetAccessoryInfo -- string 형태로 저장된 장신구 정보를 받아 테이블 형태로 반환합니다.
AccessoryLogic:WrapAccessoryInfoToString -- 실제 연산에 사용되는 장신구 정보들을 받아 string 형태로 반환합니다.
AccessoryLogic:SetStatus -- 80% ~ 120% 범위 사이로 스탯값이 결정됩니다.
AccessoryMergeShopUI:RefreshMainPanel -- 메인 패널 새로고침 - 재료 슬롯, 결과 등급, 합성 버튼 상태 업데이트
AccessoryMergeShopUI:ShowMaterialListPanel -- 재료 선택 패널 표시 - 합성 가능한 아이템들의 리스트 생성
AccessoryMergeShopUI:RegistMaterial -- 재료를 대기중인 슬롯에 등록하고 메인 패널 업데이트
AccessoryMergeShopUI:InitAllSetting -- 모든 설정 초기화 - 재료 슬롯, 등급, 대기 인덱스 리셋
AccessoryMergeShopUI:PlayDirection_Merge -- 장신구 합성 연출 재생 - 이펙트, 사운드, 결과창 표시
AccessoryMergeShopUI:HandleButtonClickEvent -- 첫 번째 재료 슬롯 클릭 - 재료 선택 리스트를 열고 대기상태로 설정
AccessoryMergeShopUI:HandleButtonClickEvent2 -- 두 번째 재료 슬롯 클릭 - 재료 선택 리스트를 열고 대기상태로 설정
AccessoryMergeShopUI:HandleButtonClickEvent3 -- 합성 버튼 클릭 - 재료 준비 확인 후 장신구 합성 실행
AccessoryMergeShopUI:HandleButtonClickEvent4 -- 리셋 버튼 클릭 - 모든 설정 초기화 후 메인 패널 새로고침
AccessoryMergeShopUI:HandleKeyDownEvent -- ESC 키 입력 시 재료 선택 패널 또는 샵 닫기
AccessoryMergeShopUI_SelectMaterialSlotButton:HandleButtonClickEvent -- 재료 슬롯 버튼 클릭 시 해당 재료를 선택하여 합성 창에 등록
PlayerAccessory:OnBeginPlay -- 장신구 컴포넌트 초기화 - 테이블 리스트와 타입 설정
PlayerAccessory:SetTableClient -- 서버에서 클라이언트로 테이블 데이터 전체 동기화
PlayerAccessory:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 인덱스 값 동기화
PlayerAccessory:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 리셋
PlayerAccessory:ChangedTable -- 테이블 변경 시 장비 보관함 UI 새로고침
PlayerAccessory:LoadedData -- 데이터베이스에서 장신구 데이터 로드 후 완보 상태, 장착 인덱스, 숙련도 설정
PlayerAccessory:GetItems -- 장신구 획득 - 부위/등급/세트/능력치 순으로 정렬하여 삽입
PlayerAccessory:EquipItem -- 장신구 장착/해제 - 능력치 적용 및 클라이언트 동기화
PlayerAccessory:UpgradeProficiency -- 장신구 숙련도 업그레이드 - 희귀등급 이상 3개 사용
PlayerAccessory:PlayUpgradeProficiencyDirection -- 숙련도 업그레이드 연출 재생
PlayerAccessory:OpenAccessoryBox -- 장신구 상자 열기 - 무작위 부위/등급/세트 생성
PlayerAccessory:PlayDirection_AccessoryBoxOpen -- 장신구 상자 열기 연출 재생
PlayerAccessory:MergeItems -- 장신구 합성 - 2개 재료로 등급 1 높은 장신구 생성 (희귀미만)
PlayerAccessory:PlayMergeDirection -- 장신구 합성 연출 재생
ChairBuffNova:OnBeginPlay -- 의자 버프 노바 시작 - 이팩트 재생 및 0.5초 후 자동 삭제
ChairBuffNova:HandleTriggerEnterEvent -- 플레이어가 버프 노바에 닿으면 의자 버프 적용 (원 주인 제외)
ChairStorageUI:OnBeginPlay -- 의자 보관함 UI 초기화 - 의자 슬롯들을 복제하여 리스트 생성
ChairStorageUI:RefreshUI -- 전체 UI 새로고침 - 장착 의자, 보유 리스트, 능력치, 수집 개수 업데이트
ChairStorageUI:ShowDetailInfoPopup -- 의자 상세 정보 팝업 표시 - 이름, 설명, 능력치, 버프들을 표시
ChairStorageUI:HandleButtonClickEvent -- 닫기/취소 버튼 클릭 - 선택 인덱스 리셋 및 UI 새로고침
ChairStorageUI:HandleButtonClickEvent2 -- 장착 버튼 클릭 - 선택된 의자로 장착 대상 변경
ChairStorageUI:HandleButtonClickEvent3 -- 아마 상세 팝업 닫기 버튼 - 선택 인덱스 리셋 및 UI 새로고침
ChairStorageUI:HandleKeyDownEvent -- ESC 키 입력 시 의자 보관함 UI 닫기
ChairStorageUI_EquipButton:HandleButtonClickEvent -- 의자 장착 버튼 클릭 시 해당 의자로 장착 대상 변경
ChairStorageUI_SlotButton:HandleButtonClickEvent -- 의자 슬롯 버튼 클릭 시 해당 의자의 상세 정보 팝업 표시
PlayerChair:OnBeginPlay -- 의자 컴포넌트 초기화 및 기본 의자 엔티티 생성
PlayerChair:OnSyncProperty -- 장착 의자 인덱스 변경 시 엔티티 및 UI 업데이트
PlayerChair:SetSitEnable -- 의자에 앉기 가능/불가 설정 - 중력 비활성화, 스프라이트 표시
PlayerChair:AddItem -- 의자 획득 - 중복 획득 시 젠 보상, 로그 출력, 능력치 적용
PlayerChair:ChangeEquipedItem -- 장착 의자 변경 - 보유 여부 확인 후 장착 인덱스 업데이트
PlayerChair:ApplyEquipedChairEntity -- 장착한 의자를 실제 엔티티에 적용 - 스프라이트와 위치 설정
PlayerChair:SetSortingOrder -- 의자 부분별 렌더링 순서 설정 - 전면, 후면 레이어 구분
PlayerChair:OnUpdate -- 의자에 앉아있는 시간을 측정하여 30초마다 버프 발동
PlayerChair:GenerateChairBuff -- 의자 군중 버프 노바 생성 - 30초 앉은 후 버프 이팩트 및 노바 생성
PlayerChair:SetTableClient -- 서버에서 클라이언트로 테이블 데이터 전체 동기화
PlayerChair:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 인덱스 값 동기화
PlayerChair:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 리셋
PlayerChair:ChangedTable -- 테이블 변경 시 관련 UI 새로고침
PlayerChair:ClearAllProperty -- 모든 의자 데이터 입장/환생 시 초기화
PlayerChair:LoadedUserData -- 데이터베이스에서 의자 데이터 로드 후 클라이언트 동기화
PlayerChair:HandleChangedLookAtEvent -- 플레이어 바라보는 방향 변경 시 의자 위치와 방향 조정
PlayerChair:HandleOrderInLayerChangedEvent -- 렌더링 순서 변경 시 의자 렌더링 순서 업데이트 (현재 비활성화)
PlayerChair:HandleSortingLayerChangedEvent -- 렌더링 레이어 변경 시 의자 렌더링 레이어 업데이트 (현재 비활성화)
PlayerChair:HandleKeyDownEvent -- 음직임 키 누룬 때 의자에서 일어서기 및 중력 활성화
CollectionOpenButton:HandleButtonClickEvent -- 컴렉션 UI 열기 버튼 클릭 처리
CollectionSlotButton:HandleButtonClickEvent -- 컴렉션 슬롯 클릭 시 아이템 상세 정보 표시 처리
CollectionUI:OnBeginPlay -- 컴렉션 UI 초기 설정 (아이템 슬롯 생성)
CollectionUI:OnUpdate -- UI 갱신 요청 플래그 확인 및 처리
CollectionUI:RefreshUI -- UI 갱신 플래그 설정
CollectionUI:RefreshUI_Inner -- 컴렉션 UI 전체 갱신 (드롭 아이템 목록)
CollectionUI:RefreshDescUI -- 컴렉션 설명 패널 초기화
CollectionUI:SetDescUI -- 선택된 아이템의 상세 정보를 설명 패널에 표시
CollectionUI:HandleKeyDownEvent -- ESC 키 입력 시 컴렉션 UI 닫기 처리
PlayerCollection:OnBeginPlay -- 컴렉션 컴포넌트 초기화 및 드롭 아이템 초기 설정
PlayerCollection:RecordData -- 드롭 아이템 획득 데이터 기록 및 클라이언트 동기화
PlayerCollection:SetTableClient -- 서버에서 전송된 테이블 데이터를 클라이언트에 동기화
PlayerCollection:SetTableElementClient -- 서버에서 전송된 특정 테이블 요소를 클라이언트에 동기화
PlayerCollection:ClearTableClient -- 클라이언트의 테이블을 초기화하여 모든 값을 기본값으로 설정
PlayerCollection:ChangedTable -- 테이블 변경 시 관련 UI 갱신 처리
PlayerCollection:ClearAllProperty -- 모든 드롭 아이템 컴렉션 데이터 초기화
PlayerCollection:LoadedUserData -- 저장된 유저 데이터를 로드하여 컴렉션 상태 복원
ConstructionObject:OnBeginPlay -- 건설 오브젝트 초기화 및 표시 설정
ConstructionObject:RefreshEntityEnable -- 건설 레벨에 따른 오브젝트 활성화 상태 갱신
ConstructionObject:SetNametagLocalization -- 건설 오브젝트의 이름 태그 다국어 설정
ConstructionObject:HandleLocalPlayerConstructed -- 플레이어 건설 완료 이벤트 수신 시 오브젝트 상태 갱신
ConstructionShopUI:RefreshUI -- 건설 상점 UI 전체 갱신 (재화, 리스트, 상태 등)
ConstructionShopUI:SetBuyCheckPopup -- 건설/레벨업 확인 팝업 UI 설정
ConstructionShopUI:SetUnlockCheckPopup -- 건설 시설 잠금 해제 확인 팝업 UI 설정
ConstructionShopUI:PlayUnlockDirection -- 건설 시설 잠금 해제 성공 연출 및 토스트 메시지 표시
ConstructionShopUI:PlayPurchaseDireciton -- 건설/레벨업 성공 연출 및 토스트 메시지 표시
ConstructionShopUI:HandleButtonClickEvent3 -- 건설/레벨업 확인 버튼 클릭 시 실제 구매 처리
ConstructionShopUI:HandleButtonClickEvent5 -- 잠금 해제 확인 버튼 클릭 시 실제 해제 처리
ConstructionShopUI:HandleKeyDownEvent -- ESC 키 입력 시 상점 UI 닫기 처리
ConstructionShopUI_BuyButton:HandleButtonClickEvent -- 건설/레벨업 버튼 클릭 시 확인 팝업 표시 처리
ConstructionShopUI_UnlockButton:HandleButtonClickEvent -- 건설 시설 잠금 해제 버튼 클릭 시 확인 팝업 표시 처리
DailyRewardReceiveButton:HandleButtonClickEvent -- 데일리 보상 수령 버튼 클릭 처리
DailyRewardUI:RefreshUI -- 데일리 보상 UI 전체 갱신 (진척도, 버튼 상태 등)
DailyRewardUI:OnUpdate -- 다음 보상까지 남은 시간 실시간 계산 및 표시
DailyRewardUI:HandleButtonClickEvent -- 보상 설명 패널 토글 버튼 클릭 처리
DailyRewardUI:HandleKeyDownEvent -- ESC 키 입력 시 데일리 보상 UI 닫기 처리
PlayerDailyRewardComponent:OnBeginPlay -- 데일리 보상 컴포넌트 초기화 및 테이블 설정
PlayerDailyRewardComponent:ClearAllProperty -- 모든 데일리 보상 수령 상태를 초기화
PlayerDailyRewardComponent:SetTableClient -- 서버에서 전송된 테이블 데이터를 클라이언트에 동기화
PlayerDailyRewardComponent:SetTableElementClient -- 서버에서 전송된 특정 테이블 요소를 클라이언트에 동기화
PlayerDailyRewardComponent:ChangedTable -- 테이블 변경 시 관련 UI 갱신 처리
PlayerDailyRewardComponent:LoadedUserData -- 저장된 유저 데이터를 로드하여 데일리 보상 상태 복원
PlayerDailyRewardComponent:RefreshDailyRewardTime -- 현재 날짜 기준으로 데일리 보상 진척도 갱신
PlayerDailyRewardComponent:GiveReward -- 해당 날짜의 데일리 보상을 플레이어에게 지급
PlayerDailyRewardComponent:OnSyncProperty -- 동기화된 속성 변경 시 UI 갱신 처리
PlayerDailyRewardComponent:DateToNumber -- 연월일을 숫자로 변환하여 날짜 계산에 사용
PlayerDailyRewardComponent:RefreshDailyRewardTimeOnCheat -- 치트 기능으로 날짜를 조작하여 데일리 보상 진척도 갱신
EmblemStorageUI:RefreshUI -- 엠블럼 보관소 UI 전체 갱신 (리스트, RP, 랜킹, 칭호)
EmblemStorageUI:HandleButtonClickEvent -- 엠블럼 보관소 새로고침 버튼 클릭 처리
EmblemStorageUI:HandleKeyDownEvent -- ESC 키 입력 시 엠블럼 보관소 UI 닫기 처리
PlayerEmblem:OnBeginPlay -- 엠블럼 컴포넌트 초기화 및 랜킹 제목 엔티티 생성
PlayerEmblem:SetTableClient -- 서버에서 전송된 테이블 데이터를 클라이언트에 동기화
PlayerEmblem:SetTableElementClient -- 서버에서 전송된 특정 테이블 요소를 클라이언트에 동기화
PlayerEmblem:ClearTableClient -- 클라이언트의 테이블을 초기화하여 모든 값을 기본값으로 설정
PlayerEmblem:ChangedTable -- 테이블 변경 시 관련 UI 갱신 처리
PlayerEmblem:LoadedData -- 저장된 유저 데이터를 로드하여 엠블럼 상태 복원
PlayerEmblem:AddItems -- 지정된 엠블럼을 인벤토리에 추가하고 RP 계산
PlayerEmblem:CalculateRP -- 보유한 엠블럼들의 레벨 합을 계산하여 RP 산출
PlayerEmblem:GetRank -- 리더보드를 조회하여 자신의 랜킹 위치 결정
PlayerEmblem:SetRankTitleEntity -- 랜킹에 따른 칭호 엔티티 설정 및 표시
PlayerEmblem:PurchaseWithLegacyCoins -- 레거시 코인을 사용하여 랜덤 엠블럼 구매
PlayerEmblem:PlayExchangeDirection -- 레거시 코인 교환 결과 UI 연출 재생
PlayerEmblem:OnSyncProperty -- 동기화된 속성 변경 시 UI 갱신 처리
EmoticonPlayButton:HandleButtonClickEvent -- 장착된 이모티콘 재생 버튼 클릭 처리
EmoticonShopUI:OnUpdate -- UI 갱신 요청 플래그 확인 및 처리
EmoticonShopUI:RefreshUI -- UI 갱신 플래그 설정
EmoticonShopUI:RefreshUI_Inner -- 이모티콘 상점 UI 전체 갱신 (토큰, 버튼 상태)
EmoticonShopUI:SetGachaResultUI -- 가차 결과 UI 설정 및 표시
EmoticonShopUI:OnBeginPlay -- 이모티콘 상점 UI 초기화
EmoticonShopUI:HandleButtonClickEvent -- 이모티콘 구매 버튼 클릭 처리 (조건 검증 및 새 이모티콘 획득)
EmoticonShopUI:HandleKeyDownEvent -- ESC 키 입력 시 상점 UI 닫기 처리
EmoticonStorageChangeEquipedSlotButton:HandleButtonClickEvent -- 이모티콘 장착 슬롯 교체 버튼 클릭 처리
EmoticonStorageSlotButton:HandleButtonClickEvent -- 이모티콘 보관 슬롯 선택 버튼 클릭 처리
EmoticonStorageUI:OnBeginPlay -- 이모티콘 보관소 UI 초기 설정 (보관/장착 슬롯 생성)
EmoticonStorageUI:OnUpdate -- UI 갱신 요청 플래그 확인 및 처리
EmoticonStorageUI:RefreshUI -- UI 갱신 플래그 설정
EmoticonStorageUI:RefreshUI_Inner -- 이모티콘 보관소 UI 전체 갱신 (보관/장착 리스트)
EmoticonStorageUI:SelectStorageSlot -- 보관소에서 선택된 이모티콘 슬롯 처리
EmoticonStorageUI:ChangeEquipedSlot -- 선택된 이모티콘을 지정 장착 슬롯에 교체
EmoticonStorageUI:HandleKeyDownEvent -- ESC 키 입력 시 보관소 UI 닫기 처리
PlayerEmoticon:OnBeginPlay -- 이모티콘 컴포넌트 초기화 및 서버/클라이언트별 설정
PlayerEmoticon:PlayEmoticon -- 장착된 이모티콘을 화면에 표시하며 페이드인/아웃 애니메이션 재생
PlayerEmoticon:SetEmoticonUI -- 장착된 이모티콘 정보를 UI에 반영하여 화면 갱신
PlayerEmoticon:ChangeEquipedSlot -- 지정된 슬롯에 보유한 이모티콘을 장착 처리
PlayerEmoticon:GetNewEmot -- 이모토큰을 사용하여 새로운 이모티콘 획득
PlayerEmoticon:UseEmotToken -- 이모토큰 소모 처리
PlayerEmoticon:SetTableClient -- 서버에서 전송된 테이블 데이터를 클라이언트에 동기화
PlayerEmoticon:SetTableElementClient -- 서버에서 전송된 특정 테이블 요소를 클라이언트에 동기화
PlayerEmoticon:ClearTableClient -- 클라이언트의 테이블을 초기화하여 모든 값을 기본값으로 설정
PlayerEmoticon:ChangedTable -- 테이블 변경 시 관련 UI 갱신 처리
PlayerEmoticon:ClearAllProperty -- 모든 이모티콘 관련 속성을 초기화
PlayerEmoticon:LoadedUserData -- 저장된 유저 데이터를 로드하여 이모티콘 상태 복원
PlayerEmoticon:OnSyncProperty -- 동기화된 속성 변경 시 UI 갱신 처리
PlayerEmoticon:SetUIGachaResult -- 새로 획득한 이모티콘의 가챠 결과 UI 표시
EquipmentStorageUI:OnBeginPlay -- 장비 보관함 UI 초기화
EquipmentStorageUI:RefreshUI -- 장비 보관함 UI를 현재 상태에 맞게 새로고침
EquipmentStorageUI:Refresh_Normal -- 일반 장비 탭의 UI를 새로고침
EquipmentStorageUI:Refresh_Mythic -- 신화 장비 탭의 UI를 새로고침
EquipmentStorageUI:Refresh_Accessory -- 장신구 탭의 UI를 새로고침
EquipmentStorageUI:ShowNormalEquipmentDetailInfo -- 일반 장비의 상세 정보 팝업을 표시
EquipmentStorageUI:ShowBeadsDetailInfo -- 신화 장비의 구슬 상세 정보 팝업을 표시
EquipmentStorageUI:ApplyAvatarInfo -- 현재 장착한 장비에 따라 아바타 외형을 적용
EquipmentStorageUI:SetFilterIdx -- 장비 보관함의 필터 인덱스를 설정하여 탭을 변경
EquipmentStorageUI:SetSecondFilterIdx -- 장비 보관함의 2차 필터 인덱스를 설정하여 세부 카테고리를 변경
EquipmentStorageUI:ShowAccessoryDetailInfo -- 장신구의 상세 정보 팝업을 표시
EquipmentStorageUI:RefreshAccessoryGradeupPanel -- 장신구 숙련도 업그레이드 패널을 새로고침
EquipmentStorageUI:SelectAccessoryGradeupMaterial -- 장신구 숙련도 업그레이드에 사용할 재료를 선택
EquipmentStorageUI:PlayAccessoryGradeupDirection -- 장신구 숙련도 업그레이드 연출을 재생
EquipmentStorageUI:HandleButtonClickEvent -- 일반 장비 필터 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent2 -- 신화 장비 필터 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent5 -- 장신구 필터 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent6 -- 구슬 상세 정보 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent7 -- 일반 장비 필터 버튼 클릭 이벤트 처리 (중복)
EquipmentStorageUI:HandleButtonClickEvent8 -- 장비 장착 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent9 -- 장비 해제 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent3 -- 장신구 장착 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent4 -- 장신구 해제 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent10 -- 장신구 숙련도 업그레이드 재료 초기화 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent11 -- 장신구 숙련도 업그레이드 재료 슬롯 1 선택 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent12 -- 장신구 숙련도 업그레이드 재료 슬롯 2 선택 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent13 -- 장신구 숙련도 업그레이드 재료 슬롯 3 선택 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent14 -- 장신구 숙련도 업그레이드 실행 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent15 -- 장신구 숙련도 업그레이드 확인 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleButtonClickEvent16 -- 장신구 숙련도 업그레이드 취소 버튼 클릭 이벤트 처리
EquipmentStorageUI:HandleKeyDownEvent -- ESC키 입력 시 장비 보관함 UI를 닫는 이벤트 처리
EquipmentStorageUI_AccessoryProficiencyUp_SlotSelectButton:HandleButtonClickEvent -- 장신구 숙련도 업그레이드용 재료 선택 버튼 클릭 이벤트 처리
EquipmentStorageUI_AccessorySlotButton:HandleButtonClickEvent -- 장신구 슬롯 버튼 클릭 시 상세 정보 표시 이벤트 처리
EquipmentStorageUI_MythicItemMouseHover:SetHoverUI -- 신화 장비 아이템에 마우스 호버 시 툴팁 UI 표시 설정
EquipmentStorageUI_MythicItemMouseHover:HandleButtonStateChangeEvent -- 신화 장비 아이템 버튼 상태 변경 시 호버 UI 표시 처리
EquipmentStorageUI_SecondFilterButton:HandleButtonClickEvent -- 장비 보관함 2차 필터 버튼 클릭 이벤트 처리
PlayerMythicEquipment:OnBeginPlay -- 컴포넌트 초기화 시 테이블 리스트와 타입 정보를 설정하여 클라이언트 동기화 준비
PlayerMythicEquipment:SetTableClient -- 서버에서 전달받은 테이블 데이터를 클라이언트 측에서 동기화하고 UI 갱신
PlayerMythicEquipment:SetTableElementClient -- 테이블의 특정 인덱스 요소를 클라이언트에서 업데이트하고 타입에 맞게 파싱
PlayerMythicEquipment:ClearTableClient -- 클라이언트 측에서 테이블 전체를 초기값으로 클리어하고 UI 갱신
PlayerMythicEquipment:ChangedTable -- 테이블 데이터가 변경되었을 때 해당하는 UI 컴포넌트를 새로고침
PlayerMythicEquipment:LoadedData -- 저장된 유저 데이터를 로드하여 신화 장비 레벨과 원소 정보를 복원하고 클라이언트에 동기화
PlayerMythicEquipment:PurchaseMythicEquipment -- 지정된 신화 장비의 레벨을 업그레이드하고 비용 차감, 원소 획득 및 연출 재생
PlayerMythicEquipment:PlayPurchaseDirection -- 장비 구매 완료 후 클라이언트에서 업그레이드 연출을 재생
PlayerMythicEquipment:RedistributionPowerOfGod -- 선택된 신석을 랜덤하게 재분배하여 장비의 원소 구성을 변경하는 기능 수행
PlayerMythicEquipment:PlayRedistributionDirection -- 신석 재분배 연출을 클라이언트에서 재생하고 UI 버튼을 일시적으로 비활성화
PlayerMythicEquipment:RedistributionDirection_Inner -- 개별 신석의 재분배 애니메이션을 처리하는 내부 함수
PlayerMythicEquipment:UnlockUpgradeLimit -- 황금열쇠를 사용하여 신화 장비의 업그레이드 레벨 제한을 해제
PlayerMythicEquipment:PlayUnlockDirection -- 레벨 제한 해제 완료 후 클라이언트에서 해제 연출을 재생
PlayerMythicEquipment:ResetPropertiesByReborn -- 환생 시 모든 신화 장비의 레벨과 원소 정보를 초기화하고 클라이언트에 동기화
InfiniteQuestUI:OnBeginPlay -- 무한 퀘스트 UI 초기화 및 기본 설정
InfiniteQuestUI:FoldUI -- 무한 퀘스트 UI의 접기/펼치기 토글 처리
InfiniteQuestUI:HandleKeyDownEvent -- Tab키 입력으로 퀘스트 보상 수령 및 UI 접기 처리
InfiniteQuestUI:HandleButtonClickEvent2 -- 새 퀘스트 시작 버튼 클릭 이벤트 처리
PlayerInfiniteQuest:GetNewQuest -- 플레이어 레벨에 맞는 새로운 무한 퀘스트를 생성하고 설정
PlayerInfiniteQuest:GetReward -- 퀘스트 완료 시 보상을 지급하고 새 퀘스트를 시작
PlayerInfiniteQuest:GetScore -- 퀘스트 진행도 점수를 추가
PlayerInfiniteQuest:UpdateQuestUI -- 퀘스트 진행 상황에 따라 UI를 업데이트
PlayerInfiniteQuest:NewQuestAlert -- 새 퀘스트 시작 시 알림 연출 재생
PlayerInfiniteQuest:OnSyncProperty -- 퀘스트 관련 속성 동기화 시 UI 업데이트 처리
PlayerInfiniteQuest:PlayRewardDirection -- 퀘스트 보상 획득 시 연출 재생
PlayerInfiniteQuest:OnMapEnter -- 맵 진입 시 퀘스트 UI 위치 조정
EquipmentStorageUI_NormalSlotButton:HandleButtonClickEvent -- 일반 장비 슬롯 버튼 클릭 시 상세 정보 표시 이벤트 처리
InventoryEquipedSlotButton:HandleButtonClickEvent -- 인벤토리 장착 슬롯 버튼 클릭 시 상세 정보 표시 이벤트 처리
InventorySlotButton:HandleButtonClickEvent -- 인벤토리 슬롯 버튼 클릭 시 상세 정보 표시 이벤트 처리
InventoryUI:OnBeginPlay -- 인벤토리 UI 초기화 및 슬롯 생성
InventoryUI:OnUpdate -- 매 프레임 UI 새로고침 체크
InventoryUI:RefreshUI -- 인벤토리 UI 새로고침 요청
InventoryUI:RefreshUI_Inner -- 인벤토리 UI 실제 새로고침 처리
InventoryUI:SetFilterIdx -- 인벤토리 필터 인덱스를 설정하여 탭을 변경
InventoryUI:SetDetailInfoUI -- 선택한 슬롯의 상세 정보를 표시하는 UI를 설정
InventoryUI:RefreshStatusInfoUI -- 플레이어의 상태 정보를 UI에 표시
InventoryUI:SetFilterButtonEnable -- 현재 맵에 따라 필터 버튼의 활성화 상태를 설정
InventoryUI:SetDetailInfoUI_RelicBox -- 유물 상자의 상세 정보를 표시하는 UI를 설정
InventoryUI:HandleKeyDownEvent -- 키보드 입력 이벤트 처리 (I키로 인벤토리 열기/닫기, ESC키로 팝업 닫기)
InventoryUI:HandleButtonClickEvent2 -- 광물 필터 버튼 클릭 이벤트 처리
InventoryUI:HandleButtonClickEvent3 -- 장비 필터 버튼 클릭 이벤트 처리
InventoryUI:HandleButtonClickEvent4 -- 의자 필터 버튼 클릭 이벤트 처리
InventoryUI:HandleButtonClickEvent5 -- 펫 필터 버튼 클릭 이벤트 처리
PlayerBackpack:AddItem -- 플레이어에게 아이템을 추가하되 배낭 용량과 행운 스탯을 고려하여 처리
PlayerBackpack:DiscardAllItem -- 배낭의 모든 아이템을 버리고 저장소를 비우는 기능
PlayerBackpack:OnSyncProperty -- 배낭 관련 속성이 동기화될 때 해당 UI 컴포넌트들을 새로고침
PlayerBackpack:OnBeginPlay -- 배낭 컴포넌트 초기화 시 테이블 설정과 모든 아이템 클리어 수행
PlayerBackpack:SetTableClient -- 서버에서 받은 테이블 데이터를 클라이언트에 설정하고 관련 테이블 변경사항 적용
PlayerBackpack:SetTableElementClient -- 테이블의 특정 인덱스 요소를 클라이언트에서 업데이트하고 타입 파싱 후 변경사항 적용
PlayerBackpack:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 클리어하고 변경사항을 적용
PlayerBackpack:ChangedTable -- 배낭 테이블 데이터가 변경되었을 때 관련 UI 컴포넌트들을 새로고침
PlayerBackpack:ClearAllProperty -- 서버에서 모든 아이템 저장 정보를 초기화하고 클라이언트에 동기화
PlayerBackpack:PlayAttackMotion -- 플레이어의 공격 모션을 재생하고 성공/실패에 따라 다른 이펙트와 사운드 출력
PlayerBackpack:OnMapEnter -- 플레이어가 광산 맵에 입장할 때 해당 맵의 채굴 타겟들의 방문 기록을 초기화
PlayerStorage:OnBeginPlay -- 플레이어 저장소 컴포넌트 초기화 시 테이블 설정과 소모품 지속시간 데이터 준비
PlayerStorage:SetTableClient -- 서버에서 받은 테이블 데이터를 클라이언트에 동기화하고 관련 UI 갱신
PlayerStorage:SetTableElementClient -- 테이블의 특정 인덱스 요소를 클라이언트에서 업데이트하고 타입 파싱 후 UI 갱신
PlayerStorage:ClearTableClient -- 클라이언트 측에서 테이블 전체를 초기값으로 클리어하고 관련 UI 갱신
PlayerStorage:ChangedTable -- 테이블 데이터 변경 시 해당하는 모든 관련 UI 컴포넌트들을 새로고침
PlayerStorage:LoadedUserData -- 저장된 유저 데이터를 로드하여 소모품, 재화, 시작시간 정보를 복원하고 클라이언트에 동기화
PlayerStorage:AddCurrencyItems -- 플레이어에게 지정된 재화 아이템을 추가하고 특별 효과 재생 여부 결정
PlayerStorage:PlayGainGemsDirection -- 젬 획득 시 클라이언트에서 시각적 연출 효과를 재생하여 획득량 표시
PlayerStorage:AddConsumableItems -- 플레이어에게 소모품 아이템을 추가하고 로그 메시지 출력
PlayerStorage:UseCurrencyItems -- 플레이어의 재화 아이템을 소모하고 데이터를 저장 및 클라이언트 동기화
PlayerStorage:UseConsumableItem -- 소모품 아이템 사용 처리: 계약서, 뿌리기, 장신구상자 등의 타입별 로직 실행
PlayerStorage:GetConvertedTimeFromUTC -- UTC 시간을 초 단위의 누적 시간으로 변환하여 소모품 지속시간 계산에 사용
PlayerStorage:OnUpdate -- 매 프레임마다 소모품의 지속시간을 체크하고 1초마다 상태 갱신
PlayerStorage:RefreshConsumableItemAbility -- 소모품의 지속시간을 체크하여 버프 상태를 관리하고 UI에 버프 아이콘 표시
PlayerStorage:ApplySprinkleItem -- 뿌리기 아이템 사용 시 모든 클라이언트에 효과를 적용하고 시작시간 기록
StorageUI:OnBeginPlay -- 클라이언트에서 컴포넌트 초기화 수행
StorageUI:RefreshUI -- 저장소 UI 전체를 새로고침하여 필터, 재화, 아이템 정보 갱신
StorageUI:Refresh_ConsumableItems -- 소모품 아이템 목록을 새로고침하고 보유량에 따라 UI 업데이트
StorageUI:Refresh_Minerals -- 광물 아이템 목록을 새로고침하고 보유량에 따라 UI 업데이트
StorageUI:Refresh_Relics -- 유물 아이템 목록을 새로고침하여 정화된/정화되지 않은 유물 표시
StorageUI:ShowDetailPopup -- 선택된 아이템의 상세 정보 팝업을 열고 필터에 따라 적절한 정보 표시
StorageUI:UseConsumableItem -- 선택된 소모품 아이템을 사용하거나 유물상자를 열어 결과 처리
StorageUI:PlayAccessoryBoxOpenDirection -- 장신구 상자 개봉 연출을 실행하여 슬롯머신 효과와 결과 표시
StorageUI:HandleButtonClickEvent -- 첫 번째 필터 버튼 클릭 시 소모품 필터로 전환
StorageUI:HandleButtonClickEvent2 -- 두 번째 필터 버튼 클릭 시 광물 필터로 전환
StorageUI:HandleButtonClickEvent3 -- 세 번째 필터 버튼 클릭 시 유물 필터로 전환
StorageUI:HandleButtonClickEvent4 -- 저장소 UI를 새로 열 때 매번 소모품 필터로 초기화하고 새로고침
StorageUI:HandleButtonClickEvent5 -- 소모품 사용 버튼 클릭 시 선택된 소모품 사용 처리
StorageUI:HandleKeyDownEvent -- 키보드 입력 처리: I키로 인벤토리 열기/닫기, ESC키로 닫기
StorageUI:HandleButtonClickEvent6 -- 인벤토리 단축버튼 클릭 시 UI 열기/닫기 토글 처리
StorageUI_SlotButton:HandleButtonClickEvent -- 창고 슬롯 버튼 클릭 시 상세 정보 팝업 표시 이벤트 처리
PetComponent:OnBeginPlay -- 펫 컴포넌트 초기화 시 애니메이션과 상태 시스템 설정
PetComponent:ChangeState -- 펫의 상태를 변경하여 절절한 애니메이션 재생
PetComponent:ChangePos -- 플레이어의 시선 방향에 따라 펫의 위치를 이동시키고 애니메이션 재생
PetComponent:ChangeClimb -- 플레이어의 범비나 사다리 타기 상태에 따라 펫의 위치와 이팩트 처리
PetShopUI:OnBeginPlay -- 펫 상점 UI 초기화 및 로커라이제이션 설정
PetShopUI:OnUpdate -- UI 새로고침 플래그 상태 확인 및 지연 업데이트 처리
PetShopUI:RefreshUI -- UI 새로고침 플래그 활성화
PetShopUI:RefreshUI_Inner -- 플레이어의 펫 알 보유량을 표시하고 전체 펫 보유 여부에 따른 UI 상태 업데이트
PetShopUI:SetWarningPopup -- 경고 메시지를 표시하는 팝업 활성화
PetShopUI:ButtonEnable -- 펫 알 오픈 버튼의 활성화 상태 설정
PetShopUI:SetUIGettingNewPet -- 새로운 펫 획듵 결과 UI에 펫 이미지, 등급, 설명 표시 및 사운드 재생
PetShopUI:HandleButtonClickEvent2 -- 펫 알 오픈 버튼 클릭 시 조건 검사 후 새 펫 획듵 요청
PetShopUI:HandleKeyDownEvent -- ESC 키를 눌러 펫 상점 UI와 모든 팝업을 닫는 이벤트 처리
PetStorageUI:OnBeginPlay -- 펫 보관함 UI 초기화 시 슬롯 복제 및 기본 데이터 설정
PetStorageUI:OnUpdate -- UI 새로고침 플래그 상태 확인 및 지연 업데이트 처리
PetStorageUI:RefreshUI -- UI 새로고침 플래그 활성화
PetStorageUI:RefreshUI_Inner -- 펫 보관함의 전체 UI 요소들을 수집하고 레벨, 능력, 장착 상태에 따라 갱신
PetStorageUI:ChangeEquipedPet -- 지정된 인덱스의 펫을 장착하고 UI의 장착 버튼 상태 업데이트
PetStorageUI:ShowDetailInfo -- 지정된 펫의 상세 정보 팝업을 표시하고 레벨, 능력, 스킬 정보 업데이트
PetStorageUI:HandleButtonClickEvent -- 펫 상세 정보 팝업 닫기 버튼 클릭 이벤트 처리
PetStorageUI:HandleKeyDownEvent -- ESC 키를 눌러 팝업이나 전체 펫 보관함을 닫는 이벤트 처리
PetStorageUI_EquipButton:HandleButtonClickEvent -- 펫 장착 버튼 클릭 시 해당 슬롯 인덱스의 펫을 장착하도록 요청
PetStorageUI_SlotInfoPopup:HandleButtonClickEvent -- 펫 정보 팝업 버튼 클릭 시 해당 슬롯의 상세 정보를 표시하도록 요청
PetStorageUI_UseSkillButton:PlayUseSkillButtonAnim -- 펫 스킬 사용 버튼의 ON/OFF 상태에 따른 애니메이션과 시각적 업데이트
PetStorageUI_UseSkillButton:OnBeginPlay -- 스킬 버튼 초기화 시 원형 이미지 엔티티 참조 설정
PetStorageUI_UseSkillButton:HandleButtonClickEvent -- 펫 스킬 사용 버튼 클릭 시 스킬 사용 상태 토글 요청
PlayerPet:OnBeginPlay -- 플레이어 펫 시스템 초기화 및 펫 엔티티 생성
PlayerPet:OnSyncProperty -- 장착 펫 인덱스 동기화 시 펫 엔티티 설정 및 UI 업데이트
PlayerPet:ChangePetEntityParameter -- 장착된 펫의 인덱스에 따라 펫 엔티티의 외관과 애니메이션 설정
PlayerPet:EnablePetEntity -- 펫 엔티티의 활성화 상태를 설정하여 보이기/숨기기 제어
PlayerPet:ChangeEquipedPet -- 지정된 인덱스의 펫을 장착하고 능력치 적용
PlayerPet:GetNewPet -- 펫 알을 소모하여 랜덤한 새 펫을 획득하고 결과 UI 표시
PlayerPet:SetTableClient -- 서버에서 클라이언트로 테이블 전체 데이터 동기화
PlayerPet:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 요소만 동기화
PlayerPet:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 초기화
PlayerPet:ChangedTable -- 테이블 변경 시 관련 UI들을 업데이트하고 능력치 적용
PlayerPet:ClearAllProperty -- 모든 펫 관련 속성을 초기값으로 리셋
PlayerPet:LoadedUserData -- 사용자 데이터에서 펫 관련 정보를 로드하여 속성에 적용
PlayerPet:SetGettingNewPetResultUI -- 펫 획득 결과 타입에 따라 적절한 UI 팝업 표시
PlayerPet:ChangePetSkillUseState -- 지정된 펫의 스킬 사용 상태를 변경하고 클라이언트에 동기화
PlayerPet:HandleChangedLookAtEvent -- 플레이어 보는 방향 변경 시 펫의 위치 조정
PlayerPet:HandleStateChangeEvent -- 플레이어 상태 변경 시 펫의 대응 상태 및 애니메이션 조정
PlayerRelic:OnBeginPlay -- 플레이어 유물 시스템 초기화 및 테이블 설정
PlayerRelic:AddRelic -- 플레이어에게 유물을 추가하고 보너스 확률 적용
PlayerRelic:Purifying -- 더러운 유물을 정화하여 사용 가능한 유물로 변환
PlayerRelic:RegisterToBook -- 유물을 유물북에 등록하고 필요한 재료를 소모
PlayerRelic:ClearDirtyItems -- 사망했을 경우 실행하는 함수입니다.
PlayerRelic:SetTableClient -- 서버에서 클라이언트로 테이블 전체 데이터 동기화
PlayerRelic:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 요소만 동기화
PlayerRelic:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 초기화
PlayerRelic:ChangedTable -- 테이블 변경 시 관련 UI들을 새로고침하여 화면 업데이트
PlayerRelic:ClearAllProperty -- 모든 유물 관련 속성을 초기값으로 리셋
PlayerRelic:LoadedUserData -- 유물 보유 정보 갱신
PlayerRelic:SyncDirtyItem -- 더러운 유물 데이터를 클라이언트와 동기화
PlayerRelic:OnMapEnter -- 맵 진입 시 마을 지역에서 유물 자동 정화 수행
PlayerRelic:BuyRelicBox -- 유물상자를 구매하여 인벤토리에 추가
PlayerRelic:OnSyncProperty -- 속성 동기화 시 유물상자 공장 UI 업데이트
PlayerRelic:OpenRelicBox -- 조건 검증
PlayerRelic:SetUI_RelicBoxOpenResult -- 유물상자 오픈 결과를 UI에 표시하고 팝업 설정
PlayerRelic:GetRelicBox -- 지정된 인덱스의 유물상자를 인벤토리에 직접 추가
PlayerRelic:Merge -- 보유량 검증
PlayerRelic:SetMergeResultPopup -- 유물 합성 결과를 팝업 UI에 표시하고 등급에 따른 스타일 설정
PlayerRelic:RecycleToLegacyCoin -- 보유 중인 모든 유물을 등급별 점수로 환계하여 레거시 코인으로 전환
PlayerRelic:SetRecycleResultUI -- 유물 재활용 결과를 UI에 표시하고 팝업 활성화
PlayerRelic:IsPossibleRegistToBook -- 지정된 유물이 유물북에 등록 가능한지 여부를 검사
PlayerRelic:AutoMerge -- grade : 소모하는 재료의 등급. 일반(1), 고급(2), 희귀(3), 전설(4) 로 넘겨받음
PlayerRelic:SetAutoMergeResultUI -- 자동 합성 결과를 유물 합성 상점 UI에 전달하여 결과 팝업 표시
RelicBookUI:OnBeginPlay -- 유물북 UI 초기 설정 및 로커라이제이션 텍스트 적용
RelicBookUI:OnUpdate -- UI 새로고침 플래그 처리 및 지연 업데이트 처리
RelicBookUI:RefreshUI -- UI 새로고침 플래그 설정
RelicBookUI:RefreshStatusUI -- 상태 UI 새로고침 플래그 설정
RelicBookUI:RefreshUI_Inner -- 유물북 전체 UI를 새로고침하고 등록 정보에 따른 시각적 상태 업데이트
RelicBookUI:ShowRegistrationPopup -- slotIdx : 현재 페이지에서의 표시 순서 인덱스
RelicBookUI:SetFilterIdx -- 유물 등급 필터 인덱스 설정 및 페이지 초기화
RelicBookUI:RefreshStatusUI_Inner -- 유물 등록 상태에 따른 총 능력치 계산 및 달성률 표시
RelicBookUI:SetPageNavInfo -- 현재 필터와 등록 가능 여부에 따른 페이지 네비게이션 정보 설정
RelicBookUI:RefreshUI_Inner_FilteredByRegistable -- 등록 가능한 유물 만 필터링하여 UI에 표시
RelicBookUI:HandleButtonClickEvent -- 유물북 페이지 이동 버튼 클릭 이벤트 처리
RelicBookUI:HandleKeyDownEvent -- ESC 키를 눌러 유물북 팝업을 닫는 이벤트 처리
RelicBookUI:HandleButtonClickEvent2 -- 유물 등급 필터 1(일반) 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent3 -- 유물 등급 필터 2(고급) 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent4 -- 유물 등급 필터 3(희귀) 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent5 -- 유물 등급 필터 4(전설) 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent6 -- 유물북 다음 페이지 이동 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent7 -- 유물북 이전 페이지 이동 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent8 -- 등록 가능한 유물만 보기 필터 토글 버튼 클릭 이벤트 처리
RelicBookUI:HandleButtonClickEvent9 -- 유물북 초기화 버튼 클릭 이벤트 처리 (필터 해제하고 1등급으로 리셋)
RelicShowRegistPopupButton:HandleButtonClickEvent -- 유물 등록 팝업 버튼 클릭 시 해당 슬롯과 재료 인덱스를 전달하여 등록 팝업 표시
PlayerTitle:OnBeginPlay -- 플레이어 칭호 시스템 초기화 및 칭호 엔티티 생성
PlayerTitle:OnSyncProperty -- 장착된 칭호 인덱스 동기화 시 칭호 엔티티 설정 및 UI 업데이트
PlayerTitle:ChangeEquipedItem -- 지정된 인덱스의 칭호를 장착하고 보유 여부 확인
PlayerTitle:GetNewItem -- 새로운 칭호를 획듵하고 이미 보유 중인지 확인 후 추가
PlayerTitle:SpawnTitleEntity -- 칭호 표시용 엔티티를 생성하고 정렬 및 이어 설정
PlayerTitle:SetTitleEntity -- 장착된 칭호에 따라 칭호 엔티티의 외관과 색상 설정
PlayerTitle:SetTitleEntityOnClient -- 클라이언트에서 칭호 엔티티의 로커라이욨된 텍스트와 RUID 설정
PlayerTitle:OnMapEnter -- 맵 진입 시 클라이언트에서의 칭호 엔티티 설정 (현재 비활성화됨)
PlayerTitle:SetTableClient -- 서버에서 클라이언트로 테이블 전체 데이터 동기화
PlayerTitle:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 요소만 동기화
PlayerTitle:ClearTableClient -- 클라이언트에서 테이블을 초기값으로 모두 초기화
PlayerTitle:ChangedTable -- 테이블 변경 시 관련 UI들을 업데이트하고 능력치 적용
PlayerTitle:ClearAllProperty -- 모든 칭호 관련 속성을 초기값으로 리셋
PlayerTitle:LoadedUserData -- 사용자 데이터에서 칭호 관련 정보를 로드하여 속성에 적용
TitleEquipButton:HandleButtonClickEvent -- 칭호 장착 버튼 클릭 시 해당 인덱스의 칭호를 장착하도록 요청
TitleStorageUI:OnBeginPlay -- 칭호 보관함 UI 초기화 시 로커라이제이션 및 슬롯 복제 설정
TitleStorageUI:InitUI -- 칭호 보관함의 칭호 목록과 능력치 리스트를 초기화하고 기본 데이터 설정
TitleStorageUI:OnUpdate -- UI 새로고침 플래그 상태 확인 및 지연 업데이트 처리
TitleStorageUI:RefreshUI -- UI 새로고침 플래그 활성화
TitleStorageUI:RefreshUI_Inner -- 칭호 보유와 장착 상태에 따른 UI 업데이트 및 누적 능력치 계산 및 표시
TitleStorageUI:ChangeEquipedTitle -- 지정된 인덱스의 칭호를 장착하고 능력치 적용
TitleStorageUI:HandleKeyDownEvent -- ESC 키를 눌러 칭호 보관함 UI를 닫는 이벤트 처리
PlayerVoidItem:OnBeginPlay -- 공허 아이템 시스템 초기화 및 테이블 설정
PlayerVoidItem:LoadedData -- 사용자 데이터에서 공허 아이템 보유 정보와 랜덤 목록을 로드
PlayerVoidItem:SetTableClient -- 서버에서 클라이언트로 테이블 전체 데이터 동기화
PlayerVoidItem:SetTableElementClient -- 서버에서 클라이언트로 테이블의 특정 요소만 동기화
PlayerVoidItem:ChangedTable -- 테이블 변경 시 관련 UI들을 새로고침
PlayerVoidItem:GetItem -- 지정된 인덱스의 공허 아이템을 얻고 레벨을 올리며 능력치 적용
PlayerVoidItem:PurchaseItem -- 랜덤 목록에서 선택된 공허 아이템을 구매하고 재화 소모, 업적 처리
PlayerVoidItem:SetPurchaseResultPopup -- 공허 아이템 구매 결과 팝업을 UI에 표시
PlayerVoidItem:SetRandomList -- 3개의 랜덤한 공허 아이템 목록을 생성하여 상점에 표시
VoidItemShopUI:ShowSelectItemPopup -- 공허 아이템 선택 팝업을 표시하고 3가지 랜덤 옵션 목록 및 선택 상태 업데이트
VoidItemShopUI:PlaySelectItemPopupDirection -- 아이템 선택 팝업의 애니메이션 효과를 순차적으로 재생
VoidItemShopUI:SetPurchaseResultPopup -- 구매 결과 팝업을 설정하고 아이템 정보와 이팩트 애니메이션 재생
VoidItemShopUI:RefreshUI -- 구매 비용과 보유 코인 정보를 UI에 업데이트하고 구매 가능 여부 처리
VoidItemShopUI:OnUpdate -- 아이콘 랜덤 변경 시간 관리와 주기적 아이콘 랜덤 바꿈 효과 처리
VoidItemShopUI:OnBeginPlay -- 공허 아이템 샵 초기화 시 아이콘 RUID 목록 로드
VoidItemShopUI:HandleButtonClickEvent -- 구매 버튼 클릭 시 코인 도부 여부 검사 및 구매 확인 팝업 활성화
VoidItemShopUI:HandleButtonClickEvent2 -- 공허 아이템 선택 팝업 버튼 클릭 시 선택 초기화 및 팝업 표시
VoidItemShopUI:HandleButtonClickEvent3 -- 첫 번째 공허 아이템 선택 시 선택 인덱스 1로 설정 및 UI 업데이트
VoidItemShopUI:HandleButtonClickEvent4 -- 두 번째 공허 아이템 선택 시 선택 인덱스 2로 설정 및 UI 업데이트
VoidItemShopUI:HandleButtonClickEvent5 -- 세 번째 공허 아이템 선택 시 선택 인덱스 3로 설정 및 UI 업데이트
VoidItemShopUI:HandleButtonClickEvent6 -- 공허 아이템 구매 확인 버튼 클릭 시 실제 구매 처리 및 버튼 비활성화
VoidItemShopUI:HandleKeyDownEvent -- ESC 키를 눌러 공허 아이템 샵 닫기 이벤트 처리
VoidItemStorageUI:RefreshUI -- 공허 아이템 보관함 UI 전체를 새로고침하고 선택 상태 초기화
VoidItemStorageUI:ShowSelectedItem -- 선택된 공허 아이템의 상세 정보를 설명 패널에 표시하고 UI 업데이트
VoidItemStorageUI:HandleButtonClickEvent -- 공허 아이템 보관함 새로고침 버튼 클릭 이벤트 처리
VoidItemStorageUI:HandleKeyDownEvent -- ESC 키를 눌러 공허 아이템 보관함 UI를 닫는 이벤트 처리
VoidItemStorageUI_SlotButton:HandleButtonClickEvent -- 공허 아이템 슬롯 버튼 클릭 시 해당 아이템의 상세 정보를 표시하도록 요청
PortalFromMineToMineInteraction:OnBeginPlay -- 광산 내에서 다음 단계 광산으로 가는 포털 가이드 UI 설정
PortalFromMineToMineInteraction:OnInteractionEvent -- 다음 단계 광산으로 텔레포트 처리
PortalFromMineToMineInteraction:HandleInteractionEvent -- 포털 인터랙션 이벤트 핸들러 (다음 단계 광산 이동)
PortalFromMineToMineInteraction:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
PortalFromMineToMineInteraction:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
PortalToHistoricSiteInteraction:HandleInteractionEvent -- 유적지로 이동하는 포털 인터랙션 처리
PortalToMineInteraction:OnBeginPlay -- 타운에서 광산으로 가는 포털 가이드 UI 설정
PortalToMineInteraction:SetLoadingUIOn -- 광산 진입 시 로딩 UI 표시 및 플레이어 이동 비활성화
PortalToMineInteraction:EnterToMine -- 지정된 광산으로 텔레포트 및 로딩 UI 설정
PortalToMineInteraction:HandleInteractionEvent -- 광산 진입 인터랙션 이벤트 핸들러
PortalToMineInteraction:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
PortalToMineInteraction:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
PortalToNextHistoricSiteInteraction:HandleInteractionEvent -- 다음 유적지로 이동하는 포털 인터랙션 (현재 주석 처리됨)
PortalToTownInteraction:OnBeginPlay -- 게임 시작 시 인터렉션 안내 숨김 설정
PortalToTownInteraction:OnInteractionEvent -- 광산에서 타운으로 돌아가는 인터랙션 처리
PortalToTownInteraction:HandleButtonClickEvent -- 결과 UI에서 타운으로 돌아가기 버튼 클릭 처리
PortalToTownInteraction:HandleButtonClickEvent2 -- 결과 UI에서 타운으로 돌아가기 두 번째 버튼 클릭 처리
PortalToTownInteraction:HandleInteractionEvent -- 인터랙션 이벤트 핸들러 (타운 복귀 처리)
PortalToTownInteraction:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
PortalToTownInteraction:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
Portal_TownToTownInteraction:OnBeginPlay -- 타운 간 이동 포털 가이드 UI 설정
Portal_TownToTownInteraction:OnInteractionEventOnClient -- 클라이언트에서 타운 간 텔레포트 실행
Portal_TownToTownInteraction:OnInteractionEvent -- 서버에서 타운 진입 권한 확인 후 텔레포트 허가
Portal_TownToTownInteraction:HandleInteractionEvent -- 타운 포털 인터랙션 이벤트 핸들러
Portal_TownToTownInteraction:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
Portal_TownToTownInteraction:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
TeleportNpcComponent:RenewUI -- 타운 정보에 따른 텔레포트 UI 갱신 (비용 및 타운명)
TeleportNpcComponent:OnInteractionEvent -- NPC와 인터랙션 시 타운 입장밌 구매 UI 오픈 처리
TeleportNpcComponent:OnBeginPlay -- NPC 스프라이트 레이어 설정
TeleportNpcComponent:HandleInteractionEvent -- NPC 인터랙션 이벤트 핸들러
TeleportNpcComponent:HandleButtonClickEvent -- 타운 입장밌 구매 UI 닫기 버튼 처리
TeleportNpcComponent:HandleButtonClickEvent2 -- 타운 입장밌 구매 버튼 클릭 처리 (재화 확인 후 구매)
TeleportNpcComponent:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
TeleportNpcComponent:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
TeleportTownController:OnBeginPlay -- 텔레포트 타운 컨트롤러 초기화 및 UI 설정
TeleportTownController:OnUpdate -- UI 갱신이 필요할 때 실행하는 업데이트 메소드
TeleportTownController:RenewUI -- UI 갱신을 위한 플래그 설정
TeleportTownController:RenewUI_Inner -- 타운별 텔레포트 버튼 상태 갱신
TeleportTownController:HandleButtonClickEvent -- 첫 번째 타운(Town) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent2 -- 두 번째 타운(Town2) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent3 -- 세 번째 타운(Town3) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent4 -- 네 번째 타운(Town4) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent5 -- 다섯 번째 타운(Town5) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent6 -- 여섯 번째 타운(Town6) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent7 -- 일곱 번째 타운(Town7) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent8 -- 여덟 번째 타운(Town8) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent9 -- 아홉 번째 타운(Town9) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleButtonClickEvent10 -- 열 번째 타운(Town10 - 신전) 텔레포트 버튼 클릭 처리
TeleportTownController:HandleKeyDownEvent -- ESC 키 눌렀을 때 텔레포트 UI 닫기
CharonBoatUI_UseButton:HandleButtonClickEvent -- 카론의 배 사용 버튼 클릭 처리 (환생 시간 단축 아이템)
LeaderBoardUI:OnUpdate -- 리더보드 UI를 60초마다 자동 갱신하는 업데이트 메소드
LeaderBoardUI:RefreshUI -- 리더보드 순위 정보 및 플레이어 랭킹 정보 갱신
LegacycoinToEmblemUI:RefreshUI -- 레거시 코인을 엠블럼 포인트로 교환하는 UI 정보 갱신
LegacycoinToEmblemUI:HandleButtonClickEvent -- 레거시 코인으로 엠블럼 포인트 교환 버튼 클릭 처리
LegacycoinToEmblemUI:HandleKeyDownEvent -- ESC 키 눌렀을 때 레거시 코인 교환 UI 닫기
NPCInteraction:RefreshTargetUI -- 대상 UI 종류에 따른 맞춤형 UI 갱신 처리
NPCInteraction:OnInteractionEvent -- NPC와 인터랙션 시 UI 오픈 및 상태 설정
NPCInteraction:OnBeginPlay -- NPC 스프라이트 레이어 자동 설정
NPCInteraction:HandleInteractionEvent -- 인터랙션 이벤트 핸들러 (NPC 상호작용)
NPCInteraction:HandleInteractionEnterEvent -- 인터랙션 영역 진입 시 가이드 키 UI 표시
NPCInteraction:HandleInteractionLeaveEvent -- 인터랙션 영역 이탈 시 가이드 키 UI 숨김
RebornUI:RefreshUI -- 환생 UI 정보 갱신 (환생 횟수, 신전 기록, 보상 등)
RebornUI:PlayRebornDirection -- 환생 연출 애니메이션 재생 (배경 및 텍스트 효과)
RebornUI:HandleButtonClickEvent -- 환생 실행 버튼 클릭 처리
RebornUI:HandleKeyDownEvent -- ESC 키 눌렀을 때 환생 UI 닫기 (연출 중이 아니면)
RelicBinUI:RefreshUI -- 렐릭 재활용 UI 정보 갱신 (보유 렐릭을 레거시 코인으로 전환)
RelicBinUI:HandleButtonClickEvent -- 렐릭 재활용 버튼 클릭 처리 (렌거시 코인으로 전환)
RelicBinUI:HandleKeyDownEvent -- ESC 키 눌렀을 때 렐릭 빈 UI 닫기
RelicGachaShopUI:RefreshUI -- 렐릭 가차 상점 UI 정보 갱신 (가격 및 구매 버튼 상태)
RelicGachaShopUI:HandleButtonClickEvent -- 렐릭 가차 박스 구매 버튼 클릭 처리
RelicGachaShopUI:HandleKeyDownEvent -- ESC 키 눌렀을 때 렐릭 가차 상점 UI 닫기
ShopUI:OnBeginPlay -- 상점 UI 초기 설정 및 인벤토리 슬롯 생성
ShopUI:RefreshUI -- 배낭 아이템 목록 기반으로 상점 UI 갱신
ShopUI:HandleButtonClickEvent -- 모두 팔기 버튼 클릭 처리
ShopUI:HandleKeyDownEvent -- ESC 키 눌렀을 때 상점 UI 닫기
ShopUI:HandleKeyDownEvent2 -- E 키 눌렀을 때 모두 팔기 기능 실행
SprinkleItem:OnBeginPlay -- 물뿌리기 아이템 생성 및 서버/클라이언트 별 초기화
SprinkleItem:HandleTriggerEnterEvent -- 플레이어가 물뿌리기 아이템에 닿았을 때 아이템 적용 처리
EquipmentShopBundleSlotButton:HandleButtonClickEvent -- 장비샵 번들 구매 슬롯 버튼 클릭 시 체크박스 상태 토글
EquipmentShopSlotButton:HandleButtonClickEvent -- 장비샵 아이템 슬롯 버튼 클릭 시 상세 정보 팝업 표시
EquipmentShopUI:OnBeginPlay -- 로컬라이징 (텍스트)
EquipmentShopUI:OnUpdate -- UI 새로고침이 필요할 때 매 프레임마다 실행
EquipmentShopUI:RefreshUI -- UI 새로고침 플래그를 설정하여 다음 프레임에 처리
EquipmentShopUI:RefreshUI_Inner -- 장비샵 UI의 실제 새로고침 처리 (금액, 아이템 리스트 갱신)
EquipmentShopUI:ChangeFilter -- 장비 타입 필터를 변경하고 번들 구매 체크 상태 초기화
EquipmentShopUI:ShowDetailPopup -- 선택한 장비 아이템의 상세 정보 팝업 표시
EquipmentShopUI:SetPurchaseCheckUI -- 장비 구매 완료 시 능력치 증가 정보를 표시하는 팝업 설정
EquipmentShopUI:PlayPurchaseDirection -- 장비 구매 완료 시 애니메이션 효과 재생
EquipmentShopUI:RefreshBundlePurchasePopup -- 번들 구매 팝업의 내용을 갱신하고 체크 상태 반영
EquipmentShopUI:Oneshot_CheckboxButtonClicked -- 번들 구매에서 체크박스 클릭 시 선택 상태 토글
EquipmentShopUI:PlayPurchaseBundleDirection -- 번들 구매 완료 시 애니메이션 효과 및 결과 표시
EquipmentShopUI:HandleKeyDownEvent -- ESC 키 입력 시 단계적으로 팝업 또는 UI 닫기
EquipmentShopUI:HandleButtonClickEvent -- 필터 버튼 1번(무기) 클릭 시 해당 장비 종류로 전환
EquipmentShopUI:HandleButtonClickEvent2 -- 필터 버튼 2번(방어구) 클릭 시 해당 장비 종류로 전환
EquipmentShopUI:HandleButtonClickEvent3 -- 필터 버튼 3번(액세서리) 클릭 시 해당 장비 종류로 전환
EquipmentShopUI:HandleButtonClickEvent4 -- 필터 버튼 4번(스킹) 클릭 시 해당 장비 종류로 전환
EquipmentShopUI:HandleButtonClickEvent5 -- 장비 상세 정보 팝업에서 구매 버튼 클릭 시 처리
EquipmentShopUI:HandleButtonClickEvent6 -- 번들 구매 버튼 클릭 시 체크 상태 초기화하고 팝업 표시
EquipmentShopUI:HandleButtonClickEvent11 -- 번들 구매 팝업에서 구매 확정 버튼 클릭 시 실제 구매 처리
EquipmentShopUI:HandleButtonClickEvent12 -- 구매 결과창에 생성해두었던 슬롯들을 모두 제거
EquipmentShopUI:HandleButtonClickEvent7 -- 상점을 닫으면 묶음구매를 닫습니다.
MythicEquipmentShopUI:OnBeginPlay -- 신화장비 UI 초기화 시 재분배 체크 상태를 모두 false로 설정
MythicEquipmentShopUI:RefreshUI -- 다른 팝업 끄기
MythicEquipmentShopUI:SetUpgradeCheckPopup -- 신화장비 업그레이드 확인 팝업 설정 및 표시
MythicEquipmentShopUI:PlayUpgradeDirection -- 신화장비 업그레이드 완료 시 연출 효과 재생
MythicEquipmentShopUI:SetUnlockCheckPopup -- 신화장비 레벨 제한 해제 확인 팝업 설정 및 표시
MythicEquipmentShopUI:OpenRedistributionPopup -- 신석 재분배 팝업을 열고 체크 상태를 초기화
MythicEquipmentShopUI:PlayUnlockDirection -- 레벨 제한 해제 완료 시 열쇠와 자물쇠 애니메이션 재생
MythicEquipmentShopUI:RefreshRedistributionInfoPanel -- 신석 재분배 팝업의 내용을 갱신하고 체크 상태 반영
MythicEquipmentShopUI:RefreshDevineStonesInfoPanel -- 신석 세부 정보 패널을 열고 대미 세트에 따라 정보 갱신
MythicEquipmentShopUI:HandleButtonClickEvent -- 레벨업 버튼 클릭 시 업그레이드 체크 팝업 표시
MythicEquipmentShopUI:HandleButtonClickEvent2 -- 업그레이드 확인 버튼 클릭 시 신화장비 구매 실행
MythicEquipmentShopUI:HandleButtonClickEvent3 -- 필터 버튼 1번 클릭 시 해당 장비로 전환
MythicEquipmentShopUI:HandleButtonClickEvent4 -- 필터 버튼 2번 클릭 시 해당 장비로 전환
MythicEquipmentShopUI:HandleButtonClickEvent5 -- 필터 버튼 3번 클릭 시 해당 장비로 전환
MythicEquipmentShopUI:HandleButtonClickEvent6 -- 필터 버튼 4번 클릭 시 해당 장비로 전환
MythicEquipmentShopUI:HandleButtonClickEvent7 -- 언락 버튼 클릭 시 레벨 제한 해제 팝업 표시
MythicEquipmentShopUI:HandleButtonClickEvent8 -- 재분배 버튼 클릭 시 신석 재분배 팝업 표시
MythicEquipmentShopUI:HandleButtonClickEvent9 -- 재분배 실행 버튼 클릭 시 신석 재분배 처리
MythicEquipmentShopUI:HandleButtonClickEvent10 -- 언락을 시도합니다.
MythicEquipmentShopUI:HandleButtonClickEvent11 -- 닫기 버튼 클릭 시 UI 새로고침
MythicEquipmentShopUI:HandleButtonClickEvent12 -- 신석 상세 정보 버튼 클릭 시 대미 세트 정보 표시
MythicEquipmentShopUI:HandleButtonClickEvent13 -- 신석 상세 정보 버튼 클릭 시 대미 세트 정보 표시
MythicEquipmentShopUI:HandleButtonClickEvent14 -- 레벨 업 버튼 클릭 시 업그레이드 레벨 1단계 증가
MythicEquipmentShopUI:HandleButtonClickEvent15 -- 최대 레벨 버튼 클릭 시 사용 가능한 최대 레벨로 업그레이드 설정
MythicEquipmentShopUI:HandleButtonClickEvent16 -- 레벨 다운 버튼 클릭 시 업그레이드 레벨 1단계 감소
MythicEquipmentShopUI:HandleButtonClickEvent17 -- 최소 레벨 버튼 클릭 시 업그레이드 레벨을 1로 리셋
MythicEquipmentShopUI:HandleButtonClickEvent18 -- 닫기 버튼 클릭 시 UI 새로고침
MythicEquipmentShopUI:HandleKeyDownEvent -- ESC 키 입력 시 상세 정보 패널 또는 UI 닫기
MythicEquipmentShopUI_RedistributionCheckPopup_CheckButton:HandleButtonClickEvent -- 신석 재분배 체크 버튼 클릭 시 체크 상태 토글 및 UI 갱신
GemShopLogic:BuyItem -- 젠 샵에서 아이템 구매 처리 (소모품, 추가 아이템, 특수 아이템)
GemShopLogic:GetNewChair -- 새로운 의자를 랜덤으로 획득하거나 모두 소유시 대신 유물 상자 지급
GemShopUI:OnBeginPlay -- 젠 샵 UI 초기화 시 상품 리스트 생성 및 설정
GemShopUI:RefreshUI -- 젠 샵 UI 새로고침 (필터, 선택, 재화 보유량, 상세정보)
GemShopUI:ShowDetailInfo -- 선택한 아이템의 상세 정보 팝업을 표시하고 UI 갱신
GemShopUI:SetPurchaseCheckPopup -- 아이템 구매 확인 팝업 설정 및 비용 정보 표시
GemShopUI:RefreshDetailInfoPanel -- 선택한 아이템의 상세 정보 패널을 갱신하고 구매 버튼 상태 설정
GemShopUI:SetFilterIdx -- 상품 필터를 변경하고 팝업 닫기 및 UI 새로고침
GemShopUI:HandleButtonClickEvent -- 필터 버튼 1번(박스) 클릭 시 해당 필터로 전환
GemShopUI:HandleButtonClickEvent2 -- 필터 버튼 2번(도구) 클릭 시 해당 필터로 전환
GemShopUI:HandleButtonClickEvent3 -- 필터 버튼 3번(기타) 클릭 시 해당 필터로 전환
GemShopUI:HandleButtonClickEvent4 -- 필터 버튼 4번(이벤트) 클릭 시 해당 필터로 전환
GemShopUI:HandleButtonClickEvent5 -- 상세 정보 패널에서 구매 버튼 클릭 시 처리
GemShopUI:HandleButtonClickEvent6 -- 샵 닫기 버튼 클릭 시 필터 초기화 및 BGM 재생
GemShopUI:HandleButtonClickEvent7 -- 구매 확인 팝업에서 구매 확정 버튼 클릭 시 처리
GemShopUI:HandleButtonClickEvent8 -- 상세 정보 패널 닫기 버튼 클릭 시 선택 상태 초기화
GemShopUI:HandleButtonClickEvent9 -- 구매 확인 팝업 취소 버튼 클릭 시 선택 상태 초기화 및 BGM 복원
GemShopUI:HandleKeyDownEvent -- ESC 키 입력 시 구매 확인 팝업 또는 UI 닫기
GemShopUI_SlotButton:HandleButtonClickEvent -- 젠샵 아이템 슬롯 버튼 클릭 시 상세 정보 표시
RebornShopUI:OnBeginPlay -- 리본 샵 UI 초기화 및 로컬라이징
RebornShopUI:RefreshList -- 리본 샵 리스트 새로고침 (현재 비어있음)
RelicMergeShopUI:PlayMergeDirection -- 유물 합성 완료 시 애니메이션 효과 및 결과 표시
RelicMergeShopUI:RefreshMainPanel -- 메인 패널의 유물 재료 수, 결과 수, 선택 상태 갱신
RelicMergeShopUI:IsPossibleRegistToBook -- 해당 유물을 도감에 등록 가능한지 확인
RelicMergeShopUI:SelectGrade -- 자동 합성에서 선택한 등급을 설정하고 메인 패널 갱신
RelicMergeShopUI:SetResultPopup -- 유물 합성 결과를 보여주는 팝업 설정 및 리스트 갱신
RelicMergeShopUI:HandleButtonClickEvent -- 합성하기 버튼 클릭 시 자동 합성 실행
RelicMergeShopUI:HandleKeyDownEvent -- ESC 키 입력 시 연출 중이 아닐 때 UI 닫기
RelicMergeShopUI:HandleButtonClickEvent2 -- 1등급 유물 선택 버튼 클릭 시 선택 상태 토글
RelicMergeShopUI:HandleButtonClickEvent3 -- 2등급 유물 선택 버튼 클릭 시 선택 상태 토글
RelicMergeShopUI:HandleButtonClickEvent4 -- 3등급 유물 선택 버튼 클릭 시 선택 상태 토글
RelicMergeShopUI:HandleButtonClickEvent6 -- 4등급 유물 선택 버튼 클릭 시 선택 상태 토글
RelicMergeShopUI_MaterialButton:HandleButtonClickEvent -- 유물 합성 재료 선택 버튼 클릭 시 해당 재료 등록 처리
RelicMergeShopUI_MaterialSlotButton:HandleButtonClickEvent -- 유물 합성 재료 슬롯 버튼 클릭 시 대기 인덱스 설정 및 재료 선택 패널 표시
DynamicFootholdManager:HandleInteractionEvent -- 동적 발판과 상호작용 시 발판 활성화 및 사운드 재생
Trap:OnBeginPlay -- 함정 초기화 시 피격 가능 상태로 설정
Trap:MakeCanHit -- 함정의 피격 가능 상태를 외부에서 설정
Trap:HandleTriggerEnterEvent -- 플레이어와 충돌 시 데미지, 이팩트, 중독, 널백 처리
TrapBullet:OnUpdate -- 함정 총알이 일정 속도로 이동하고 생존 시간 초과시 제거
TrapBullet:HandleTriggerEnterEvent -- 플레이어와 충돌 시 눈덩이/일반 총알 타입에 따른 효과 처리
TrapBulletShooter:Fire -- 투사체를 생성하고 설정된 각도로 발사하며 이펙트 재생
TrapBulletShooter:OnBeginPlay -- 함정 총알 발사기 초기화 시 쿨다운 설정 및 재귀 함수 시작
TrapBulletShooter:RecursiveFunc -- 일정 간격으로 쿨다운을 감소시키고 0이 되면 발사하는 재귀 함수
TrapContinuous:OnUpdate -- 지속 대미지 함정의 쿨다운 체크 및 타격 실행
TrapContinuous:Hit -- 플레이어에게 지속적으로 데미지, 사운드, 이팩트 적용
TrapContinuous:HandleTriggerEnterEvent -- 플레이어가 지속 대미지 범위에 진입할 때 타격 시작
TrapContinuous:HandleTriggerLeaveEvent -- 플레이어가 지속 대미지 범위를 벗어날 때 타격 중지
TrapGuardian:SpawnAttack -- 가디언 공격 미사일을 생성하고 속성 설정
TrapGuardian:GetAttackModelId -- 가디언 타입에 따른 공격 모델 ID 반환
TrapGuardian:OnUpdate -- 플래이어 감지 시 쿨타임 체크하여 공격 실행
TrapGuardian:OnBeginPlay -- 가디언 초기화 시 쿨다운 설정
TrapGuardian:HandleTriggerStayEvent -- 플레이어가 범위 내에 머물 때 감지 상태로 설정
TrapGuardian:HandleTriggerLeaveEvent -- 플레이어가 범위를 벗어났을 때 감지 해제
TrapGuardianBullet:OnUpdate -- 플레이어를 추적하고 생존 시간 검사 후 제거
TrapGuardianBullet:ChasePlayer -- 플레이어 방향으로 이동하고 회전 업데이트
TrapGuardianBullet:HandleTriggerEnterEvent -- 플레이어와 충돌 시 감전 데미지, 이팩트, 사운드 처리 후 제거
TrapGuardianBullet:HandleTriggerLeaveEvent -- 범위에서 빠져나갔을 때 엔티티 제거
TrapJump:HandleTriggerEnterEvent -- 플레이어가 점프대에 충돌할 때 위로 점프력 부여
TrapProjectile:DestroySelf -- 투사체 엔티티를 제거
TrapProjectile:SetParameter -- 투사체의 각도, 거리, 속도를 설정하여 발사
TrapProjectile:HandleTriggerEnterEvent -- 플레이어와 충돌 시 데미지 처리 및 이펙트 재생
TrapRotating:OnUpdate -- 시계방향/반시계방향으로 회전하며 20초마다 방향을 바꿈
TrapRotating:ChangeClockwise -- 시계방향과 반시계방향 회전을 전환
TrapRotating:OnBeginPlay -- 회전 방향 전환 타이머를 초기화
TrapShowHitRange:OnBeginPlay -- 트랩의 공격 범위를 시각적으로 표시하는 오브젝트들을 생성
TrapTest:OnBeginPlay -- 타겟을 로컬 플레이어로 설정하고 생명시간을 초기화
TrapTest:OnUpdate -- 생명시간이 끝나면 플레이어를 추적하여 이동
TrapTest:ChasePlayer -- 플레이어 추적 로직 (구현되지 않음)
TrapTriggerStay:OnUpdate -- 타격 쿨다운 시간을 업데이트
TrapTriggerStay:HandleTriggerStayEvent -- 플레이어가 트랩에 머물 때 지속적으로 데미지를 입힘
TrapUprisingSpearSensor:SpawnUprisingSpearTrap -- 솟아오르는 창 트랩을 생성하고 0.5초 후에 제거
TrapUprisingSpearSensor:OnUpdate -- 감지 쿨다운 시간을 업데이트
TrapUprisingSpearSensor:OnBeginPlay -- 감지 쿨다운을 초기화
TrapUprisingSpearSensor:HandleTriggerStayEvent -- 플레이어 감지 시 사운드 재생 후 창 트랩을 1초 뒤에 소환
TrapDayOrNight:OnUpdate -- 30초마다 낮과 밤 배경을 전환
TrapMonster:Sturn -- 몬스터를 기절시키거나 기절에서 회복시킴
TrapThrownRock:OnUpdate -- 3초 후에 돌 오브젝트를 제거
TrapThrownRock:HandleTriggerEnterEvent -- 몬스터와 충돌 시 기절 효과를 적용하고 이펙트를 재생
ButtonDeselect:HandleButtonClickEvent -- 버튼 클릭 시 부모의 선택 상태를 해제
ButtonSelect:Select -- 버튼의 선택 상태를 설정하고 시각적으로 표시
ButtonSelect:OnBeginPlay -- 선택 가능 여부와 선택 상태를 초기화
ButtonSelect:HandleButtonClickEvent -- 선택 가능한 상태일 때 버튼을 선택 상태로 변경
ButtonUIOpen:HandleButtonClickEvent -- 지정된 타겟 UI를 활성화
DisableWhenESCKeyInputed:HandleButtonClickEvent -- 버튼 클릭 이벤트 핸들러 (빈 구현)
DisableWhenESCKeyInputed:HandleKeyDownEvent -- ESC키나 마우스 클릭으로 UI를 비활성화
DisableWhenESCKeyInputed:HandleScreenTouchEvent -- 화면 터치로 UI를 비활성화
ExitButton:HandleButtonClickEvent -- 지정된 UI 또는 부모 UI를 비활성화하고 플레이어 움직임을 활성화
IngameUIManager:OnBeginPlay -- UI 지역화 텍스트를 적용 (현재 주석 처리됨)
IngameUIManager:HandleLocalPlayerMapEnterEvent -- 맵 진입 시 UI 활성화 상태를 맵 타입에 따라 설정
LoadingManager:SetLoadingUIOn -- 로딩 UI의 활성화 상태를 설정하고 플레이어 움직임을 제어
LoadingManager:UpdateTipMessage -- 무작위 팁 메시지를 생성하여 UI에 표시
LoadingManager:OnUpdate -- 로딩 중일 때 4초마다 팁 메시지를 업데이트
LoadingManager:SetPlayerMovement -- 플레이어의 움직임 컴포넌트 활성화 상태를 설정
LoadingManager:OnBeginPlay -- 게임 시작 시 로딩 상태를 초기화하고 모험 시작 버튼을 활성화
LoadingManager:HandleButtonClickEvent -- 모험 시작 버튼 클릭 시 게임 데이터를 초기화하고 맵 진입 UI를 표시
LoadingManager:HandleKeyDownEvent -- E키 입력으로 모험을 시작할 수 있도록 처리
OutgameUIManager:HandleLocalPlayerMapEnterEvent -- 맵 진입 시 아웃게임 UI 상태를 맵 타입에 따라 설정
RainbowSprite:OnUpdate -- 스프라이트의 색상을 무지개색으로 순환하며 변경
RainbowText:OnUpdate -- 텍스트의 색상을 무지개색으로 순환하며 변경
UIButtonSound:HandleButtonClickEvent -- 버튼 클릭 시 사운드 타입에 따라 다른 소리를 재생
UIFlickering:OnUpdate -- UI 계열 깜뿡임 효과를 1초 주기로 업데이트
UIGuideAndButtonInteraction:PlayButtonClickDirection -- 버튼 클릭 시 안내 텍스트와 버튼 아이콘에 애니메이션 효과 지연 재생
UIGuideAndButtonInteraction:HandleButtonClickEvent -- 인터랙션 버튼 클릭 이벤트 처리하여 다양한 오브젝트 상호작용 수행
UIGuideNavigatorButton:HandleButtonClickEvent -- 가이드 내비게이션 버튼 클릭 시 대상 페이지를 활성화하고 나머지는 비활성화
UIHelpGuide:ChangePage -- 도움말 가이드의 페이지를 변경하고 해당 버튼 상태 업데이트
UIHelpGuide:OnBeginPlay -- 도움말 가이드 UI 초기화 및 로컬라이제이션 설정
UIHelpGuide:HandleKeyDownEvent -- ESC 키 입력 이벤트 처리하여 도움말 창 닫기
UIHelpGuideNavButton:HandleButtonClickEvent -- 도움말 가이드 내비게이션 버튼 클릭 시 해당 페이지로 변경
UIMouseHover:SetHoverUI -- 지정된 UI 타입에 따라 마우스 호버 툴팁을 표시하거나 숨김
UIMouseHover:OnBeginPlay -- 컴포넌트 초기화 시 아이템/유물 데이터 테이블 로드 및 로컬라이제이션 설정
UIMouseHover:HandleButtonStateChangeEvent -- 버튼 상태 변화 이벤트 처리하여 플랫폼별로 호버 UI 표시/숨김
UISeekerComponent:OnUpdate -- 매 프레임마다 타겟으로 이동하는 UI 요소의 위치 및 속도 계산
UISeekerComponent:Guide -- 타겟 위치를 향한 단위 벡터 계산으로 이동 방향 결정
UISeekerComponent:OnBeginPlay -- 컴포넌트 초기화 시 UI 트랜스폼 컴포넌트 참조 설정
UIWorldIngressLoading:OnUpdate -- 매 프레임마다 로컬 플레이어의 맵 진입 상태를 검사하여 로딩 UI 비활성화
UIWorldIngressLoading:OnBeginPlay -- 언어 설정에 따라 적절한 로고 표시 및 로딩 UI 활성화
UIWorldIngressLoading:SetLoadingUIOff -- 로딩 UI를 서서히 페이드아웃 효과로 비활성화
UIWorldIngressLoading:SetLoadingUIOn -- 로딩 UI를 즉시 활성화하여 표시
WarningFlickeringUI:OnUpdate -- 경고 UI의 사이클릭 깜뿡임 효과를 설정된 주기로 업데이트
UIInventory:OnBeginPlay -- 인벤토리 UI 초기화와 인벤토리 버튼 연결 설정
UIInventory:HandleInventoryItemInitEvent -- 인벤토리 아이템 초기화 이벤트 처리하여 모든 아이템 슬롯 생성
UIInventory:HandleInventoryItemAddedEvent -- 인벤토리에 새로운 아이템이 추가될 때 슬롯 생성
UIInventory:HandleInventoryItemRemovedEvent -- 인벤토리에서 아이템이 제거될 때 해당 슬롯 삭제
UIInventory:HandleInventoryItemModifiedEvent -- 인벤토리 아이템이 변경될 때 해당 슬롯 데이터 업데이트
UIItemSlot:SetData -- 아이템 슬롯에 아이템 데이터를 설정하고 UI 업데이트
UIItemSlot:HandleButtonClickEvent -- 아이템 슬롯 클릭 이벤트 처리 (현재 비어 있음)
UIMyInfoSimple:OnBeginPlay -- 컴포넌트 초기화 시 내 정보 UI 참조 설정
UIMyInfoSimple:OnUpdate -- 매 프레임마다 로컬 플레이어의 닉네임과 HP를 UI에 업데이트
ChasePlayer:OnUpdate -- 플레이어와의 거리를 계산하여 추격 모드 전환 판단
ChasePlayer:ChasePlayer -- 추격 모드에 따라 플레이어 추격 또는 원점 복귀 이동
ChasePlayer:OnBeginPlay -- 초기 스폰 위치를 원점으로 저장
ChasePlayer:FlipX -- 이동 방향에 따라 스프라이트 좌우 반전 제어
Gimmick_PlayerJumping:HandleTriggerEnterEvent -- 플레이어가 점프 기믹에 접촉 시 지정된 힘으로 라웄치 시키며 이팩트 재생
GraveStone:OnUpdate -- 고스트가 존재하지 않을 때 스폰 타이머 카운트다운
GraveStone:OnBeginPlay -- 묘비 초기화 및 스폰 타이머 설정
GraveStone:SpawnGhost -- 묘비에서 고스트 엔티티 생성 및 타이머 재설정
GraveStone:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 스폰 애니메이션 완료 시 고스트 생성 및 원래 스프라이트로 복귀
PlanetMovement:OnUpdate -- 매 프레임마다 행성 공전 업데이트
PlanetMovement:Rotation -- 태양 중심으로 지정된 반지름과 속도로 원형 공전 운동
PlanetMovement:OnBeginPlay -- 행성 초기화 및 충돌 시 가할 힘 설정
PlanetMovement:HandleTriggerEnterEvent -- 플레이어가 행성에 충돌 시 공전 방향으로 힘 가해
RotationShield:OnUpdate -- 매 프레임마다 회전 방패 회전 동작 업데이트
RotationShield:Rotation -- 플레이어 주위로 일정 반지름에서 원형 경로로 회전
RotationShield:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 파괴 애니메이션 완료 시 방패 제거 및 이팩트 재생
TestCode230116:OnBeginPlay -- 플레이어 좌우 이동 키 반전 설정 (테스트용)
TrapSpawnManager:SpawnRandomMiningTarget -- 지정된 개수만큼 랜덤으로 자식 트랩 엔티티를 활성화하고 나머지는 비활성화
TrapSpawnManager:OnBeginPlay -- 트랩 스폰 매니저 초기화 및 자동 트랩 활성화 실행
Trap_InkBullet:OnBeginPlay -- 묵물 발사체 수명 타이머 설정
Trap_InkBullet:OnUpdate -- 지정된 방향벡터로 매 프레임 이동
Trap_InkBullet:HandleTriggerEnterEvent -- 플레이어에게 묵물 발사체가 닿아 데미지 전달 후 자기 파괴
Trap_InkBullet:HandleFootholdCollisionEvent -- 묵물 발사체가 지면이나 장애물과 충돌 시 2초 후 자동 제거
Trap_JuniorGhost:Destroy -- 유니어 고스트를 사망 상태로 전환하여 사망 애니메이션 실행
Trap_JuniorGhost:OnBeginPlay -- 유니어 고스트 초기화 (현재 비활성화)
Trap_JuniorGhost:OnUpdate -- 사망하지 않았을 때 좌측으로 지속적으로 이동
Trap_JuniorGhost:HandleTriggerEnterEvent -- 플레이어가 유니어 고스트에 접촉 시 게임오버 처리
Trap_JuniorGhost:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 사망 애니메이션 완료 시 엔티티 삭제
Trap_PillarManager:OnBeginPlay -- 화염 기둥 가왕자 초기화 및 자동 공격 시작 설정
Trap_PillarManager:PlayAttack -- 순차적으로 화염 기둥들의 공격 발동 제어
Trap_PillarOfFire:Attack -- 화염 기둥 공격 애니메이션 시작
Trap_PillarOfFire:OnBeginPlay -- 화염 기둥 초기화 및 원본 스프라이트 저장
Trap_PillarOfFire:HandleTriggerEnterEvent -- 플레이어가 화염 기둥 연소 영역에 진입 시 화상 데미지 처리
Trap_PillarOfFire:HandleTriggerStayEvent -- 플레이어가 화염 기둥 연소 영역에 머물 때 화상 데미지 처리
Trap_PillarOfFire:HandleSpriteAnimPlayerEndFrameEvent -- 공격 애니메이션 종료 시 원래 스프라이트로 복귀 및 다음 공격 예약
Trap_PillarOfFire:HandleSpriteAnimPlayerChangeFrameEvent -- 공격 애니메이션 프레임 진행 추적
Trap_SeaOfPoseidon:InToTheWater -- 물에 진입하면 페널티 시작
Trap_SeaOfPoseidon:SpawnBubble -- 플레이어 위치에서 물방울을 생성하여 상승 애니메이션 실행
Trap_SeaOfPoseidon:HandleTriggerEnterEvent -- 플레이어가 포세이돈의 바다 트랩 영역에 진입했을 때 다이빙 상태로 전환
Trap_SeaOfPoseidon:HandleTriggerLeaveEvent -- 물방울이나 플레이어가 바다 트랩 영역에서 벗어날 때 처리
Trap_SeaOfPoseidon:HandleTriggerStayEvent -- 플레이어가 물 속에 머무를 때 렌더링 레이어와 중력 조정
Trap_Snow:HandleTriggerEnterEvent -- 플레이어가 눈에 접촉 시 눈사람 상태가 아니면 빙결 스택 추가
Trap_SnowShooter:OnBeginPlay -- 눈덩이 발사기 초기화 및 주기적 공격 타이머 설정
Trap_SnowShooter:Throwing -- 눈덩이 발사 애니메이션 시작 및 공격 상태 활성화
Trap_SnowShooter:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 공격 애니메이션 프레임에 따라 눈덩이 발사체 생성 및 스프라이트 전환
Trap_SnowShooter:HandleSpriteAnimPlayerEndFrameEvent -- 애니메이션 종료 시 처리 (현재 비활성화)
Trap_SpawnSnow:OnBeginPlay -- 눈 생성기 초기화 및 주기적 눈 생성 타이머 설정
Trap_SpawnSnow:SpawnSnow -- 지정된 범위 내에서 랜덤 개수의 눈 엔티티를 랜덤 위치에 생성
Trap_Squid:OnBeginPlay -- 스퀼드 트랩 초기화 및 공격 타이머 설정
Trap_Squid:ReadyShot -- 공격 준비 상태에 따라 스퀼드 색상 변경 애니메이션 실행
Trap_Squid:ShotInk -- 묵물을 360도 전방위로 사격하여 데미지 전달
Trap_Squid:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 스퀼드 애니메이션 프레임 변경 시 공격 타이밍 제어
Trap_ThunderCloud:OnBeginPlay -- 천둑 구름 초기화 및 주기적 번개 공격 타이머 설정
Trap_ThunderCloud:Lightning -- 천둥 구름 스프라이트 깜빡임 후 랜덤 위치에 번개 공격 생성
Trap_ThunderCloud:SpawnBullet -- 번개 좌우 확산용 전기 발사체 생성
Trap_ThunderMonster:OnBeginPlay -- 번개 먬스터 초기화 및 주기적 번개 공격 타이머 설정
Trap_ThunderMonster:Lightning -- 좌우로 확산되는 번개 발사체 생성
Trap_ThunderMonster:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 번개 애니메이션 프레임에 따라 발사체 생성 및 스프라이트 전환
Trap_ThunderMonsterBullet:OnUpdate -- 초기화 후 좌우 방향으로 이동하며 때에 떨어지면 자동 파괴
Trap_ThunderMonsterBullet:OnBeginPlay -- 번개 발사체 초기화 및 1.5초 후 이동 시작 설정
Trap_ThunderMonsterBullet:HandleTriggerEnterEvent -- 플레이어 충돌 시 전기 이팩트 및 소리 재생 후 엔티티 제거
Trap_ThunderPriest:OnBeginPlay -- 컴포넌트 초기화 시 원본 스프라이트 저장 및 범위 표시 활성화
Trap_ThunderPriest:Lightning -- 플레이어가 범위 내에 있을 때 번개 공격 실행 및 반복 공격 시작
Trap_ThunderPriest:RepeatLightning -- 쿨타임마다 번개 공격을 반복하는 타이머 설정
Trap_ThunderPriest:HandleEmbededSpriteAnimPlayerChangeFrameEvent -- 스프라이트 애니메이션 프레임 변화 시 번개 복원 및 투사체 생성 처리
Trap_ThunderPriest:HandleTriggerEnterEvent -- 플레이어가 트리거 범위에 진입 시 번개 공격 시작
Trap_ThunderPriest:HandleTriggerLeaveEvent -- 플레이어가 트리거 범위를 벗어나면 번개 공격 중지
Trap_Torpedo:Explosion -- 플레이어가 어뢰에 닿았을 때 폭발 효과 실행 및 넉백 적용
Trap_Torpedo:OnBeginPlay -- 어뢰 트랩 초기화 시 넉백 파워 설정
Trap_Torpedo:HandleTriggerEnterEvent -- 플레이어가 트리거에 진입 시 폭발 상태로 변경하고 폭발 실행
Trap_Torpedo:HandleSpriteAnimPlayerChangeFrameEvent -- 폭발 애니메이션이 끝나면 엔터티 비활성화
GoldApple:OnUpdate -- 골드 애플이 타겟 위치를 향해 지정된 속도로 이동
GoldApple:OnBeginPlay -- 골드 애플 생성 시 3초 후 자동으로 제거되도록 타이머 설정
GoldAppleReward:HandleFootholdCollisionEvent -- 골드 애플이 바닥에 충돌 시 서서히 투명해지며 사라짐
Trap_Cupid:OnBeginPlay -- 큐피드 트랩 초기화 및 주기적 공격 타이머 설정
Trap_Cupid:SpawnArrow -- 큐피드 화살 생성 및 속성 설정, 생명주기 관리
Trap_Cupid:HandleSpriteAnimPlayerEndFrameEvent -- 공격 애니메이션 종료 시 스프라이트를 원상복구하고 화살 생성
Trap_CupidArrow:OnUpdate -- 초기화 완료 후 방향과 가속도에 따라 화살 이동
Trap_CupidArrow:Init -- 큐피드 화살의 방향, 속도, 회전, 플립 상태 초기화
Trap_CupidArrow:HandleTriggerEnterEvent -- 플레이어와 충돌 시 마법 효과 적용 및 화살 제거
Trap_DevilBullet:OnUpdate -- 초기화 완료 후 방향과 가속도에 따라 악마 총알 이동
Trap_DevilBullet:Init -- 악마 총알의 방향, 속도, 크기, 회전, 플립 상태 초기화
Trap_DevilBullet:HandleTriggerEnterEvent -- 플레이어와 충돌 시 마법 해제 효과 적용 및 총알 제거
Trap_HeartBullet:OnUpdate -- 하트 총알의 이동 - 전진 후 역방향으로 빠르게 되돌아감
Trap_HeartBullet:OnBeginPlay -- 하트 총알 생성 시 생명주기 절반 지점에서 역방향 전환 타이머 설정
Trap_HeartBullet:HandleTriggerEnterEvent -- 스폰포인트 도달 시 소멸, 플레이어 충돌 시 마법 효과 및 데미지 적용
Trap_LittleDevil:OnBeginPlay -- 악마 기믹은 좌우로만 배치 (대각배치하면 스폰 로직 꼬임)
Trap_LittleDevil:SpawnArrow -- 좌우 방향에 따라 악마 화살 생성 위치 설정 및 발사
Trap_LovePoison:HandleTriggerEnterEvent -- 플레이어가 러브 포이즌에 접촉 시 사운드 재생 및 마법 효과 적용
Trap_LoveStatus:OnBeginPlay -- 러브 상태 트랩 초기화, 주기적으로 예고 효과 후 하트 총알 발사
Trap_LoveStatus:Shot -- 5~8개의 하트 총알을 360도 원형으로 발사
TempleApollonManager:OnBeginPlay -- 아폴론 신전 관리자 초기화, 지정된 시간에 숭배 오브젝트 생성
Trap_Sun:FireCircle -- 태양 트랩에서 원형으로 총알 발사 (현재 주석 처리됨)
Trap_Sun:OnBeginPlay -- 태양 트랩 초기화 및 반복 발사 패턴 설정 (현재 주석 처리됨)
Trap_Sun:HandleTriggerEnterEvent -- 플레이어가 태양 트랩에 접촉 시 즉사 데미지 적용
Trap_SunBullet:OnUpdate -- 태양 총알의 방향별 이동 및 회전 효과
Trap_SunBullet:OnBeginPlay -- 태양 총알 생성 시 생명주기 타이머 설정으로 자동 소멸
Trap_SunBullet:HandleTriggerEnterEvent -- 플레이어 충돌 시 화상 스택 적용, 데미지 적용 및 총알 소멸
RotateDegree180:OnUpdate -- 180도 회전 범위 내에서 시계방향/반시계방향으로 연속 회전
RotateDegree180:OnBeginPlay -- 회전 상태 초기화 및 스프라이트 투명도 설정
RotateDegree180:HandleTriggerEnterEvent -- 플레이어 접촉 시 회전 방향에 따라 밀어내는 힘을 가하고 상태 변경
Trap_Arrow:OnUpdate -- 화살 트랩의 방향과 속도에 따라 이동
Trap_Arrow:HandleTriggerEnterEvent -- 플레이어 충돌 시 밀어내기 및 화살 소멸 (현재 주석 처리됨)
Trap_ArrowShooter:OnBeginPlay -- 화살 발사기 초기화 및 주기적 발사 타이머 설정
Trap_ArrowShooter:Shot -- 화살 발사 준비 효과 표시 후 일정 시간 뒤 화살 생성 및 발사
DemeterTempleManager:Rebirth -- 플레이어를 봄 테마로 다시 태어나게 하여 맵 환경을 변경하고 함정을 해제함
DemeterTempleManager:SetColorAlpha -- 화면 전환 효과를 위해 마스킹 UI의 알파값을 조절하여 페이드 인/아웃 에니메이션을 실행함
DemeterTempleManager:OnBeginPlay -- 데메테르 신전 입장 시 플레이어의 이동 드래그를 설정
DemeterTempleManager:HandleInteractionEvent -- 제단과 상호작용 시 봄 매직 효과를 실행하여 신전을 변화시킴
DemeterTempleManager:HandleInteractionEnterEvent -- 제단 근처에 들어올 때 가이드 키 UI를 표시함
DemeterTempleManager:HandleInteractionLeaveEvent -- 제단에서 벗어날 때 가이드 키 UI를 숨김
SnowMan:destroy -- 눈사람 파괴 애니메이션을 빠르게 재생하고 파괴 사운드와 이팩트 실행
SnowMan:HandleSpriteAnimPlayerEndFrameEvent -- 파괴 애니메이션이 끝날 때 플레이어를 원래 상태로 복원하고 눈사람 엔티티를 제거
HadesWaterBuff:Use -- 하데스 물을 사용하여 플레이어의 이동 속도를 증가시킨 다음 사용 완료 표시를 위해 투명도를 낮춤
HadesWaterBuff:HandleInteractionEnterEvent -- 플레이어가 하데스 물 근처에 들어올 때 사용 가이드를 표시
HadesWaterBuff:HandleInteractionLeaveEvent -- 플레이어가 하데스 물에서 벗어날 때 가이드 UI를 숨김
HadesWaterBuff:HandleInteractionEvent -- 플레이어가 하데스 물과 상호작용할 때 속도 버프를 적용하고 가이드 UI를 제거
SpawnThroneManager:SpawnRandomMiningTarget -- 지정된 수만큼의 랜덤 왕좌 함정을 활성화하고 데미지 설정
SpawnThroneManager:OnBeginPlay -- 초기화 시 로컬 플레이어를 대상으로 왕좌 함정을 랜덤 생성
TempleHadesManager:OnBeginPlay -- 하데스 신전 입장 시 초기화를 수행하여 게임 환경을 설정함
TempleHadesManager:StartGame -- 사신 추격 게임을 시작하고 3초 후 게임 상태를 활성화함
TempleHadesManager:SetHadesPlay -- 하데스 신전 게임 모드를 설정하고 플레이어 상태를 초기화함
TempleHadesManager:HandleButtonClickEvent -- 입장 확인 버튼 클릭 시 게임을 시작하고 UI를 닫음
TempleHadesManager:HandleKeyDownEvent -- E키 입력 시 입장 확인 버튼 클릭과 동일한 기능을 수행
Trap_ChaseSasin:OnUpdate -- 하데스 게임 시작 시 사신이 플레이어를 추격하고 게임오버 시 속도 배수 증가
Trap_ChaseSasin:Chase -- 플레이어를 추격하여 일정 거리 안에 오면 공격을 실행하고 게임오버 처리
Trap_ChaseSasin:OnBeginPlay -- 초기화 시 원래 속도를 저장하여 나중에 속도 증가 처리에 활용
Trap_GhostSpawner:OnBeginPlay -- 하데스 게임 시작 시 설정된 쿨타임에 따라 유령을 반복 생성
Trap_Hades_Throne:HandleTriggerEnterEvent -- 플레이어가 하데스 왕좌에 닿으면 게임 오버 상태로 전환하고 성공 이팩트 실행
Trap_StoneFish:OnUpdate -- 돌 물고기의 좌우 이동과 공격 상태를 관리하며 주기적으로 데미지를 가함
Trap_StoneFish:OnBeginPlay -- 초기화 시 공격 범위를 활성화하고 쿨타임을 설정
Trap_StoneFish:HandleTriggerEnterEvent -- 플레이어가 돌 물고기 공격 범위에 들어올 때 공격 이팩트를 활성화
Trap_StoneFish:HandleTriggerLeaveEvent2 -- 플레이어가 공격 범위에서 벗어날 때 공격 이팩트를 비활성화하고 쿨타임 초기화
Trap_StoneFishRangeCheck:HandleTriggerLeaveEvent -- 플레이어가 돌 물고기 공격 범위에서 벗어날 때 공격 모드 비활성화
Trap_StoneFishRangeCheck:HandleTriggerStayEvent -- 플레이어가 돌 물고기 공격 범위에 머문 때 공격 모드 활성화
sampleBullet:OnUpdate -- 설정된 방향과 속도로 탄알을 직선 이동시킴
sampleBullet:HandleTriggerEnterEvent -- 플레이어와 충돌 시 화상 스택을 상승시키고 탄알을 소멸
Trap_RotateShooter:Shooter -- 사방으로 회전하며 탄알을 발사하는 함정 시스템을 실행
Trap_RotateShooter:OnUpdate -- 탄알 발사 지점을 지속적으로 회전시켜 다양한 방향으로 공격
Trap_RotateShooter:OnBeginPlay -- 초기화 시 원래 색상을 저장하고 설정된 쿨타임으로 반복 발사 시작
CloudLightningTriggerCheck:HandleTriggerStayEvent -- 플레이어가 번개 공격 영역에 있고 공격 선택 상태일 때 전기 데미지 실행
ElectricWarpInteraction:teleport -- 지정된 방향으로 전기 워프를 실행하여 플레이어를 이동시킴
ElectricWarpInteraction:reset -- 워프 사용 후 모든 방향 화살표와 가이드 UI를 초기화함
ElectricWarpInteraction:destroyGuideKey -- 워프 사용 가이드 키 UI를 제거함
ElectricWarpInteraction:OnBeginPlay -- 컴포넌트 초기화 시 포털 사용 가능 상태를 false로 설정
ElectricWarpInteraction:HandleKeyDownEvent -- 방향키 입력을 받아 해당 방향으로 전기 워프를 실행함
ElectricWarpInteraction:HandleInteractionEvent -- 플레이어가 워프 패드와 상호작용할 때 사용 가능한 방향을 표시하고 워프 모드를 활성화함
ElectricWarpInteraction:HandleInteractionEnterEvent -- 플레이어가 워프 패드 근처에 들어올 때 사용 가이드 UI를 표시함
ElectricWarpInteraction:HandleInteractionLeaveEvent -- 플레이어가 워프 패드에서 벗어날 때 가이드 UI를 제거함
ElectricWarpSwitchInteraction:Switch -- 전기 워프 스위치를 오프에서 온으로 전환하여 워프 라인을 활성화함
ElectricWarpSwitchInteraction:destoryGuideKey -- 사용 가이드 UI를 비활성화하고 숨김
ElectricWarpSwitchInteraction:OnBeginPlay -- 서버에서 가이드 이미지 레퍼런스를 설정
ElectricWarpSwitchInteraction:HandleInteractionEvent -- 스위치와 상호작용 시 스위치를 온으로 전환하여 워프를 활성화함
ElectricWarpSwitchInteraction:HandleInteractionEnterEvent -- 스위치 근처에 들어올 때 가이드 UI를 표시하고 사용법을 알림
ElectricWarpSwitchInteraction:HandleInteractionLeaveEvent -- 스위치에서 벗어날 때 가이드 UI를 숨기고 기본 이미지를 표시
TrapRotatingForward:OnUpdate -- 설정된 회전 속도로 엔티티를 지속적으로 회전시킴
Trap_DeathLightning:OnBeginPlay -- 초기화 시 벢개를 투명하게 설정하고 2.5초 후 발동 가능으로 설정
Trap_DeathLightning:Init -- 초기화 딱지 해제로 전기 데미지 발동 가능 상태로 전환
Trap_DeathLightning:HandleTriggerStayEvent -- 플레이어가 발둥 범위에 머문 때 전기 데미지를 가하고 벢개를 완전히 만듬
Trap_DeathLightning:HandleTriggerLeaveEvent -- 플레이어가 발둥 범위를 벗어날 때 벢개를 다시 투명하게 설정
AbilityIcon:GetAbilityIconRUID -- 능력 이름을 기반으로 해당 능력 아이콘의 RUID를 반환
AbilityIcon:GetAbilityIconRUIDByIndex -- 인덱스를 기반으로 능력 아이콘의 RUID를 반환
AbilityIcon:GetAbilityNameByIndex -- 인덱스를 기반으로 능력 이름을 반환
CustomLocalizationLogic:OnBeginPlay -- 클라이언트 시작 시 다국어 테이블 로드하고 UI 요소들에 다국어 텍스트 적용
CustomLocalizationLogic:ApplyLocalizeOfCommonWordOnUI -- 공통으로 사용되는 UI 요소들(버튼, 메시지 등)에 수동으로 다국어 적용
CustomLocalizationLogic:SendLocalizedToastMessageFromServer -- 서버에서 전달받은 메시지 키로 다국어 토스트 메시지를 표시
CustomLocalizationLogic:SendLocalizedFormattedToastMessageFromServer -- 서버에서 전달받은 메시지 키와 인자들로 포매팅된 다국어 토스트 메시지를 표시
CustomLocalizationLogic:SetInstallationObjectsNametag -- 설치물 엔티티에 소유자와 아이템 타입을 포함한 다국어 네임태그 설정
LeaderBoard:SaveData -- 플레이어의 랜킹 점수(RP)와 닉네임을 데이터베이스에 저장
LeaderBoard:LoadData -- 서버에서 랜킹 데이터를 내림차순으로 로드하고 접속중인 유저들의 랜킹 업데이트
LeaderBoard:OnUpdate -- 매 시가 정각에 랜킹 데이터를 자동으로 업데이트
LeaderBoard:OnBeginPlay -- 서버 시작 시 초기 랜킹 데이터 로드
ParsingLogic:ParseByType -- 문자열 값을 지정된 타입(string, number, boolean)으로 변환하여 반환
ParsingLogic:GetInitValueByType -- 지정된 타입의 기본 초기값을 반환 (string:"", number:0, boolean:false)
ThousandsSeparator:Separate -- 숫자를 3자리마다 쉰표(,)로 구분하여 이해하기 쉬운 형식으로 변환
ThousandsSeparator:ConvertToMetricPrefixString -- 큰 숫자를 지역 설정에 따라 애럥형(만, 억, K, M 등) 문자열로 변환
ThousandsSeparator:Round -- 지정된 단위(유의도)로 숫자를 반올림하여 정확한 값으로 변환
ThousandsSeparator:OldConvertToMetricPrefixString -- 이전 버전의 애럩형 문자열 변환 방식(지역별 단위 지원)
TutorialGuide:PlayGuide -- 특정 인덱스의 튜토리얼 가이드를 재생하고 화면에 표시
TutorialGuide:ShowNextMessage -- 큐에서 다음 메시지를 가져와서 화면에 애니메이션과 함께 출력
TutorialGuide:OnBeginPlay -- 클라이언트 시작 시 튜토리얼 데이터를 초기화하고 저장된 데이터를 로드
TutorialGuide:LoadData -- 유저의 튜토리얼 진행 상태와 조건 데이터를 서버에서 로드
TutorialGuide:SaveData -- 유저의 튜토리얼 진행 상태와 조건 데이터를 서버에 저장
TutorialGuide:OnTableChanged -- 서버에서 받은 테이블 데이터를 클라이언트의 해당 테이블에 적용
TutorialGuide:AddCondition -- 특정 튜토리얼 조건을 추가하고 조건이 만족되면 가이드를 재생
TutorialGuide:HandleButtonClickEvent -- 다음 메시지 버튼 클릭 시 다음 튜토리얼 메시지를 표시
TutorialGuide:HandleButtonClickEvent2 -- 종료 버튼 클릭 시 튜토리얼 종료 후 해당 UI를 열어줌
TutorialGuide:HandleLocalPlayerMapEnterEvent -- 플레이어가 맵에 진입할 때 조건에 따라 해당 튜토리얼을 재생
UIAlarmMarker:SetEnableMarker -- 지정된 UI에 해당하는 알람 마커를 활성화/비활성화하고 메뉴 버튼 마커도 관리
UIAlarmMarker:HandleButtonClickEvent -- 칭호 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIAlarmMarker:HandleButtonClickEvent2 -- 이모티콘 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIAlarmMarker:HandleButtonClickEvent3 -- 유물 도감 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIAlarmMarker:HandleButtonClickEvent4 -- 의자 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIAlarmMarker:HandleButtonClickEvent5 -- 펫 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIAlarmMarker:HandleButtonClickEvent6 -- 공허 아이템 시스템 버튼 클릭 시 해당 알람 마커를 비활성화
UIGetLog:AddLog -- 아이템 획득 로그를 메시지 큐에 추가하고 화면에 애니메이션과 함께 표시
UIGetLog:PrintVoidItemLog -- 공허 아이템 획득 로그를 화면에 애니메이션과 함께 생성하고 표시
UIGetLog:AddLog_Accessory -- 액세서리 획득 로그를 특별한 색상과 스타일로 표시
UIGetLog:PrintLuckAbilityLog -- 행운 능력 발동 로그를 특수 효과와 함께 화면에 표시
UIGetLog:OnBeginPlay -- 클라이언트 시작 시 로그 표시 엔티티들을 초기화하고 대기 상태로 설정
UIGetLog:OnUpdate -- 매 프레임마다 로그 메시지들의 시간을 업데이트하고 페이드 아웃 애니메이션 처리
UIPopup:Open -- 팝업 대화상자를 메시지와 콜백 함수로 열고 등장 애니메이션 시작
UIPopup:OnClickOk -- 확인 버튼 클릭 시 OK 콜백 실행 후 팝업 닫기
UIPopup:OnClickCancel -- 취소 버튼 클릭 시 Cancel 콜백 실행 후 팝업 닫기
UIPopup:Close -- 팝업 대화상자를 닫으며 이벤트 연결 해제과 사라짐 애니메이션 시작
UIPopup:StartTween -- 팝업의 등장/사라짐 애니메이션을 타이머로 처리하여 부드럽게 시전
UIToast:ShowMessage -- 토스트 메시지를 기본 2초 동안 표시하고 애니메이션 시작
UIToast:StartTween -- 지정된 기간동안 토스트 메시지의 등장/사라짐 애니메이션 처리
UIToast:ShowMessageDuration -- 사용자 지정 기간동안 토스트 메시지를 표시하고 애니메이션 시작
TempleExplorerBox:SetTravelerBoxResultUI -- 탐험자 상자 상호작용 결과 UI를 설정하고 얻은 아이템 정보를 표시
TempleExplorerBox:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleExplorerBox:OnInteractionEvent -- 탐험자 상자 상호작용 시 사운드 재생과 무작위 탐험도구 지급 및 UI 표시
TempleExplorerBox:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleExplorerBox:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleExplorerBox:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleFountain:SetTravelerBoxResultUI -- 포션 생성기 상호작용 결과 UI를 설정하고 얻은 포션 정보를 표시
TempleFountain:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleFountain:OnInteractionEvent -- 포션 제조기 상호작용 시 사운드 재생과 고정 포션 지급 및 UI 표시
TempleFountain:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleFountain:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleFountain:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleGemBox:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleGemBox:OnInteractionEvent -- 하데스의 보물상자 상호작용 시 사운드 재생과 서버 로직 호출 및 UI 표시
TempleGemBox:OnInteractionEventOnServer -- 서버에서 보물상자 상호작용 처리: 쿨다운 체크 후 건설 레벨에 따른 젠 지급
TempleGemBox:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleGemBox:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleGemBox:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleGoldstatus:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleGoldstatus:OnInteractionEvent -- 플루투스의 황금지팡이 상호작용 시 사운드 재생과 서버 로직 호출
TempleGoldstatus:OnInteractionEventOnServer -- 서버에서 황금 지팡이 상호작용 처리: 쿨다운 확인, 골드 지급, UI 업데이트
TempleGoldstatus:SetGoldRewardUI -- 황금 지팡이 상호작용 결과 UI를 설정하고 일정 시간 후 비활성화
TempleGoldstatus:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleGoldstatus:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleGoldstatus:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleHarp:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleHarp:OnInteractionEvent -- 아폴론의 하프 상호작용 시 사운드 재생과 기력 회복 및 UI 표시
TempleHarp:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleHarp:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleHarp:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleMinerva:SetTravelerBoxResultUI -- 미네르바의 지혜 상호작용 결과 UI를 설정하고 얻은 포션 정보를 표시
TempleMinerva:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleMinerva:OnInteractionEvent -- 미네르바의 지혜 상호작용 시 사운드 재생과 2-3개의 포션 지급 및 UI 표시
TempleMinerva:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleMinerva:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleMinerva:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TemplePegasus:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TemplePegasus:OnInteractionEvent -- 페가수스 상호작용 시 인벤토리 아이템 체크및 서버 로직 처리
TemplePegasus:OnInteractionEventOnServer -- 서버에서 페가수스 상호작용 처리: 쿨다운 및 사용 횟수 체크후 아이템 판매
TemplePegasus:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TemplePegasus:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TemplePegasus:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
TempleSiren:OnBeginPlay -- 서버 시작 시 상호작용 가능한 가이드 이미지를 초기화
TempleSiren:OnInteractionEvent -- 시렌 상호작용 시 사운드 재생과 기력 회복 및 UI 표시
TempleSiren:HandleInteractionEvent -- 엔티티 상호작용 이벤트 핸들러: OnInteractionEvent 메소드 호출
TempleSiren:HandleInteractionEnterEvent -- 상호작용 영역 진입 시 E키 가이드 UI를 생성하고 표시
TempleSiren:HandleInteractionLeaveEvent -- 상호작용 영역 떠날 때 E키 가이드 UI를 비활성화하고 기본 가이드 이미지 표시
PortalToSpawnInteraction:HandleInteractionEvent -- 플레이어가 포털과 상호작용하면 현재 맵의 스폰 포인트로 순간이동
StarMovement:OnBeginPlay -- 스타의 초기 이동 방향을 랜덤하게 설정
StarMovement:OnUpdate -- 스타를 지정된 영역 내에서 연속적으로 이동시키고 경계에서 방향 전환
StarMovement:HandleInteractionEvent -- 플레이어가 스타와 상호작용했을 때 스타 수집을 처리
StarMovementManager:OnBeginPlay -- 자식 스타들의 랜덤한 색상과 위치를 설정하여 맵 내에서 관리
SwitchButtonUI:HandleButtonClickEvent -- 버튼 클릭 시 대상 UI의 활성화/비활성화 상태를 토글
TrapBallonRope:OnBeginPlay -- 로프의 원래 위치를 저장하여 원상복귀 기준점으로 사용
TrapBallonRope:OnUpdate -- 매달린 플레이어 수에 따라 로프를 위아래로 움직이는 처리
TrapBallonRope:HandleTriggerEnterEvent -- 플레이어가 로프를 타는 상태에서 대상 영역에 진입시 매달린 인원 집계
TrapBallonRope:HandleTriggerLeaveEvent -- 플레이어가 로프 영역에서 나갔을 때의 전용 처리 (현재 비어 있음)
TrapBigRock:OnUpdate -- 바위를 계속 회전시키며 일정 시간마다 사운드 재생
TrapBigRock:OnBeginPlay -- 바위 함정 초기화 및 쿨다운 설정
TrapBigRock:HandleTriggerEnterEvent -- 플레이어가 바위에 접촉시 대미지를 가하고 밀백 속도 제공
TrapBlinkFoothold:OnUpdate -- 플레이어가 올라타을 때 발판이 박명 처리를 하여 경고 효과 제공
TrapBlinkFoothold:OnBeginPlay -- 게임 시작 시 발판 비활성화 타이머 초기화
TrapBlinkFoothold:HandleTriggerLeaveEvent -- 플레이어가 발판에서 떠났을 때 박명 상태 캐셔
TrapBlinkFoothold:HandleTriggerEnterEvent -- 플레이어가 발판에 올라타을 때 단시간 중력 증가후 발판 비활성화 예약
TrapBlinkFoothold:HandleTriggerStayEvent -- 플레이어가 발판 위에 있는 동안 지속적으로 상호작용 상태 유지
TrapBlinkRope:OnUpdate -- 플레이어가 로프에 올라타을 때 로프가 박명 처리를 하여 경고 효과 제공
TrapBlinkRope:HandleTriggerLeaveEvent -- 플레이어가 로프에서 떠났을 때 박명 상태 캐셔
TrapBlinkRope:HandleTriggerEnterEvent -- 플레이어가 로프에 올라타을 때 초 강력한 중력 증가후 로프 비활성화 예약
TrapBlinkRope:HandleTriggerStayEvent -- 플레이어가 로프를 타고 있는 동안 지속적으로 상호작용 상태 유지
TrapCactus:OnUpdate -- 일정 시간 후 선인장 스폰 예약을 위한 쿨타임 처리
TrapCactus:SpawnCactus -- 선인장 스폰 생성 및 일정 시간 후 자동 제거 처리
TrapChaseMobController:OnBeginPlay -- 컴트롤러 초기화 및 신호 버튼 UI 설정
TrapChaseMobController:SetUsed -- 컴트롤러의 사용 상태를 서버에서 동기화
TrapChaseMobController:HandleButtonClickEvent -- 신호 버튼 클릭으로 알파/베타 신호 전환
TrapChaseMobController:HandleButtonClickEvent2 -- 전송 버튼 클릭으로 로봇에게 신호 전송 및 UI 닫기
TrapChaseMobController:HandleInteractionEvent -- 플레이어가 컴트롤러와 상호작용하여 제어 UI 열기
TrapChaseMonster:OnBeginPlay -- 게임 시작 시 랜덤하게 알파 또는 베타 신호로 설정
TrapChaseMonster:Destroy -- 전송받은 신호에 따라 로봇을 정지시키거나 플레이어를 공격
TrapChaseMonster:SendMessage -- 특정 플레이어에게 메시지를 전송하고 사운드 재생
TrapChaseMonster:OnUpdate -- 로봇이 정지된 동안 수리 시간을 표시하고 업데이트
TrapChaseMonster:HandleTriggerEnterEvent -- 플레이어가 로봇 주변에 접근했을 때 대미지를 가하고 쿨타임 적용
TrapControllerLava:OnBeginPlay -- 소화전 이름 설정과 용암 고체화 시각적 이펙트 초기화
TrapControllerLava:OnInteractionEvent -- 소화전 조작 시 용암을 일시적으로 고체화시키고 쿨타임 적용
TrapControllerLava:HandleInteractionEvent -- 인터렉션 이벤트를 받아 소화전 작동 메서드 호출
TrapControllerLava:HandleInteractionEnterEvent -- 소화전에 접근했을 때 가이드 UI를 생성하거나 활성화
TrapControllerLava:HandleInteractionLeaveEvent -- 소화전에서 멀어졌을 때 가이드 UI를 비활성화
TrapDirShooter:OnUpdate -- 일정 시간마다 4방향으로 회전하며 번개 투사체를 발사하는 함정 처리
TrapFillWater:HandleTriggerEnterEvent -- 플레이어가 물에 들어갔을 때 불 상태를 제거하거나 지역별 특수 효과 적용
TrapFillWater:HandleTriggerLeaveEvent -- 플레이어가 물에서 나왔을 때 기존 타이머를 정리하고 상태 초기화
TrapFireParabola:OnBeginPlay -- 필터 효과와 사운드 ID를 초기화
TrapFireParabola:HandleTriggerEnterEvent -- 플레이어가 화염 투사체에 닿았을 때 대미지와 효과 적용 후 투사체 파괴
TrapFireParabola:HandleFootholdCollisionEvent -- 투사체가 바닥이나 다른 오브젝트에 쉦았을 때 즉시 파괴
TrapGasLava:OnUpdate -- 2초간 가스 분출 후 2초 휴식을 반복하는 사이클 처리
TrapGasLava:HandleTriggerEnterEvent -- 플레이어가 가스 용암에 닿았을 때 공격 가능 상태이면 대미지와 밀백 효과
TrapGreatRock:ControlAngle -- 발사각도를 좌우로 조절하고 범위를 제한
TrapGreatRock:Shoot -- 현재 설정된 각도로 바위 투사체를 발사
TrapGreatRock:Shift -- 플레이어의 바라보는 방향에 따라 UI와 발사 방향을 전환
TrapGreatRock:HandleKeyDownEvent -- 키보드 입력으로 발사각도 조절과 발사를 처리
TrapGreatRock:HandleKeyHoldEvent -- 키를 지속적으로 누르고 있을 때 각도를 연속적으로 조절
TrapGreatRock:HandleChangedLookAtEvent -- 플레이어가 바라보는 방향이 바뀔 때 UI를 동기화
TrapGreatRock:HandleTriggerEnterEvent -- 플레이어가 대포에 접근했을 때 조종 모드를 활성화
TrapGreatRockUI:HandleKeyDownEvent -- 키보드 입력을 위한 핸들러 (현재 구현되지 않음)
TrapGuidedMissile:OnBeginPlay -- 유도 미사일의 대상을 로컬 플레이어로 설정
TrapGuidedMissile:OnUpdate -- 타겟과의 거리를 계산하고 사정 내에 있으면 유도 이동 수행
TrapIceFall:OnUpdate -- 떨어지는 상태일 때 매 프레임마다 떨어지는 로직 실행
TrapIceFall:Falling -- 고드름을 아래로 떨어뜨리고 5초 후에 소멸시킴
TrapIceFallSensor:OnUpdate -- 타이머를 감소시키고 0에 도달하면 고드름 경고 모델을 생성
TrapIceFallSensor:SpawnCautionModel -- 고드름 떨어지는 위역에 경고 모델을 생성하고 위치적 사운드 재생
TrapInteractionRock:ControlAngle -- 바위 발사 각도를 제어하고 UI 화살표 방향을 업데이트
TrapInteractionRock:Shoot -- 설정된 각도와 방향으로 바위를 발사하고 플레이어 제어를 복원
TrapLava:OnUpdate -- 용암 발사체인 경우 3초마다 용암 탄을 발사하도록 관리
TrapLava:HandleTriggerEnterEvent -- 용암에 들어갔을 때 화상 스택을 초기에 적용하고 지속 데미지 타이머 시작
TrapLava:HandleTriggerLeaveEvent -- 용암에서 나갔을 때 실행 중인 모든 지속 데미지 타이머를 정지
TrapLavaProjectile:MoveUp -- 용암 탄을 년물선 깄지로 위로 발사하고 일정 시간 후 비활성화
TrapLavaProjectile:OnBeginPlay -- 유적지에서만 데미지 상향 조정 (주석 처리된 상태)
TrapMagnetFieldMaker:Attack -- 자기장 공격을 실행하며 이팩트와 사운드 재생, 플레이어에게 데미지와 넷백 적용
TrapMagnetFieldMaker:OnBeginPlay -- 게임 시작 시 쿨다운을 초기화하고 공격 시작
TrapMagnetFieldMaker:Start -- 쿨다운 타이머를 시작하고 공격 예고 및 실행을 반복 수행
TrapMagnetFieldMaker:OnSyncProperty -- 쿨다운 시간이 동기화될 때 카운트다운 텍스트 UI 업데이트
TrapMagnetFieldMaker:HandleTriggerLeaveEvent -- 플레이어가 충돌 영역에서 나갔을 때 트리거 상태를 해제
TrapMagnetFieldMaker:HandleTriggerEnterEvent -- 플레이어가 충돌 영역에 들어왔을 때 트리거 상태를 활성화
TrapMagneticField:OnUpdate -- 자기장 트랩의 쿨다운 상태를 관리하고 범위/경보/공격 UI를 전환
TrapMagneticField:Attack -- 자기장 내에 플레이어가 있을 때 전기 데미지와 넛백을 적용
TrapMagneticField:HandleTriggerStayEvent -- 플레이어가 자기장 내에 머물러 있는 동안 트리거 상태 유지
TrapMagneticField:HandleTriggerLeaveEvent -- 플레이어가 자기장 영역에서 나갔을 때 트리거 상태를 해제
TrapPoison:OnUpdate -- 독 트랩에 들어있는 동안 지속적으로 독 데미지를 적용
TrapRotateBar:OnUpdate -- 회전 막대의 각도를 일정 속도로 왕복 회전시키는 업데이트 로직
TrapRotateBar:HandleTriggerEnterEvent -- 플레이어에게 데미지와 화상 스택을 적용하고 사다리/로프 상태를 중단
Trap_Electric:OnUpdate -- 공격 쿼다운을 업데이트하여 0 이하로 떨어지지 않도록 제한