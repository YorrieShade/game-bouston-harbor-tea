# 🫖 Bouston Harbor Tea Toss / 某ストン湾 紅茶投げ込みゲーム

クリックで某ストン湾に紅茶（茶箱）を投げ込み続ける、1ファイル完結のブラウザミニゲームです。
一定点数をクリアすると、見事**イマジナリー合衆国の市民**に認定され、**Fable5 利用権（ネタ）**が贈られます。

A one-file browser mini-game: click to keep dumping crates of tea into the harbor.
Clear the score goal and you're certified as a **citizen of the Imaginary United States**, complete with a **Fable5 license** (a joke reward).

> ⚠️ これはジョークゲームです。実在の権利・市民資格・製品（Fable5 など）とは一切関係ありません。
> For entertainment only. No real citizenship, rights, or product is granted.

▶ **遊ぶ / Play now:** https://yorrieshade.github.io/game-bouston-harbor-tea/

遊んだら、よければ **#某ストン湾紅茶投込** / **#BoustonTeaToss** を付けてシェアしてください。
If you share it, the tags **#某ストン湾紅茶投込** / **#BoustonTeaToss** are appreciated.

---

## 2つのモード / Two modes

スタート画面でモードを選べます。
Pick a mode on the start screen.

- **認定モード / STORY** — 20秒以内に **1000点**でクリア。市民認定証＋Fable5利用権（ネタ）。
  Reach **1000 points** within 20s to clear and get certified.
- **スコアアタック / SCORE ATTACK** — 早期クリアなし。**20秒フル**で稼ぎ、最終点に応じて**特典が段階的にUP**。
  No early finish — play the **full 20s**; your final score unlocks a **bigger reward tier**.

## 遊び方 / How to play

- **クリック / タップ**で、船から茶箱を湾に投げ込みます。海（水面）の上を狙ってください。
  Click or tap on the water to throw a crate from the ship.
- 光る**🎯ターゲット（埠頭の真上）**に近いほど高得点。中心ほど得点が大きいです。
  The closer you land to the glowing **🎯 target**, the more points — bullseye scores most.
- **連続で素早く**投げ込むと**コンボ**が育ち、倍率が上がります（最大 ×3）。
  Throw in quick succession to build **combos** (up to ×3).
- 画面下の**潮ゲージ（TIDE）**が**明るい帯**にあるタイミングで投げると**倍率 ×2**。
  Throw while the **tide bar** marker is inside the **bright band** for a **×2 multiplier**.
- たまに現れる**👑 御用船（ROYAL CARGO）**に茶箱を当てると **+250点**の大量ボーナス（さらに潮・コンボ倍率も乗る）。
  Hit the occasional **👑 ROYAL CARGO** ship for a **+250 bonus** (tide/combo multipliers stack on top).

スコアアタック中は画面上部に「今の特典／次のランクまであと何点」が表示され、狙いながら遊べます。
In Score Attack, a banner shows your current reward and points to the next tier, so you can chase it.

---

## 表示と言語 / Display & language

- **日英切替 / Bilingual toggle** — 画面右上のボタンで日本語⇄英語を切り替えできます（初期は日本語）。説明・ルール・HUD・認定証などUI全体が連動します。ゲームタイトルと「⚠️ ジョークゲームです」の注意書きは、どちらの言語でも常時表示のまま（切替対象外）です。
  Use the button at the top right to switch Japanese ⇄ English (Japanese by default). The whole UI follows. The game title and the "parody game" disclaimer stay visible in both languages.
- **スマホ対応 / Mobile-friendly** — 画面幅に合わせてレイアウトが調整されます。スタート画面はスマホ幅でもスクロールなしで収まります。スマホでは、時間切れ・認定証などの画面は盤面（4:3）の枠を飛び出して画面全体に表示されるので、本文やボタンが見切れません。プレイ中のランク表示は不透明カードにして読みやすくし、コンボ演出は下寄りに置いて上部のランク表示と重ならないようにしています。
  The layout adapts to screen width. The start screen fits phones without scrolling. On phones, the fail/certificate screens break out of the 4:3 stage and use the full viewport so nothing is clipped; the in-play rank banner is a solid card for readability, and the combo popup sits lower so it doesn't overlap that banner.

> 倍率演出の「TIDE / TIDE BONUS」は、隣の「COMBO」と語感を揃えるため、日本語表示でも英語のままにしています。
> The "TIDE / TIDE BONUS" callouts stay in English even in Japanese mode, to match the neighboring "COMBO".

---

## ファイル構成 / Files

```
index.html    # ゲーム本体（HTML + CSS + JS すべて入り）/ the whole game in one file
README.md     # この説明 / this file
CHANGELOG.md  # 変更履歴と判断理由 / change log and rationale
```

外部ライブラリ・ビルド・サーバー不要。`index.html` をブラウザで開くだけで遊べます。
No dependencies, no build step, no server. Just open `index.html` in a browser.

