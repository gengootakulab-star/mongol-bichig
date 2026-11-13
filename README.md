# モンゴル文字 縦書き単語帳(mongol-bichig)

モンゴル語の単語を、伝統的なモンゴル文字(ᠮᠣᠩᠭᠣᠯ ᠪᠢᠴᠢᠭ)の縦書きで表示し、1文字ずつに分けて調べるツールです。

- 公開ページ: https://gengootakulab-star.github.io/mongol-bichig/
- サイト: [言語オタクの多言語学習ラボ](https://gengootakulab-star.github.io/)

## できること

- キリル文字・日本語・英語・ローマ字で単語を探す
- 伝統文字の綴りを縦書きで表示(上から下へ、行は左から右へ)
- 単語を1文字ずつに分け、語頭・語中・語末などの形と、ローマ字・キリル文字の目安を表示
- モンゴル文字を貼りつけると、辞書にない語でも文字に分ける
- 字形表(文字ごとの 独立・語頭・語中・語末 の形と、その文字を使う単語)
- `?w=単語` で、その単語を開いた状態で表示(例: `?w=морь`)

## データ

- 辞書: [kaikki.org](https://kaikki.org/) が Wiktionary から抽出したモンゴル語データを加工。約2,000語(伝統文字の綴りが分かる語だけ)
  - 綴りの出どころは3種類あり、画面に表示しています: Wiktionary の伝統文字の表記 / 語源欄の古典モンゴル語の綴り / 運営者の追加(10語)
- 日本語の意味: 運営者が約110語に付けたもの
- ライセンス: 辞書データは CC BY-SA 4.0(Wiktionary)

## 仕組み

- `index.html` 1ファイル。辞書データも中に入っています。ビルドなし
- フォント: Google Fonts の Noto Sans Mongolian。縦書きは CSS の `writing-mode: vertical-lr`
- 文字ごとの形は、ゼロ幅接合子(U+200D)を前後に付けて表示しています。単語の中では前後の文字でさらに形が変わることがあるので、目安です
- 保存するのは「最近見た単語」だけ(localStorage: `mn-bichig-recent` / `mn-bichig-tab`)
- ページの下に、サイトの `data.js` からモンゴル語の記事(lang に `MONGOLIAN` を含むもの)を自動で表示します
- 閲覧数: GoatCounter(Cookieなし)

## 注意

- 綴りと意味は自動で取り出したもので、誤りが含まれる可能性があります
- 語源欄から取った綴りは、古い時代の綴りで、今の綴りと違う場合があります
- 表示が崩れる機種・ブラウザがあるかもしれません

## 誤りの報告

- [Googleフォーム(アカウント不要)](https://forms.gle/c2BxTpxS1v8K5iba6)
- [GitHub Issue](https://github.com/gengootakulab-star/mongol-bichig/issues/new?template=report.yml)
