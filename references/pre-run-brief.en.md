# sci-paper-plot-skill pre-run brief

Before copying demos, generating preview galleries, running plotting scripts, or replacing placeholder data with real data, collect this brief from the user. If key information is missing, Codex should ask first instead of writing files immediately.

## Minimum information to confirm

1. Figure goal: time response, error distribution, FRF, heatmap, one-row three-column comparison, etc.
2. Data source: real data or placeholder data first. If real data exists, ask for absolute CSV/TXT/NPY/Excel paths.
3. Output location: where scripts and figures should be written. It must be outside the installed skill folder.
4. Language and fonts: English SCI, Chinese report, or mixed. Confirm whether Chinese titles should use SimSun.
5. Panel labels: top-center by default; use bottom-center only when required by the journal template or reference figure.
6. Layout constraints: single/double column, rows and columns, legend, colorbar, or inset needs.

## Prompt to ask the user

```text
Before I run the plotting program, please tell me:
1. What is the figure goal?
2. Do you have real data? If yes, provide absolute data paths; otherwise I will use placeholder data first.
3. Which working folder should receive the script and generated figures? I will not write them into the skill install folder.
4. Should the text use English SCI style, Chinese report style, or mixed language? Should Chinese titles use SimSun?
5. Panel labels use top-center by default. Does the journal template or reference figure require bottom-center? If not, I will keep the default.
6. Is the layout single panel, 1x3, 2x2, 2x3, or based on a reference figure?
```

## Pre-run rule

- `beginner-guide`, `recommend`, `list-demos`, and `style-guide` are read-only and can be run directly.
- `copy-demos`, `preview-gallery`, `check-demos`, and real plotting scripts write files, so collect the brief first.
- If the user already provided enough information, summarize it briefly and then run.
- If only one or two fields are missing, ask only for the missing fields.
