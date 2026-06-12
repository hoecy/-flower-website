# -flower-website
This project is a website showcasing information about flowers and the ordering process.
這個項目是一個有關花朵簡介及訂購的網站展示
主页（index.html）
全屏滚动分区（section），每部分介绍一种花卉（百合、硫磺波斯菊、银莲花、虞美人、紫色郁金香）

顶部导航指示器，点击可平滑滚动到对应分区

“about us”、“pricing”、“more” 三个快捷入口

about us → 滚动到底部联系方式

pricing → 打开价格页面

more → 打开可拖拽照片墙页面

每个花卉卡片配有“Learn more”按钮，点击后打开对应的详情页（flower1.html / flower2.html 循环）

底部 footer 包含联系方式、营业时间、客户服务链接（带打字机效果）

价格页面（pricing.html）
展示标准花束、高级花艺、定制订单、季节性特惠、订阅计划、配送费、大宗订单等价格

采用卡片式清晰列表，联系信息置于底部

花卉详情页（flower1.html / flower2.html）
百合花 / 硫磺波斯菊的详细介绍

包含植物特征、意义、养护技巧等信息

采用卡片式图文混排，带有半透明水印背景

照片墙（more.html）
使用 GSAP 实现可拖拽移动的横向/纵向无缝照片墙

照片按行排列，鼠标拖拽时整行平移，超出边界时循环位移（无限滚动感）

初始弹出提示框，告知用户“尝试拖动!”

响应式设计（根据屏幕宽高比调整照片尺寸）

公共样式与脚本
common.css 定义全局 CSS 变量（颜色主题）、基础重置

bg.css 提供背景样式（可能是动态渐变或花饰）

insertbg.js 统一插入背景元素

type.js 实现 footer 中逐字打印的动画效果

技术栈
HTML5：语义化结构

CSS3：Flexbox/Grid 布局、CSS 变量、媒体查询、过渡动画

原生 JavaScript：DOM 操作、事件监听、模块化对象（如 photobox）

GSAP 3.10.4：用于照片墙的平滑拖拽动画

无外部依赖（除 GSAP 库外均为原生实现）

如何运行
将所有文件下载到本地，保持原始目录结构不变。

使用任意 Web 服务器（如 VS Code Live Server、Python HTTP Server 或直接双击 HTML 文件）打开 index.html 即可。

注意：直接双击打开可能会因跨域策略影响某些功能（如背景图片加载），建议使用本地服务器。

主页中点击不同按钮可跳转至价格、详情页或照片墙。

在照片墙页面（more.html）按住鼠标拖拽即可移动整行照片，松开停止。

浏览器兼容性
现代浏览器（Chrome, Edge, Firefox, Safari）

需要使用 requestAnimationFrame、CSS transform 等特性，不支持 IE11
