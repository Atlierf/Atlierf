# 12 V to 5 V DC-DC Buck Converter — LTspice Simulation Demo

**[View Repository: `Atlierf/dc-dc-buck-converter-ltspice`](https://github.com/Atlierf/dc-dc-buck-converter-ltspice)**

A closed-loop 12 V-to-5 V (10–14 V input, up to 1 A load, 100 kHz) buck-converter simulation and engineering study in LTspice, using datasheet-based component models (`onsemi MBRS340`, `Bourns SRR1260-101M`, `Panasonic EEU-FR1C221`) and a tuned behavioral PID/PWM controller (`KP=0.015`, `KI=65`, `KD=1.2`).

### Measured LTspice 17.2.4 Results (`0.5 A → 1.0 A` load step at `2 ms`)

| Input (V) | Post-step `Vout` avg (V) | Post-step ripple (mVpp) | `IL` ripple (App) | Load-step min (V) | Settling time (`4.9–5.1 V`) | Efficiency (%) |
|---:|---:|---:|---:|---:|---:|---:|
| 10 | 4.9269 | 72.71 | 0.2597 | 4.5814 | 2.200 ms | 92.21% |
| 12 | 4.9887 | 45.88 | 0.3049 | 4.8149 | 0.460 ms | 92.58% |
| 14 | 5.0144 | 53.84 | 0.3401 | 4.9661 | 0.034 ms | 92.68% |

### Nominal 12 V Load-Step Response (`1.9–3.2 ms`)

![12 V Load-Step Response](https://raw.githubusercontent.com/Atlierf/dc-dc-buck-converter-ltspice/main/results/vin12v_load_step_closeup.svg)

### Explore the Project
- [Closed-Loop Netlist (`ltspice/buck_converter_closed_loop.cir`)](https://github.com/Atlierf/dc-dc-buck-converter-ltspice/blob/main/ltspice/buck_converter_closed_loop.cir)
- [Engineering Report (`docs/project_report.md`)](https://github.com/Atlierf/dc-dc-buck-converter-ltspice/blob/main/docs/project_report.md)
- [Component Models & Ratings (`docs/component_models.md`)](https://github.com/Atlierf/dc-dc-buck-converter-ltspice/blob/main/docs/component_models.md)
- [Simulation Results & Waveforms (`results/`)](https://github.com/Atlierf/dc-dc-buck-converter-ltspice/tree/main/results)
