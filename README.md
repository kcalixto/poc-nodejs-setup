# poc-nodejs-setup

- npm init -y
- yarn add typescript @types/node
- npx tsc --init
- tsconfig.json

```json
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "src",
    "outDir": "./dist",
    "moduleResolution": "node",
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}
```

- yarn add -D ts-node nodemon
- added start:dev script

```json
"start:dev": "nodemon --watch 'src/' --exec 'ts-node src/index.ts' -e ts"
```

- yarn add -D prettier eslint
- npx eslint --init
  - To check syntax and find problems
  - JavaScript modules (import/export)
  - None of these
  - Yes
  - Node
  - JSON
  - Yes
- add jest in eslint env

```json
    "env": {
        "es2021": true,
        "node": true,
        "jest": true
    },
```

- add tsconfig in eslint

```json
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module",
        "project": ["./tsconfig.json"]
    },
```

- add .prettierrc.json file

```json
{
  "semi": false,
  "singleQuote": true,
  "tabWidth": 2
}
```

- yarn add -D eslint-config-prettier
- add prettier in extends

```json
    "extends": [
        "eslint:recommended",
        "plugin:@typescript-eslint/recommended",
        "prettier"
    ],
```
