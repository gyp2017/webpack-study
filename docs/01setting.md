# 1 설정


## 1.1 yarn 확인
package manager [yarn](https://yarnpkg.com/)
```sh
$ yarn --version
0.19.1
```


## 1.2 yarn init
`package.json` 파일이 생성
```sh
$ yarn init
```


## 1.3 add lodash
library [lodash](https://lodash.com/)
```sh
$ yarn add lodash
```

`package.json`
```json
{
  ...
  "dependencies": {
    "lodash": "^4.17.4"
  }
}
```

## 1.4 add webpack
bundler [webpack 2](https://webpack.js.org/)
```sh
$ yarn add webpack@beta --dev
```

`package.json`
```json
{
  ...
  "dependencies": {
    "lodash": "^4.17.4"
  },
  "devDependencies": {
    "webpack": "beta"
  }
}
```
