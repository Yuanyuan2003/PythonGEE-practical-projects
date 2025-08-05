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
## 更多内容继续更新！（我是个小菜鸡，专业问题我也不懂，学着玩的哈哈哈😄）
