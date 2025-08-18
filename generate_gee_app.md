# 💻 用GEE发布一个交互式APP
## 🧰 准备工作注册 GEE 账号
- 登录代码编辑器
- 熟悉 ui.Panel, ui.Select, Map.addLayer() 等基础 UI 控件
## 🧱 基础功能：选择区域 + 显示地图
### ✅ 目标功能：
- 从下拉菜单中选择一个区域
- 自动在地图中显示该区域边界
- 地图自动缩放和聚焦
- 支持 GEE 一键发布成 Web App
```javascript
// 引用二级行政边界（可选国家）
var admin2 = ee.FeatureCollection('YOUR/COLLECTION/ID');
// 主面板
UIvar mainPanel = ui.Panel({style: {width: '600px'}});
mainPanel.add(ui.Label({  value: '区域选择界面模板',  style: {'fontSize': '24px', 'margin': '10px 5px'}}));
// 下拉菜单区域面板
var admin2Panel = ui.Panel({layout: ui.Panel.Layout.flow('vertical')});
mainPanel.add(admin2Panel);
// 过滤国家（可更改为其他国家名）
var filtered = yourRegionCollection.filter(ee.Filter.eq('ADMIN_FIELD', '某国家或上级单位'));
var regionNames = filtered.aggregate_array('REGION_NAME_FIELD');
// 定义显示逻辑
var display = function(admin2Name) {
  var selected = ee.Feature(filtered.filter(ee.Filter.eq('ADM2_NAME', admin2Name)).first());
  var geometry = selected.geometry();
  Map.clear();
  Map.addLayer(geometry, {color: 'grey'}, admin2Name);
  Map.centerObject(geometry, 7);};
// 创建下拉菜单
admin2Names.evaluate(function(names) {
  var dropDown = ui.Select({
  placeholder: '请选择区域边界',
  items: names,
  onChange: display
  });
  admin2Panel.add(dropDown);});
ui.root.add(mainPanel);
```
