# Web Tools - プロジェクト情報

## 技術スタック
- バニラ HTML/CSS/JS（ビルドツールなし）
- ホスティング: GitHub Pages
- ドメイン: piktool.net（XServer Domain で取得）
- リポジトリ: Nyaaa0011/web-tools
- GA4 測定ID: G-792H51BDVS

## ディレクトリ構成
```
/                          ← JP ポータル（全ページ単一HTML・CSS/JS埋込）
├── moji-count/            ← 文字数カウンター (JP)
├── color-code/            ← カラーコード変換 (JP)
├── password-gen/          ← パスワード生成 (JP)
├── json-format/           ← JSON整形 (JP)
├── warikan/               ← 割り勘計算 (JP)
├── age-calc/              ← 年齢計算 (JP)
├── unit-conv/             ← 単位変換 (JP)
├── en/                    ← English versions
│   ├── char-count/        ← Character Counter
│   ├── color-code/        ← Color Code Converter
│   ├── password-gen/      ← Password Generator
│   ├── json-format/       ← JSON Formatter
│   ├── split-bill/        ← Bill Splitter
│   ├── age-calc/          ← Age Calculator
│   └── unit-conv/         ← Unit Converter
├── privacy.html           ← プライバシーポリシー (JP)
├── en/privacy.html        ← Privacy Policy (EN)
├── contact.html           ← お問い合わせ
├── sitemap.xml
└── robots.txt
```

## デザイントークン
- ベース背景: #ffffff (light) / #1a1a2e (dark)
- テキスト: #333333 (light) / #e0e0e0 (dark)
- 各ツールのアクセントカラー:
  - 文字数カウンター/Char Count: #4A90D9
  - カラーコード/Color Code: #E91E63
  - パスワード/Password: #4CAF50
  - JSON整形/Formatter: #FF9800
  - 割り勘/Split Bill: #9C27B0
  - 年齢計算/Age Calc: #00BCD4
  - 単位変換/Unit Conv: #795548

## SEO構成（各ツールページ共通）
1. title + meta description（JP/EN別最適化）
2. hreflang タグ（ja ↔ en 相互リンク）
3. ツール本体
4. 使い方説明（500〜1000文字）
5. FAQ（JSON-LD構造化データ付き）
6. 関連ツール内部リンク
7. 広告プレースホルダー `<!-- AD SLOT -->`
8. WebApplication型 JSON-LD

## 設計パターン
- 全ページ単一HTML（CSS/JS埋め込み、外部依存なし）
- CSS変数でダークモード切替（prefers-color-scheme + 手動トグル + localStorage）
- 言語切替: ヘッダーのリンクボタンで / ↔ /en/ 遷移
- GA4 + AdSense: コメントアウト状態で全ページに埋め込み済み（ID置換で即有効化）

## 進捗
- [x] 共通CSS・i18n・ポータル
- [x] 文字数カウンター (JP/EN)
- [x] カラーコード変換 (JP/EN)
- [x] パスワード生成 (JP/EN)
- [x] JSON整形 (JP/EN)
- [x] 割り勘計算 (JP/EN)
- [x] 年齢計算 (JP/EN)
- [x] 単位変換 (JP/EN)
- [x] privacy / contact / sitemap / robots.txt
- [x] GitHub リポジトリ作成・push
- [x] GitHub Pages 有効化
- [x] 独自ドメイン piktool.net 取得・設定
- [x] 全ページ URL を piktool.net に更新
- [x] DNS レコード設定（A レコード × 4 + CNAME）
- [x] ネームサーバーを ns1-ns3.xdomain.ne.jp に変更
- [x] HTTPS 強制有効化
- 公開URL: https://piktool.net/
