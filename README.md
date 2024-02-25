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
```
"start:dev": "nodemon --watch 'src/' --exec 'ts-node src/index.ts' -e ts"
```
- 