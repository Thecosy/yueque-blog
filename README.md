### YQBlog 是一个基于语雀文档开放接口开发的极简博客系统

### 技术原理
+ 通过语雀开放接口获取文章信息并渲染。
+ 通过反向代理CDN实现语雀静态资源的展示。
+ 通过acme实现自动https证书

### 设计初衷
+ 折腾各种博客系统，各种模板眼花缭乱，很多时候在选择博客模板上花费了巨量的时间。希望回归博客的本质：专注于写作而非专注于博客本身。
+ 语雀的编辑功能是目前写作体验最好的。但是不支持域名绑定， 且官方的博客知识库只能单知识库发布，想要分类只能靠目录。而实际场景需要多知识库来对内容进行分类。
+ 希望文章完成写作即发布，无需构建deploy过程。无需繁重的各种配置、样式适配。
+ 不用关心闹心的图床问题，直接粘贴图片发布到语雀即可。
+ YQBlog一次部署好之后，可以遗忘， 专注的创作即可。博客内容创作即所得。

### 功能介绍
+ 基于语雀文档开放API实现， 在语雀中编辑文档，博客即所得。
+ 自动维护https证书，通过autoSSL参数控制https开关
+ 支持主题， 虽然目前仅有唯一的一个极简(懒)主题，其实YQBlog的主题很容易做， 参照themes中的四个html文件的实现即可。欢迎贡献。


### 为什么不用 xxx ？？？
+ wordpress
    + 过于臃肿
    + markdown编辑体验差是硬伤，编辑器支持的markdown样式发布后会变成另外一个样子。
    + 速度慢。
    
+ hexo等静态博客系统
    + 折腾成本较高
    + 编辑完文章需要构建发布
    + 让人头痛的图床问题
    + 管理文章心累
    + 编辑体验不好
  
+ github pages
  + 慢
  + 需要hexo等静态博客方案，所以具有其所有缺点。