# 18-19 January 2026 X1.9 Flare and Subsequent LSTID

**Title:** Analysis of a TID seen during the January 18, 2026 X1.9-class solar flare induced geomagnetic storm

**Contributed by:** Bob Mattaliano, N6RFM and Gwyn Griffiths, G3ZIL

**Reviwed by:**

## Overview

This case study documents the prompt ionospheric response to the
X1.9 solar flare of 18 January 2026 (peak 18:09 UTC) and the
Large-Scale Traveling Ionospheric Disturbance (LSTID) that arrived
over the central US several hours later. A four-station HamSCI
Grape array recorded the event on WWV 10 MHz.

A four-station direction-of-arrival inversion using cross-correlation
of Doppler-vs-time series yielded a horizontal phase speed of
**666 m/s** with the wave propagating **toward azimuth 215° true (SW)**,
the source direction being **NE (35° true)**. This is consistent with
an equatorward-traveling LSTID driven by auroral-zone heating during
the early phase of the geomagnetic disturbance.

The complete analysis pipeline is available as an open-source Python
toolkit at [github.com/N6RFM/psws-drf-tid-tools](https://github.com/N6RFM/psws-drf-tid-tools).

## Stations and instrumentation

Four Grape-class receivers were used, all recording WWV 10 MHz from
Fort Collins, CO:

| Station   | Grid    | Latitude  | Longitude   | Instrument                              |
|-----------|---------|-----------|-------------|-----------------------------------------|
| N6RFM/5   | EM12jw  | 32.94°N   | -97.21°W    | Grape v1.12 (single-channel)            |
| AA6BD     | EM75kb  | 35.06°N   | -85.13°W    | AA6BDGrape1 (single-channel)            |
| W7LUX     | DM45dc  | 35.10°N   | -111.71°W   | Grape66 (single-channel)                |
| AC0G/ND   | EN16ov  | 46.88°N   | -96.83°W    | KA9Q_DXE_WWV (WSPRdaemon, subchannel 4) |

```{figure} ../_static/jan2026_lstid/array_map.png
:alt: Four-station array geometry with WWV-path midpoints and wave-direction arrow
:width: 95%

**Figure 1.** Four-station HamSCI Grape array geometry. Receiving
stations are shown as squares, WWV-path great-circle midpoints as
circles, the great-circle propagation paths as thin coloured lines,
and the inferred wave-propagation direction as a red arrow at the
array centroid. The map covers roughly 25° of longitude across the
central United States.
```

WWV-to-receiver great-circle midpoints span the central US, ranging
from southwestern Kansas (N6RFM/5 midpoint) to northern North Dakota
(AC0G_ND midpoint). The largest pairwise midpoint baseline is 1207 km
(W7LUX to AA6BD); bearings from the N6RFM/5 midpoint to the others are
72° (E to AA6BD), 282° (W to W7LUX), and 359° (N to AC0G_ND), giving
azimuthal coverage in three of four quadrants. The southerly direction
is unobserved — a geographic limitation, as no HamSCI Grape stations
operate south of Keller within single-hop WWV range.

Raw Digital RF I/Q data was reduced to Doppler-vs-time at 10-second
cadence by FFT peak-tracking the WWV carrier within a ±5 Hz search
band.

## Observation 1: Solar flare direct detection

A long-duration X1.9 flare from active region AR4341 peaked at 18:09
UTC on 18 January 2026 (NOAA/SWPC, SANSA reports). The Grape data
captured the prompt ionospheric response unambiguously.

```{figure} ../_static/jan2026_lstid/n6rfm_jan18_annotated.png
:alt: N6RFM/5 Doppler spectrogram, 16:00-24:00 UTC 18 January 2026, showing X1.9 flare SWF
:width: 95%

**Figure 2.** N6RFM/5 Doppler spectrogram, 16:00–23:59 UTC on 18 January
2026. The WWV 10 MHz carrier track (red) is clearly visible before
and after the cyan-bracketed Short-Wave Fadeout window. The lower
panel shows peak amplitude per minute; the carrier collapses to
near-noise during the SWF and recovers slowly through the evening.
```

At approximately **17:45 UTC**, N6RFM/5 recorded a Short-Wave Fadeout
(SWF): the WWV 10 MHz carrier became undetectable on the spectrogram,
with received signal amplitude collapsing to near-noise level. The
fadeout persisted for approximately 45 minutes before the carrier
returned around 18:30 UTC. This is the textbook prompt ionospheric
absorption signature of a major solar flare: the X-ray pulse causes a
sudden enhancement of D-layer ionization, which strongly absorbs HF
signals propagating through it.

The fadeout duration (~45 min) and timing (centred on the X1.9 flare
peak at 18:09 UTC) is consistent with an X-class flare's expected
short-wave radio impact at mid-latitudes during local daytime
illumination.

## Observation 2: TID onset and 4-station propagation analysis

The post-flare ionosphere remained quiet from approximately 19:00 to
22:30 UTC on 18 January. Beginning around 22:30–23:00 UTC, organized
Doppler oscillations appeared, growing in amplitude through 00:00–01:45
UTC on 19 January.

```{figure} ../_static/jan2026_lstid/n6rfm_jan19_annotated.png
:alt: N6RFM/5 Doppler spectrogram, full day 19 January 2026, with 4-station DOA analysis window annotated
:width: 95%

**Figure 3.** N6RFM/5 Doppler spectrogram for the full 24 hours of
19 January 2026, with the 4-station DOA analysis window
(00:00–01:15 UTC) bracketed in cyan. The clean wavy carrier track
inside the window shows approximately one full cycle of the dominant
~80-minute LSTID wave. Subsequent activity from approximately 13:30
UTC onward marks the storm main phase.
```

Looking at the N6RFM/5 spectrogram in Figure 3, the first ~90 minutes
of the UTC day show an unmistakable slow oscillation in the WWV 10 MHz
carrier track:

- A negative excursion down to about -0.8 Hz around 00:40 UTC
- A return through zero near 01:00 UTC
- A positive peak near +0.6 Hz around 01:13 UTC
- A return to near-zero by ~01:30 UTC

That is approximately one full cycle of an ~80–100 minute wave — a
textbook TID signature. The remainder of the day shows unrelated
storm-driven activity beginning in the local afternoon.

In the results shown below, a slow wavetrain with period ~80–100 min and Doppler amplitude
±0.7–1.5 Hz dominated all four station traces. The waveform shape is
similar across stations, with AA6BD (NE of N6RFM/5) and AC0G_ND (N)
clearly leading N6RFM/5, while W7LUX (W) is approximately synchronous
with N6RFM/5.

```{figure} ../_static/jan2026_lstid/stack_jan19.png
:alt: Four-station stacked Doppler comparison showing successive peak times
:width: 95%

**Figure 4.** Four-station Doppler comparison, 00:00–01:15 UTC on
19 January 2026. Each panel shows one station on a shared time axis;
the inverted-triangle markers indicate each trace's peak. The
successive peak times — AC0G_ND at 00:50:40, AA6BD at 00:57:38,
W7LUX at 01:05:07, N6RFM/5 at 01:13:14 — span 23 minutes and reveal
the wave's NE-to-SW propagation directly.
```

### Cross-correlation pairwise analysis

All six station pairs were cross-correlated over the 00:00–01:15 UTC
window. The Doppler series were mean-subtracted and z-normalized;
no bandpass filter was applied (see Methodology note below for why).

| Pair                  | Lag (s) | Lag (min) | Correlation |
|-----------------------|--------:|----------:|------------:|
| N6RFM/5 → AA6BD         |    -940 |     -15.7 |       0.577 |
| N6RFM/5 → W7LUX         |     -70 |      -1.2 |       0.564 |
| N6RFM/5 → AC0G_ND       |   -1340 |     -22.3 |       0.698 |
| AA6BD → W7LUX         |   +1280 |     +21.3 |       0.688 |
| AA6BD → AC0G_ND       |       0 |       0.0 |       0.771 |
| W7LUX → AC0G_ND       |    -980 |     -16.3 |       0.737 |

Sign convention: positive lag means the second station's signal
arrives later than the first; negative lag means the second station
leads.

The three independent triangles close to within ~7 minutes on lag
sums, indicating internally consistent timing across the array.

### Slowness-vector inversion

The six pairwise lags `τ_ij` were used to solve the overdetermined
linear system

$$\tau_{ij} = \mathbf{s} \cdot (\mathbf{r}_j - \mathbf{r}_i)$$

by ordinary least-squares, where $\mathbf{r}_i$ is the projection of
station $i$'s WWV-path midpoint onto a local east–north tangent plane
and $\mathbf{s}$ is the 2D slowness vector. The phase speed is then
$v = 1/|\mathbf{s}|$ and the azimuth of motion is $\theta = \arctan(s_x/s_y)$.

**Result:**

- Horizontal phase speed: **666 m/s** (2398 km/h)
- Azimuth of motion (heading toward): **214.9° true** (SW)
- Source azimuth (coming from): **34.9° true** (NE)
- Classification: **LSTID** — consistent with the conventional
  300–1000 m/s range for Large-Scale Traveling Ionospheric Disturbances

## Discussion

The 5-hour delay between flare peak (18:09 UTC Jan 18) and TID
arrival over the central US (~23:00 UTC Jan 18 onward) is consistent
with acoustic-gravity-wave propagation timescales from a high-latitude
source to the mid-latitude F-region. The SW propagation direction
(coming from azimuth 35° true) is inconsistent with direct flare-
driven waves from the subsolar point (which was over the central
Pacific at 18 UTC). It is, however, consistent with **auroral-zone
heating** during the early geomagnetic disturbance phase.

The X1.9 flare's CME impact reached Earth on 19 Jan 2026, eventually
producing G4-level conditions, but precursor solar-wind effects can
drive auroral electrojet activity and Joule heating earlier. Such
heating in the polar thermosphere generates equatorward-propagating
LSTIDs that reach mid-latitudes in 3–6 hours, matching the observed
arrival timing and propagation direction.

The horizontal phase speed of 666 m/s places this event firmly in the
LSTID category. With a dominant period of 80–100 min, the wavelength
is ~3000–4000 km, which is at the long end of typical LSTID wavelengths
and is consistent with a single coherent gravity wave mode rather than
a superposition of smaller features.

## Methodology

The complete analysis pipeline used in this study comprises:

1. **Station discovery** — Query PSWS for all stations with DRF I/Q
   recordings on the event date, ranked by midpoint-baseline geometry.
2. **Per-station metadata verification** — Read DRF metadata to
   confirm the correct subchannel index for the target frequency.
3. **Doppler extraction** — FFT peak-tracking with Hanning window and
   quadratic sub-bin interpolation, yielding ~0.01 Hz resolution.
4. **Direction-of-arrival inversion** — Pairwise cross-correlation
   over all station pairs, followed by least-squares slowness-vector
   solution.

All scripts are MIT-licensed and available at
[github.com/N6RFM/psws-drf-tid-tools](https://github.com/N6RFM/psws-drf-tid-tools).

```{note}
**A methodological pitfall worth knowing about.** An earlier version
of this analysis applied a 40–90 minute bandpass filter to each
Doppler trace before cross-correlation. The result was qualitatively
wrong: AA6BD appeared to *lag* N6RFM/5 by 2.7 minutes (instead of
leading by 15.7), with a deceptively high correlation of 0.93. The
DOA solution claimed the wave was moving at 1221 m/s heading 165°
(due south).

The problem is that bandpassing produces a nearly sinusoidal signal
whose autocorrelation has high-correlation lobes spaced one wave
period apart. The lag-finder grabbed a secondary lobe rather than
the true peak. Removing the bandpass (and using just mean-subtracted
raw Doppler) recovered the correct answer.

For cross-correlation of slowly varying TID signals, narrow-band
filtering before correlation can be actively harmful. The toolkit's
default is to disable it.
```

## Data access

Raw DRF I/Q files for all stations on 18–19 January 2026 are available
on the PSWS Central Control System:

- N6RFM/5: <https://pswsnetwork.eng.ua.edu/observations/select_download_range/142035/>
- AA6BD:   <https://pswsnetwork.eng.ua.edu/observations/select_download_range/142027/>
- W7LUX:   <https://pswsnetwork.eng.ua.edu/observations/select_download_range/142042/>
- AC0G/ND: <https://pswsnetwork.eng.ua.edu/observations/select_download_range/142067/>

## Acknowledgments

Thanks to the operators of AA6BD, W7LUX, and AC0G/ND for keeping
clean Grape stations running through the event. To W. Engelke (AB4EJ),
University of Alabama, for the original spectrogram plotting approach.
To Nathaniel Frissell (W2NAF) and colleagues at the University of
Scranton for the HamSCI / PSWS infrastructure. To MIT Haystack
Observatory for the Digital RF format. The analysis toolkit was
developed collaboratively with Anthropic's Claude AI.
