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

<img width="936" height="483" alt="image" src="https://github.com/user-attachments/assets/5f61ad1f-c106-4e95-9cb2-9db25f99fcdb" />

The great circle distance between CHU and G4HZX is 5385 km. The 'S' shape Doppler curve shown in the Feature Spectrogram entry is clearly present between about 0900 and 1100 UTC. In itself this is remarkable: on non-eclipse days in March 2025 7.85 MHz closed across the Atlantic around or before 0900 UTC. Admittedly the signal was weak during the eclipse - see the amplitude trace - but nevertheless this is a useful signal to study. 
Several observations can be made:
* There are two distinct Doppler traces, signifying two propagation modes were present. The mode with largest Doppler variation was weaker but persisted after the stronger mode ended.
* PyLap ray tracing showed the two modes to be three- and four-hop F region propagation: three-hop being the stronger (fewer reflections and crossings of the high absorption D region).
* The signal level increased around the time of maximum obscuration, that is, around the zero-Doppler up-crossing. Reduced solar UV radiation from the sun led to reduced ionisation in the D region, reducing absorption hence the increased signal level.
  
The presence of two co-propagating modes makes further analysis complicated (but it should be done...).

**CHU 14.67 MHz**

![14 67MHz](https://github.com/user-attachments/assets/7f63ad34-21ad-4163-8c6b-82441bbdaae8)

Here we have a partial record of the eclipse-induced Doppler shift. In contrast to 7.85 MHz, on which propagation usually ends around the time the eclipse started, 14.67 MHz in late March is usually closed. Several observations can be made:
* There was only one great circle path (fine line) Doppler trace. PyLap ray tracing showed two- and three-hop paths were possible. It is difficult to know which was most likely.
* The very start of the eclipse, from around 0900 UTC, was not captured. But soon after a signal appeared and continuted until around the time of peak negative Doppler shift. It then disappeared, only to return as a weak signal around maximum positive Doppler shift, merging into the positive Doppler shift of the normal, daily dawn descent of the F region reflection height.
* The feint, fuzzy, wide trace is from sidescatter. The trace is very clear before the eclipse signal and continued to be present through the eclipse. However, it went negative and then positive earier than the great circle path. This suggests the sidescatter path was to the south of the great circle path, hence affected earlier by the eclipse.

While these features are interesting the partial record makes further analysis difficult (but it should be done...).

**WWVH 15 MHz**

![15MHz](https://github.com/user-attachments/assets/f6a90091-6fc6-403a-8dce-9c76d9808a96)

The 15 MHz trace is also partial, in that it ends around the time of peak positive Doppler. As only a single propagation mode was present, this record has been studied in more detail. First it is vital to know which of the three transmitters - WWV, WWVH and BPM - produced this signal. The Chinese station BPM can be eliminated as it stops transmitting at 0900 UTC. The question of WWV or WWVH was answered using [Proppy](https://soundbytes.asia/proppy/p2p), an online implementation of the ITU propagation prediction code [ITU-R P.533-14](https://www.itu.int/dms_pubrec/itu-r/rec/p/R-REC-P.533-14-201908-I!!PDF-E.pdf). From the Proppy output for the paths from WWV and WWVH on 15 MHz the predicted signal levels were plotted, figure below, showing that during the eclipse WWVH, as the strongest signal, was the most likely source. This ties in with the wider, slightly fuzzy trace from the trans-polar propagation path from WWVH.

<p align="center">
  <img width="425" height="207" alt="image" src="https://github.com/user-attachments/assets/de3f4b18-da72-4f44-97c5-e53b4ce48bba" />
</p>

***Propagation path, hops and reflection locations***

<p align="left">
  <img src="https://github.com/user-attachments/assets/f92e7671-5692-4256-9140-39c4b87ff419" alt="Eclipse_29March2025" />
</p>

PyLap ray tracing showed four-hop propagation for 1100 UTC with a chordal hop between the first and second ioniospheric reflections. (In a chordal hop there is no ground reflection bwteen two ionospheric reflections). From the ray trace both the third and fourth reflections were likely affected by the eclipse. The map shows these reflections at substantially different latitudes and longitudes hence different sun altitudes. Therefore the next step was to calculate an eclipse function.

***Eclipse function and timing coincidence with observed Doppler***

<p align="center">
  <img width="418" height="257" alt="image" src="https://github.com/user-attachments/assets/b0b90b0a-b08e-4203-86e7-dce68cfcb79d" />
</p>

Eclipse times at ray-trace inferred reflection locations and heights (72.75˚N 27.6˚W at 250 km for 3rd reflection and 58.25˚N 4.65˚W at 210 km for 4th reflection) were calculated in a Python script by [Verhulst and Stankov](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020JA028088) modified to calculate solar zenith angles at reflection heights. Of course, reflection locations are indicative. Actual locations depend on effective sunspot number and height of reflections on the day. Also important is whether the first two hops were chordal as in PyLap. Nevertheless the time sequence for the 3rd and 4th reflections individually and the additive composite is likely robust.

My hypothesis is that the eclipse Doppler variation with time should follow the composite curve more closely than the individual curves: showing that the signal was Doppler shifted at the 3rd and 4th reflections. The additive curve at the earth’s surface is shown for reference.

![Eclipse_29March2025](https://github.com/user-attachments/assets/069d0ab8-d6e6-4a62-a959-9ee1b035b810)

These three time series plots show 15 MHz WWVH Doppler shift computed using an [autocorrelation algorithm](https://github.com/g3zil/grapeDRF_doppler_model). Recalling that Doppler shift is __rate of change__ of phase path length, plotting the negative __rate of change__ of solar obscuration produces an 'S' curve. I am not looking for a shape match only the timing of maximum negative. As is clear, the observed maximum negative Doppler shift was coincident with the maximum negative rate of change of obscuration for the combined third and fourth reflections, supporting the ray trace prediction that the signal was eclipse-affected at both those reflections.

***Relationships between Doppler shift and Obscuration***

![Eclipse_29March2025](https://github.com/user-attachments/assets/eaebc70c-b945-4722-b84b-6c39c57fd8c9)

On the left are the time series of observed Doppler shift and rate of change of obscuration divided into five regions. On the right is a scatterplot of Doppler shift against the sum of the obscuration factors at the PyLap locations of the two reflections for Regions 2, 3 and 4. Comments and quetions follow:

* ***Region 0:*** </span> 09:00–09:54 Pre-eclipse. Short-period (~6 minute) variations, mean ~ -0.2 Hz.
* ***Region 1:*** 09:55–10:04 Pre-eclipse but step to more –ve Doppler. Step to more negative Doppler could be in keeping with fluctuations in Region 0. Or, was it induced by another mechanism? Why is the Doppler negative (mean -0.7 Hz), implying rising height of reflection if the dominant process is advection?, Conventionally at this time, it should be positive and reducing.
* ***Region 2:*** 10:05–10:14 Eclipse only at 4th reflection. The question why the initial Doppler is negative remains. Rate of change with obscuration % at -0.019 Hz/% is less than Region 3 but not by much.
* ***Region 3:*** 10:15–10:43 Spanning interval of start of eclipse at both reflections to inflexion in Doppler slope from negative to positive. Clear relationship between Doppler and obscuration, slope -0.025 Hz/% and R^2 0.922. Small-scale wave-like features modulate the relationship, e.g. at ~10:22 UTC and ~10:30 UTC.
* ***Region 4:*** 10:44– 11:01 From Doppler inflexion to end of smooth, stable Doppler variation, marked by step in Doppler spread. After inflexion at 10:43 UTC the slope is almost double at +0.046 Hz/% with R^2 0.963. There’s an absence of small-scale features in mean Doppler (possibly why R^2 was higher). Why the marked difference in slopes?
* ***Region 5:*** 11:02–11:31 Variable measured Doppler when positive half cycle (descent) expected, which is there until 11:12. At 11:31 assured propagation from WWVH ended. Can we trust the measurements? Analysis showed that the received spectrum was sufficiently wide in Region 5 to be 'spectrally clipped'. That is, with a positive Doppler the skirt of the spectrum, only some 20 dB down from the peak, extended right to +5 Hz, the positive limit. The skirt at the the negative limit of -5 Hz was some 30 dB down. Hence the autocorrelation Doppler estimate would be biassed positive, making the data unreliable in Region 5.

**Conclusion**

The 29 March 2025 partial eclipse over the Atlantic Ocean provided a nice peturbation to the Doppler shift on paths from CHU and WWVH to the UK. While the spectrograms illustrate the Doppler response of the ionosphere through change in Doppler shift the existence of three- and four-hop propagation modes on the CHU 7.85 MHz record and the gap in the CHU 14.67 MHz record leaves the 15 MHz WWVH record as the most complete. The time of maximum negative Doppler on the 15 MHz path was within a minute of the time of maximum rate of change of combined bscuration at the ray-trace inferred locations of the third and fourth reflections. Notable was the difference in slope Doppler shift : Obscuration before and after the maximum rate of change of obscuration during the darkening phase of the eclipse.
