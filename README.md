# Radiosonde-decoder-and-tracker-for-Windows
The Radiosonde decoder and tracker is designed for the Windows 64-bit operating system. It is distributed as a single EXE file which, upon launch, sets up everything necessary for operation. It is based on the RS1729 decoder for meteorological sondes and supports the following four sonde types: RS-41, M10, M20, and DFM (with subtypes).
Originally, it was intended to run standalone with the popular RTL-SDR device based on the RTL2832 chip. In order to function correctly, you must install the ZADIG driver. If you have already used SDRs, you probably have everything set up.
Later, I added support for decoding via the PC’s audio input using tools such as Virtual Audio Cable with SDR#, SDR++, etc. In this mode, decoding quality depends on audio settings. However, when using RTL-SDR directly, no configuration is needed and IQ signals are processed for better performance.
The decoder tracks radiosondes and displays their telemetry in a dedicated window. All data is saved into a log file located in the LOG directory inside the application folder.
It also supports real-time map display in your default web browser, showing the full flight path and the last packet's data via marker popup. The map can also be loaded from a log file.
The application can optionally upload telemetry to APRS servers.


Since version 6.1, a second, optional APRS server has been introduced, under the fields Server2 and Port2.


Binary file is in Release ready for download.


Starting from version 6.2 of the Radiosonde Decoder and Tracker, it is possible to use Sonde_handler_gui.exe to automatically track a radiosonde that enters the predefined area of interest (based on the radius set in config.ini). When a radiosonde is detected within that radius, the handler automatically configures the decoder with the correct frequency and radiosonde type, and starts decoding telemetry.
The download link is:
https://github.com/9A4AM/Radiosonde-handler-from-Radiosondy.info/releases/tag/v1.0




IMPORTANT: Antivirus programs may report that the Radiosonde decoder and tracker EXE is infected with a virus or is a virus itself, however, the application is safe!
The reason is the background launching of instances (SDR, Decoder, APRS connection), which some antivirus programs mistakenly identify as malicious behavior.
