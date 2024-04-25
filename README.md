# eslint-config-pnix

ESLint configurations based on pnix style guide

## Installation
```
npm install @wemade-phoenix/eslint-config-pnix@1.0.0
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
3. vscode 에디터에 설치한 prettier가 동작하여 충돌이 일어나 원하는 동작이 이뤄지지 않을 수 있습니다. 에디터내 prettier 비활성화 해주세요.

## Usage
### 1. eslintrc.js

##### Javascript
```javascript
module.exports = {
  extends: [
    '@wemade-phoenix/pnix'
    '@wemade-phoenix/pnix/prettier'
  ]
}
```

##### Javascript + React
```js
module.exports = {
  extends: [
    '@wemade-phoenix/pnix',
    '@wemade-phoenix/pnix/react',
    '@wemade-phoenix/pnix/prettier'
  ],
}
``` 


##### Typescript + React
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
### 2.tsconfig.json
```
"include": [
    ".eslintrc.js",
    "src"
  ]
  ```
  



