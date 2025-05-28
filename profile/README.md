![image](https://github.com/user-attachments/assets/847ea062-8792-4f46-a8a6-50eb44ef1421)- 목차
  - [장르](#장르--3d-타워-디펜스)
  - [스토리](#스토리)
  - [개발 타임라인](#개발-타임라인)
  - [기술적인 도전 과제](#기술적인-도전-과제)
  - [사용된 기술 스택](#사용된-기술-스택)
  - [씬 구조](#씬-구조)
  - [MVP 기능구현](#mvp-기능구현)
  - [트러블 슈팅](#트러블-슈팅)
  - [사용자 개선 사항](#사용자-개선-사항)
  - [팀원 구성 및 연락처](#팀원-구성-및-연락처)

![슬라이드2](https://github.com/user-attachments/assets/6b0f8a31-c8ec-4104-8a1c-0c608c92ab0a)

## ✨장르 : 3D 타워 디펜스

- **3D 캐주얼 판타지 스타일의 드래곤 합성 디펜스 게임**
- **랜덤으로 등장하는 드래곤을 배치·합성·강화해 적의 웨이브를 막아내는 전략 중심 플레이**
- **속성 간 상성과 보스 웨이브, 제한된 자원 속 선택과 판단의 재미**
- **불, 물, 바위, 풀, 빛 다섯 속성이 각각 고유한 전투 능력을 지님**
- **빠른 판단과 배치로 몰려오는 적을 처치하며 긴장감 넘치는 생존 전투!**

## ✨스토리
```
수 많은 적들을 막기 위해 드래곤을 소환하라!

다음에 어떤 드래곤이 소환될지 알 수 없다…
예측할 수 없는 전장에서 살아남는 방법은 단 하나..!
순간의 선택과 합성, 그리고 속성 간 상성을 완벽히 활용하는 것!

끝이 보이지 않는 웨이브 속,

살아남을 수 있을 것인가?
```

## ✨개발 타임라인

- **개발기간:  `2024.0**4. 05 ~ 2024.05.21`

- **타임라인**
    | 주차 | 요약 | 설명 |
    | --- | --- | --- |
    | **1주차** | 기획 / S.A 작성 | - 어떤 게임을 개발할 건지 주제 선정 (레퍼런스) - 주요 메카닉, 게임 사이클 확정 - 개발 착수 |
    | **2주차** | 주요 메카닉 구현 | - 버그 픽스- 디버깅 |
    | **3주차** | 추가 기능 구현 | - 게임씬 구현 |
    | **4주차** | 추가 기능 구현 | - 특수 기능 구현 |
    | **5주차** | 게임 폴리싱 로비씬 제작 | - 로비씬 제작 및 게임 플로우 정립 |
    | **6주차** | 배포 시도 User Test | - 유저테스트 진행 - 안드로이드/iOS/웹 배포 시작 - 버그픽스 - 최적화 |
    | **7주차** | 게임 포장하기 User Test | - 유저테스트 진행- 최적화 |
    | **8주차** | 프로젝트 정리 발표 준비 | - 개발 마무리 - 포트폴리오 정리 |

## ✨기술적인 도전 과제
<details>
  <summary><b>Realtime DataBase</b></summary>
    <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>원래 <strong>ScriptableObject</strong>를 통해 데이터 관리를 하고 있었으나, 기획자가 밸런싱 작업을 하기에는 부적합하다는 의견이 있어 데이터 테이블 연결을 고려하게 됨</li>
        <li><strong>확장성과 보안을 생각</strong>해 <code>파이어 베이스</code>를 메인으로 삼되, <strong>기획자와의 원활한 협업을 위해</strong> 데이터 테이블을 작성은 <code>구글 스프레드시트</code>를 이용하기로 결정</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>구글 스프레드 시트를 통해 데이터를 한 곳에서 관리할 수 있게 됨<br>→ 기획자와의 협업이 용이</li>
        <li>서버에서 게임 데이터를 받아오게 됨<br>→ 데이터 수정 / 버전 관리 용이<br>→ 빌드 이후에도 데이터 수정이 가능해짐</li>
      </ul>
    </li>
    <li><strong>이미지 :</strong></li>
      <img src="https://github.com/user-attachments/assets/253084b0-1e38-46ef-a783-ea6c04b36eab" alt="image">
  </ul>
</details>

<details>
  <summary><b>애널리틱스</b></summary>
  <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>따로 설문조사를 하지 않아도 유저가 어떤 상황에서 어떤 선택을 하는지 알 수 있다면 추후 개발할 때 도움이 될 것 같아 기능 추가를 결심</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>해당 기능을 통해 유저가 어떤 선택을 선호하고, 어떤 구간을 어려워 하는지 알 수 있게 됨 → 데이터 분석을 통해 유저가 선호할 수 있는 방향을 미리 알 수 있게 됨.</li>
      </ul>
    </li>
    <li><strong>이미지 :</strong></li>
      <img src="https://github.com/user-attachments/assets/57bfe642-997d-4880-bbf9-54953d0d81ab" alt="image">
  </ul>
</details>

<details>
  <summary><b>구글 로그인</b></summary>
  <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>BM 적용을 고려하려면 로그인 기능이 필요했음</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>유저 개개인의 데이터를 수집할 수 있게 됨</li>
        <li>별다른 회원가입 절차 없이 기존 구글 플레이 게임즈 계정을 통해 로그인 기능을 사용할 수 있게 됨</li>
        <li>추후 친구 찾기/추가 기능, 도전과제 기능을 추가하게 된다면 구글 플레이 게임즈를 이용해 구현할 수 있게 됨</li>
      </ul>
    </li>
    <li><strong>이미지 : (추후 추가) (인게임 로그인 장면 캡쳐)</strong></li>
  </ul>
</details>

<details>
  <summary><b>로컬라이징</b></summary>
  <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>글로벌 시장에 대비해 영어 서비스를 우선적으로 추가하였으며, 이를 통해 다국어 지원을 위한 기반을 마련.</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>테이블 중심의 설계를 통해 다국어 데이터 관리가 보다 체계화되었으며,
    향후 다른 언어를 추가하거나 수정할 때 유지보수가 편리해짐.</li>
      </ul>
    </li>
    <li><strong>이미지 :</strong></li>
      <img src="https://github.com/user-attachments/assets/73bbeb52-5b71-41c0-aa57-32fd1e9695e7" alt="image">
  </ul>
</details>

<details>
  <summary><b>어드레서블</b></summary>
  <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>프로젝트에 사용하는 리소스가 많아짐에 따라 앱 용량이 커졌고, 이로 인해 사용자가 다운로드 중 이탈하는 문제가 발생할 우려가 있었음.</li>
        <li>이를 방지하고자 앱에 리소스를 직접 포함하지 않고 서버에서 필요한 리소스를 받아오는 방식으로 전환하여 앱 용량을 주임</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>구글 플레이 스토어 내부 테스트 기준 앱 용량 `193 MB → 53.8MB` 로 약 `72%` 감소</li>
      </ul>
    </li>
    <li><strong>이미지 :</strong></li>
      <img src="https://github.com/user-attachments/assets/58c99b4c-54c1-4403-8053-76ac421c605b" alt="image">
  </ul>
</details>

<details>
  <summary><b>오브젝트풀링_팩토리 패턴</b></summary>
  <ul>
    <li><strong>도입배경 :</strong>
      <ul>
        <li>GC를 줄이기 위해서 풀링 시스템 도입</li>
        <li>풀링 도입 시 다양한 오브젝트 생성 시 각기 다른 컴포넌트 초기화 문제 발생 / 풀링 로직을 최소화 필요</li>
      </ul>
    </li>
    <li><strong>개선사항 :</strong>
      <ul>
        <li>풀링은 인터페이스 타입만 가지고있고, 생성은 펙토리를 통해 진행함</li>
        <li>생성과 초기화는 펙토리에서 진행하기 때문에 오브젝트 별 고유한 데이터 초기화 문제를 해결 가능</li>
        <li>풀링과 오브젝트 생성/초기화 로직을 분리 가능</li>
      </ul>
    </li>
    <li><strong>이미지 :</strong></li>
      <img src="https://github.com/user-attachments/assets/3458f9de-9edd-4dcd-9cbe-575cc07466aa" alt="image">
  </ul>
</details>

## ✨사용된 기술 스택

- FireBase
- Google Cloud
- Google Sheet
- Unity
- C#
- Github

## ✨씬 구조
<details>
  <summary><b>🔆 게임 사이클 - 플로우차트</b></summary>
  <img src="https://github.com/user-attachments/assets/b94ca53e-de1a-45de-96a0-ce84bfc3d780" alt="image">
</details>

### 씬 미리보기
<details>
  <summary><b>🔆 1. 데이터 씬</b></summary>
  <img src="https://github.com/user-attachments/assets/9024f558-3d7b-4bf4-a616-3d76e5d679b3" alt="image">
  <p>데이터 불러오기 완료 후 화면 터치를 통해 게임에 입장할 수 있습니다.</p>
</details>
<details>
  <summary><b>🔆 2. 로비</b></summary>
  <p>로비에는 가이드 , 플레이, 설정 버튼이 있습니다</p>
  <img src="https://github.com/user-attachments/assets/74e0470d-16f4-401d-88fa-9428e6c41ff1" alt="image">

  <ul>
    <li>모드 선택
      <ul>
        <li>플레이 버튼을 누르면 모드를 선택할 수 있습니다</li>
        <li>현재 플레이 가능한 모드는 싱글 플레이 - 쉬움과 어려움 난이도 입니다.</li>
      </ul>
    </li>
  </ul>
  <img src="https://github.com/user-attachments/assets/e3dd9dbb-87f1-4a9e-83b5-50329c07761b" alt="image">

  <ul>
  <li>가이드
    <ul>
      <li>가이드 버튼을 누르면 게임에 관련한 전반적인 설명을 볼 수 있습니다. </li>
    </ul>
  </li>
</ul>
  <img src="https://github.com/user-attachments/assets/2c152367-1a5e-40c6-8789-47fb59d3d8f3" alt="image">
</details>
<details>
  <summary><b>🔆 인게임</b></summary>
  <p>게임은 총 40라운드로 진행됩니다.</p>
  <p>10라운드마다 보스가 등장합니다</p>
  <img src="https://github.com/user-attachments/assets/9df1ec4e-7fa9-4dcb-b08f-1f214a5aee8c" alt="image">

  <p>드래곤을 설치하고 합성하고 강화하여 몬스터를 물리치세요!</p>
  <p>게임이 끝나거나 우측 상단의 버튼을 통해 다시 로비로 돌아갈 수 있습니다.</p>
  <img src="https://github.com/user-attachments/assets/f274c27e-acb2-4078-b8c2-89f9c868ce9d" alt="image">
</details>

## ✨MVP 기능구현
<details>
  <summary><b>🐲 타워</b></summary>
  <h3><b>⭐ 재미요소</b></h3>
  <ul>
    <li>타워 랜덤생성</li>
    <img src="https://github.com/user-attachments/assets/d548abb0-4871-4947-b626-1904fb0db384" alt="image">
  </ul>
  <ul>
    <li>타워 합성</li>
    <img src="https://github.com/user-attachments/assets/7d42b668-3720-408d-b8a2-19de7e60c7ac" alt="image">
  </ul>
  <ul>
    <li>상성</li>
    <img src="https://github.com/user-attachments/assets/4e7bf342-6b9f-4a57-94d0-23c452d3a8ad" alt="image">
  </ul>
  <h3><b>🔔 기능</b></h3>
  <ul>
    <li><b>타일 클릭 시 사거리 & 정보 표시</b></li>
    <li>타일 클릭 시 상태에 따라 타워 생성 UI 또는 타워의 정보 시각화 기능 실행</li>
    <li>IPointerClickHandler 인터페이스를 통해 타일 클릭 이벤트 감지</li>
    <img src="https://github.com/user-attachments/assets/973613f7-fc58-4c8b-84f1-05af6a794f76" alt="image">
    <img src="https://github.com/user-attachments/assets/4d5d7467-baa3-494b-a1ef-d5b84562ef95" alt="image">
  </ul>
  <ul>
    <li><b>Drag & Drop , 타워 합성 & 판매</b></li>
    <li>마우스 위치에 따라 타워가 이동하도록 구현</li>
    <img src="https://github.com/user-attachments/assets/1c055067-79d7-4634-8af8-cf162da85cd6" alt="image">
    <img src="https://github.com/user-attachments/assets/d348a680-beea-4122-8c2d-36f896e1341f" alt="image">
  </ul>
  <ul>
    <li><b>티어에 따른 외형 / 이펙트 차이 </b></li>
    <img src="https://github.com/user-attachments/assets/f845fdd9-7a18-4205-a8aa-f1e8eca4a257" alt="image">
  </ul>
</details>

<details>
  <summary><b>👾 스테이지 / 몬스터</b></summary>
  <h3><b>⭐ 재미요소</b></h3>
</details>

<details>
  <summary><b>📱 UI</b></summary>
</details>

<details>
  <summary><b>🗨️ 로컬라이징</b></summary>
</details>

## ✨트러블 슈팅

## ✨사용자 개선 사항

## ✨팀원 구성 및 연락처
[팀원 구성 (1)](https://www.notion.so/1fa2dc3ef514808bb7c0d267fdd072cb?pvs=21)
