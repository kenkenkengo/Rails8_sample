# Rails 8 App

以下コマンドで作成したサンプルプロジェクトです。

```
rails-new -u 3.3.6 -r 8.0.0 rails8app --devcontainer -d mysql --api --skip-kamal
```

以下の設定で開発します。

- db は mysql を用いており、api モードを使います。
- kamal はスキップしています。
- devcontainer を使用して開発します。

# setup

command + shift + p で Rebuild and Reopen in Container を選択し、backend を選択してください。
すると、devcontainer が起動し、他のコンテナも起動します。
リモートエクスプローラーで、frontend-client を新しいウィンドウで開いてください。

# frontend-client

frontend-client のコンテナ で npm などを用いて nuxt や vite などでプロジェクトを作成してください。
その後、frontend-client/devcontainer.json の postCreateCommand を npm install などで適切に設定してください。
vite.config.ts や nuxt.config.ts などの dev server における backend へのプロキシ設定の際は、`http://backend:3000` を参照先にしてください。（localhost ではなくサービス名を使う）
この指定により、コンテナ間の名前解決が可能です。
https://docs.docker.com/compose/how-tos/networking/

# backend

既にソースコードが作成されているので、開発可能です。
