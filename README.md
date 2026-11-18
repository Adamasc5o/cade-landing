# CADE Love & Balance Landing Page

静态网页，无需后端、无需数据库，上传即可运行。

## 文件

```
index.html        整个页面（HTML + CSS + JavaScript 全部在这一个文件里）
assets/           32 张图片（产品图、配套海报、Logo、瓶身标签等）
README.md         本说明
```

**注意**：`index.html` 和 `assets/` 必须放在同一层目录，不要改文件夹名或图片文件名。

## 本地预览

双击 `index.html` 用浏览器打开即可。中英文衬线字体从 Google Fonts 加载，需要联网；断网时会退回系统字体，排版略有差异。

## 部署

### Cloudflare Pages
1. 登录 Cloudflare → Workers & Pages → Create → Pages → Upload assets
2. 把整个文件夹拖进去（包含 index.html 和 assets 文件夹）
3. 部署完成后会得到一个 `xxx.pages.dev` 的网址
4. 在该项目的 Custom domains 里添加 `cade.adamasc5o.com`
5. 如果域名的 DNS 已托管在 Cloudflare，点确认即可；否则按它给出的 CNAME 记录，到域名后台添加

### Netlify / Vercel
1. 注册后在首页把文件夹拖进 Deploy 区域
2. 得到临时网址后，进 Domain settings 添加 `cade.adamasc5o.com`
3. 到域名后台加一条 CNAME：主机记录 `cade`，指向它给的地址

### 已有虚拟主机（cPanel / FTP）
1. 在主机控制面板为 `cade.adamasc5o.com` 建一个子域名，记下它的目录（例如 `/public_html/cade`）
2. 用 FTP 或文件管理器把 `index.html` 和 `assets/` 上传到该目录
3. 建议开启 SSL（cPanel 的 AutoSSL 或 Let's Encrypt）

### DNS 记录（通用）
| 类型 | 名称 | 值 |
|---|---|---|
| CNAME | cade | 托管服务给的地址 |

DNS 生效通常几分钟到几小时。

## 还需要补的内容

- **购买入口**：页面上所有「选购礼盒」按钮目前只跳到页内的「三种配套」区块，三个配套卡片里也没有下单按钮。拿到购买链接或 WhatsApp 后需要补上。
- **联系方式与配送说明**：页面上没有。
- **优惠截止日期**：「限时优惠」标签没有写截止日期。

## 浏览器兼容

iOS 16+ / Android Chrome / Edge / Safari / Firefox 的较新版本均可。
滚动进场动画、顶部滚动进度条在较旧的浏览器上不播放，内容会直接显示，不影响阅读。
系统开启「减少动态效果」时，页面会自动关闭动画。
