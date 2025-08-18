 <h1>
    🛰️ GEE 学习笔记与代码实践 🌏
  </h1>

  <p>
    <strong>从零开始，用代码探索地球的奥秘。记录我的 Google Earth Engine 学习历程、常见问题解决方案和前沿技术追踪。</strong>
  </p>

---
## 👤 关于我

你好，我是一名智慧农业的研究生，致力于打造smart farming！
正在努力学习 GEE 和云端地理空间分析技术，希望未来能用技术为地球做点什么。

如果你想和我交流，可以通过以下方式联系我：2942204237@qq.com

---
## 🚀 项目简介

欢迎来到我的 Google Earth Engine (GEE) 学习空间！

这个仓库是我个人的学习日记和工具箱，主要用于：

* **系统整理**：记录从入门到进阶的学习过程中的知识点。
* **解决难题**：分享我在实践中遇到的问题和行之有效的解决方案（详见Q&A部分）。
* **代码沉淀**：收集和编写可直接在 GEE 中复用的代码片段和项目模板。
* **追踪前沿**：关注并学习 GEE 生态的最新技术和数据集。

我希望通过这个仓库，不仅能构建扎实的个人知识体系，也能为同样在 GEE 海洋中探索的朋友们点亮一盏小小的灯塔。欢迎 **Star** 🌟 和 **Fork** 🍴！

---

# Awesome Earth Engine [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of Google Earth Engine resources. Please visit the [Awesome-GEE](https://github.com/giswqs/Awesome-GEE) GitHub repo if you want to contribute to this project.

