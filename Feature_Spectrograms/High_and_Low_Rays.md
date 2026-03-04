#### High and Low Rays

**Title:** Example of how rays from both high and low take-off angles reach a station via F region reflection

**Contributed by:** Gwyn Griffiths G3ZIL

**Reviewed by:**

**Receiving Station Location:** W2NAF near Scranton, Pa. FN21eh

**Receiving Station Details** WSPRDaemon Grape SDR receiver.

**Feature Description**

<img width="1416" height="384" alt="image" src="https://github.com/user-attachments/assets/8e889467-e018-437b-9f64-125dc5a63a44" />

This spectrogram at 25 MHz from WWV to W2NAF just happens to be from 8 April 2024, the day of the total solar eclipse. Hence the gap in great circle propagation between ~1900 and ~2015 UTC. Those examining this spectrogram as part of eclipse studies noticed the very small curls as the band opened just after 1400 UTC and as the eclipse temporarily closed the band at ~1900 UTC. What were the curls? To traces suggest two propagation paths, both via the F region, from the transmitter to the receiver. Immediately the band opened (or closed) there was only one F region path (for the ordinary ray) but within moments two paths became possible. The two paths had different initial ray elevations (take off angles). They are the so-called 'low ray' - at lower elevation - and a 'high ray' at a higher elevation. The high elevation ray penetrates higher into the ionosphere before being refracted (reflected) back to earth. 

PyLap ray tracing shows the geometry of the high and low rays. The example below is for 10 MHz on the path from WWV to N8GA Ohio on 26 July 2024. This type of feature is very common. It is usual for the two ray paths to diverge, for the low ray's elevation angle to reduce as its height of reflection falls and for the high ray's elevation angle to increase as ionisation reduces in the upper ionosphere. The high ray may reach an elevation angle where it escapes the ionosphere and not refracted to earth, in which case only the low ray will persist. Or the high ray may persist, as careful examination of the W2NAF spectrogram above shows two traces present most of the time.

![WWV_N8GA_26July2024_1145](https://github.com/user-attachments/assets/6b58910b-7197-45b2-bf42-636168ae2398)
