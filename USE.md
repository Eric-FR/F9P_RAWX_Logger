# Use cases
Recommandations for pratical uses of the logger
## Messages sent
Messages emitted by F9P/F9R depending on the configuration (may not reflect the current state of the code)

| Configuration | UART1(log) | UART2(BT) |
| --- | --- | --- |
| F9P (base) | _NMEA_<br>GNGGA<br>_UBX_<br>RXM-RAWX<br>RXM-SFRBX<br>(NAV-SVIN if Survey-In used)| _RTCM_ |
| F9P (rover) | _NMEA_<br>GNGGA<br>GNGSA<br>GNGST<br>GNGSV<br>GNRMC<br>_UBX_<br>RXM-RAWX<br>RXM-SFRBX<br>NAV_POSLLH<br>NAV-PVT<br>NAV-SAT<br>TIM-TIM2 (timestamp of waypoints) | _NMEA_<br>GNGGA<br>GNGGL<br>GNGSA<br>GNGST<br>GNGSV<br>GNRMC |
| F9R (no HPS) | _NMEA_<br>same as previous<br>_UBX_<br>same as previous<br>+<br>ESF-RAW | _NMEA_<br>same as previous |
| F9R (with HPS) | _NMEA_<br>same as previous<br>+<br>GNTHS<br>_UBX_<br>same as previous<br>+<br>ESF-STATUS<br>ESF-ALG<br>NAV-ATT | _NMEA_<br>same as previous<br>+<br>GNTHS |
| F9R (with HPS & automotive) | _NMEA_<br>same as previous<br>_UBX_<br>same as previous<br>+<br>NAV-RELPOSNED | _NMEA_<br>same as previous |
