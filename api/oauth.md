# OAuth

## 获取code
GET https://server.jx3box.com/oauth/jx3box/authorize  
params_name|value|ex
---|---|--- 
client_id | varchar | j3pz
redirect_uri | varchar | https://j3pz.com

*=> 跳转至callback并附带code*

## 获取token
GET https://server.jx3box.com/oauth/jx3box/access_token  
params_name|value|ex
---|---|--- 
client_id | varchar | j3pz
client_secret | varchar | ****
code | varchar | 上一步返回的code

*=> 会直接返回token和uid,如无需查询资料的情况下,可只使用uid创建*

## 获取资料
GET https://server.jx3box.com/user/info  
params_name|value|ex
---|---|--- 
uid | int | 8

*=> 此接口无需使用token*