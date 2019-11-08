---
layout: page
title: Radio
permalink: /radio
---

## Modulation methods:
- Analog
    - Amplitude Modulation (AM)
    - Frequency Modulation (FM)
- Digital
    - Single Carrier
        - Amplitude Shift Keying
        - Frequency Shift Keying
        - Phase Shift Keying
        - Orthogonal Amplitude Modulation
    - Multicarrier
        - Orthogonal Frequency Division Multiplexing
- Pulse
    - Pulse Width Modulation (PWM)
- Spread Spectrum
    - Frequency Hopping Spread Spectrum
    - Direct Sequence Spread Spectrum (DSSS)
    - Time Hopping Spread Spectrum
    - Chrip Spread Spectrum

## Wifi
- 802.11b (<=11 Mbps) 
    - 2.4 GHz
    - Radio link uses complementary coded keying (CCK), a type of DSSS 
    - Bit stream uses Quadrature Phase Shift Keying
- 802.11a and g (<=54 Mbps) 
    - 5 GHz
    - Radio link used 64-channel orthogonal frequency division multiplexing (OFDM)
    - Bit stream uses Binary Phase Shift Keying (BPSK), Quadrature Phase Shift Keying (QPSK), or one of two levels of Quadrature Amplitude Modulation (16, or 64-QAM)



## RTL SDR:
- Based on the RTL2832U chipset
- Freq. range for variant with Rafael Micro R820T/2 tuner = 24 – 1766 MHz (Can be improved to ~13 - 1864 MHz with experimental drivers)
- Max. sample rate = 3.2 MS/s (might be unstable)
- Max. sample rate without sample drops = 2.56 MS/s
- ADC
    - Native resolution = 8 bits
    - Effective Number of Bits (ENOB) = ~7
- Input impedance =  75 Ohms approximate, will change with freq.

## Further reading:
- Forward error correction
- https://hackaday.com/2019/06/29/an-sdr-transceiver-the-old-school-way/
- https://hackaday.com/2016/11/20/five-watt-sdr-transciever-for-hams/
- https://en.wikipedia.org/wiki/Antenna_(radio)
- https://en.wikipedia.org/wiki/Radio_spectrum
- [About RTL SDR](https://www.rtl-sdr.com/about-rtl-sdr/)
- [HackRF FAQ](https://github.com/mossmann/hackrf/wiki/FAQ)
- [5 Cool Things You Can Do With An RTL SDR Receiver](https://www.youtube.com/watch?v=9QzklSyKqQM)
- [Intro to RTL-SDR, Part I - Principles and Hardware](http://ajoo.blog/intro-to-rtl-sdr-part-i-principles-and-hardware.html)
- [Intro to RTL-SDR, Part II - Software](http://ajoo.blog/intro-to-rtl-sdr-part-ii-software.html)