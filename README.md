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
https://github.com/9A4AM/Radiosonde-handler-from-Radiosondy.info/releases/tag/v2.0


Source code is partially published — the basic principle of this decoder can be seen at the following link:
https://github.com/9A4AM/Radiosonde-decoder



IMPORTANT: Antivirus programs may report that the Radiosonde decoder and tracker EXE is infected with a virus or is a virus itself, however, the application is safe!
The reason is the background launching of instances (SDR, Decoder, APRS connection), which some antivirus programs mistakenly identify as malicious behavior.




⚠️ External Tools Licensing Notice
This project utilizes external command-line tools that are licensed under the GNU General Public License (GPL), including but not limited to:

SoX – Licensed under GPLv2

rtl_fm (from the rtl-sdr package) – Licensed under GPLv2

rs (radiosonde decoders) – Licensed under GPLv3

These tools are used as standalone programs executed via system calls or subprocesses. No GPL-licensed code is included directly in this project's source code, nor are any GPL libraries linked or modified.

As such, this project is not a derivative work of those GPL programs and is not subject to GPL licensing terms. However, users are responsible for complying with the licenses of the external tools they install and use.


****************************************************************************************************************************************************************************************************************************
Included External Tools (GPL Notice)
This application uses several external open-source command-line tools, which are bundled in the executable distribution and invoked only via subprocess (i.e., as separate processes). These tools are licensed under the GNU General Public License (GPL), and are not integrated directly into the application's codebase.

The included tools are:

Radiosonde decoders (rs1729)
rs41mod.exe, m10mod.exe, dfm09mod.exe, mXXmod.exe

License: GNU GPL v3

Source: https://github.com/rs1729/RS

RTL-SDR Tool
rtl_fm.exe

License: GNU GPL v2

Source: https://github.com/rtlsdrblog/rtl-sdr-blog

Audio Processor
sox.exe (SoX - Sound eXchange)

License: GNU GPL v2

Source: https://sourceforge.net/projects/sox/

These tools are invoked as external processes and are not linked or imported into the main application code. Their inclusion is solely for convenience and proper operation of the system.
Each tool remains under its original license, and full source code or links to the official repositories are provided above in accordance with their respective GPL licenses.

Licensing Clarification
The main application does not include or derive from GPL-licensed code. Therefore, the GPL requirements apply only to the tools listed above, not to the rest of this application.

****************************************************************************************************************************************************************************************************************************

This application uses map data from OpenStreetMap, licensed under the Open Database License.

