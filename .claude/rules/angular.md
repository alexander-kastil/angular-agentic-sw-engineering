---
paths:
  - "demos/**"
  - "labs/**"
---

# Angular apps

- Owner agent: `angular-expert`.
- The global `angular-conventions` skill (repo copy in `.claude/skills/angular-conventions/`) carries the standards; this file holds only where the repo deviates and what only it has.
- Change detection: OnPush is the v22 default; never write `changeDetection` explicitly (the skill's explicit `ChangeDetectionStrategy.OnPush` does not apply here).
- Testing is Vitest through the native Angular 22 support in `@angular/build`.
- Start every app from its project folder (e.g. `demos/02-signals/ng-signals`), never from the repository root.
- Scaffold with the Angular CLI: `ng generate component`, `ng generate service`, etc.
- Never use PowerShell for Angular code refactoring; use bash.
- `.claude/hooks/no-legacy-angular.sh` blocks legacy APIs (`*ngIf`, `@Input()`, `ngClass`, `@HostBinding`, `standalone: true`, ...) in `.ts` and `.html` files under `labs/`; the demos teach them deliberately.
- Each demo app holds `db.json` (demo catalog with `url`, `title`, `teaches`, `topic`, `sortOrder`, `md` fields), `src/app/demos/demo.routes.ts` (route definitions), `public/markdown/<name>.md` (the markdown guide of each demo) and `src/app/demos/samples/<name>/` (the component implementation).
