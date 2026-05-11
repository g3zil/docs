#### SID and Doppler Flash

**Title:** Example of effect of a Sudden Ionospheric Disturbance (SID) with a Doppler Flash at 15, 20 and 25 MHz from WWV

**Contributed by:** Gwyn Griffiths G3ZIL

**Reviewed by:**

**Receiving Station Location(s):** N8GA Miamisburg, Ohio EN80ee and GB0PSC Baldock, UK IO92wa

**Receiving Station Details** WSPRDaemon Grape SDR receiver.

**Feature Description**

<img width="996" height="1503" alt="S000113_117_2024-05-14T00-00_EN80ee" src="https://github.com/user-attachments/assets/b55bf850-ae50-4a33-87b5-ef8365d26faa" />


***Sudden Ionospheric Disturbance***
This set of Doppler spectrograms at 15, 20 and 25 MHz from WWV to N8GA on 14 May 2024 is rich in propagation mode features including E and F region one hop and two-hop sidescatter. It is also a nice example of the effect of a Sudden Ionospheric Disturbance (SID) in response to an X8.79 solar flare that [peaked](https://svs.gsfc.nasa.gov/14592/) at 12:51 EDT (16:51 UTC). On all three frequencies the spectrograms and the peak signal level graphs show a precipitous drop at about 16:47 UTC. This was during the sharp increase in free electron production in response to the X-ray radiation causing increased ionisation hence absorption in the D region. Signals had reached the noise level by 16:48:30 UTC, that is, in just 90 seconds. Recovery began after 15 minutes on 25 MHz and after 22 minutes at 20 and 15 MHz, taking over an hour to match the pre-SID level. SIDs from less intense solar flares may not have an effect extending to 25 MHz or may not reduce the signal level to the local noise, but the signal level drop will be sudden.

***Doppler Flash***
The sudden increase in free electron production also results in a change in refractive index, affecting path length, hence seen as a sudden Doppler shift. Doppler shift also arises from a change in height of the reflection. These factors are well described in a [paper](https://link.springer.com/content/pdf/10.1186/s40623-018-0976-4.pdf) by Chum and colleagues. The term 'Doppler flash' is indeed appropriate: the response during the SID example at N8GA, above, following the X8.79 flare, was so fast as to not show in the spectrograms. However, through processing the raw Doppler data at 15 MHz and changing from a processing interval of one minute to 18 seconds once the X-ray flux started to rise we can see in the plot below that the PSWS RX888 at N8GA did indeed capture a Doppler flash. Doppler changed by about 1.2 Hz in 90 seconds before absorption caused the signal to descend into the noise. 

<img width="498" height="345" alt="Hi_Res_N8GA_2024-05-14" src="https://github.com/user-attachments/assets/fc3ab9bc-9e4e-4d93-9db8-5ea077a02d7f" />

With a moderately strong solar flare a lower rate of increase of absorption may allow the associated Doppler flash to be visible directly on the PSWS spectrogram. This wasthe case for the M5.7 flare on 10 May 2026. Starting at 13:19 UTC peaking at 13:39 UTC a Doppler flash followed by a short blackout was observed at 14.67 MHz from CHU and 20 MHz from WWV at the RSGB Propagation Studies Committee site GB0PSC, Baldock UK.

<img width="964" height="252" alt="S000262_334_2026-05-10T00-00_IO92wa_CHU" src="https://github.com/user-attachments/assets/2cbf3dd6-3f4a-44c7-be2a-4e2261ef9723" />

<img width="959" height="253" alt="S000262_334_2026-05-10T00-00_IO92wa_WWV" src="https://github.com/user-attachments/assets/6feb6e59-446f-4763-acaf-9d406194dc79" />
