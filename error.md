# Failed to connect to github.com port 443 after 75010 ms: Couldn't connect to server
## 报错
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git push origin main
fatal: unable to access 'https://github.com/huanhuan0728/DataStructure/': Failed to connect to github.com port 443 after 75010 ms: Couldn't connect to server

## 解决办法
看csdn说是网络配置造成的一直无法和github连接，但是网页是能直接访问GitHub的
```
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git config --global --get http.proxy
(base) xuhuanlu@xuhuandeMacBook-Pro tree % git config --global --get https.proxy 

```
之后就能正常使用了

## 参考资料
https://blog.csdn.net/qq_27281247/article/details/135925956?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ECtr-2-135925956-blog-141175039.235%5Ev43%5Epc_blog_bottom_relevance_base4&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ECtr-2-135925956-blog-141175039.235%5Ev43%5Epc_blog_bottom_relevance_base4&utm_relevant_index=3
  
