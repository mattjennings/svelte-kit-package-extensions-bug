# svelte-kit package extensions bug

This demonstrates the bug described in https://github.com/sveltejs/kit/issues/2040

- first, run `pnpm install`
- go to `svelte-library/src/lib/index.ts`
- notice the two different exports. One will work only in webpack but fail when used internally in `src/routes`, and the other vice-versa.
- both projects can be started with `pnpm run dev`, `svelte-library` can be rebuilt using `pnpm run build` after changing the exports
