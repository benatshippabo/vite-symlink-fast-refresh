# Minimal example for monorepo `resolve.preserveSymlinks: true` Vite bug

https://github.com/vitejs/vite/issues/6479

## Reproduction

1. `yarn && yarn dev`
2. edit `packages/another-package/index.tsx` by changing `Hey!!` to `Hey!`
3. notice the app doesn't update
4. comment out `resolve.preserveSymlinks` in `packages/app/vite.config.ts`
5. undo changes in `packages/another-package/index.tsx`
6. notice the app now updates properly
