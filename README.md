### 핵심 함수들

- `renderTasks()` - 화면 렌더링
- `addTodo(text)` - 할 일 추가
- `completeTodo(todo)` - 할 일 완료 처리
- `deleteTodo(todo)` - 완료된 할 일 삭제
- `createTodoElement(todo, isDone)` - DOM 요소 생성

### 상태 관리

```typescript
let todos: Todo[] = []; // 진행 중인 할 일들
let doneTasks: Todo[] = []; // 완료된 할 일들
```

## 🔄 실행 흐름

1. **페이지 로드** → HTML 요소 선택 → 초기 렌더링
2. **할 일 추가** → 폼 제출 → `addTodo()` → 화면 업데이트
3. **할 일 완료** → 버튼 클릭 → `completeTodo()` → 화면 업데이트
4. **할 일 삭제** → 버튼 클릭 → `deleteTodo()` → 화면 업데이트

## �� 실행 방법

1. 프로젝트 클론
2. TypeScript 컴파일: `npx tsc`
3. Live Server로 `index.html` 실행

## 📝 주요 특징

- **타입 안전성**: TypeScript 타입 시스템 활용
- **상태 중심**: 배열 기반 상태 관리
- **이벤트 기반**: 사용자 상호작용에 따른 이벤트 처리
- **재렌더링**: 상태 변경 시마다 전체 화면 업데이트
