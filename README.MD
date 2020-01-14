# Parcel Experiments

Test

## env setting
1. yarn global add parcel
2. git init && git remote add origin ${github url} && git pull origin master
3. yarn init -y
4. yarn add react react-dom
5. yarn add babel-preset-env babel-preset-react --dev
6. .babelrc 생성 및 아래 코드 추가
```
{
    "presets": ["env", "react"]
}
```
7. index.js
App.js 생성후 아래코드 추가
```
import React from "react";
import ReactDom from "react-dom";
import App from "./src/App";

ReactDom.render(<App />, document.getElementById('app'));
```
6. index.html
body 에 아래 코드 추가
```
<body>
    <div id="app"></div>
    <script src="./index.js"></script>
</body>
```
7. package.json 에 scripts 항목 추가
```
"scripts": {
    "start": "parcel index.html",
    "build": "parcel build index.html -d build --public-url ./"
}
```

## Feater

- React
- ES6 with Babel
- SCSS
- CSS Modules
- Typography.js
- Build for production (--public-url=http://amazon.com/ 옵션은 src="http://amazon.com/" frefix 해줌)
