# MAML Grammar

This repository contains a TextMate grammar for the [MAML](https://maml.dev) language.

## Files

- [maml.json](maml.json) — the TextMate (TM) grammar definition.

## Use with VitePress

VitePress uses [Shiki](https://github.com/shikijs/shiki) under the hood for code highlighting. You can register the MAML
grammar and enable highlighting for code blocks like:

````markdown
```maml
# your MAML code here
```
````

Copy [maml.json](maml.json) to `.vitepress` directory.

Update configuration like this:

```diff
+const __dirname = new URL('.', import.meta.url).pathname
+const mamlLang = JSON.parse(fs.readFileSync(__dirname + '/maml.json', 'utf8'))

export default defineConfig({
  ...
  markdown: {
+    shikiSetup(shiki) {
+      shiki.loadLanguage(mamlLang)
+    },
  },
  ...
})
```

## License

[MIT](LICENSE)
 
