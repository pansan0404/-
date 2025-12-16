# 修論プロジェクト

このプロジェクトはOverleafとGitHubを連携させて、ローカルPCとOverleafの両方で編集できるように設定されています。

## セットアップ手順

### 1. GitHubリポジトリの作成

1. GitHubにログインして、新しいリポジトリを作成します
2. リポジトリ名を設定（例: `thesis`）
3. **重要**: リポジトリは**空の状態**で作成してください（README、.gitignore、ライセンスは追加しない）

### 2. ローカルリポジトリをGitHubに接続

以下のコマンドを実行してください（`YOUR_USERNAME`と`YOUR_REPO_NAME`を実際の値に置き換えてください）：

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git add .
git commit -m "Initial commit"
git push -u origin main
```

### 3. OverleafでのGitHub連携設定

1. Overleafにログインして、プロジェクトを開きます
2. 左側のメニューから「**Menu**」をクリック
3. 「**Git**」を選択
4. 「**Link GitHub Account**」をクリックしてGitHubアカウントを連携
5. 「**Push to GitHub**」または「**Pull from GitHub**」を選択して、GitHubリポジトリを選択
6. リポジトリを選択して「**Link**」をクリック

### 4. 作業フロー

#### Overleafで編集した場合
1. Overleafで編集・保存
2. 「**Menu**」→「**Git**」→「**Push to GitHub**」をクリック
3. コミットメッセージを入力して「**Push**」

#### ローカルPCで編集した場合
1. ローカルでファイルを編集
2. 以下のコマンドを実行：
```bash
git add .
git commit -m "変更内容の説明"
git push origin main
```
3. Overleafで「**Menu**」→「**Git**」→「**Pull from GitHub**」をクリックして変更を取得

#### GitHubから最新の変更を取得する場合（ローカル）
```bash
git pull origin main
```

## 注意事項

- **競合を避けるため**、編集前に必ず最新の変更を取得（pull）してください
- Overleafとローカルの両方で同時に編集しないように注意してください
- コミットメッセージは変更内容が分かるように記述してください

## ファイル構成

- `.gitignore`: Gitで管理しないファイル（LaTeXの一時ファイルなど）を指定
- `README.md`: このファイル

