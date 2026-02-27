####  BPM Signal


**Title:** 15MHz Chinese Time Signal BPM ceasing transmission at 09:00 UTC

**Contributed by:**  Nigel G4HZX

**Reviewed by:**

**Receiving Station Location:** IO91XK, South East London, UK

**Receiving Station Details** WSPRDaemon RX888 SDR receiver with a Leo Bodnar Electronics Mini GPS disciplined oscillator (GPSDO) set at 27 MHz. Omnidirectional vertical antenna.

**Feature Description**

![BPM](https://github.com/user-attachments/assets/31cab1f1-5cc1-4882-98bf-ea7359e25929)


This plot had me scratching my head for some time. Why did strong time signals - presumably from WWV - suddenly stop exactly at 09:00 UTC ?  This is not just a single event, but occurs every day.  If it was the band suddenly closing, it was remarkably repeatable. The answer is that the signal that stops at 09:00 is not WWV, but BPM, the Chinese time signal, which is intentionally switched off at 09:00 UTC. This time signal is transmitted from a site in eastern China, on exactly the same frequencies as WWV, 2.5, 5.0, 10.0 and 15.0 MHz.  London is very roughly half way on a great circle between WWV and BPM (7472 km to WWV, 8225km to BPM), so is well placed to observe both transmitters. 
    BPM transmits continuously on 5 and 10 MHz, but unlike WWV, the 15 MHz BPM transmitter is only operational between 01:00 and 09:00 UTC, and on 2.5 MHz, the hours are restricted to 07:30 to 01:00.  From a latitude point of view, BPM is 34.948 degrees North, and WWV is 40.679 North, so WWV is some 640 km further north,  - not a huge difference from an RF perspective. Looking at the day / night times, it is clear that the best - or indeed any -  reception from both stations occurs when both the tx and rx are in daylight, (or just passing into darkness)  which is to be expected for F2 layer multihop propagation. 
    It is unlikely that North American stations will easily receive BPM, as the great circle distance exceeds 11000 Km, but users should be aware of this co-channel signal. 


**References**

https://en.wikipedia.org/wiki/BPM_(time_service)
