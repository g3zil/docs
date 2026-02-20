### Contribution Details
#### Title: Analysis of Grape-1 DRF data for the January 18, 2026 X1.9-class solar flare induced geomagnetic storm
#### Contributed by: Robert Mattaliano, N6RFM and Gwyn Griffiths, G3ZIL
#### Reviewed by:
#### Receiving Station Location
Keller, TX EM12jw (near Fort Worth, TX)
#### Receiving Station Details
Half wave dipole for the 30M amateur radio band mounted at 10 feet and oriented east to west. The antenna is equipped with a 1:1 choke/balun at the feed-point (N9SAB Aetherwave Antenna). Signals are routed using LMR-195 coax to a lightning arrestor/surge protector (Riotaxy) followed by a 10.7 MHz center frequency, 2 MHz bandwidth pass band filter (Mini Circuits SBP 10.7+) then to the Grape-1 DRF receiver.  Receiver audio output is passed through a ground loop noise isolator (Besign). Audio levels are further adjusted using an in-line volume control (Volbox) and routed to an external soundcard (Behringer UCA202). Soundcard audio output is processed using a GNURadio [flowgraph](https://hamsci.org/grape1-drf-docs/) which includes a 25 Hz low pass filter. Resulting data are stored in the [Digital RF format](https://github.com/MITHaystack/digital_rf). The plots in this note were prepared using [plotspectrum_V4a.py](https://github.com/HamSCI/DRF_processing).

#### Brief Introduction 
On January 18, 2026, the Sun produced a long-duration [X1.9-class solar flare](https://www.swpc.noaa.gov/news/x-class-flare-activity-observed-18-january-2026). This strong flare launched a full-halo coronal mass ejection (CME) directed toward Earth. The results below were obtained just prior to, during and after this space weather event. The data were collected by a station in Keller, Texas (grid square EM12jw, near Fort Worth) while monitoring WWV on 10 MHz from Fort Collins, Colorado. The separation distance is approximately 1100 kilometers (about 680 miles). This means that signals from WWV in Fort Collins to north Texas travel through the D and E and often the F ionospheric regions. This distance also explains why both day/night and space-weather effects are observed along that path in the resulting spectrograms. 

#### 18 January 2026 (prior day sunset 2347 UTC sunrise 1330 UTC)

![Doppler Spectrogram of WWV 10 MHz at N6RFM on 18 January 2026](https://github.com/user-attachments/assets/121350de-a827-4c6f-8ecf-fe1d9a3decb8)

* A.	~ 0000-0145 F region propagation with minimal, but variable Doppler, the path then rapidly closed. Very light thin-trace reflections above and below the main signal are Grape-1 receiver system mixing artifacts.
* B.	~ 0145-1000 Very weak, fuzzy (wide spectrum) trace consistent with two-hop sidescatter via the F region (Griffiths et al., 2023). Somewhat stronger signals with near zero-Doppler at B1 and B2 may have been from sporadic E (Es) propagation. Ionosonde data is very useful for checking the possibility of Es. However, ionosondes are few and those that openly report data even fewer. The ionosonde near Austin TX, some 800 km SSE of the WWV-N6RFM midpoint did show weak Es around 0600 UTC. Open the [GIRO Ionosonde Data Portal](https://giro.uml.edu/ionoweb/#) then click code AU930 and find date.
* C.	~0700-1530 and later are likely interference rather than WWV-related.
* D.	~ 1345 Dramatic F region one-hop propagation opening close to local sunrise with weaker lower amplitude (D1 yellow) trace likely representing a higher-elevation path.  The positive and reducing Doppler is consistent with morning descending height of reflection. D2, the yellow curl above the one-hop F region Doppler in red, is two-hop F region propagation involving four passes through the D and E region resulting in additional absorption hence a weaker signal. The subsequent yellow trace is variable Doppler via the two-hop mode.
* E.	~ 1400- 1930 F region propagation path open, then closes, but with very weak two-hop sidescatter persisting, then reopens. 
* F.	~ 2030-2345 First, weak E region propagation with near-zero Doppler, then both F region one-hop (red) and weaker and more variable (yellow) propagation is observed.  The latter is consistent with two-hop F region propagation.

#### 19 January 2026 (prior day sunset 2348 UTC sunrise 1330 UTC)
![Doppler Spectrogram of WWV 10 MHz at N6RFM on 19 January 2026](https://github.com/user-attachments/assets/9088cf22-d305-4452-bdf0-017e5a2b4496)

* A.	~ 0000-0200 One-hop F region propagation showing a Travelling Ionospheric Disturbance (TID). Evidence for a travelling disturbance is that the pattern here is delayed by 23 minutes compared with the Doppler variation at [N5TNL](https://pswsnetwork.caps.ua.edu/observations/select_download_range/142094/) in EM25ui 375 km to the NE. 
* B.	~0100 Short lived two-hop F region propagation opening as the electron density temporarily increases during the downward part of the TID cycle (Griffiths, 2025)
* C.	~ 0200 F region propagation path rapidly closes. C1 is a brief appearance of the higher elevation one-hop F region ray with negative and rapidly reducing Doppler.
* D.	~ 0200-1330 Weak two-hop F region side-scatter propagation.
* E.	~1330-1350 Weak near-zero Doppler characteristic of E region propagation.
* F.	~ 1330 Dramatic F region path opening at local sunrise with short-lived lower amplitude (yellow) upward-curling feature F1, likely a higher-elevation F region path. F2 yellow trace is the two-hop path opening.
* G.	~ 2030-0000 Impact of the CME from the 18 Jan 2026 X1.9-class solar flare resulting in dramatic off-scale variations in Doppler shift. At ~2017 G1 is the response of the two-hop F region ray, with its first hop further north than the one-hop F region path and both reflections higher in the ionosphere than the one-hop. At G2 one-hop F region propagation persists with minimal Doppler until ~2041 G3 when the one-hop F region ray is affected by the disturbance. G4 is possibly the high elevation ray starting with off-scale Doppler, reducing, and meeting the lower elevation Doppler value. There is a short gap in one-hop F region propagation before a weak Doppler half-cycle returning to 'normal' G5 before an off-scale negative pulse at G6. During this time E region propagation appears to be unaffected, with near-zero Doppler, G7.
  
While it is common to assume Doppler shift to be caused by vertical motion of the height of reflection, e.g. as at dawn and dusk or due to a TID, Doppler can also be caused by a change to the electron density (Chum et al., 2018). Attribution of these observed changes in Doppler to vertical motion and changes in electron density is a research question worthy of in-depth analysis.

#### 20 January 2026 (prior day sunset 2349 UTC sunrise 1330 UTC)
![Figure 3 20 January 2026](https://github.com/user-attachments/assets/d4f69719-eb67-4d1d-b92d-3f2fa9379c4f)

* A.	~ 0000-0245 one-hop and, until ~ 0130, weak two-hop F region propagation.  Just before the band closes there is a brief appearance of the higher ray with negative and reducing Doppler shift A1.
* B.	The band briefly closes and ~ 0300 re-opens until ~ 0530 with near-zero Doppler shift sporadic E propagation. The Austin ionosonde showed a distinct Es layer from 0245–0555.
* C.	Weaker lower amplitude (yellow) traces likely represent two-hop side scatter F region propagation, which diminishes then disappears ~ 1000.  Two-hop sidescatter can occur from multiple ground and or sea regions, hence several traces are not uncommon. These observations deserve an in-depth study including simple PyLap ray trace modeling (Griffiths et al., 2023).
* D.	~ 1000-1500 10 MHz propagation is closed, with fine-line artifacts visible.
* E.	 ~1500 Start of near-zero Doppler shift E region propagation, persisting until ~2200.
* F.	 ~1730 abrupt F region propagation start at ~ 1730 with over 2 Hz Doppler shift. At four hours after local sunrise this is not the usual morning event (as on the 19th): it is unusual and deserves in-depth study to understand how/why the geomagnetic storm delayed normal band opening time (reduced electron density?).  ~1800 lower-amplitude two-hop propagation begins (F1) with significant Doppler shift. Why there is such a radical difference in Doppler shift variations for the one-hop and two-hop paths truly deserves an in-depth study. One hypothesis to test is whether the one-hop path was perhaps via the F1 layer at the base of the F region and the two-hop path via the higher F2 layer. The associated hypothesis is that the F1 layer behaves more like the E region with less Doppler variation than via the F2 layer.



