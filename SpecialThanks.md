# 特别感谢

## 背景图图源API

[2X.NZ 二叉树树的博客](https://2x.nz/posts/acg-randompic-api/)

```
博客用的API端点： https://eopageapi.2x.nz/pic?img=ua （EdgeOne Pages Functions）
新版实现

图源存放在 cnb.cool ，如 https://cnb.cool/2x.nz/r3/-/git/raw/main/ri/h/1.webp 。分为横屏和竖屏随机图，统一重命名为 数字.webp ，如 2333.webp 。关于重命名插件的编写，可以参阅：这里

EdgeOne Pages Functions作为入口，当收到请求后首先区分 横屏、竖屏、自适应，即 ?img=h ?img=v ?img=ua ，然后内部随机出一个数字，最大值在代码中硬编码并且代理请求 https://cnb.cool/2x.nz/r3/-/git/raw/main/ri/h|v/*.webp ，其中，代理请求设置一个独特的 Accept 请求头来绕过防盗链。从而使客户端能得到正确的图片响应，关于更多详情，请参考源码： EdgeOne_Function_PicAPI/functions/pic.js at main · afoim/EdgeOne_Function_PicAPI
```