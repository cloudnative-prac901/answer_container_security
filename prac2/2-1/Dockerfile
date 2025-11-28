FROM python:3.12-alpine

# ユーザー追加
RUN adduser -D appuser
# ワークディレクトリ
WORKDIR /app

# 簡易アプリ
COPY <<'APP' app.py
print("Hello Secure World!")
APP
USER appuser

# 起動時にメッセージを表示してから待機
CMD ["sh", "-c", "python3 app.py && sleep infinity"]

