FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Asia/Tokyo

# Node.jsとnpmをインストール
RUN apt-get update && apt-get install -y nodejs npm

# 作業ディレクトリを設定
WORKDIR /app

# package.jsonをコピーして依存関係をインストール
COPY package.json .
RUN npm install

# アプリケーションのソースコードをコピー
COPY . .


# ポートを公開
EXPOSE 3000

# 開発サーバーを起動
CMD ["npm", "run", "serve"]
