# Failed to connect to github.com port 443 after 75010 ms: Couldn't connect to server
## 报错
```
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git push origin main
fatal: unable to access 'https://github.com/huanhuan0728/DataStructure/': Failed to connect to github.com port 443 after 75010 ms: Couldn't connect to server
```
## 解决办法
看csdn说是网络配置造成的一直无法和github连接，终端、xcode和xcode都不能连接，但是网页是能直接访问GitHub的
```
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git config --global --get http.proxy
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git config --global --get https.proxy 

```
之后就能正常使用了

## 参考资料
https://blog.csdn.net/qq_27281247/article/details/135925956?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ECtr-2-135925956-blog-141175039.235%5Ev43%5Epc_blog_bottom_relevance_base4&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ECtr-2-135925956-blog-141175039.235%5Ev43%5Epc_blog_bottom_relevance_base4&utm_relevant_index=3
  
#连接github时使用token取代密码
## 报错 
```
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git push origin main
Username for 'https://github.com': 1477405138@qq.com
Password for 'https://1477405138@qq.com@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/huanhuan0728/DataStructure/'
```

### 描述
这里输入password的时候我输入了github账户的密码，查询报错后得知GitHub 在 2021 年 8 月 13 日之后已经不再支持通过用户名和密码进行身份验证。因此，不能再通过直接输入用户名和密码来推送代码。GitHub 推荐使用 个人访问令牌 (Personal Access Token) 或 SSH 来代替传统的密码认证。

## 解决办法
使用token代替password登录
### token的获取方法
1. 前往https://github.com/settings/tokens
2. general a new token （classical）
3. 设置note（大概描述这个token拿来干嘛？），选择repo和delete_repo权限
4. **保存密钥**密钥只会出现一次

















