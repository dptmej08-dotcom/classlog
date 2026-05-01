# FitLog — 트레이너 수업 기록 앱

## 파일 구조
```
fitlog/
├── index.html       ← 앱 전체 (이게 핵심)
├── vercel.json      ← Vercel 설정
└── public/
    └── manifest.json ← 홈 화면 추가용
```

## 배포 방법 (깃허브 → Vercel → 사파리)

### 1단계 — 깃허브에 올리기
1. github.com 에서 새 저장소(repository) 만들기
   - Repository name: `fitlog`
   - Public 선택 → Create repository
2. 이 폴더 안의 파일들을 전부 업로드 (Upload files 버튼)

### 2단계 — Vercel 연결
1. vercel.com 접속 → 구글/깃허브 계정으로 가입
2. "Add New Project" → 방금 만든 `fitlog` 저장소 선택
3. 설정 건드리지 말고 바로 "Deploy" 클릭
4. 배포 완료되면 `fitlog-xxx.vercel.app` 주소 생성됨

### 3단계 — 아이폰 홈 화면에 추가
1. 사파리에서 위 주소 접속
2. 하단 공유 버튼(네모+화살표) 탭
3. "홈 화면에 추가" 탭
4. 이름 "FitLog" 확인 후 추가

→ 앱 아이콘이 생기고 앱처럼 전체화면으로 실행돼요!

## Anthropic API 키 설정 (AI 손글씨 인식용)

현재 코드는 Anthropic API를 직접 호출해요.
보안을 위해 나중에 서버리지 함수로 분리하는 걸 추천드리지만,
먼저 테스트할 때는 이대로 사용 가능해요.

## 회원 이름 변경하기

`index.html` 파일에서 이 부분을 찾아서 수정:
```javascript
const MEMBERS = ['김지수','이민준','박서연','최현우','오소영'];
```
실제 회원 이름으로 바꿔주세요.
