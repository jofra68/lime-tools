Introdcution:

Welcome to the LimeMon software.  LimeMon produces automated power sweep measurements vs time and frequency in .csv, .xls and .gif formats.  Software has compatible command line to Soapy Power.

Usage:

For best results use an external antenna.  Fit antenna to RX input, and run the following script.
./testScript.sh

This script contains various example commands, and the results are stored in separate directories.  The parameters for the LimeScan command are as follows.

-f Center frequency (Hz) e.g. 800M
-C Channel number 0:1
-A Antenna name LNAH,LNAL,LNAW
-w IF filter bandwidth, e.g. 35M (Hz), should be twice as large as -r
-r Sample rate, e.g. 16M (S/s)
-OSR Oversample rate for ADC e.g. 8
-b FFT bins
-g SDR gain
-n Number of repeats for RMS FFT
-o -O Output folder name. e.g. -o TESTmini.
-h help
-v version
-T Measurement time (s)
-gps "/dev/ttyACM0" (supports UBLOX-7 NMEA GPRMC messages)
-tst LVL Generate test signal at 860MHz LVL dBm -50:-6 e.g. -test -50
-pwla Apply pwl correction file to antenna response
-pwlh Apply pwl correction file to LNAH response
-pwlw Apply pwl correction file to LNAW response
-pwll Apply pwl correction file to LNAL response

Compatible with LimeSDR and LimeSDRmini.
Note: LimeSDRmini contains an RF switch that selects LNAH or LNAW
Note: LimeSDRmini only has channel 0 (-C 0)
Note: Aluminium LimeSDR requires cables to change to select LNAH,LNAL,LNAW

Note: GPS Ublox-7 USB sticks, sudo adduser $USER dialout # then reboot
Note: GPS Ublox-7 USB sticks work best outside.  Accuracy will be degraded using indoors, and may become unusable.

Note: Testfrequency is 860MHz+SampleRate/8
Note: PWL can be used to correct for LNA gain vs frequency, and Antenna gain vs frequency
Idea is this would allow use as a calibrated measurement instrument.
#Note: PWL files are approximate.  More accurate calibration will give better results.
Note: If matching network is altered, default PWL filles will be invalid.


