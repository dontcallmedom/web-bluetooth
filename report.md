# Bluetooth and Web Apps

Bluetooth provides short-range connectivity between devices once they have been paired one with another.

## Pairing
Before they can communicate, Bluetooth devices need to associate one with another; this requires that they both have bluetooth turned on, and that one of the devices be made visible, while the other scans for devices.

See also the [report specifically on Bluetooth LE](report-le.md).

## Bluetooth profiles
### Standard profiles
#### Telephony
* Common ISDN Access (CIP)
* Cordless Telephony (CTP)
* Fax (FAX)
* Phone Book Access (PBAP, PBA)
* SIM Access (SAP, SIM, rSAP)

#### Networking
* Dial-up Networking (DUN)
* LAN Access (LAP)
* Personal Area Networking (PAN)

#### Audio/Video
* Advanced Audio Distribution (A2DP)
* Audio/Video Remote Control (AVRCP)
* Generic Audio/Video Distribution (GAVDP)
* Hands-Free (HFP)
* Headset (HSP)
* Video Distribution (VDP)

#### File exchange
* File Transfer (FTP)
* OBject EXchange (OBEX)

#### Misc
* Attribute (ATT)
* Device ID (DIP)
* Generic Access (GAP)
* Generic Attribute (GATT)
* Generic Object Exchange (GOEP)

#### To be classified
* Basic Imaging (BIP)
* Basic Printing (BPP)
* Hard Copy Cable Replacement (HCRP)
* Health Device (HDP)
* Human Interface Device (HID)
* Intercom (ICP)
* Message Access (MAP)
* Object Push (OPP)
* Proximity (PXP)
* Serial Port (SPP)
* Service Discovery Application (SDAP)
* Synchronization (SYNCH)
* Synchronisation Mark-up Language (SyncML)
* Wireless Application Protocol Bearer (WAPB)

## Bluetooth services

## Using bluetooth devices from the Web
### Transport-neutral APIs
Bluetooth-paired devices are often exposed by the operating system as integral part of the host device, and thus are made available seamlessly on the Web. This includes:

* bluetooth headset via the `navigator.mediaDevices` API
* bluetooth mouse, keyboard, gamepad via the relevant APIs

### Specific bluetooth integration
#### Existing APIs
* FirefoxOS has a [Bluetooth Manager API](https://wiki.mozilla.org/WebAPI/WebBluetooth), but that API (as of v1.3) is restricted to certified applications (thus not open to third-party applications.)
* [Chrome Apps Bluetooth API](http://developer.chrome.com/apps/bluetooth)
* [Tizen Bluetooth interface](https://developer.tizen.org/dev-guide/2.2.0/org.tizen.web.device.apireference/tizen/bluetooth.html)

#### Security and Privacy implications
* iOS / Android lessons
* privileges include:
** determining if bluetooth is enabled
** turning bluetooth on/off
** turning visibility on/off
** turning scan on/off
** discovering visible devices in proximity
** accepting pairing requests
** using specific bluetooth profiles
** transmiting generic data over bluetooth
* privacy risks include:
** fingerprinting via nearby devices
** implicit geolocation via well-known nearby devices
