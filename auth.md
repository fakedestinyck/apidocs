## 鉴权说明

### SSO
默认单点登录地址 v2.jx3box.com/account/login   
所有鉴权服务接口，请先在 v2.jx3box.com/account/login 进行登录

### Token
1. 分配`.jx3box.com`跨域cookie，cookie name 为 `token` 
2. 同时会给`v2.jx3box.com`的localstorage添加`token`项

### 本地模拟
#### 方式一 : 通过Cookie效验,绑定本地测试域
1. 通过nginx反代**xxx.jx3box.com**至**localhost:8080**
```nginx
location /
{
    if ($request_uri ~* "(php|jsp|cgi|asp|aspx)")
    {
         expires 0;
    }
    proxy_pass http://127.0.0.1:8080;
    proxy_set_header Host 127.0.0.1;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header REMOTE-HOST $remote_addr;

    add_header X-Cache $upstream_cache_status;
    
    proxy_set_header Accept-Encoding "";
	
    sub_filter_once off;
    
    proxy_cache cache_one;
    proxy_cache_key $host$uri$is_args$args;
    proxy_cache_valid 200 304 301 302 12h;
}
```
2. 异步请求设置`witCredentials = true` 

#### 方式二 : 通过Basic Auth校验
1. 通过`localstorage.getItem('token')`拿到本地token
2. 异步请求中设置basic auth请求头，将token附加在username中
目前 server.jx3box.com 的接口会优先校验basic auth的token，但其它后端服务API是否有部署相应鉴权方式需以相应接口文档为准。

对于跨主域(.jx3box.com)项目的接口只能使用方式二进行校验。  
相关cookie过期，重登录引导等，可使用已封装的前端[User](https://github.com/JX3BOX/apidocs/blob/master/api/user.md)模块。