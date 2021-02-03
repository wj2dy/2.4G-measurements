This is usage measurement data in the 2.4 GHz ISM band in Seoul, South Korea.

Signals in 2400-2480 MHz were recorded with a NI USRP-2900 Software Defined Radio Device.
Recording took place during Jan 2021, and was unfortunately in the middle of social distancing due to the coronavirus pandemic.

Consecutive 512 x 1024 samples were recorded with 40 MHz bandwidth, and then 9 x 512 x 1024 samples were dropped. This "frame" was repeated 200 times, and this 200 frame procedure was repeated twice, once with center frequency 2420 MHz, and the other 2460 MHz.

The samples were divided into 1024-sample blocks, then the FFT of each block were roughly calibrated (with a Agilent N5181A Signal Generator) to power spectral density (dBm/Hz). Phase values were dropped. Each resulting power spectral desity value was quantized to 256 steps, in range [-200, -80].

dBm/Hz = val / 255 * ((-80) - (-200)) + (-200)

Therefore, each file (in the torrent) contains 2 x 200 x 512 x 1024 unsigned 8-bit integers, and represents measurement in a single location. We recorded signals in 63 different places including indoor and outdoor, and the 63 files represent each of them.

24meas_short.zip contains short version, with only 4 (non-consecutive but equally spaced) frames for each center frequency. Hence 2 x 4 x 512 x 1024 unsigned 8-bit-integers for each file.