---

## ローカルで遊ぶ / Run locally

`index.html` をダブルクリックしてブラウザで開くだけです。
Just double-click `index.html`.

---

## 公開 / Hosting

`index.html` を GitHub Pages などの静的ホスティングにそのまま置けば遊べます（リポジトリ直下に置けば、そのURLがゲーム画面になります）。
Drop `index.html` on any static host such as GitHub Pages — at the repo root, the page URL serves the game directly.

▶ Play（テンプレ / template）: `https://<ユーザー名>.github.io/<リポジトリ名>/`
▶ このゲーム / this game: https://yorrieshade.github.io/game-bouston-harbor-tea/

---

## 得点のしくみ / Scoring

| 要素 / Factor | 効果 / Effect |
|---|---|
| 着弾位置 / Landing spot | 🎯中心 100 点、内側 60、近く 30、外側 10 / bullseye 100, inner 60, near 30, far 10 |
| コンボ / Combo | 1.3秒以内に連投で倍率上昇（最大 ×3）/ chain throws within 1.3s, up to ×3 |
| 潮タイミング / Tide timing | 明るい帯で投げると ×2 / ×2 when in the bright band |

最終得点 ＝ （着弾点 ＋ 御用船ボーナス）× 潮倍率 × コンボ倍率。
Final = (landing + royal-cargo bonus) × tide × combo.

## スコアアタックの特典ランク / Score Attack reward tiers

最終スコアに応じて、もらえる（ネタの）Fable5特典が増えていきます。
Your final score sets the (joke) Fable5 reward you "earn":

| スコア / Score | 称号 / Title | 特典 / Reward（ネタ・not real） |
|---|---|---|
| 0+ | 紅茶見習い / Tea Apprentice | Fable5 利用権 1ヶ月分 |
| 1000+ | 紅茶男爵 / Tea Baron | Fable5 利用権 2ヶ月分 |
| 2000+ | 紅茶伯爵 / Tea Earl | Fable5 利用権 3ヶ月分 ＋ トークン2倍 |
| 3500+ | 紅茶侯爵 / Tea Marquess | Fable5 利用権 6ヶ月分 ＋ トークン3倍 |
| 5500+ | 紅茶大公 / Grand Duke of Tea | Fable5 利用権 1年分 ＋ トークン5倍 |

しきい値や特典文言は `index.html` の `TIERS` 配列で自由に編集できます。
Edit the thresholds and reward text in the `TIERS` array in `index.html`.

---

## カスタマイズ / Tweaks

`index.html` 内の `Config` 付近を編集できます。
Edit near the `Config` section in `index.html`:

- `GOAL` … クリアに必要な点数 / score needed to win（既定 1000）
- `GAME_TIME` … 制限時間（秒）/ time limit（既定 20）
- `sweetStart`, `sweetEnd` … 潮の「おいしい帯」の範囲 / size of the bright tide band
- `target.r` … ターゲットの大きさ / target size

難しくしたいなら `GOAL` を上げる・`GAME_TIME` を下げる・`target.r` を小さくしてください。
To make it harder: raise `GOAL`, lower `GAME_TIME`, or shrink `target.r`.

### 文言の編集・翻訳 / Editing & translating text

日英切替は、`<html data-lang="ja">` 属性とCSSの出し分けで動いています。
The language toggle works via the `data-lang` attribute on `<html>` plus CSS show/hide.

- 画面に出る文言は `<span class="t-ja">日本語</span><span class="t-en">English</span>` のペアで書きます。`data-lang` に応じて片方だけ表示されます。
  On-screen text is written as `<span class="t-ja">…</span><span class="t-en">…</span>` pairs; only one shows per language.
- JS内で動的に出る文言（特典ランクやコンボ演出など）は `L('日本語','English')` ヘルパーと `TIERS` 配列の `ja` / `en` で言語ごとに持っています。
  Dynamic text in JS (reward tiers, combo callouts) uses the `L('ja','en')` helper and the `ja` / `en` fields of the `TIERS` array.
- タイトルと注意書きは意図的に切替対象外（常時表示）です。常時表示にしたい文言は `t-ja` / `t-en` ではなく通常のテキストにしてください。
  The title and disclaimer are intentionally not toggled. To keep any text always visible, write it as plain text rather than `t-ja` / `t-en`.

別言語を足したい場合は、`data-lang` の値・CSSの出し分け・`L()` を拡張すれば対応できます。
To add another language, extend the `data-lang` values, the CSS rules, and the `L()` helper.

---

## ライセンス / License

自由に使ってください（パブリックドメイン相当）。すべてフィクションのジョークゲームで、実在の出来事・国・製品とは一切関係ありません。
Free to use (public-domain-ish). Entirely a fictional parody — not related to any real event, country, or product.
