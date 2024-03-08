# eslint-config-pnix

ESLint configurations based on pnix style guide

## Installation
```
npm install @wemade-phoenix/eslint-config-pnix@1.0.0
```

## Usage
.eslintrc.js

### Javascript
```javascript
module.exports = {
  extends: [
    '@wemade-phoenix/pnix'
    '@wemade-phoenix/pnix/prettier'
  ]
}
```

#### Javascript + React
```js
module.exports = {
  extends: [
    '@wemade-phoenix/pnix',
    '@wemade-phoenix/pnix/react',
    '@wemade-phoenix/pnix/prettier'
  ],
}
``` 


#### Typescript + React
```javascript
module.exports = {
  extends: [
    '@wemade-phoenix/pnix',
    '@wemade-phoenix/pnix/typescript',
    '@wemade-phoenix/pnix/react',
    '@wemade-phoenix/pnix/prettier'
  ]
}
```
#### tsconfig.json
```
"include": [
    ".eslintrc.js",
    "src"
  ]
  ```
  
## Note
#### ✅ 프로젝트에서 `.prettierrc` 파일은 생략해도 됩니다.
ESLint의 Prettier를 사용하는 방식으로 별도의 Prettier 설정 파일은 생성하지 않아도 됩니다.

1. 만약 파일 저장 시 자동 포맷이 적용되지 않는다면, 기본 포맷터를 ESLint로 설정해야 합니다.

2. settings.json에 아래 내용 있는지 확인해주세요

```
"eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],
```



