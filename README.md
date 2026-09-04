# 🐧 akios-public

**あき本人が見るための2つのサイト。** GitHub Pages で動いています。

| | URL |
|---|---|
| 🏠 入口 | https://zenmode-aki.github.io/akios-public/ |
| 🐧 自分PJ | https://zenmode-aki.github.io/akios-public/me/ |
| 📖 名言と価値観 | https://zenmode-aki.github.io/akios-public/words/ |

2つのサイトは、お互いにリンクで行き来できます。

## ⚠️ ここは「出力物」です。直接編集しない

このリポジトリのHTMLは、**非公開の `aki-os` から自動で作られています。**
ここを直しても、次のビルドで上書きされます。

```
aki-os/projects/aki-viewer/index.html  ─┐
aki-os/projects/jibun-pj/source.html   ─┴→ scripts/build_public_sites.py → ここ
```

中身を変えるときは `aki-os` の側を直して、あちらで：

```bash
./scripts/publish_public_sites.sh
```

## 🔒 このリポジトリは公開です

**GitHubの公開リポジトリなので、URLを知らない人でも中身を読めます。**
そのためビルドの途中で、個人が特定できる記述（実名・勤務先・学校・収入・健康・友人の名前・住所）を
含む項目を落としています。ルールは `aki-os/scripts/build_public_sites.py` の `BLOCK`。

- 「分析レポート」「トリセツ」「AIに渡す」の3タブは、**公開版には入っていません**
- 検索よけに `noindex` と `robots.txt` を置いていますが、**リポジトリが公開である以上、隠し場所ではありません**
- ⚠️ **一度pushしたものは、あとで消してもgitの履歴に残ります。** 迷ったら push しない
