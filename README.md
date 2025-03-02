# Next.js (App Router) チュートリアルお試し環境  

## 概要
- Next.js (App Router) チュートリアルに取り組むための Docker 環境を用意しました。  
- Dockerfile で npm install -g pnpm をしているので、Dockerコンテナを起動したら、すぐ create-next-app を試せます。  

## 参照
Next.js の App Router のチュートリアル  
https://nextjs.org/learn/dashboard-app  

## 起動、利用方法
- Macで動作確認しています。(WSL だとファイルを修正するときに対処が必要かもしれません)  
- Github からダウンロードしたら以下を実行  
  ```
    # ダウンロードして配置したディレクトリへ
  $ cd next_js_tutorial/

    # ビルド～起動 (ビルドのときに pnpm がインストールされます)
  $ docker compose up

    # 以下は別のウィンドウで実行
  $ docker ps    # next_js_tutorial が Up 状態になっていれば OK
  $ docker exec -it next_js_tutorial ash    # Docker コンテナのシェル起動

    # 以下は Docker コンテナのシェルで実行
  $ npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm

    ※あとは、cd nextjs-dashboard して、、チュートリアルの内容のとおりに進めていきます
  ```
