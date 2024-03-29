# **Space Rocket Delivery**
## 팀 이름: **우리가 고티라고 생각하면 그게 고티 아닐까?**
## 팀원 목록 및 역할:
- 윤도현 (팀장, 클라이언트)
- 서우린 (서버)
- 박준표 (클라이언트)
- 이상훈 (클라이언트)
- 권용진 (클라이언트, 서버)
- 김희제 (클라이언트, 서버)

---
## **기획 의도**

개인 방송 플랫폼과 커뮤니케이션 앱의 보편화로 게임 내에서 얻을 수 있는 재미 뿐만 아니라 타인과 함께 즐기는 재미도 중요해졌다. 그러므로 협동 플레이 요소와 타일 생성이라는 자유도를 통해 게임의 본연의 재미와 소통 및 협동의 재미를 제공하는 게임을 만들고자 한다.


---

## **발표자료 및 빌드 파일 노션 링크**

https://www.notion.so/031a0972917349e299f5c3959bf5040c

<br>

## **기능명세서 링크**

https://www.notion.so/4f61b6d63b34422588bcea33a6a7eb1d

---

# **프로젝트 2주차**

### 게임의 기반이 되는 기능들을 학습하고 구현해보는 것을 목표로 하였다.

---
## **클라이언트**

<br>

### **캐릭터 및 캐릭터 애니메이션 구현**
![캐릭터](/images/character.png)

원하는 캐릭터 모습이 있는 유니티 에셋을 불러온 후 앞뒤, 좌우 움직임에 대한 애니메이션과 물체를 들어올리는 애니메이션을 구현하였다. <br>
캐릭터의 방향이 바뀔 때 몸체를 회전하는 속도를 지정해주어 어떤 느낌으로 방향을 전환할 지 정할 수 있었다.
<br>
<br>

### **우주선의 움직임 표현 구현**
![우주선](/images/spaceship_background.png)
우주선이 움직이는 것이 아니라 배경이 움직임으로써 우주선의 움직임을 표현하였다.<br>
하위 오브젝트의 좌표값은 상위 게임 오브젝트에 대해 상대적으로 표현된 값임을 알게 되었다.<br>
우주선의 방향이 바뀜을 표현하기 위해 배경이 방향을 틀어서 움직이는 것을 구현하였다. 이 때 방향 벡터는 우주선을 기준으로 z축의 -(마이너스)방향으로 설정해주어야만 했다.
<br>
<br>

### **캐릭터 상호작용에 따른 타일의 추가 생성**
![타일생성](/images/character_tiles.png)
캐릭터가 타일의 벽면 쪽으로 가까이 가게되면 새롭게 타일을 생성할 수 있는 청사도가 보여야 한다. <br>
미리 21x21의 타일을 깔아 둔 후, 중앙의 3x3 타일을 제외하곤 모두 투명한 상태로 둔다. 타일을 생성하고자 하는 방향의 벽면에 다가가면 충돌을 감지하여 생성가능한 타일의 투명한 상태를 해제하여 생성가능함을 보여준다. 유저가 생성버튼을 누를 경우 리소스 폴더에 있는 프리팹을 불러와서 생성한다.
<br>

---

## **서버**
포톤 서버와 같은 기존 프레임워크를 사용하지 않고 딜레이를 줄이기 위해 직접 서버를 구축하기 위해 학습중


---
## **공통**
![SCM](/images/plastic_SCM.png)
프로젝트의 상태관리를 위해 plastic SCM 리포지토리를 만든 후 6명 모두 참여되었다.

---

### **차주 목표**
- 우주선 형태의 디테일화
- 배경의 디테일화
- 모듈 및 타일과의 상호작용 구현
- UI/UX 디자인
- 적의 생성과 움직임 구현
- 서버 프로토 타입 생성


---

<br>

<br>

# **프로젝트 3주차**

### 각자 맡은 기초적인 기능들을 구현한 후 빌드하여 발표까지 진행하였다.


---
## **클라이언트**
<br>

### **보급기 및 산소발생기 모듈 구현**
보급기에서 지속적으로 자원이 생성 가능하다.<br>
플레이어가 보급기에 접근하여 SPACE 키를 누르는 것으로 생성되는 자원을 바꿀 수 있다.

![보급기](/images/보급기.PNG)
<br>
보급기에서 연료가 생성되는 상태이다.

![보급기2](/images/보급기2.PNG)
<br>
보급기에서 광물이 생성되는 상태이다.

![산소발생기](/images/산소발생기.PNG)
<br>
산소발생기 <br>
지속적으로 관리하지 않으면 고장나고, 고장날 경우 산소가 공급되지 않아 게임오버가 된다.
<br>
<br>

### **캐릭터 상호작용으로 타일 생성 구현**
![타일생성](/images/타일생성.gif)
우주선 외곽에 플레이어가 다가가면 설치할 수 있는 타일의 청사도가 보이고 SPACE를 눌러서 타일을 설치할 수 있다.

