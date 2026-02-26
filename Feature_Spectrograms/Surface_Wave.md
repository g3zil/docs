#### Surface Wave
**Title:** Example of Surface Wave from WWV at 25 MHz

**Contributed by:** Gwyn Griffiths G3ZIL

**Reviewed by:**

**Receiving Station Location:** WW0WWV/0 (keeper Dave Swartz W0DAS) 7 km east of WWV, near Fort Collins, CO DN70mq

**Receiving Station Details:** WSPRDaemon Grape SDR receiver with a Leo Bodnar Electronics [Mini GPS](https://www.leobodnar.com/shop/index.php?main_page=product_info&cPath=145&products_id=301) disciplined oscillator (GPSDO) set at 27 MHz. 

**Feature Description**
![WW0WWV_25MHz_26July2024](https://github.com/user-attachments/assets/96534737-0bbd-4737-9d94-3b897b89d3ae)

It is good practice in experimental scientific research to have a control. That is, a set of observations where, with high certainty, one can be sure that the measurements are not affected by the factors being studied. For a HamSCI PSWS the control is provided by station WW0WWV/0, maintained by Dave Swartz W0DAS, some 7 km line of sight from WWV. At 25 MHz propagation is assuredly via surface wave only on this 7 km path. Hence the Doppler trace above is completely flat at zero Hz. 

The digital_RF data from WW0WWV/0 can be post processed to examine the PSWS measured frequency with sub-milliHz resolution. Having the control station at WW0WWV/0 means that we can see two artifacts, one to the mini Bodnar GPSDO and the other a combination of ionospheric variability and the mini Bodnar GPSDO. Both can be seen in the plot below:
* Frequency offset - Older Bodnar GPSDOs such as the mini GPS used at WW0WWV/0 use a Frequency Lock Loop (FLL) rather than a Phase Locked Loop. According to Leo Bodnar this provides, "less hunding and quicker settling Allan Deviation ... in exchange for a non-zero frequency offset". At 25 MHz in this data set with the at 27 MHz GPSDO the median frequency offset was 0.36 mHz, that is 1.3 parts in 10^11 of the GPSDO frequency. This offset may be important for some HamSCI applications, particularly Time of Flight measurements. The more recent Leo Bodnar LBE-1420 and LBE1421 have PLL as default with FLL selectable and hence have no frequency offset.
* Periodic variation - The mini Bodnar GPSDO is a single frequency device receiving only the L1 signal (1575.42 MHz) and despite sophisticated code to correct the pseudoranges from the satellites the GPSDO frequency will be affected by changes in total electron content bewteen the satellites and the receiver. Consequently, a travelling ionospheric disturbance (TID) will affect the frequency of a GPSDO. As HamSCI is interested in Doppler shifts on WWV signals over ionospheric paths it is useful to know to what extent a GPSDO is itself affected. In the example below a TID was observed on the CHU to WW0WWV/0 path at 14.67 MHz with rms Doppler variation of 740 mHz. From the plot below we calculated the rms frequency peturbation to the GPSDO itself as about 0.090 mHz. Hence, for HamSCI prurposes, the measured Doppler shifts can be taken as 100% from the signals of interest and not the GPSDO.

  <img width="1674" height="250" alt="WW0WWV_offsets_25MHz" src="https://github.com/user-attachments/assets/09c3d1fb-47b6-40af-bbb5-70d9d4de77f3" />

  **Reference**
  WWV, WWVH and WWVB Technical details of frequency and time accuracy in [NIST Special Publication 250-67](https://www.nist.gov/sites/default/files/documents/calibrations/sp250-67.pdf) 
