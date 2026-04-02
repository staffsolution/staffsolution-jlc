# GitHub Pages セットアップ手順（JLC）

## 1. GitHubでリポジトリを作る

1. https://github.com/new を開く（staffsolution アカウントでログイン済みの状態で）
2. 以下の設定で作成：
   - **Repository name**: `staffsolution-jlc`
   - **Visibility**: Public
   - Initialize README：チェックしない
3. 「Create repository」をクリック

## 2. このフォルダ（docs-jlc）を push する

Cursor のターミナルで以下を実行：

```bash
cd "/Volumes/OWC Envoy Pro FX/w-work/s-スタッフソリューション/staffsolution_cursor/docs-jlc"
git init
git add .
git commit -m "初回：JLC 運営ナレッジサイト"
git branch -M main
git remote add origin https://github.com/staffsolution/staffsolution-jlc.git
git push -u origin main
```

## 3. GitHub Pages を有効にする

1. https://github.com/staffsolution/staffsolution-jlc を開く
2. **Settings → Pages**
3. Source：「Deploy from a branch」
4. Branch：`main` / Folder：`/ (root)`
5. 「Save」

## 4. 公開URL

```
https://staffsolution.github.io/staffsolution-jlc/
```

設定後 1〜2 分で公開されます。

---

## コンテンツを追加するときのルール

### グルコン議事録を追加する場合

1. `グルコン/` に MD ファイルを置く
   - 例：`グルコン/20260410_グルコン議事録.md`
2. `グルコン/index.md` にリンクを追記する
3. `git add . && git commit -m "グルコン議事録追加 20260410" && git push`

### 成果事例シェア会を追加する場合

1. `成果事例シェア会/YYYY-MM/` に MD ファイルを置く
   - 例：`成果事例シェア会/2026-04/シェア会_20260XXX_氏名.md`
2. `成果事例シェア会/index.md` にリンクを追記する
3. `git add . && git commit -m "成果事例シェア会追加 20260XXX" && git push`

> **注意**：`JLC/運営/` 内の元ファイルを編集した場合、`docs-jlc/` 側にも同じファイルをコピーしてから push する。
