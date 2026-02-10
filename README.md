# 🏮 杭州三日游旅行攻略网站

一个精美的杭州旅行攻略网页，融合现代设计与实用功能，为您的杭州之旅提供完整指南。

## 🌟 项目特色

### 🎨 设计亮点
- **现代简约风格**：采用渐变背景和卡片式布局
- **响应式设计**：完美适配手机、平板、桌面设备
- **交互动画**：流畅的悬停效果和页面过渡
- **中文优化**：专为中文用户设计的字体和排版

### 🗺️ 地图功能
- **高德地图集成**：使用Leaflet.js + 高德地图瓦片
- **景点标注**：西湖、灵隐寺、千岛湖等热门景点
- **路线规划**：三日游完整路线可视化
- **实时定位**：支持GPS定位和导航

### 📱 用户体验
- **一键分享**：支持原生分享和剪贴板复制
- **回到顶部**：智能显示的回到顶部按钮
- **键盘快捷键**：Ctrl+S打印，Ctrl+D收藏
- **加载优化**：性能监控和错误处理

## 🚀 快速部署

### 方法1：GitHub Pages（推荐）

#### 步骤1：创建仓库
1. 登录 [GitHub](https://github.com)
2. 点击右上角 `+` → `New repository`
3. 命名为 `hangzhou-travel-guide`
4. 选择 `Public`，勾选 `Add a README file`
5. 点击 `Create repository`

#### 步骤2：上传文件
1. 在新仓库页面，点击 `uploading an existing file`
2. 上传 `hangzhou-travel-guide.html` 文件
3. **重要**：将文件重命名为 `index.html`
4. 点击 `Commit changes`

#### 步骤3：启用Pages
1. 进入 `Settings` → `Pages`
2. Source选择 `Deploy from a branch`
3. Branch选择 `main` 和 `/ (root)`
4. 点击 `Save`

#### 步骤4：访问网站
等待2-3分钟后，访问：
```
https://[您的用户名].github.io/hangzhou-travel-guide/
```

### 方法2：本地预览
```bash
# 使用Python启动本地服务器
python -m http.server 8080
# 访问 http://localhost:8080/hangzhou-travel-guide.html

# 或使用Node.js
npx serve .
```

### 方法3：Netlify快速部署
1. 访问 [netlify.com](https://netlify.com)
2. 拖拽 `hangzhou-travel-guide.html` 到部署区域
3. 自动获得网址，立即访问

## 📋 文件结构

```
hangzhou-travel-guide/
├── hangzhou-travel-guide.html  # 主页面（部署时请重命名为index.html）
├── README.md                   # 项目说明文档
├── 部署指南.md                 # 详细部署教程
├── .github/
│   └── workflows/
│       └── deploy.yml         # GitHub Actions自动部署配置
├── netlify.toml               # Netlify部署配置
└── vercel.json                # Vercel部署配置
```

## 🎯 功能详解

### 📅 行程规划
- **Day 1**：西湖经典路线（断桥残雪→白堤→孤山→西泠印社）
- **Day 2**：文化古迹游（灵隐寺→法喜寺→宋城→河坊街）
- **Day 3**：自然风光游（千岛湖一日游）

### 🌤️ 天气信息
- **实时天气**：温度、湿度、风速
- **穿衣建议**：根据天气的智能推荐
- **空气质量**：AQI指数和健康建议
- **旅游指数**：综合适宜度评分

### 🍜 美食推荐
- **杭帮菜**：西湖醋鱼、东坡肉、龙井虾仁
- **小吃**：葱包桧、定胜糕、猫耳朵
- **茶馆**：西湖龙井、特色茶楼
- **价格参考**：详细的消费预算

### 🏨 住宿指南
- **豪华酒店**：五星级推荐和价位
- **精品民宿**：特色住宿体验
- **经济型**：性价比高的选择
- **位置建议**：各区域的优缺点

### 🚇 交通出行
- **地铁线路**：最新地铁图和站点
- **公交系统**：主要线路和票价
- **共享单车**：使用指南和费用
- **打车软件**：滴滴、高德等推荐

### 🛍️ 购物攻略
- **特产推荐**：龙井茶、丝绸、藕粉
- **购物街区**：湖滨银泰、武林商圈
- **古玩市场**：河坊街、南宋御街
- **价格参考**：避免被坑的贴士

## 🔧 技术栈

### 前端技术
- **HTML5**：语义化标签和SEO优化
- **CSS3**：渐变、动画、Flexbox/Grid布局
- **JavaScript**：ES6+语法和DOM操作
- **Leaflet.js**：开源地图库
- **高德地图API**：地图瓦片和地理服务

### 优化特性
- **SEO友好**：完整的meta标签和结构化数据
- **性能优化**：图片懒加载和资源压缩
- **错误处理**：全面的错误捕获和处理
- **响应式**：移动优先的设计理念

## 🎨 自定义指南

### 修改景点信息
在HTML文件中找到 `attractions` 数组：
```javascript
const attractions = [
    { name: "西湖", lat: 30.2500, lng: 120.1667, type: "scenic" },
    // 添加或修改景点信息
];
```

### 调整配色方案
在CSS部分修改渐变色彩：
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### 更新天气信息
修改天气API调用部分，支持您的城市：
```javascript
// 在天气API调用处修改城市参数
const city = '您的城市名称';
```

## 📱 浏览器兼容性

| 浏览器 | 最低版本 | 支持情况 |
|--------|----------|----------|
| Chrome | 60+ | ✅ 完全支持 |
| Firefox | 55+ | ✅ 完全支持 |
| Safari | 11+ | ✅ 完全支持 |
| Edge | 79+ | ✅ 完全支持 |
| IE | 不支持 | ❌ 建议使用现代浏览器 |

## 🔗 相关资源

### 官方文档
- [Leaflet.js 文档](https://leafletjs.com/reference.html)
- [高德地图API](https://lbs.amap.com/api/javascript-api/summary)
- [GitHub Pages 文档](https://docs.github.com/en/pages)

### 设计资源
- [渐变色生成器](https://cssgradient.io/)
- [图标库](https://fontawesome.com/)
- [字体选择](https://fonts.google.com/)

### 旅游数据
- [中国天气网](https://weather.com.cn/)
- [高德地图](https://www.amap.com/)
- [携程旅行](https://www.ctrip.com/)

## 📊 更新日志

### v1.0.0 (2024-02-10)
- ✨ 初始版本发布
- 🗺️ 集成高德地图
- 📱 添加响应式设计
- 🌤️ 实现天气功能
- 🚀 支持GitHub Pages部署

## 🤝 贡献指南

欢迎提交Issue和Pull Request来改进这个项目！

### 提交建议
- 🐛 错误报告：请提供浏览器版本和复现步骤
- 💡 功能建议：详细描述您期望的功能
- 🎨 设计改进：欢迎UI/UX优化建议
- 📖 文档完善：帮助改进README和教程

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🙏 致谢

- 高德地图提供优秀的地图服务
- Leaflet.js开源社区
- 所有贡献者和使用者

---

**🎉 祝您使用愉快，杭州之旅充满美好回忆！**

如有问题，请在GitHub提交Issue，我们会及时回复。🏮