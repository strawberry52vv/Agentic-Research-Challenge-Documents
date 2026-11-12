# MPR 原文数据（2001Q1–2026Q2）

## 内容

- `mpr/`：102 期《中国货币政策执行报告》PDF 全文，按报告期命名（如 `2001Q1.pdf`）
- `mpr_meta.csv`：期数元数据（period, pub_date, pub_time, url, page_url, title, pages, chars, fetch_date, status）

## 来源

中国人民银行官网「货币政策执行报告」栏目，逐期抓取：
https://www.pbc.gov.cn/zhengcehuobisi/125207/125227/125957/index.html

## 说明

- 样本区间 2001Q1–2026Q2，共 102 期；2026Q3 报告按惯例尚未发布
- 所有 PDF 均有文字层，无需 OCR
- 文本提取用 pypdf layout 模式（默认模式对部分期数会拆成单字一行）
- 抓取日期 2026-11-12

## 复现

```bash
python -m src.data.fetch_mpr --start 2001Q1 --end 2026Q2 --out data/raw/mpr
```

抓取脚本见项目仓库 `Agentic_Research_Challenge` 的 `src/data/fetch_mpr.py`。
