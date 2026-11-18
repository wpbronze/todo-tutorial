# Todo Tutorial

[Claude Code Playbook](https://docs.claude-hunt.com) 강의에서 작은 할 일 앱을 직접 만들어 보며 Claude Code 쓰는 법을 배우는 연습용 저장소입니다.

## 관련 링크

- 강의 본문: https://docs.claude-hunt.com
- 수강생 결과물 공유: https://claude-hunt.com

## 기술 스택

- Next.js 16 (App Router, Turbopack)
- React 19
- Tailwind CSS v4
- shadcn/ui (radix-maia 스타일, taupe 베이스)
- TypeScript / ESLint / Prettier
- 패키지 매니저: bun 1.3.6

## 시작하기

### 1. 준비물

- [Git](https://git-scm.com)
- [Bun](https://bun.sh) (이 저장소는 bun 1.3.6 기준이며, 그 이상 버전도 동작합니다)
- [Node.js](https://nodejs.org) 20.9 이상 (Next.js 16이 요구합니다)

설치 확인:

```bash
bun --version
node --version
```

### 2. 저장소 받기

```bash
git clone <저장소 주소>
cd todo-tutorial
```

### 3. 의존성 설치

```bash
bun install
```

### 4. 개발 서버 실행

```bash
bun run dev
```

터미널에 `Ready`가 표시되면 브라우저에서 [http://localhost:3000](http://localhost:3000) 을 엽니다. 3000번 포트가 이미 사용 중이면 Next.js가 다른 포트(3001 등)를 골라 터미널에 알려 줍니다. 서버는 `Ctrl+C`로 끝냅니다.

### 5. 동작 확인 (선택)

```bash
bun run test       # 테스트 (Vitest)
bun run typecheck  # 타입 검사
bun run lint       # ESLint
```

### 자주 쓰는 스크립트

```bash
bun run dev        # 개발 서버 (Turbopack)
bun run build      # 프로덕션 빌드
bun run start      # 빌드 결과 실행 (먼저 build 필요)
bun run test       # 테스트 한 번 실행
bun run test:watch # 테스트 감시 모드
bun run lint       # ESLint
bun run typecheck  # tsc --noEmit
bun run format     # Prettier 포맷팅
```

## 레슨별 시작 브랜치

레슨마다 시작 시점의 코드를 `lesson/<레슨 이름>` 브랜치로 제공합니다. 레슨 본문이 안내하는 브랜치로 바꾼 뒤 따라가세요.

```shell
git checkout lesson/claude-md
```

## 컴포넌트 추가

shadcn/ui 컴포넌트는 다음과 같이 추가합니다.

```bash
bunx --bun shadcn@latest add button
```

`components/ui` 디렉토리에 컴포넌트가 추가됩니다.

## 컴포넌트 사용

```tsx
import { Button } from "@/components/ui/button";
```
