#### Partial Eclipse 29 March 2025
**Title:** Peturbations to Doppler shift on paths from CHU and WWVH to the UK during this partial eclipse

**Contributed by:** Gwyn Griffiths, G3ZIL

**Reviewed by:**

**Receiving Station Location:** IO91XK, South East London, UK

**Receiving Station Details** WSPRDaemon RX888 SDR receiver with a Leo Bodnar Electronics Mini GPS disciplined oscillator (GPSDO) set at 27 MHz. Omnidirectional Hustler trap vertical antenna 5B-TV.

**Brief Introduction**
While not an 'official' eclipse within the HamSCI [Festivals of Elcipse Ionospheric Science](https://hamsci.org/eclipse) the [deep partial eclipse](https://science.nasa.gov/eclipses/future-eclipses/mar-29-2025-eclipse/) over the North Atlantic on 29 March 2025 produced interesting Doppler peturbations from CHU and WWVH to the UK. This example also shows the usefulness of having PSWS in Europe.

![Eclipse_29March2025_map](https://github.com/user-attachments/assets/ddf28b31-9795-4c52-8117-b3ad5be54b67)
This map shows the great circle paths from CHU and WWVH to G4HZX, south east London, UK together with the eclipse obscuration contours. Both paths cross the 80% obscured contour, although only briefly for WWVH. Note the 11620 km path from WWVH is across the Auroral Oval.

**Results**

**CHU 7.85 MHz**

<img width="624" height="322" alt="image" src="https://github.com/user-attachments/assets/5f61ad1f-c106-4e95-9cb2-9db25f99fcdb" />

The great circle distance between CHU and G4HZX is 5385 km. The 'S' shape Doppler curve shown in the Feature Spectrogram entry is clearly present between about 0900 and 1100 UTC. In itself this is remarkable: on non-eclipse days in March 2025 7.85 MHz closed across the Atlantic around or before 0900 UTC. Admittedly the signal was weak during the eclipse - see the amplitude trace - but nevertheless this is a useful signal to study. 
Several observations can be made:
* There are two distinct Doppler traces, signifying two propagation modes were present. The mode with largest Doppler variation was weaker but persisted after the stronger mode ended.
* PyLap ray tracing showed the two modes to be three- and four-hop F region propagation: three-hop being the stronger (fewer reflections and crossings of the high absorption D region).
* The signal level increased around the time of maximum obscuration, that is, around the zero-Doppler up-crossing. Reduced solar UV radiation from the sun led to reduced ionisation in the D region, reducing absorption hence the increased signal level.
* 
The presence of two co-propagating modes makes further analysis complicated (but it should be done...).

**CHU 14.67 MHz**

![14 67MHz](https://github.com/user-attachments/assets/7f63ad34-21ad-4163-8c6b-82441bbdaae8)

Here we have a partial record of the eclipse-induced Doppler shift. In contrast to 7.85 MHz, on which propagation usually ends around the time the eclipse started, 14.67 MHz in late March is usually closed. Several observations can be made:
* There was only one great circle path (fine line) Doppler trace. PyLap ray tracing showed two- and three-hop paths were possible. It is difficult to know which was most likely.
* The very start of the eclipse, from around 0900 UTC, was not captured. But soon after a signal appeared and continuted until around the time of peak negative Doppler shift. It then disappeared, only to return as a weak signal around maximum positive Doppler shift, merging into the positive Doppler shift of the normal, daily dawn descent of the F region reflection height.
* The feint, fuzzy, wide trace is from sidescatter. The trace is very clear before the eclipse signal and continued to be present through the eclipse. However, it went negative and then positive earier than the great circle path. This suggests the sidescatter path was to the south of the great circle path, hence affected earlier by the eclipse.

While these features are interesting the partial record makes further analysis difficult (but it should be done...).

**WWVH 15 MHz**


