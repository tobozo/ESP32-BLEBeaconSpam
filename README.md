# ESP32-BLEBeaconSpam

This tool was used when testing [ESP32-BLECollector](https://github.com/tobozo/ESP32-BLECollector/)

It is based on the [iBeacon](https://github.com/nkolban/ESP32_BLE_Arduino/blob/master/examples/BLE_iBeacon/BLE_iBeacon.ino) example from the [ESP32_BLE_Arduino](https://github.com/nkolban/ESP32_BLE_Arduino) library with the following changes :

- Uses `ESP.restart()` instead of `esp_deep_sleep()`
- Brownout detector is disabled
- Random mac address is generated based on a reduced version of the [oui list](https://code.wireshark.org/review/gitweb?p=wireshark.git;a=blob_plain;f=manuf)
- Random company identifier is injected in manufacturer data based on an exhaustive list of [companies](https://www.bluetooth.com/specifications/assigned-numbers/company-identifiers)
- Random service UUID is generated (this part still needs improvements)



Credits/source: 
---------------
- https://github.com/1337ninja/UUIDGenerator
- https://code.wireshark.org/review/gitweb?p=wireshark.git;a=blob_plain;f=manuf
- https://www.bluetooth.com/specifications/assigned-numbers/company-identifiers
