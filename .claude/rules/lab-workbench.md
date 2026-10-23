---
paths:
  - "labs/**"
  - "db/**"
  - "design-system/**"
---

# Secrets and Document Vault lab workbench

- Owner agent: `angular-expert`.
- The labs build one Angular workbench against the Secrets and Document Vault API. The backend is given and is never edited from a lab.
- Lab app: `labs/lab-<NN>/l<NN>-secrets-vault-starter`, solved in `l<NN>-secrets-vault-solution` beside it.
- API base: `/api`, proxied to `http://localhost:5093` by the app's `proxy.conf.json`.
- Domain source: the C# records in `labs/secrets-vault-mcp/Contracts/`.
- Design tokens: `design-system/secrets-and-document-vault/MASTER.md`, mirrored in the app's `src/styles.css`.
- Lists: `GET /api/lists` returns `listId`, `name`, `description`, `type`, `secretCount`.
- List type: `1` is Secrets, `2` is Vault.
- Derive every TypeScript interface from the matching C# record. Do not invent a field.
- Style from the CSS custom properties in the app's `src/styles.css`. A raw hex value in a component stylesheet is a defect.
- Scaffold with `ng generate`, never by hand.
