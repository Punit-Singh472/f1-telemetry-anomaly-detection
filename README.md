# F1 Telemetry Analysis and Anomaly Detection

## Overview
This project analyses Formula 1 telemetry using Python and FastF1.
It explores vehicle speed, engine RPM, throttle, braking and gear
selection, then identifies unusual telemetry patterns using
statistical analysis and Isolation Forest.

## Objectives
- Retrieve and inspect F1 qualifying telemetry.
- Visualise vehicle behaviour over lap distance.
- Detect local speed deviations statistically.
- Apply unsupervised machine learning to multiple telemetry features.
- Compare detections and export results for further investigation.

## Tools
- Python
- FastF1
- Pandas and NumPy
- Matplotlib
- Scikit-learn

## Dataset
2024 British Grand Prix qualifying session.
Driver selected for the initial analysis: Max Verstappen.
Telemetry is obtained through the FastF1 Python package.

## Methodology
1. Load session and lap telemetry.
2. Explore data quality and telemetry distributions.
3. Plot speed, RPM, throttle and braking against lap distance.
4. Detect speed deviations using a rolling median and MAD-based threshold.
5. Detect multivariate anomalies using Isolation Forest.
6. Compare results and export an anomaly report.

## Results
- Telemetry points analysed: 659
- Statistical anomalies: 0
- Isolation Forest anomalies: 20
- Points flagged by both methods: 0

## Limitations
Anomalies represent unusual telemetry patterns, not confirmed power-unit
or engine failures. The Isolation Forest contamination setting is a
modelling assumption. Public lap telemetry does not provide access to
all internal power-unit sensors, engineering logs or labelled failures.

## Future Improvements
- Analyse multiple drivers and laps.
- Compare telemetry across different sessions and tyre compounds.
- Investigate anomaly locations on the circuit.
- Evaluate sensitivity to model parameters.
- Add richer visualisations and reproducible analysis.

## Disclaimer
This is an independent educational project using publicly accessible
motorsport telemetry. It is not affiliated with Red Bull Racing or
Red Bull Powertrains.
