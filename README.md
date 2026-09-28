# CutSync — 更新情報 / Update feed

Premiere Pro 用プラグイン「CutSync」のパネルが、**新しい版があるかどうかだけ**を見に来るための置き場所です。
This is where the CutSync panel checks **only whether a newer version exists**.

- 本体（購入・ダウンロード）: https://yas-tools.booth.pm/items/8569410
- パネルが読むファイル / File the panel reads: [`version.json`](version.json)

## version.json の見かた

| 鍵 | 意味 |
|---|---|
| `latest` | 最新版の番号 |
| `url` | 「入手ページを開く」で案内するページ（売り場の指定が無いとき） |
| `notes` | 一言の説明。`{ "ja": "…", "en": "…" }`（空でもよい）。お知らせの欄に出ます |
| `channels.<売り場>` | **売り場ごとの上書き**（`latest` / `url` / `notes`）。パネルは自分がどの売り場の配布物か（`js/channel.js`）を知っていて、あればこちらを使います |

🔵 **ファイルはここでは配りません。**買った人は、買ったところ（BOOTH ならライブラリ、aescripts ならアカウントのページ）から落とします。
そのため、どこで売っても同じ1本のプラグインで「新しい版があります」を知らせられます。
売り場を増やしたら `channels` に1つ足すだけです。

## 新しい版を出したときの手順

1. **売り場に新しい版を上げる**（BOOTH など）
2. **このファイルの `latest` を書き換える**（`notes` も要れば1行ずつ）。
   売り場によって出す日がずれるときは、`channels.<売り場>.latest` で分けます
3. 以上。パネルは次の起動時に気づきます

⚠️ `latest` を先に上げると、**まだ落とせない版を案内する**ことになるので、**売り場が先**。
⚠️ 反映まで**数分**かかります（GitHub のキャッシュ）。すぐ出なくても正常です。

## 集めているもの / What is collected

**ありません。**パネルはこのファイルを取りに来るだけで、こちらへ何も送りません（GitHub 側に通常のアクセスログが残るだけです）。
**Nothing.** The panel only downloads this file and sends nothing back (GitHub keeps its usual access logs).
