# KAINORIA 公式サイト

KAINORIA の公開用ウェブサイト。GitHub Pages で公開している静的サイトです。
Stripe の「ビジネスウェブサイト」にもこのサイトの URL を登録しています。

## 構成

```
index.html                  トップページ（事業内容 / 製品・サービス / お知らせ / お問い合わせ）
about.html                  事業者情報
products/
  smartstock-sme.html       製品ページ: SmartStock SME
assets/
  style.css                 全ページ共通のスタイル（色・余白は :root 変数で管理）
  favicon.svg               ファビコン（全ページの <head> で参照）
```

## ページ・機能の足し方

### 製品・サービスを足す
1. `products/` に新しい製品ページ（例: `products/new-product.html`）を作る。
   既存の `smartstock-sme.html` をコピーして書き換えるのが早い。
   CSS のパスは `../assets/style.css`、トップへのリンクは `../index.html`。
2. `index.html` の `#products` セクションに `.card` を 1 枚追加し、
   詳細ページへリンクする。

### 機能紹介を足す
- 製品ページの `.feature-list` に `<li>` を 1 行追加する。

### お知らせを足す
- `index.html` の `#news` セクションの `.news-list` に `<li>` を 1 行追加する
  （新しいものを上に）。

### ご依頼の流れ・FAQを直す
- 流れは `index.html` の `#process` セクションの `.steps`（`<li>` が 1 手順）。
- FAQ は `#faq` セクションの `.faq-item`（`<details>`）をコピーして増やす。
- 回答は、実際に提供できる内容だけを書く（未確定の料金・納期は書かない）。

### 製品の機能・動作環境を足す
- 製品ページの `.spec` テーブルに `<tr>` を 1 行追加する。
  機能表は「区分 / 機能 / 内容」、動作環境は「項目 / 内容」の並びをそろえる。

### デザインを変える
- `assets/style.css` の `:root` 変数（--navy / --teal など）を変えると
  全ページに一括で反映される。

## 公開方法

- このリポジトリの `main` ブランチを GitHub Pages で公開している。
- ファイルを編集して push すれば、数分で自動的に反映される。

## 注意

- 料金はオーナーが決定する事項のため、このサイトには掲載しない。
- 所在地・電話番号などの個人情報は掲載しない（問い合わせ窓口はメールのみ）。
- 特定商取引法に基づく表記は、有料販売の開始時に about.html へ追加する（オーナー確認事項）。
