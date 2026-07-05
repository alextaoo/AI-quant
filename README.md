# 📈 StockChart Pro

> 技术指标可视化工具 — 支持 MA / MACD / KDJ / RSI 实时计算

**👉 在线访问：https://alextaoo.github.io/AI-quant/master/**

---

## 功能特性

- **K 线图** — 实时绘制股票 OHLCV 蜡烛图
- **均线 MA** — 支持多条均线叠加（5/10/20/60/120/250 日）
- **MACD** — DIF / DEA / MACD 柱状图
- **KDJ** — K / D / J 三线指标
- **RSI** — 相对强弱指标，支持超买超卖标注
- **CSV 数据导入** — 直接拖拽 CSV 文件加载数据
- **参数实时调节** — 滑块动态修改指标周期
- **截图导出** — 一键保存图表为图片
- **预设管理** — 保存 / 加载自定义指标配置

---

## 数据来源

配合 [stock-api](https://github.com/alextaoo/AI-quant) 使用：

```bash
# 启动 API 服务
cd stock-api && pip install -r requirements.txt && run.bat

# 获取数据示例
curl http://localhost:8000/api/v1/history/688981.SH?limit=300&adjust=qfq
```

---

## 使用方法

1. 打开 👉 https://alextaoo.github.io/AI-quant/
2. 拖拽 CSV 文件到页面，或在数据目录加载预置数据
3. 选择指标类型，调整参数
4. 点击右上角截图按钮保存图片

---

## 数据格式

支持 CSV 格式，列顺序：

```
date, open, high, low, close, volume, amount, change_pct, adjust, source, symbol, name
```

示例数据：
- 中芯国际 A股：`688981.SH`
- 比亚迪：`002594.SZ`
- 长江电力：`600900.SH`

---

## 技术栈

- ECharts 5（K 线图渲染）
- Bootstrap 5（UI 框架）
- 原生 JavaScript（指标计算 / 数据处理）
