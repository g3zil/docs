[← Back to Home](../index.md)
#### Local Oscillator: Precision

**Title:** Spurious zero-Doppler trace from local high precision oscillator and an unknown spurious trace

**Contributed by:** Gwyn Griffiths G3ZIL

**Reviewed by:**

**Receiving Station Location:** Fulton, MO EM38ww (near Columbia, MO)

**Receiving Station Details** WSPRDaemon Grape at AC0G

**Results**
![20MHz](https://github.com/user-attachments/assets/15404f4c-0acb-4fe2-9e85-c8a53b0e53a6))

It is not uncommon for a radio amateur's shack to have one or more precision local oscillators running continuously. This example is courtesy Michael Hauan AC0G. Michale has a precision 10 MHz oscillator as the timing signal to three OpenHPSDR radios. On 10 MHz the signal from WWV was usually strong enough to mask the leakage signal from the local 10 MHz oscillator. However, on 20 MHz with a weaker signal, hence higher 'color gain' in the spectrograms, there was a thin, essentially perfectly flat red line at zero Doppler throughout the day. Ray tracing showed no E layer propagation, which can show steady and near-zero Doppler. Although, once having seen a very thin (very narrow spectral width) trace from a local precision oscillator there can be no confusion with E region propagation.

One implication for data analysis is to be careful if using an algorithm that assumes a single spectral peak (e.g. autocorrelation) as the spurious peak at zero will bias positive or negative Doppler toward zero.

This spectrogram also includes a very narrow spectral width trace, slowly varying in frequency around  -2 Hz with little change in amplitude through the day. Perhaps a TCXO type of crystal oscillator?

