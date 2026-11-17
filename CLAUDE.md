# Project: CodeTeam_Project

## Stack
React 18 + TypeScript + Vite, React Router, TanStack Query, Vitest + React Testing Library.

## Lệnh
- Dev: `npm run dev`
- Build: `npm run build`
- Test: `npm run test -- --run`
- Lint: `npm run lint`
- Typecheck: `npx tsc --noEmit`

## Quy ước
- Function component + hooks, không dùng class component.
- Mỗi component một thư mục: `Button/Button.tsx`, `Button.test.tsx`, `index.ts`.
- Không dùng `any`; props luôn có type rõ ràng.
- Logic dùng lại được tách thành custom hook trong `src/hooks/`.
- Gọi API qua `src/api/`, không fetch trực tiếp trong component.
- Truy cập được (a11y): dùng thẻ semantic, có label cho input, test theo role/text.

## Definition of Done
Typecheck, lint và test đều pass; có test cho code mới.