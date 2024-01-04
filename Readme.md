这是一个基于 Giscus 的个人博客评论仓库, 除此之外, 没有其他用途.

### Butterfly 中的 giscus 配置

下面是配置 Butterfly 中配置 Giscus 步骤:

1. 在 github 上新开一个公共的项目: https://github.com/unlessbamboo/blog.unusebamboo.top
2. 按照https://giscus.app/zh-CN提示的步骤一步步进行设置调整:

- 设置项目为公开
- 为该项目安装 giscus app
- 在项目中开启 Discussions

3. 在`https://giscus.app/zh-CN`页面的仓库中输入 unlessbamboo/blog.unusebamboo.top, 该网站会自动识别输入的仓库是否正确, 如果没有问题, 在下方选择好推荐的`公告`分类, 选择特性, 那么在`启用giscus`就会出现专属于当前项目的 script 信息, 里面包含的 repo, `repo-id`, `category-id`等重要信息

至此在 github 的配置完成, 此时还需要这些信息放到 Butterfly 中, 在\_config.butterfly.yml 中找到 Comments, 设置如下配置:

```yml
comments: # 通用设置
  use: Giscus
  text: true
  lazyload: false
  count: false
  card_post_count: false

giscus:
  repo: unlessbamboo/blog.unusebamboo.top
  repo_id: xxxxid
  category_id: ccccccid
  theme:
    light: light
    dark: dark
  option:
```

之后重启整个 hexo 就能看到文章最下方有评论了.
