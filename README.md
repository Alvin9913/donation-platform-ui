# 剩余食物捐赠平台 · 前端原型

把「商家剩余食物发布出去、由受助方预约领取」做成可点的原型。单文件 HTML，无构建、无依赖，双击就能在浏览器打开：

```
second-table-ui-prototype v2.html
```

## 原型里有什么

| 界面 | 作用 |
|---|---|
| 登录 / 角色选择 | 区分捐赠方与领取方，进来看到不同的界面 |
| My listings / New listing | 发布剩余食物：品类、数量、取货时间、地址 |
| My requests / Collection history | 领取方追踪申请状态（提交 → 通过 → 已取）与历史 |
| Report an issue | 领取出问题时向管理员报备 |
| 文件上传 | 点击选择与拖拽上传，上传前本地预览、可移除 |

## 交互实现

全部原生 JS，没有框架：

- 多屏切换：`showScreen` / `navTo`
- 子标签：`toggleSubtab`
- 表格行展开：`toggleDetailRow`
- 弹窗：`openRequestModal` / `closeRequestModal`
- 列表筛选：`filterReportList`
- 拖拽上传：`handleFileDrop`（含 `readAndPreview` 本地预览）

## 设计文档

`A10_Speech_Script_CN_EN.md` 是配套的中英双语演讲稿，讲这个原型的场景、用户流程与设计取舍——不是代码注释，是"为什么这么做"。

## 怎么跑

浏览器直接打开 `second-table-ui-prototype v2.html`，无需服务器。
