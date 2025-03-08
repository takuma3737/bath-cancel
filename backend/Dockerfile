FROM golang:1.24-alpine

# 作業ディレクトリを設定
WORKDIR /app

# Airをインストール
RUN go install github.com/air-verse/air@latest

# アプリケーションのソースコードをコピー
COPY . .

# 依存関係のインストール
RUN go mod download

# ポートを公開
EXPOSE 8080

# Airを使用してアプリケーションを起動
CMD ["air", "-c", ".air.toml"]
