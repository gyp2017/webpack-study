# 3 webpack.config.js

## 3.1 설정 파일 작성
`./webpack.config.js`
```js
module.exports = {
  entry: './src/app.js',
  output: {
    filename: 'bundle.js',
    path: './dist'
  }
}
```

`package.json` 파일 수정
```json
{
  ...
  "scripts": {
    "server": "python -m SimpleHTTPServer 8000",
    "bundle": "webpack"
  }
  ...
}
```

`webpack --config webpack.config.js` 기본 설정
