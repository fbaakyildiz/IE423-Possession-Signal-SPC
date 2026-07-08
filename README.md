# Possession Signal SPC

Statistical process control analysis of live football ball-possession dynamics for IE 423 Quality Engineering.

Possession Signal SPC applies control-chart thinking to soccer match data. The project monitors ball-possession behavior, detects interesting matches and potential mean shifts, and studies how goals, cards, and penalties are reflected in possession trends.

> Course project repository for IE 423. This project is for academic analysis only and is not betting advice.

## Project Links

- [Project homepage](https://fbaakyildiz.github.io/IE423-Possession-Signal-SPC/)
- [Final report](reports/final-report.md)
- [Control chart notebook](notebooks/control_charts.ipynb)
- [Event shift notebook](notebooks/event_shift_analysis.ipynb)
- [Developer design document](docs/DESIGN.md)

## Project Summary

The project uses minute-level football match data to test whether ball-possession patterns provide insight into match outcomes and event-driven momentum changes. It selects interesting fixtures, builds Shewhart-style control charts, and interprets possession shifts around events such as goals, yellow cards, red cards, and penalties.

Core workflow:

1. Load match-level football event and statistics data.
2. Rank fixtures by an interest score using events and out-of-control behavior.
3. Select high-signal fixtures for manual interpretation.
4. Build control charts for home and away ball possession.
5. Compare first-40-minute and first-80-minute possession trends.
6. Relate possession shifts to match events and final outcomes.

## Repository Structure

```text
.
├── README.md
├── index.md
├── _config.yml
├── requirements.txt
├── assets/
│   └── control-charts/
├── data/
│   └── ie423_match_data.csv
├── docs/
│   └── DESIGN.md
├── notebooks/
│   ├── control_charts.ipynb
│   └── event_shift_analysis.ipynb
└── reports/
    └── final-report.md
```

## Reproducing The Analysis

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/control_charts.ipynb
```

The notebooks expect the dataset at:

```text
data/ie423_match_data.csv
```

## Academic Disclaimer

This repository is an IE 423 term project. It should not be used for betting, scouting, or production sports analytics decisions without additional validation.
