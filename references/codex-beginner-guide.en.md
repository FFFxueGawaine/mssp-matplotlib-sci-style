# sci-paper-plot-skill beginner guide

Use this guide when you are new to Codex plotting skills or do not know which template to choose.

## 1. Pick your current level

| Level | You say | Best next step | Output |
|---|---|---|---|
| Level 1 | I have paper figures, but I do not know their types. | Audit and classify figures first. | Markdown inventory and recommended categories. |
| Level 2 | I know the target figure style, but I need a runnable example. | Copy the closest demo into a project folder. | A `.py` script and placeholder PNG output. |
| Level 3 | I have real CSV/TXT/NPY data and want the final figure. | Adapt one copied demo to your real data. | Project-specific script and regenerated figure. |

## 2. Commands to start

```bash
python scripts/scimplstyle_mssp_cli.py audit "<paper-figure-folder>" --markdown
python scripts/scimplstyle_mssp_cli.py list-demos
python scripts/scimplstyle_mssp_cli.py beginner-guide --lang en
python scripts/scimplstyle_mssp_cli.py run-brief --lang en
python scripts/scimplstyle_mssp_cli.py recommend "time response" --lang en
python scripts/scimplstyle_mssp_cli.py copy-demos "<working-folder-outside-the-skill>"
```

## 3. Choose a template by goal

| User goal | Start from | Why |
|---|---|---|
| Time response, validation curve, or method comparison | `demo_validation_compare.py`, `demo_line_plot.py`, `demo_hb_fig14_three_column.py` | Direct SCI-style axes, legends, and panel labels. |
| Zoomed local difference near a peak or transient | `demo_validation_inset_zoom.py` | Keeps full trend and local detail in one figure. |
| Error distribution or uncertainty | `demo_error_boxplot.py`, `demo_kde_uncertainty.py`, `demo_matplotlib_distribution_gallery.py` | Good for repeated trials, posterior density, and uncertainty checks. |
| Frequency response or time-frequency result | `demo_frf_compare.py`, `demo_time_frequency_map.py` | Uses engineering labels, colorbars, and compact layout. |
| Common Matplotlib plot types | `demo_matplotlib_relation_gallery.py`, `demo_matplotlib_categorical_gallery.py`, `demo_matplotlib_field_gallery.py` | Best when final manuscript layout needs precise Matplotlib control. |
| Common Seaborn/DataFrame plots | `demo_seaborn_common_gallery.py` | Best when data is already a tidy table with group columns. |
| Machine-learning result figure | `demo_ml_classification_curves.py`, `demo_ml_confusion_matrix.py`, `demo_ml_feature_importance.py` | Covers common model-comparison and evaluation figures. |

## 4. Ask Codex like this

```text
Use $sci-paper-plot-skill. I am a beginner. Please audit my figure folder and tell me which demo is closest.
```

```text
Use $sci-paper-plot-skill. I do not know which plot type to choose. Please recommend one template based on my goal before writing code.
```

## 5. Safe defaults

- Do not edit original paper images during the first pass.
- Do not write generated figures into the installed skill folder.
- Before running commands that write files, confirm the user goal, data source, output folder, language/font, panel labels, and layout.
- Start with one figure type before converting a whole paper.
- Use Matplotlib for final journal layout; use Seaborn for grouped table data and quick faceting.
