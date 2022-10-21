## 1. 找不到模块“./App.vue”或其相应的类型声明

根目录新建tsconfig.json 

```json
{
  "compilerOptions": {
    "target": "esnext",
    "module": "esnext",
    "strict": false,
    "jsx": "preserve",
    "moduleResolution": "node"
 }
```

