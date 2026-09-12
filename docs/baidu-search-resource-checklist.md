# 百度搜索资源平台操作清单

最后更新：2026-09-12

## 前置条件

- [ ] `https://qingwushan.cn/` 使用有效且覆盖 `qingwushan.cn` 的证书
- [ ] `http://qingwushan.cn/` 自动 301 或 308 跳转到 HTTPS
- [ ] GitHub Pages 已开启 Enforce HTTPS
- [ ] `robots.txt`、`sitemap.xml` 与下方全部正式页面返回 200
- [ ] 没有 `noindex`、`nofollow` 或 `X-Robots-Tag` 抓取限制

HTTPS 未完成前，不进行百度站点验证、Sitemap 提交或普通收录提交。

## 添加网站

1. 登录百度搜索资源平台，进入“用户中心 / 站点管理”。
2. 添加站点：`https://qingwushan.cn/`。
3. 协议必须选择 HTTPS，站点领域按平台当期选项选择与品牌官网最接近的分类。
4. 选择平台提供的网站验证方式。

## 验证文件位置

若选择 HTML 文件验证：

1. 从百度平台下载它实时生成的验证文件，不要修改文件名或内容。
2. 将文件放在 GitHub Pages 发布根目录，与 `CNAME`、`robots.txt`、`sitemap.xml` 同级。
3. 发布后先在浏览器打开百度给出的完整验证 URL，确认返回 200 且内容一致。
4. 再回到百度平台点击“完成验证”。

本仓库没有创建虚构的验证文件或验证码。取得百度实际文件后再添加。

## Sitemap 提交

验证通过后，在“搜索服务 / 普通收录 / Sitemap”提交：

- `https://qingwushan.cn/sitemap.xml`

提交后记录平台显示的抓取时间、状态与错误信息；不要反复删除后重提。

## 普通收录 URL 清单

- `https://qingwushan.cn/`
- `https://qingwushan.cn/brand/`
- `https://qingwushan.cn/matcha/`
- `https://qingwushan.cn/faq/`
- `https://qingwushan.cn/cooperation/`
- `https://qingwushan.cn/knowledge/`
- `https://qingwushan.cn/knowledge/what-is-qingwushan/`
- `https://qingwushan.cn/knowledge/tongren-matcha/`
- `https://qingwushan.cn/knowledge/matcha-vs-green-tea-powder/`
- `https://qingwushan.cn/knowledge/how-to-prepare-matcha/`
- `https://qingwushan.cn/knowledge/how-to-store-matcha/`

优先提交首页、品牌页、产品页、FAQ、合作页和5篇知识文章；知识中心入口可一并提交。收录工具只用于发现 URL，不保证收录或排序。

## 提交后检查

- [ ] 百度平台能够正常读取 Sitemap
- [ ] Sitemap 解析的 URL 数量为 11
- [ ] 抓取诊断返回正式页面，而不是 GitHub 404 页面
- [ ] 页面 canonical 与提交 URL 完全一致
- [ ] 后续内容真实更新时同步修改页面更新时间与 Sitemap `lastmod`
- [ ] 不使用隐藏文字、关键词堆砌、批量垃圾页、虚假新闻或购买垃圾外链
