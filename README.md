# GridSplit Downloader

日本語 / English

---

## 日本語

GridSplit Downloader は、画像を **n×n** に分割し、左上から右下へ連番を付けて、**ZIPファイルで一括ダウンロード** できるシンプルなWebツールです。

GitHub Pages でそのまま公開できるように、**単一の `index.html`** で動作します。

### 主な機能

- 画像ファイルを選択して読み込み
- ドラッグ&ドロップ対応
- `n` を指定して **n×n 分割**
- 左上から右下へ連番付与
- `sample_001.png` のようなファイル名で保存
- 分割結果を **ZIP形式で一括ダウンロード**
- ブラウザ内処理のみで完結
- GitHub Pages で公開可能

### デモ

GitHub Pages で公開後、以下のURLで利用できます。

    https://YOUR_GITHUB_USERNAME.github.io/image-grid-splitter-web/

### ファイル構成

    index.html
    README.md
    LICENSE

### 使い方

1. サイトを開く
2. 画像ファイルを選択する、またはドラッグ&ドロップする
3. 分割数 `n` を入力する
4. **ZIPでダウンロード** を押す
5. 分割済み画像がZIPで保存される

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

`n=2` の場合は 4枚、`n=3` の場合は 9枚、`n=4` の場合は 16枚です。

### 動作仕様

- ブラウザで画像を読み込みます
- JavaScript で画像を分割します
- 分割した各画像を ZIP にまとめます
- サーバへ画像を送信せず、**ローカル処理のみ** で完結します

### GitHub Pages での公開方法

#### 1. リポジトリを作成

例:

    image-grid-splitter-web

#### 2. ファイルを配置

リポジトリのルートに以下を置きます。

    index.html
    README.md
    LICENSE

#### 3. GitHub に push

    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/YOUR_GITHUB_USERNAME/image-grid-splitter-web.git
    git push -u origin main

#### 4. GitHub Pages を有効化

GitHub の以下を設定します。

- **Settings**
- **Pages**
- **Build and deployment**
- **Source: Deploy from a branch**
- **Branch: main / root**

#### 5. 公開URL

数分後に以下のようなURLで公開されます。

    https://YOUR_GITHUB_USERNAME.github.io/image-grid-splitter-web/

### 依存関係

このツールは以下を使用しています。

- JSZip

`index.html` 内で CDN 読み込みしています。

### 注意

- 非常に大きな画像や極端に大きい `n` を指定すると、ブラウザのメモリ使用量が増えます
- 画像サイズより大きい `n` は指定できません
- 対応形式は、ブラウザが読み込める一般的な画像形式です
- 出力形式は元画像の拡張子をできるだけ維持します
  （対応外拡張子の場合は `png` として保存します）

### ライセンス

このプロジェクトは MIT License のもとで公開しています。

詳細は [LICENSE](LICENSE) を参照してください。

---

## English

GridSplit Downloader is a simple web tool that splits an image into an **n×n** grid, assigns sequential filenames from top-left to bottom-right, and lets you **download all pieces as a ZIP file**.

It is designed to run as a **single `index.html` file**, making it easy to publish on GitHub Pages.

### Features

- Load an image file from your computer
- Drag and drop support
- Split the image into an **n×n** grid
- Sequential numbering from top-left to bottom-right
- Save files with names like `sample_001.png`
- Download all split images as a **ZIP file**
- Runs entirely in the browser
- Can be published on GitHub Pages

### Demo

After publishing with GitHub Pages, the site will be available at:

    https://YOUR_GITHUB_USERNAME.github.io/image-grid-splitter-web/

### Files

    index.html
    README.md
    LICENSE

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

Example:

    sample.png
    ↓
    sample_001.png
    sample_002.png
    sample_003.png
    sample_004.png

If `n=2`, 4 images are generated.  
If `n=3`, 9 images are generated.  
If `n=4`, 16 images are generated.

### How It Works

- The browser loads the image
- JavaScript splits the image into pieces
- All pieces are packed into a ZIP file
- No server upload is required; everything is processed locally in the browser

### GitHub Pages Deployment

#### 1. Create a repository

Example:

    image-grid-splitter-web

#### 2. Add the files

Place the following files in the root of the repository:

    index.html
    README.md
    LICENSE

#### 3. Push to GitHub

    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/YOUR_GITHUB_USERNAME/image-grid-splitter-web.git
    git push -u origin main

#### 4. Enable GitHub Pages

In GitHub, go to:

- **Settings**
- **Pages**
- **Build and deployment**
- **Source: Deploy from a branch**
- **Branch: main / root**

#### 5. Published URL

After a few minutes, your site will be available at:

    https://YOUR_GITHUB_USERNAME.github.io/image-grid-splitter-web/

### Dependencies

This project uses:

- JSZip

It is loaded via CDN inside `index.html`.

### Notes

- Very large images or very large `n` values may increase browser memory usage
- `n` cannot be larger than the image dimensions
- Supported formats depend on what the browser can load
- The output format keeps the original extension when possible
  (unsupported extensions are saved as `png`)

### License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for details.
