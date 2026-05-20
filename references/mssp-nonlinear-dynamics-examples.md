# MSSP-Style Nonlinear Dynamics Figure Examples

These examples are synthetic templates for mechanical nonlinear dynamics papers, not benchmark data.

## Common Figure Types

| Figure type | Typical manuscript question | Template file |
|---|---|---|
| Phase portrait + Poincare section | Does the response settle to periodic, quasi-periodic, or complex motion? | `demo_phase_poincare.py` |
| Bifurcation diagram | How does the response branch as excitation frequency or amplitude changes? | `demo_bifurcation_diagram.py` |
| Time response + time-frequency map | Where do transient frequency components appear in time? | `demo_time_frequency_map.py` |
| Basin of attraction | Which initial conditions converge to different attractors? | `demo_basin_attraction.py` |
| Error boxplot | How robust is each identification or prediction method over repeated trials? | `demo_error_boxplot.py` |

## Style Notes

- Use double-column width for dense phase/Poincare and time-frequency composites.
- Use single-column width for one-panel bifurcation, basin, boxplot, and bar chart figures.
- For dense scatter plots, reduce marker size before increasing figure size.
- For color maps, keep labels and colorbar compact; avoid decorative colormaps unless the physics requires them.
- For categorical method comparison, use restrained colors and black edges.
