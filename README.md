<p align="center">
  <img src="https://raw.githubusercontent.com/Coccinella-Labs/pathutils/main/.github/assets/thumbnail.png" alt="pathutils" width="100%">
</p>

path handling for node.js.

TypeScript utilities for cross-platform path handling and secure file operations (Node 14+).

## Install

```bash
npm install @harpertoken/cross-platform-path-utils
```

## Usage

```ts
import { createPath, resolveFromFile, isPathInDirectory, safeReadFile } from "@harpertoken/cross-platform-path-utils";

const p = createPath("data", "models", "m.json");
const root = resolveFromFile(import.meta.url, "..");
if (isPathInDirectory(p, root)) {
  const text = await safeReadFile(p);
}
```

## Develop

```bash
npm test     # vitest run
npm run build  # tsc
```

## Layout

- `src/utils/` - `pathUtils.ts`, `pathHandling.ts`
- `src/types.ts`, `src/index.ts` - public exports
- `src/examples/`, `src/tests/` - examples and tests