<br>
<br>

### **우주선 움직인 구현 및 게임 배경 제작**
![게임배경1](/images/게임배경1.PNG)

<br>

![게임배경2](/images/게임배경2.PNG)

구매한 에셋과 제공된 에셋들을 조합하여 난파된 배들과 소행성 지역들을 구현하였다.

몇 가지 방법으로 우주선이 움직이는 것을 표현하였다.
- 배경이 정해진 좌표 값을 기준으로 움직임을 바꾸는 방법
- 우주선이 정해진 좌표 값을 기준으로 움직임을 바꾸는 방법
- 웨이포인트를 정해둔 후 우주선이 웨이포인트까지 가는 방법
- 웨이포인트를 정해둔 후 배경이 웨이포인트까지 가는 방법
- Bézier Path Creator 에셋으로 경로를 만들고 우주선이 그 경로를 따라가는 방법

현재 Bézier Path Creator로 우주선의 움직임을 구현하였으나 다른 팀원과의 Merge 후 오류가 생기고 움직임이 자연스럽지 않아서 배경이 Bézier Path를 따라 움직이는 것으로 변경 중에 있다.

![우주선움직임](/images/우주선움직임.gif)

<br>
<br>

### **적 생성 구현 및 적 근접 충돌 구현**
우주선 주위에 적들이 생성되고, 생성된 적들이 우주선을 향해 돌진하여 공격하는 방식으로 구현하였다. <br>
우주선과 충돌할 경우 우주선은 데미지를 입으며 충돌한 적은 사라진다. <br>
적의 에셋은 새롭게 설정할 예정이며 데미지 계산은 아직 진행되지 않았다. <br>
충돌시 흔들림 효과가 생성되도록 하였다.

![적공격](/images/적공격.gif)


### **빌드 테스트**

유니티 기능을 이용하여 빠르게 빌드해볼 수 있었다. <br>
**문서 위의 빌드 링크 확인**

---

## **서버**
레퍼런스와 교재를 활용하여 서버 구축을 학습하였다.
다음 주 내로 서버의 프로토타입을 만들어 테스트해 볼 예정이다. 


---

### **차주 목표**
- 구현되지 않은 모듈의 추가 구현
- 서버 프로토타입 통신 테스트
- UI/UX 디자인
- 모듈별 기능 구현
- 원거리 공격 적의 구현

---
<br>
<br>

# **프로젝트 4주차**

### 각자 맡은 부분의 심화 기능들을 구현하였다.

---
## **클라이언트**
<br>

### **레이저 포탑 회전 및 공격 구현**

레이저 포탑이 실시간으로 가장 가까이에 있는 적을 찾아내어 공격한다. <br>
레이저 포탑의 포탑 회전 속도와 각도를 지정하여 특정 회전 속도로 회전하되, x축과 y축 기준으로는 특정 회전 각도 이상 회전하지 못하도록 만들었다.


![레이저포탑](/images/레이저공격.gif)

<br>

### **적의 공격**

근거리 공격을 하는 적은 우주선에 닿게 되면 충돌하여 데미지를 준다. <br>
원거리 공격을 하는 적은 우주선에서 일정 거리를 둔 후 투사체를 날려서 공격을 한다.
공격 받은 타일은 불이 나는 이펙트가 난다.


![적_요격](/images/적_요격.gif)

<br>

### **기본포탑**

플레이어가 직접 조종할 수 있는 포탑으로 기능은 구현 중에 있다.

![기본포탑](/images/기본포탑.PNG)

<br>

### **보급기**

보급기 모듈의 디자인이 변경되었다. 
자원이 생설될 때 앞에 달린 문이 열린다.

![보급기](/images/new_보급기.PNG)

<br>

### **제작기**

기존의 보급기 디자인이 제작기의 디자인이 되었다.
생산을 위해 필요한 자원과 이미 들어가있는 자원이 표시된다.

![제작기](/images/new_제작기.PNG)

<br>

---

## **서버**
서버 프로토타입이 완성되었고 클라이언트와 통신을 확인하였다.

![서버통신](/images/서버.png)

현재 클라이언트인 C#과 서버인 C++의 데이터가 직렬화, 역직렬화 과정을 거칠 때 데이터가 올바르게 전달되고 있는지 확인 중에 있다.


<br>

서버에서 처리해주어야하는 로직에 대한 API를 작성 중에 있다.

https://www.notion.so/API-0ec863edf3de45b8a43d7685e700c09b


---

### **차주 목표**
- 모든 포탑의 기능 구현
- UI/UX 구현
- 서버에 데이터를 전달할 API 구현
- 게임매니저 스크립트 작성 및 정리 (게임의 시작과 끝까지 진행되는 방법)
