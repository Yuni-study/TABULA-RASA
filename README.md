  ## * 주의 *
  현재 프로젝트는 유료 에셋을 제외한 포트폴리오용 레퍼지토리 이므로 유니티 내부에서 플레이는 불가합니다!
  플레이 하시려면 아래에 링크를 참조해주세요!

  게임 플레이 하러 가기 [Google Drive](https://drive.google.com/drive/folders/1QxzHXSrusEX_jaqvbvi0E0EIKgHbYkzh)
  
# <i>게임 제목: TABULA RASA</i>
<img width="700" height="600" alt="1" src="https://github.com/user-attachments/assets/05309864-0964-4af1-ac9b-8d05c379f74c" />


## 목차
- [프로젝트 소개](#-프로젝트-소개)
- [팀원 소개](#-팀원-소개)
- [게임 화면](#-게임-화면)
- [게임 조작 방법](#-게임-조작-방법)
- [사용 기술](#-사용-기술)
- [기술 구현](#-기술-구현)
- [트러블 슈팅](#-트러블-슈팅)

<br>

---

## 🎮 프로젝트 소개
**『타불라 라사』**는 유령인 주인공이 월드를 탐사하며 각기 다른 특징을 가진 빙의체들을 이용하여 퍼즐을 해결하는 어드벤처 게임입니다. 

- 장르: 어드벤처 

- 플랫폼: PC (Windows)

- 개발 툴: Unity 2022.3.17f1, Visual Studio, GitHub, Git Fork, GitHub Desktop, Excel

- 개발 기간: 2025.09.09 ~


## 🚀 팀원 소개
| 이름 (역할) | 담당 업무 | GitHub |
| :--- | :--- | :--- |
| **이서연 (기획 팀장)** | <ul><li>UX 디자인</li><li>스토리 디자인</li><li>시스템 기획</li></ul> | [Github](https://github.com/Isillith) | 
| **이원혁 (기획)** | <ul><li>UI 디자인</li><li>퍼즐/시스템 기획</li></ul> | [Github](https://github.com/lwh991229-glitch) | 
| **정세윤 (개발 팀장)** | <ul><li>게임 매니저</li><li>데이터 매니저</li><li>개발 PM</li></ul> | [Github](https://github.com/SeYunJung) |
| **김용민 (개발)** | <ul><li>플레이어 총괄</li><li>데이터 테이블 구현/설계</li><li>인벤토리 로직 구현</li></ul> | [Github](https://github.com/Nokddu) |
| **주의동 (개발)** | <ul><li>UI 총괄</li><li>인벤토리 로직 구현</li><li>씬 매니저 구현</li></ul> | [Github](https://github.com/Winebug) |
| **조지현 (개발)** | <ul><li>데이터 디자이너</li><li>게임 매니저 보조</li><li>UI 보조</li></ul> | [Github](https://github.com/jo-ji-hyun) |



## 🖼️ 게임 화면
<img width="600" alt="2" src="https://github.com/user-attachments/assets/b04972e7-c71d-4cdf-9ab1-0b2abc0feef1" />
<img width="600" alt="3" src="https://github.com/user-attachments/assets/540c4396-0bff-40af-a5e9-3dda63e2b440" />
<img width="600" alt="4" src="https://github.com/user-attachments/assets/1610841d-222a-4154-9951-28d03ac0f860" />


## 🕹️ 게임 조작 방법
1. **이동 조작**: WASD 또는 방향키
2개 이상의 키 입력 가능 (8방향 이동)
    - 이동 상세
        - 이동 정지 조건
            - 키보드 방향키를 입력 하지 않은 경우 정지
        - 동일 축 동시 입력 시
            - (↑ + ↓ 또는 ← + →) 누른 경우 → **마지막 입력한 방향 기준으로 이동**
                - ***동시 입력한 경우 멈추지 말고 누른 곳중 랜덤으로 이동***
        - 우선 입력 조건
            - 같은 축 (위 + 아래 / 오른쪽 + 왼쪽) 방향키 입력 시 마지막으로 누른 방향으로 기체가 이동하도록 함 (ex 위로 가다가 아래 아래 버튼 누르면 아래로 이동)
        - 대각선 이동
            - **동일 축이 아닌 서로 다른 축 (예: ↑ + →)** 동시 입력 시
            - 기본값은 이동 가능하며, playerinfo.table → allow_diagonal 로 제어
                - (ture : 이동 가능 /  false : 이동불가능)
            - 이동속도 n초 만큼 이동 (playerinfo.table → allow_diagonal_movespeed)

1. **상호작용 조작**: 키 + 마우스 포인터
    
    마우스 포인터 레퍼런스 게임: **디스코 엘리시움**
    

**모든 키 입력표**

| W | 위로 이동 | F | 아이템 획득 |
| --- | --- | --- | --- |
| A | 왼쪽으로 이동 | Q | 빙의 / 이탈 |
| S | 아래로 이동 | E | 상호작용 |
| D | 오른쪽으로 이동 | R | 아이템 회전 |
| Tab | 인벤토리 여닫음 | Esc | 메인 메뉴 여닫음 |


## 🛠 사용 기술
- Unity 2022.3 LTS
- C# (게임 로직 및 시스템 구현)
- GitHub, GitHub Desktop, Git Fork (버전 관리)
- TextMeshPro (UI 시스템 구성)
- ScriptableObject (아이템 데이터 관리)
- Newtonsoft Json (데이터 저장)
- ExcelToJson (데이터테이블 관리)
- FSM (플레이어)
- Singleton (각 매니저들)
- MVC (인벤토리)
- Post-Processing (효과 연출)
- Object Pooling (오브젝트 재사용)
- CineMachine (카메라 연출)
  
## ✨ 기술 구현 
### FSM + 상태패턴 
FSM과 상태패턴을 이용해 플레이어의 상태를 구현 
<img width="3498" height="2416" alt="5" src="https://github.com/user-attachments/assets/3919f7a4-e060-4557-aa9b-65c6b680cfe8" />


### 인벤토리
드래그 앤 드롭 방식의 그리드(격자) 인벤토리 구현 
교환 가능한 인벤토리 구현
<img width="512" height="650" alt="6" src="https://github.com/user-attachments/assets/af1d4c28-15e6-4f73-8d88-c5e933982220" />


### 데이터
Excel을 SO형식으로 바꾸어 게임내에 사용할 많은 데이터를 관리
<img width="1310" height="309" alt="7" src="https://github.com/user-attachments/assets/b23e1200-2062-4cef-b2c7-73603f9d751b" />

-> 원본의 SO를 DataManager에서 복사본을 만들어 사용하도록 만들어 기존의 데이터는 변형을 피하고 데이터를 가지고 오도록 만듦.

### 데이터테이블
구분하기 쉽게 Class 단위로 데이터를 나눔.
<img width="1143" height="614" alt="8" src="https://github.com/user-attachments/assets/74cbda80-6890-4656-90e2-30b03fc826b2" />


### 매니저 
- 리소스 매니저
게임에서 사용되는 오브젝트, 사운드 클립들을 생성, 반환

- 씬 로드 매니저
씬의 흐름을 관리해줄 중간 관리자

- **게임 전반에 걸쳐 유일하게 필요한 매니저**만 제너릭 싱글톤으로 게임 구조를 설계함.

## 🧠 트러블 슈팅 
### 상태 관리 구조 개선
- **Before**: 형태(Form)와 행동(Action)을 통합한 단일 FSM으로 인해 상태 수가 급증하고 유지보수가 어려웠습니다.
- **After**: **이중 FSM(Dual FSM)** 구조를 도입하여 형태와 행동을 분리, 확장성과 재사용성을 확보했습니다.

### 데이터 관리 효율화
- **Before**: 게임 데이터가 코드에 흩어져 있어 수정 및 관리가 비효율적이었습니다.
- **After**: **Excel to JSON/Scriptable Object** 파이프라인을 구축하여 데이터를 외부에서 체계적으로 관리하고 쉽게 게임에 적용할 수 있도록 개선했습니다.

### 데이터 로딩 최적화
- **Before**: 씬 로드 시 모든 NPC 데이터를 한 번에 로드하여 불필요한 리소스 낭비가 있었습니다.
- **After**: 구역 식별자(**`AreaIndex`**)를 사용하여 **현재 구역에 필요한 데이터만** 불러오도록 로직을 변경, 메모리 효율성을 높였습니다.

### 드래그 중 실시간 아이템 회전
- **Before**: 아이템을 한번 들면 회전시킬 수 없어, 다시 내려놓고 회전시킨 후 집어야 하는 불편함이 있었습니다.
- **After**: 드래그 상태에서 'R' 키 입력 시 아이템의 데이터(가로/세로 값)와 시각적 이미지가 실시간으로 회전하도록 구현하여, 직관적인 '테트리스' 방식의 조작이 가능해졌습니다.

### 다중 인벤토리 간 아이템 교환
- **Before**: 시스템이 단일 인벤토리만 가정하고 설계되어, 2개의 인벤토리가 열렸을 때 아이템을 옮기면 어느 쪽으로 들어가야 할지 판단할 수 없었습니다.
- **After**: `InventoryManager`가 열려있는 모든 인벤토리를 관리하도록 변경했습니다. 아이템 드롭 시 마우스 위치를 감지해 타겟 인벤토리를 정확히 찾아내고, 두 인벤토리 간의 데이터 교환을 중재하도록 하여 안정성을 높였습니다.

---
