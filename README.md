# Remix + Designsystemet on node 20

This is a repository showing how you can use remix and designsystemet with node 20.
Check `vite.config.ts` that has this:

```ts
export default defineConfig({
  ssr: {
    noExternal: [
      "@digdir/designsystemet-react",
      "@digdir/designsystemet-theme",
      "@digdir/designsystemet-css"
    ],
  },
  plugins: [...],
});
```

This seems to be needed due to **remix** and not Designsystemet.

Packages:

```json
"dependencies": {
  "@digdir/designsystemet-css": "^1.0.0-next.35",
  "@digdir/designsystemet-react": "^1.0.0-next.35",
  "@digdir/designsystemet-theme": "^1.0.0-next.35",
  "@remix-run/node": "^2.13.1",
  "@remix-run/react": "^2.13.1",
  "@remix-run/serve": "^2.13.1",
  "isbot": "^4.1.0",
  "react": "^18.2.0",
  "react-dom": "^18.2.0"
},
```
