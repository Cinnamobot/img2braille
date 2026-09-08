# img2braille

画像 → Unicode点字アスキーアート（U+2800〜U+28FF）。単一 `index.html`、サーバ不要。

## 使い方
1. 画像をドロップ / クリック選択 / ペースト
2. 幅（数値指定で上限なし・10万文字まで、簡易スライダは10〜600）・明るさ・コントラスト・ガンマ・ディザ等を調整（自動再変換）
3. 「全画面で見る」で画面いっぱいに展開（画面フィットの最大フォントで表示）
4. コピー or TXT保存

## ローカル確認
```sh
python -m http.server 8000
# http://localhost:8000/
```

## GitHub Pages 公開
1. このフォルダを `img2braille` リポジトリとして push
2. Settings → Pages → Deploy from a branch → `main` / `/ (root)`
3. `https://<user>.github.io/img2braille/` で公開

## 仕様要点
詳細は `REQUIREMENTS.md`。1文字=2×4ドット、高さ=幅×縦横比÷2×補正、空白は U+2800。
