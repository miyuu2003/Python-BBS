# 基盤となるPythonのイメージを使用
FROM python:3.12-slim

# 作業ディレクトリを設定
WORKDIR /app

# 必要なライブラリをインストールするため、requirements.txtをコピー
COPY requirements.txt /app/

# 依存関係をインストール
RUN pip install --no-cache-dir -r requirements.txt

# ソースコードをコンテナにコピー
COPY . /app/

# ポート8000を公開
EXPOSE 8000

# サーバーを起動
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]