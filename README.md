# GridSplit Downloader

日本語 / English

公開URL / Live site:  
https://tarosay.github.io/image-grid-splitter/

---

## 日本語

GridSplit Downloader は、画像を **n×n** に分割し、左上から右下へ連番を付けて、**ZIPファイルで一括ダウンロード** できるシンプルなWebツールです。

現在は GitHub Pages で公開しています。  
**Live site:** https://tarosay.github.io/image-grid-splitter/

### 主な機能

- 画像ファイルを選択して読み込み
- ドラッグ&ドロップ対応
- `n` を指定して **n×n 分割**
- 左上から右下へ連番付与
- `sample_001.png` のようなファイル名で保存
- 分割結果を **ZIP形式で一括ダウンロード**
- ブラウザ内処理のみで完結
- GitHub Pages で公開可能

### 公開ファイル構成

    index.html
    README.md
    LICENSE
    favicon.svg
    og-image.png

### 使い方

1. サイトを開く
2. 画像ファイルを選択する、またはドラッグ&ドロップする
3. 分割数 `n` を入力する
4. **ZIPでダウンロード** を押す
5. 分割済み画像が ZIP で保存される

### 出力ルール

- 画像は **n×n** に分割されます
- 連番は **左上から右下へ、行優先** で付与されます
- 出力ファイル名は元ファイル名を使って生成されます

例:

    sample.png
    ↓
    sample_001.png
    sample_002.png
    sample_003.png
    sample_004.png

### OGP と favicon

このリポジトリには以下を含みます。

- `favicon.svg`
- `og-image.png`

`index.html` には OGP / Twitter Card / favicon の設定を入れています。

### 注意

- 非常に大きな画像や極端に大きい `n` を指定すると、ブラウザのメモリ使用量が増えます
- 画像サイズより大きい `n` は指定できません
- 画像はサーバへ送信されません
- すべてブラウザ内で処理されます

### ライセンス

このプロジェクトは MIT License のもとで公開しています。  
詳細は [LICENSE](LICENSE) を参照してください。

---

## English

GridSplit Downloader is a simple web tool that splits an image into an **n×n** grid, assigns sequential filenames from top-left to bottom-right, and lets you **download all pieces as a ZIP file**.

It is currently published on GitHub Pages.  
**Live site:** https://tarosay.github.io/image-grid-splitter/

### Features

- Load an image file from your computer
- Drag and drop support
- Split the image into an **n×n** grid
- Sequential numbering from top-left to bottom-right
- Save files with names like `sample_001.png`
- Download all split images as a **ZIP file**
- Runs entirely in the browser
- Can be published on GitHub Pages

### Files

    index.html
    README.md
    LICENSE
    favicon.svg
    og-image.png

### Usage

1. Open the website
2. Select an image file or drag and drop it
3. Enter the split count `n`
4. Click **Download ZIP**
5. The split images will be downloaded as a ZIP file

### Output Rules

- The image is split into an **n×n** grid
- Filenames are assigned **row by row**, from top-left to bottom-right
- Output filenames are generated from the original filename

### OGP and favicon

This repository includes:

- `favicon.svg`
- `og-image.png`

The `index.html` file includes OGP, Twitter Card, and favicon metadata.

### Notes

- Very large images or very large `n` values may increase browser memory usage
- `n` cannot be larger than the image dimensions
- Images are not uploaded to any server
- Everything is processed locally in the browser

### License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.
