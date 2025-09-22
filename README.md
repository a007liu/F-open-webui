```nginx
server {
        listen       8888;
        server_name  localhost;

        location / {
             proxy_pass http://127.0.0.1:5173/;
        }

        location /api/ {
          proxy_pass http://127.0.0.1:8080/api/;
        }

        location /ollama/ {
          proxy_pass http://127.0.0.1:8080/ollama/;
        }

        location /openai/ {
          proxy_pass http://127.0.0.1:8080/openai/;
        }
    }
```

* 启动nginx
* 修改constants端口为 8888
* 启动后台 `open-webui serve`
* `npm install` `npm run dev`
* static/static文件夹
    * 替换favicon.ico、favicon.png
    * 删除favicon-dark、favicon-96*96、favicon.svg
    * 替换logo.png
    * 删除splash.png、splash-dark.png
* 全局搜索.py文件
  * Open Webui 替换为 Fawer AI
* 全局搜索.svelte文件
  * Open Webui 替换为 Fawer AI
* 修改constants App-name
* 修改+layout.svelte 的 await WEBUI_NAME.set('富奥智慧AI助手');
* 修改登录页面
* 修改title
* 修改loading
* 删除关于 等无用信息
