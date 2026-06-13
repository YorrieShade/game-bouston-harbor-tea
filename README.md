# 🫖 Bouston Harbor Tea Toss / 某ストン湾 紅茶投げ込みゲーム

クリックで某ストン湾に紅茶（茶箱）を投げ込み続ける、1ファイル完結のブラウザミニゲームです。
一定点数をクリアすると、見事**イマジナリー合衆国の市民**に認定され、**Fable5 利用権（ネタ）**が贈られます。

A one-file browser mini-game: click to keep dumping crates of tea into the harbor.
Clear the score goal and you're certified as a **citizen of the Imaginary United States**, complete with a **Fable5 license** (a joke reward).

> ⚠️ これはジョークゲームです。実在の権利・市民資格・製品（Fable5 など）とは一切関係ありません。
> For entertainment only. No real citizenship, rights, or product is granted.

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

## ファイル構成 / Files

```
index.html   # ゲーム本体（HTML + CSS + JS すべて入り）/ the whole game in one file
README.md    # この説明 / this file
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

▶ Play: `https://<ユーザー名>.github.io/<リポジトリ名>/`

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

---

## ライセンス / License

自由に使ってください（パブリックドメイン相当）。すべてフィクションのジョークゲームで、実在の出来事・国・製品とは一切関係ありません。
Free to use (public-domain-ish). Entirely a fictional parody — not related to any real event, country, or product.
