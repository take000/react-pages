# react-pages
{}内は自分の環境によって変わります。
## Reactアプリの作成
```sh
$ create-react-app {project-name}
```

## gh-pagesのインストール
```sh
$ cd react-pages
$ npm install gh-pages --save-dev
```

## package.jsonに設定を追加
```json
//...
"homepage": "http://{user-name}.github.io/{project-name}"

"scripts": {
    //...
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
}
```

## GitHubにpush
まずpushする。
```sh
$ git init
$ git add -A
$ git commit -m "{commit-message}"
$ git remote add origin https://github.com/{user-name}/{project-name}.git
$ git push -u origin master
```

## デプロイ
GitHubPagesで表示できるようにする
```sh
$ npm run deploy
```