# BOOX设备对比工具

这是一个用于比较BOOX电子墨水屏设备的网页工具，帮助用户轻松对比和选择合适的BOOX设备。

## 功能特点

- 📱 支持多种BOOX设备型号的对比
- 🔍 强大的筛选功能：
  - 屏幕尺寸筛选
  - 显示类型（彩色/黑白）筛选
  - 前光照明筛选
  - 手写笔支持筛选
  - Super Refresh功能筛选
  - 价格区间滑块筛选
- 📊 表格功能：
  - 首行首列固定，方便浏览
  - 支持按列排序
  - 自适应列宽
  - 设备图片展示
- 💡 其他特性：
  - 响应式设计，支持移动端
  - 简洁现代的UI设计
  - 实时筛选结果统计

## 技术栈

- HTML5
- CSS3 (Tailwind CSS)
- JavaScript (原生)
- 第三方库：
  - Tailwind CSS (样式框架)
  - noUiSlider (价格滑块组件)
  - PapaParse (CSV数据解析)

## 使用说明

1. 直接打开`index.html`文件即可使用
2. 设备数据存储在页面内的CSV格式字符串中
3. 图片应放置在`images`文件夹下，命名需与CSV数据中的`Image File`字段对应

## 数据结构

设备数据包含以下字段：
- Model: 设备型号
- Image File: 图片文件名
- Price ($): 价格
- Released: 发布年份
- Display Type: 显示类型
- Display Size (inch): 屏幕尺寸
- Resolution: 分辨率
- Color Display?: 是否彩色显示
- Pixel Density (PPI): 像素密度
- Screen Light?: 是否有前光
- Stylus Input?: 是否支持手写笔
- Operating System: 操作系统
- Internal Storage: 内部存储
- RAM: 内存
- BOOX Super Refresh?: 是否支持超级刷新
- Battery Capacity: 电池容量
- Weight: 重量
- MicroSD Card Reader?: 是否支持MicroSD卡

## 项目结构

```
booxcomparev2/
├── index.html      # 主页面
├── README.md       # 说明文档
└── images/         # 设备图片目录
    ├── notemax.jpg
    ├── palma2.jpg
    └── ...
```

## 开发说明

如需修改或扩展功能：

1. 设备数据更新：
   - 修改`loadDeviceData()`函数中的CSV数据字符串
   - 确保新增设备的图片放入images目录

2. 筛选条件修改：
   - 在HTML中添加新的筛选选项
   - 在`applyFilters()`函数中添加对应的筛选逻辑

3. 表格列修改：
   - 更新表格头部的列定义
   - 在`renderTable()`函数中相应更新数据渲染逻辑

## 浏览器兼容性

- Chrome (推荐)
- Firefox
- Safari
- Edge

## 许可证

MIT License

## 贡献指南

欢迎提交Issue和Pull Request来改进这个项目。

## 致谢

- Tailwind CSS 团队
- noUiSlider 开发者
- PapaParse 开发者 