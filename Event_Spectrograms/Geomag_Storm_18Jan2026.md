### Contribution Details
#### Title: Analysis of Grape-1 DRF data for the January 18, 2026 X1.9-class solar flare induced geomagnetic storm
#### Contributed by: Robert Mattaliano, N6RFM and Gwyn Griffiths, G3ZIL
#### Reviewed by:
#### Receiving Station Location
Keller, TX EM12jw (near Fort Worth, TX)
#### Receiving Station Details
Half wave dipole for the 30M amateur radio band mounted at 10 feet and oriented east to west. The antenna is equipped with a 1:1 choke/balun at the feed-point (N9SAB Aetherwave Antenna). Signals are routed using LMR-195 coax to a lightning arrestor/surge protector (Riotaxy) followed by a 10.7 MHz center frequency, 2 MHz bandwidth pass band filter (Mini Circuits SBP 10.7+) then to the Grape-1 DRF receiver.  Receiver audio output is passed through a ground loop noise isolator (Besign). Audio levels are further adjusted using an in-line volume control (Volbox) and routed to an external soundcard (Behringer UCA202). Soundcard audio output is processed using a GNURadio [flowgraph](https://hamsci.org/grape1-drf-docs/) which includes a 25 Hz low pass filter. Resulting data are stored in the [Digital RF format](https://github.com/MITHaystack/digital_rf). The plots in this note were prepared using [plotspectrum_V4a.py](https://github.com/HamSCI/DRF_processing).

### Brief Introduction 
On January 18, 2026, the Sun produced a long-duration [X1.9-class solar flare](https://www.swpc.noaa.gov/news/x-class-flare-activity-observed-18-january-2026). This strong flare launched a full-halo coronal mass ejection (CME) directed toward Earth. The results below were obtained just prior to, during and after this space weather event. The data were collected by a station in Keller, Texas (grid square EM12jw, near Fort Worth) while monitoring WWV on 10 MHz from Fort Collins, Colorado. The separation distance is approximately 1100 kilometers (about 680 miles). This means that signals from WWV in Fort Collins to north Texas travel through the D and E and often the F ionospheric regions. This distance also explains why both day/night and space-weather effects are observed along that path in the resulting spectrograms. 
