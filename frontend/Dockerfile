# Node.jsのイメージを基に作成
FROM node:14

# 作業ディレクトリを設定
WORKDIR /app

# パッケージ管理ファイルをコンテナにコピー
COPY package.json /app/
COPY package-lock.json /app/

# 依存関係をインストール
RUN npm install

# ソースコードをコピー
COPY . /app/

# アプリケーションのポート3000を公開
EXPOSE 3000

# 開発サーバーを起動
CMD ["npm", "start"]
