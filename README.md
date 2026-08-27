# 家具のソムリエ ｜ トフィー（Toffy）調理家電 特集

家具のソムリエ（楽天市場 sid=333706 / 店舗ID `sommelier`）で取り扱うトフィーの**調理家電20台**だけを集めた1ページ特集。カラフルポップ・レトロ路線。`index.html` 1ファイル完結（CSS/JSインライン）。

## いまの状態：ドラフト

- 商品画像は楽天「家具のソムリエ」の掲載画像（`tshop.r10s.jp/sommelier/...`）を**直リンク**しています。
- 本番用にする場合は各画像を `images/` に保存し、`index.html` 内 `scenes` 配列の `img:` を差し替えてください（直リンクは店舗側の画像入れ替え・ホットリンク制限で表示が消える可能性があります）。
- 価格・ポイントは2026年8月時点で確認した税込価格です。変わったら `scenes` 配列の `price:` を更新。

## 差し替え箇所（`index.html` 下部の `<script>` 内）

| 変数 | 内容 |
|---|---|
| `scenes` | シーン（4つ）と商品データ。`m`=型番 / `name`=商品名 / `note`=ひとこと / `price`=税込価格（¥なし） / `img`=画像パス / `url`=商品ページURL |
| `IMG()` | 画像URLの組み立て。`images/` 運用に切り替えるなら `const IMG = u => "images/" + u;` にして `img:` をファイル名に |
| `STORE_TOFFY_URL` | 「ぜんぶ見る」ボタンのリンク先（店舗内トフィー検索） |
| `tickText` | FV下の流れる帯の文言 |

商品の増減は `items` 配列に足す／削るだけ。各シーンの**先頭の商品**が大きい「主役」カードになります。シーン見出しの「◯台」の数字は手動で直してください。

## ローカル確認

```
powershell -ExecutionPolicy Bypass -File scripts/serve.ps1
```

→ http://localhost:8735/

## 公開

GitHub Pages（このリポジトリの Pages 設定）。`index.html` と `images/` を置くだけ。相対パスなのでサブディレクトリでも動きます。

## フォント

Google Fonts：見出し=Zen Maru Gothic / 本文=Zen Kaku Gothic New / 数字アクセント=Rampart One / 英字=Josefin Sans。レトロでまるい調理家電の世界観に合わせ、標準の Kaisei Opti は使わず角丸ゴシック主体にしています。

## 掲載商品（20台）

- **SCENE 01 めざめの家電**：K-TS5 / K-TS4 / K-HTS1 / K-HS3 / K-HS6 / K-FS2 / K-HKT1
- **SCENE 02 コーヒーのある暮らし**：K-CM9 / K-CM8 / K-CM12 / K-CM11
- **SCENE 03 ごはんとおかず**：K-DR2 / K-DR3 / K-HP4 / K-AS2 / K-SY1 / K-GP1
- **SCENE 04 たのしい食卓**：K-BE1 / K-WS2 / K-CP1

※日傘・台車・扇風機・掃除機・加湿器・衣類スチーマー・レンジ調理器（グリルパン等）・保存容器などの非・調理家電は今回は除外しています。
