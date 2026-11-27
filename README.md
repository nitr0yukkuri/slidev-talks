# Slidev Talks

技術カンファレンス・LT用のスライド開発環境。

## Setup

Node.js 22.12.0 以上と npm が必要です。

```sh
npm install
npm run dev
```

`slides.md` を編集します。Vue コンポーネントは `components/` に、画像は `public/` に追加します。

## Build / Export

```sh
npm run build
npm run export
npm run export:pptx
```

エクスポートには Chromium が必要です。必要に応じて `npx playwright install chromium` を実行してください。
初回 `npm install` 後に `package-lock.json` をコミットしてください。

[Slidev documentation](https://sli.dev/)

## Field Notes layouts

`slides.md` contains a seven-slide sample deck. Custom layouts: `atmos-cover`, `atmos-content`, `atmos-section`, `atmos-code`, `atmos-quote`, `atmos-closing`. The warm paper palette is the default for every layout. Add an optional `kicker` or `tone: dark` to the frontmatter. See [design notes](docs/design.md).
