---

title: vue

tags: 基础命令

---

# 1、plugins

```cmd
# axios
npm install axios
# NPM
npm install element-plus --save
```

# 2、Element-plus

```ts
// main.ts
import { createApp } from 'vue'
import ElementPlus from 'element-plus'
import 'element-plus/dist/index.css'
import App from './App.vue'

const app = createApp(App)

app.use(ElementPlus)
app.mount('#app')
```

## 自动导入

```
npm install -D unplugin-vue-components unplugin-auto-import
```

## vite.config.ts

```ts
import { defineConfig } from 'vite'
import AutoImport from 'unplugin-auto-import/vite'
import Components from 'unplugin-vue-components/vite'
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers'

export default defineConfig({
  // ...
  plugins: [
    // ...
    AutoImport({
      resolvers: [ElementPlusResolver()],
    }),
    Components({
      resolvers: [ElementPlusResolver()],
    }),
  ],
})
```

# 3、plugins

https://devtools.vuejs.org/guide/installation.html

# 4、vue3

## 1、TS





## 2、vue

### 计算属性

```ts
<script setup lang="ts">
const fullName = computed(() => {
	return lastName.value + firstName.value
})
</script>
```

### xhr

```ts
<script setup lang="ts">
//	fetch xhr XMLHttpRequest
    
const xhr = new XMLHttpRequest()
xhr.onload = function() {
	//	接收响应
    res = xhr.response()
}
//	发请求
xhr.open('GET', URL)
xhr.reponseType = 'json'
xhr.send()


</script>
```

#### function

```ts
try {
    const resp = await get("")
} catch (e) {
    console.error(e)
}
function get(url: string) {
    return new Promise( (resolve, reject) => {
        const xhr = new XMLHttpRequest()
        xhr.onload = function() {
            //	接收响应
            if(xhr.status === 200) {
                resolve(xhr.response)
            } else {
                reject(xhr.response)
            }
        }
        //	发请求
        xhr.open('GET', URL)
        xhr.reponseType = 'json'
        xhr.send()
    })
}
```

### axios

#### 安装

```cmd
npm install axios
```

#### 封装使用

```ts
<script setup lang="ts">
import axios from 'axios'

async function get() {
    const resp = await axios.get(url)
}

</script>   
```

.env.production - 生产

.env.development - 开发

```
VITE_BACKEND_API_BASE_URL = ''
```



### onMounted - 页面组件加载完成后执行

```ts
onMounted(() => {
	get
})
```

