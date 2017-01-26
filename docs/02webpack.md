# 2 webpack

[babeljs modules](https://babeljs.io/learn-es2015/#ecmascript-2015-features-modules)

## 2.1 bar.js 파일 작성
`./src/bar.js`
```js
export default 'HiHello';
```


## 2.2 app.js 파일 작성
`./src/app.js`
```js
import _ from 'lodash';
import bar from './bar';

console.log(_.startCase(bar));
```

## 2.3 index.html 파일 작성
`./index.html`
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>test</title>
  </head>
  <body>
    <script src="./dist/bundle.js" charset="utf-8"></script>
  </body>
</html>
```

## 2.3 bundle 실행
```sh
$ ./node_modules/.bin/webpack /src/app.js /dist/bundle.js
```

`./dist/bundle.js` 파일 확인

## 2.4 server 스크립트 작성 & 실행
`package.json` 파일 수정
```json
{
  ...
  "scripts": {
    "server": "python -m SimpleHTTPServer 8000"
  }
  ...
}
```

```sh
$ yarn run server
```

```sh
$ open http://loaclhost:8000
```

## 2.5 bundle 스크립트 작성 & 실행
`package.json` 파일 수정
```json
{
  ...
  "scripts": {
    "server": "python -m SimpleHTTPServer 8000",
    "bundle": "webpack /src/app.js /dist/bundle.js"
  }
  ...
}
```

```sh
$ yarn run bundle
```
