# 📝 투두리스트 TypeScript 프로젝트

- ✅ **할 일 추가**: 실시간 입력 및 즉시 반영
- ✅ **할 일 완료**: 진행 중 → 완료 상태로 이동
- ✅ **완료된 할 일 삭제**: 완료된 작업 정리
- ✅ **빈 상태 안내**: 할 일이 없을 때 메시지

### 🚀 **사용자 경험 최적화**

- 🔄 **자동 포커스**: 할 일 추가 후 입력 필드에 자동 포커스
- ⚡ **즉시 반영**: 모든 변경사항이 실시간으로 화면에 반영
- 🎨 **직관적 UI**: 완료/삭제 버튼이 색상으로 구분
- 📱 **반응형 디자인**: 다양한 화면 크기에 대응

## 프로젝트 구조

```
todoList-ts/
├── 📁 src/
│   └── 📄 script.ts          # TypeScript 소스 코드
├── 📁 dist/
│   └── 📄 script.js          # 컴파일된 JavaScript
├── 📄 index.html             # HTML 구조
├── 📄 style.css              # 스타일링
├── 📄 tsconfig.json          # TypeScript 설정
└── 📄 README.md              # 프로젝트 문서
```

## 빠른 시작

### 1. TypeScript 컴파일

```bash
npx tsc
```

### 2. 개발 서버 실행

```bash
# Live Server 또는 다른 로컬 서버 사용
# index.html 파일을 브라우저에서 열기
```

## 💡 핵심 기능 구현

### 📝 할 일 추가

```typescript
const addTodo = (text: string): void => {
  todos.push({ id: Date.now(), text });
  todoInput.value = "";
  todoInput.focus(); // 자동 포커스
  renderTasks();
};
```

### ✅ 할 일 완료

```typescript
const completeTodo = (todo: Todo): void => {
  todos = todos.filter((t): boolean => t.id !== todo.id);
  doneTasks.push(todo);
  renderTasks();
};
```

### 🗑️ 할 일 삭제

```typescript
const deleteTodo = (todo: Todo): void => {
  doneTasks = doneTasks.filter((t): boolean => t.id !== todo.id);
  renderTasks();
};
```