## Table of Contents（复刻wqs大佬的整理合集，请star大佬）
[Awesome-GEE](https://github.com/giswqs/Awesome-GEE)

- [Earth Engine official websites](#earth-engine-official-websites)
- [Get Started](#get-started)
- [Get Help](#get-help)
- [JavaScript API](#javascript-api)
- [Python API](#python-api)
- [R](#r)
- [QGIS](#qgis)
- [GitHub Developers](#github-developers)
- [Twitter](#twitter)
- [Apps](#apps)
- [Free Courses](#free-courses)
- [Presentations](#presentations)
- [Videos](#videos)
- [Projects](#projects)
- [Websites](#websites)
- [Datasets](#datasets)
- [Papers](#papers)
- [Contributing](#contributing)
- [License](#license)

---

## 🗺️ 我的学习路线图

这是一个动态更新的路线图，记录了我的学习计划和进度。

-   [x] **Phase 1: GEE 基础入门**
    -   [x] 掌握 GEE Code Editor 基本操作
    -   [x] 理解 `Image` 和 `ImageCollection`
    -   [x] 理解 `Feature` 和 `FeatureCollection`
    -   [x] 学习基础语法
    -   [x] 完成第一个地图
-   [ ] **Phase 2: 核心数据处理**
    -   [ ] 影像数据的筛选、裁剪、拼接和计算
    -   [ ] 矢量数据的创建、筛选和空间分析
    -   [ ] `map` 和 `filter` 函数的应用
    -   [ ] `reducer` 的原理与实践
-   [ ] **Phase 3: 遥感专题应用**
    -   [ ] 计算植被指数 (NDVI, EVI) 并进行时序分析
    -   [ ] 提取水体范围 (NDWI, MNDWI)
    -   [ ] 监督与非监督分类
    -   [ ] 计算地表温度 (LST)
-   [ ] **Phase 4: GEE 进阶**
    -   [ ] UI 设计与交互式 App 开发
    -   [ ] GEE Python API 的使用
    -   [ ] 结合 `geemap` 和 `Jupyter Notebook` 进行分析
-   [ ] **Phase 5: 毕业项目**
    -   [ ] 设计并完成一个综合性项目（例如：多源数据融合实现虫害对作物生长的大面积灾害损失预测）

---

## 🌟 精选案例展示

<details>
<summary><strong>点击查看：案例一 - 基于EC JRC 2020全球森林覆盖图与MODIS NDVI的森林健康动态监测（Python版本）</strong></summary>

**简介**: 热带雨林生态系统在碳循环、水分调节和生物多样性维系中发挥着关键作用，尤其是在东南亚区域。然而由于农业扩张、城市化、基础设施建设等压力，局部森林区域出现退化甚至破碎化趋势。为此，我们希望：
*获取2020年森林覆盖图，识别研究区域内的森林像元；
*利用MODIS NDVI产品，计算2023年森林区域内的平均植被活力；
*设置 NDVI 阈值（<4000）识别潜在退化森林区域；通过 Python 完成全过程自动化渲染与图例生成。

**核心技术**: `ImageCollection`, `map`, `updateMask`, `filter`

**成果展示** [forest_ndvi.ipynb](https://github.com/Yuanyuan2003/PythonGEE-practical-projects/blob/main/forest_NDVI.png)</details>

---

## 🤝 如何贡献

非常欢迎你参与到这个项目中来！你可以通过以下方式贡献：

* **提交 Issue**：发现 Bug、内容错误或者有任何建议，请随时提交 Issue。
* **提供代码**：如果你有更好的实现方式或新的实用案例，欢迎提交 Pull Request。

在贡献之前，请确保你的代码在 GEE 中可以无误运行。



---

## 📚 学习难点与解决方案 (Q&A)

这里汇总了我在学习过程中遇到的“拦路虎”以及对应的解决方法，希望能帮你节省一些调试的时间。

<details>
<summary><strong>Q1: GEE 账号注册不顺利怎么办？</strong></summary>

**办法**：
*由于网络环境问题，建议使用稳定可靠的科学上网工具进行访问和注册 

</details>

<details>
<summary><strong>Q2: 在本地 Python 环境 (如 VS Code) 中运行 `ee.Initialize()` 时出现授权失败？</strong></summary>

**原因**：
这通常是由于系统用户对 GEE 认证凭证文件夹的写入权限不足导致的。该文件夹通常位于：
**Windows**: `C:\Users\USERNAME\.config\earthengine\credentials`
**Linux**: `/home/USERNAME/.config/earthengine/credentials` 
**MacOS**: `/Users/USERNAME/.config/earthengine/credentials` 

**办法 (以MacOS为例)**：
打开终端，运行以下命令赋予当前用户对该文件夹的所有权，然后再重新执行Python脚本进行授权。
```bash
sudo chown -R $(whoami) ~/.config

---
## Google Earth Engine 学习难点及解决办法
- 本章节整理了在使用 Google Earth Engine (GEE) 过程中遇到的常见问题及解决方案，帮助您快速上手和解决实际应用中的困难。

## 📋 目录

1. [账号注册问题](#账号注册问题)
2. [本地环境配置](#本地环境配置)
3. [云端编辑器使用](#云端编辑器使用)
4. [地图操作技巧](#地图操作技巧)
5. [数据处理技巧](#数据处理技巧)
6. [高级应用案例](#高级应用案例)
7. [最新技术动态](#最新技术动态)

---

## 🔑 账号注册问题

### 问题描述
无法成功注册或访问 Google Earth Engine 平台

### 解决方案

#### 1. VPN 网络配置
- **推荐工具**: 龙猫云 VPN ([totorocloud.net](https://totorocloud.net))
- **账号信息**: 
  - 邮箱: `你自己的邮箱`
  - 谷歌账号: `你自己的谷歌账号`

#### 2. 注册流程
1. 使用 Google Cloud 平台注册 GEE
2. 利用谷歌学生账号可简化注册流程
3. 完成邮箱验证和权限申请

---

## ⚙️ 本地环境配置

### 问题描述
在本地代码编辑器运行时出现授权问题

### 错误示例
```python
import ee
ee.Authenticate()
ee.Initialize()  # 可能出现权限错误
```

### 解决方案

#### MacOS 系统
```bash
# 修复权限问题
sudo chown -R $(whoami) ~/.config
```

#### 各系统凭证路径
| 操作系统 | 凭证文件路径 |
|---------|-------------|
| Windows | `C:\Users\USERNAME\.config\earthengine\credentials` |
| Linux   | `/home/USERNAME/.config/earthengine/credentials` |
| MacOS   | `/Users/USERNAME/.config/earthengine/credentials` |

#### 完整初始化代码
```python
import ee

# 触发认证流程
ee.Authenticate()

# 初始化库
ee.Initialize(project='你自己的项目')
```

---

## ☁️ 云端编辑器使用

### 可用平台
- [GEE 代码编辑器](https://developers.google.com/earth-engine/guides/playground?hl=zh_CN)
- [Google Colab](https://colab.research.google.com/)

### 推荐学习资源
- **geemap.org**: wqs 开发的 Python 包，包含丰富的学习资源
- 官方文档和社区教程

---

## 🗺️ 地图操作技巧

### 1. 坐标顺序问题
**问题**: `gee.Map(center=[x,y], zoom=, height=)` 参数顺序混淆
**解决**: **纬度在前，经度在后**

### 2. 界面简化
**问题**: 地图界面显示过多控件
**解决**: 
```python
# 隐藏控件
geemap.Map(data_ctrl=False, toolbar_ctrl=False, layer_ctrl=False)
```

### 3. 路径处理问题
**问题**: Windows 系统路径解析错误
**解决**: 使用原始字符串，r"路径"
```python
data_path = r"C:\Users\username\data\gee_files"
```

---

## 📊 数据处理技巧

### 1. 获取数据信息
```python
# 函数后加 .getInfo() 获取信息
dataset_info = image_collection.getInfo()
```

### 2. 数据筛选方法
```python
# 按日期筛选
filtered = collection.filterDate('2025-01-01', '2025-12-31')

# 按属性筛选
pop = fc.filter(ee.Filter.gt('POP_EST', 1e9)) #gt大于
pop = fc.filter(ee.Filter.lt('POP_EST', 1e9)) #lt小于
pop = fc.filter(ee.Filter.eq('NAME', '中国')) #eq等于

# 按云量筛选
clear_images = collection.filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE', 5))
```

### 3. 获取用户选择区域
```python
# 获取用户在地图上定义的 ROI，利用.user_roi和.getInfo()方法
user_region = Map.user_roi.getInfo()
```

---

## 🎯 高级应用案例

### 案例1: 基于人口筛选国家
```python
# 过滤出人口大于10亿的国家
pop_countries = fc.filter(ee.Filter.gt('POP_EST', 1e9))
# 添加到地图
Map.addLayer(pop_countries, {}, 'High Population Countries')
```

### 案例2: 区域特定分析
```python
# 定义数据路径，替换成你自己的路径
data = "/Users/mayuanyuan/Desktop/gee/chapters/countries.geojson"

# 转换为 Earth Engine 对象，geojson_to_ee()方法
fc = geemap.geojson_to_ee(data)

# 筛选中国区域，filter()方法
china = fc.filter(ee.Filter.eq('NAME', 'China'))

# 处理 Sentinel-2 数据
collection = (
    ee.ImageCollection('COPERNICUS/S2_SR')
    .filterDate('2025-07-01', '2025-08-01')
    .filterBounds(china)
    .filter(ee.Filter.lt('CLOUDY_PIXEL_PERCENTAGE', 5))
)

# 创建中位数合成影像
image = collection.median()

### 可视化参数使用说明
可视化参数用于定义图像在地图上的显示样式，以下是常见参数及使用方法：
- `min` 和 `max`：设置图像显示的最小值和最大值，用于将像素值映射到颜色空间。例如 `min: 0.0` 和 `max: 3000` 表示将像素值 0.0 映射为颜色范围的最小值，3000 映射为最大值。
- `bands`：指定要显示的波段，按顺序排列。例如 `['B4', 'B3', 'B2']` 表示使用红、绿、蓝三个波段合成真彩色图像。

下面是一个可视化参数的使用示例，该参数将用于显示 Sentinel - 2 数据的真彩色图像：
vis_params = {
    'min': 0.0,
    'max': 3000,
    'bands': ['B4', 'B3', 'B2']  # RGB真彩色
}

# 添加到地图
Map.addLayer(image, vis_params, 'Sentinel-2 China')
```

---

## 🚀 最新技术动态

### DeepMind 发布 AlphaEarth 数字孪生
**发布时间**: 2025年7月30日

#### 技术突破
- **高精度网格**: 10米×10米分辨率，每个网格64维嵌入向量
- **数据融合**: 整合20余种数据源（光学、雷达、激光测绘）
- **效率提升**: 存储效率提升16倍，错误率降低24%

#### 应用场景
| 领域 | 应用案例 |
|------|----------|
| **农业监测** | 印度灌溉泄漏识别、巴西大豆干旱风险预测 |
| **气候行动** | 北极海冰90天预测、城市热岛效应量化 |
| **灾害响应** | 山体滑坡预警（89%准确率）、飓风灾害图谱 |
| **生态保护** | 大堡礁0.1℃水温监测、非洲象群迁移追踪 |

#### 行业影响
- 联合国粮农组织、哈佛森林等50+机构采用
- 结合Gemini大模型，支持自然语言查询
- 开放2018-2024年卫星嵌入数据集

---

## 📡 Google 卫星嵌入数据集

### Satellite Embedding V1 数据集
**合作机构**: Google Earth Engine + Google DeepMind

#### 核心特点
- **嵌入向量**: 每个10米像素对应64维时间序列嵌入
- **数据覆盖**: 全球范围，年度更新
- **多源融合**: 光学、雷达、地形、气象数据

#### 数据访问
- **数据集链接**: [Satellite Embedding V1](https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_SATELLITE_EMBEDDING_V1_ANNUAL?hl=zh-cn)

#### 使用示例
```python
import ee
import geemap
ee.Initialize()
dataset = ee.ImageCollection('GOOGLE/SATELLITE_EMBEDDING/V1/ANNUAL')
filtered = dataset.filterDate('2020-01-01', '2020-12-31')
region = ee.Geometry.Rectangle([73.66, 18.15, 135.08, 53.56]) #定义中国区域范围（大致范围）
clipped = filtered.mosaic().clip(region) #裁剪中国区域
vis_params = {
  'bands': ['A00_0', 'A01_0', 'A02_0'],  # 根据数据集说明，选择前三个波段用于可视化，实际使用时可按需调整
  'min': 0,  # 需根据数据分布调试，可通过统计工具获取合理范围
  'max': 100,
}
Map = geemap.Map()
Map.addLayer(clipped, vis_params, 'Satellite Embedding V1')
Map.centerObject(region, 6)
Map
```

---

## 📚 学习资源

### 推荐工具
- **geemap**: Python GEE接口增强包
- **Google Colab**: 免费云端计算环境
- **Jupyter Notebook**: 本地交互式开发

---

## 🔗 相关链接

- [GEE官方文档](https://developers.google.com/earth-engine)
- [geemap文档](https://geemap.org)
- [Google Colab](https://colab.research.google.com)

---

*最后更新: 2025年8月*  

