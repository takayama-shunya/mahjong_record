# Node.jsの公式イメージをベースにする
FROM node:16

# 作業ディレクトリを設定
WORKDIR /app

# ローカルのfrontendディレクトリをコンテナ内の/appディレクトリにコピー
COPY . /app

# パッケージをインストール
RUN npm install

# アプリケーションをビルド
RUN npm run build

# ポートを公開
EXPOSE 3000

# コンテナ起動時にReactサーバーを実行
CMD ["npm", "start"]