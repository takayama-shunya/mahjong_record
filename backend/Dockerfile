# Pythonの公式イメージをベースにする
FROM python:3.8.3

# set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# 作業ディレクトリを設定
WORKDIR /app

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    python3-dev \
    default-libmysqlclient-dev \
    && rm -rf /var/lib/apt/lists/*

# ローカルのbackendディレクトリをコンテナ内の/appディレクトリにコピー
COPY ./backend/ /app/

# Pythonの依存パッケージをインストール
RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt

# ポートを公開
EXPOSE 8000
