# 앱개발 숙련 주차 개인과제 "사과마켓"

## 요구사항 분석

### 필수 구현 과제 - MainActivity
- [x]  디자인 및 화면 구성을 최대한 동일하게 해주세요. (사이즈 및 여백도 최대한 맞춰주세요.) ✨
- [x]  상품 데이터는 아래 dummy data 를 사용합니다. (더미 데이터는 자유롭게 추가 및 수정 가능)
- [x]  더미 데이터 : [이미지 링크](https://drive.google.com/file/d/1P5AnZI1N2AB7yNqwkgF-KxlUdDjkmrBu/view?usp=sharing),  [상품 리스트 링크](https://docs.google.com/spreadsheets/d/1m9VDxJ3Q7dLEjefnWBq4fCghtWIUFnpM/edit?usp=sharing&ouid=116688204055896164464&rtpof=true&sd=true)  (←링크 권한 없으면 [여기](https://drive.google.com/drive/folders/1ZYQIxmP8JAXpcxvQB3QekYZLYQiNlZqK?usp=sharing) 클릭)
- [x]  RecyclerViewer를 이용해 리스트 화면을 만들어주세요.
- [x]  상단 툴바를 제거하고 풀스크린 화면으로 세팅해주세요. 
(상태바(시간/배터리 표시하는 최상단바)는 남기고)
- [x]  상품 이미지는 모서리를 라운드 처리해주세요.
- [x]  상품 이름은 최대 두 줄이고, 그래도 넘어가면 뒷 부분에 …으로 처리해주세요.
- [x]  뒤로가기(BACK)버튼 클릭시 종료하시겠습니까? [확인][취소] 다이얼로그를 띄워주세요. (예시 비디오 참고)
- [x]  상단 종모양 아이콘을 누르면 Notification을 생성해 주세요. (예시 비디오 참고)
- [x]  상품 가격은 1000단위로 콤마(,) 처리해주세요.
- [x]  상품 아이템들 사이에 회색 라인을 추가해서 구분해주세요.
- [x]  상품 선택시 아래 상품 상세 페이지로 이동합니다.
- [x]  상품 상세페이지 이동시 intent로 객체를 전달합니다. (Parcelize 사용)

### 필수 구현 과제 - DetailActivity
- [x]  디자인 및 화면 구성을 최대한 동일하게 해주세요. (사이즈 및 여백도 최대한 맞춰주세요.) ✨
- [x]  메인화면에서 전달받은 데이터로 판매자, 주소, 아이템, 글내용, 가격등을 화면에 표시합니다.
- [x]  하단 가격표시 레이아웃을 제외하고 전체화면은 스크롤이 되어야합니다. (예시 비디오 참고)
- [x]  상단 < 버튼을 누르면 상세 화면은 종료되고 메인화면으로 돌아갑니다

### 선택 과제
- [x]  스크롤을 최상단으로 이동시키는 플로팅 버튼 기능 추가
- [x]  플로팅 버튼은 스크롤을 아래로 내릴 때 나타나며, 스크롤이 최상단일때 사라집니다.
- [x]  플로팅 버튼을 누르면 스크롤을 최상단으로 이동시킵니다.
- [x]  플로팅 버튼은 나타나고 사라질때 fade 효과가 있습니다.
- [x]  플로팅 버튼을 클릭하면(pressed) 아이콘 색이 변경됩니다. .

# 피드백 개선
## 2024-04-19 피드백
- [x]  postAdapter에서 viewholder 선언 방식 inner class -> nested class로 변경해주세요.
->inner class 사용시 직렬화 문제 발생 가능성 있음
->inner class 내부에 outer class 정보를 보관, 참조를 해제하지 못하면 메모리 누수 발생가능성 있음
->불필요한 메모리 낭비와 성능 이슈
-MainActivity에서 onCreate구현 부에 binding.ivAlarm.setOnClickListener 구현부를 itemClickListener()로 분리하세요.
-detailActivity에도 onCreate구현 부에 클릭리스너 구현부를 메소드로 분리해보세요.
- [x]  intent로 data를 주고 받을 때 값을 직접 “UserData”로 넣어주는 방식보다 상수로 처리해보세요
- [x]  DetailActivity에서 val v1 = layoutInflater.inflate(R.layout.manners_info_dialog, null) 의미 있는 변수명으로 지어보세요.
