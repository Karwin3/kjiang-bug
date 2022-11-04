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

## 2.  ‘defineProps‘ is not defined

```tex
查看 eslint-plugin-vue 是否安装
npm install --save-dev eslint eslint-plugin-vue

Step 1. 检查 eslint-plugin-vue 的版本
npm list eslint-plugin-vue
若版本在 v8.0.0 以上，跳转到 Step 2，否则直接到 Step 3 的内容。

Step 2. eslint-plugin-vue版本为 v8.0.0+
打开 .eslintrc.js 文件并修改如下：
env: {
node: true,
// The Follow config only works with eslint-plugin-vue v8.0.0+
"vue/setup-compiler-macros": true,
},

Step 3. eslint-plugin-vue版本为 v8.0.0 以下
打开 .eslintrc.js 文件并修改如下：

// The Follow configs works with eslint-plugin-vue v7.x.x
globals: {
defineProps: "readonly",
defineEmits: "readonly",
defineExpose: "readonly",
withDefaults: "readonly",
},
```

