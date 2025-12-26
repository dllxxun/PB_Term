# Todo Calendar Project

웹과 모바일에서 동일한 Firebase를 사용하는 Todo 관리 프로젝트입니다.

## 프로젝트 구성
- Web: React + Vite
- Mobile: React Native
- Backend: Firebase (Authentication, Firestore)

## 폴더 구조
Todo_Calendar/
├─ todo_web # 웹 애플리케이션
└─ todo_mobile # 모바일 애플리케이션

## Web 실행 방법
```bash
cd todo_web
npm install
npm run dev
```

## Mobile 실행 방법
```bash
cd todo_mobile
npm install
npx react-native run-android
```

## Firebase 연동 코드 위치
**Web App**
- `src/utils/firebase.js` : Firebase 초기화 + GoogleAuthProvider
- `src/components/Login.jsx` : `signInWithPopup` 실제 사용

**Mobile App**  
- `App.tsx` : 익명 로그인 `auth().signInAnonymously()` + Firestore `todos` 쿼리
- 동일 Firebase projectId 사용 (웹과 데이터 공유 확인)
