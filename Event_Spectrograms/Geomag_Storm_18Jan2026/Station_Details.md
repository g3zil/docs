### Contribution Details
#### Title: Analysis of Grape-1 DRF data for the January 18, 2026 X1.9-class solar flare induced geomagnetic storm
#### Contributed by: Robert Mattaliano, N6RFM and Gwyn Griffiths, G3ZIL
#### Reviewed by:
#### Receiving Station Location
Keller, TX EM12jw (near Fort Worth, TX)
#### Receiving Station Details
Half wave dipole for the 30M amateur radio band mounted at 10 feet and oriented east to west. The antenna is equipped with a 1:1 choke/balun at the feed-point (N9SAB Aetherwave Antenna). Signals are routed using LMR-195 coax to a lightning arrestor/surge protector (Riotaxy) followed by a 10.7 MHz center frequency, 2 MHz bandwidth pass band filter (Mini Circuits SBP 10.7+) then to the Grape-1 DRF receiver.  Receiver audio output is passed through a ground loop noise isolator (Besign). Audio levels are further adjusted using an in-line volume control (Volbox) and routed to an external soundcard (Behringer UCA202). Soundcard audio output is processed using a GNURadio [flowgraph](https://hamsci.org/grape1-drf-docs/) which includes a 25 Hz low pass filter. Resulting data are stored in the [Digital RF format](https://github.com/MITHaystack/digital_rf). The plots in this note were prepared using [plotspectrum_V4a.py](https://github.com/HamSCI/DRF_processing).
