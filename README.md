# ⚛️ Frontend Live Coding & Component Implementation Practice

> "The road to the perfect component is paved with practice and thoughtful structure."

본 레포지터리는 **React/JavaScript** 환경에서 실제 웹 애플리케이션에 필요한 다양한 UI 컴포넌트와 비즈니스 로직을 신속하고 정확하게 구현하는 능력을 기르는 데 중점을 둡니다.

---

## 🎯 연습 목표 및 기본 규칙

### 1. 시간 제한 (Time Limit)
* **쉬운 난이도 (Easy-Medium):** 30분 ~ 1시간 이내
* **어려운 난이도 (Hard/Advanced):** 1시간 ~ 2시간 이내
* 완료 후 커밋 메시지에 **소요 시간을 반드시 명시**합니다.
* Prac의 경우, 시간명시를 하지 않습니다 (Prac = 따라코딩)

### 2. 컴포넌트 품질 (Component Quality)
* 모든 컴포넌트는 **재사용성**과 **확장성**을 고려하여 작성합니다.
* 가능한 경우 **TypeScript**를 적용하여 타입 안정성을 확보하는 연습을 병행합니다.
* **불필요한 리렌더링 방지** (useMemo, useCallback 등)에 대한 고민이 있다면 주석으로 남깁니다.

### 3. Git Workflow
* 각 주제별 컴포넌트 구현은 독립된 커밋으로 기록합니다.
* 일반 구성용 커밋 메시지 형식은 **`Feat: [구현 내용]`**을 사용합니다.
  - 앞에는 feat, init, fix 등이 들어갑니다.
* 커밋 메시지 형식은 **`[폴더 번호] (Prac여부): [구현 주제] (XX min)`**을 사용합니다.
  - Prac의 경우, 시간명시를 하지 않습니다
  - 폴더 번호는 아래 레포지터리 구조를 따릅니다.
  - 예시: `05P: debounce` , `05: debounce (30min)`

---

## 🏗️ 레포지터리 구조 (Component-Focused Structure)

모든 작업은 `src/components/` 아래에 주제별 혹은 기능별로 폴더를 만들어 관리합니다.

| 폴더명 | 주제 및 내용 | 예시 파일 |
| :--- | :--- | :--- |
| `01_Basic_UI` | 카운터, 토글, 별점, 드롭다운 등 **기본 UI 요소** | `src/components/01_Basic_UI/Counter.js` |
| `02_Data_Handling` | API 호출, 검색 필터, 데이터 목록 렌더링 등 **데이터 처리** | `src/components/02_Data_Handling/FetchData.js` |
| `03_Forms_Logic` | 다단계 양식, 동적 필드, Yup/Formik을 사용한 **복잡한 양식 로직** | `src/components/03_Forms_Logic/DynamicForm.js` |
| `04_Advanced_UI` | 모달, 캐러셀, 드래그 앤 드롭, 가상화된 목록 등 **고급 사용자 경험** | `src/components/04_Advanced_UI/VirtualizedList.js` |
| **`05_Architecture_Optimization`** | **JS `this` 바인딩, 이벤트 루프**, 디바운스/쓰로틀링, **Context API** 및 **커스텀 Hooks**, 서버 컴포넌트 등 **고급 로직/아키텍처 및 성능 최적화** | `src/components/05_Architecture_Optimization/useDebounce.js` |
### 📁 예시 폴더 구조
* 이 예시구조를 참고하여 폴더 구조를 구성합니다. 실제 현재 파일구조와 다를 수 있습니다.

```
├── src/
│   ├── components/
│   │   ├── 01_Basic_UI/
│   │   │   ├── Counter/          # 컴포넌트 단위 폴더 (파일 묶음)
│   │   │   │   ├── Counter.js
│   │   │   │   └── index.js
│   │   │   └── ToggleSwitch.js
│   │   ├── 03_Forms_Logic/
│   │   │   ├── MultiStepForm.js
│   │   │   └── DynamicForm.js
│   │   └── 05_Context_Hooks/
│   │       ├── AuthContext.js
│   │       └── useDebounce.js
│   └── App.js                     # 컴포넌트들을 통합하여 테스트하는 파일
├── package.json
└── README.md
```

