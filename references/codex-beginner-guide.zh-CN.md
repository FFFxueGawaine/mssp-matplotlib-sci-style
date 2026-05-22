# sci-paper-plot-skill 新手向导

如果你是小白用户，可以先不要管 Matplotlib 或 Seaborn API，直接按“我现在想做什么”选择下一步。

## 1. 先选当前阶段

| 阶段 | 你的情况 | 下一步 | 输出 |
|---|---|---|---|
| Level 1 | 我有论文图片，但不知道属于哪类图。 | 先审计并分类。 | 图片清单和分类建议。 |
| Level 2 | 我知道想画成什么样，但需要能跑的例子。 | 复制最接近的 demo 到项目目录。 | 脚本和占位数据生成图。 |
| Level 3 | 我已有真实 CSV/TXT/NPY 数据，想生成最终图。 | 把 demo 替换成真实数据。 | 项目专用脚本和最终图。 |

## 2. 常用入口

```bash
python scripts/scimplstyle_mssp_cli.py audit "<论文图片文件夹>" --markdown
python scripts/scimplstyle_mssp_cli.py list-demos
python scripts/scimplstyle_mssp_cli.py beginner-guide --lang zh
python scripts/scimplstyle_mssp_cli.py run-brief --lang zh
python scripts/scimplstyle_mssp_cli.py recommend "误差分布" --lang zh
python scripts/scimplstyle_mssp_cli.py copy-demos "<skill 外部的工作文件夹>"
```

## 3. 按目标选模板

| 目标 | 推荐起点 | 适用原因 |
|---|---|---|
| 时域响应、验证曲线、方法对比 | `demo_validation_compare.py`, `demo_line_plot.py`, `demo_hb_fig14_three_column.py` | 直接给出论文式坐标轴、图例和子图标号。 |
| 峰值或瞬态附近局部放大 | `demo_validation_inset_zoom.py` | 同时保留整体趋势和局部细节。 |
| 误差分布、不确定性、后验密度 | `demo_error_boxplot.py`, `demo_kde_uncertainty.py`, `demo_matplotlib_distribution_gallery.py` | 适合重复试验、后验密度和不确定性检查。 |
| 频响或时频图 | `demo_frf_compare.py`, `demo_time_frequency_map.py` | 已带工程标签、色条和紧凑排版。 |
| 常见 Matplotlib 论文图 | `demo_matplotlib_relation_gallery.py`, `demo_matplotlib_categorical_gallery.py`, `demo_matplotlib_field_gallery.py` | 适合最终论文图，需要精确控制布局。 |
| 常见 Seaborn 表格数据图 | `demo_seaborn_common_gallery.py` | 适合已有分组列的表格数据。 |
| 机器学习结果图 | `demo_ml_classification_curves.py`, `demo_ml_confusion_matrix.py`, `demo_ml_feature_importance.py` | 覆盖常见模型对比和评价图。 |

## 4. 可以这样问 Codex

```text
Use $sci-paper-plot-skill. 我是新手，请先审计我的图片文件夹，并告诉我最接近哪个 demo。
```

```text
Use $sci-paper-plot-skill. 我不知道该选哪个图，请先根据我的目标推荐模板，不要直接写代码。
```

## 5. 安全默认规则

- 第一轮不改原始论文图片。
- 不把生成图写进已安装的 skill 文件夹。
- 会写文件的命令运行前，先确认目标、数据、输出文件夹、语言字体、子图标号和版面。
- 先完成一类图，再扩展到整篇论文。
- 最终论文排版优先 Matplotlib；已有分组表格数据优先 Seaborn。
