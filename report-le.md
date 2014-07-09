# Bluetooth LE and Web Apps

Bluetooth LE (or Bluetooth Smart) is one of the additions brought
by Bluetooth 4.0; it provides a new physical layer and a new packet
format for bluetooth devices optimized for low power consumption
(with a rough target that they should be able to function on battery
for a year).

As a consequence of this low power goal, Bluetooth LE (BLE) comes with
more restrictions than traditional Bluetooth:

* weak security (in particular, Man in the Middle attacks are much easier)
* lesser variety of data exchanges possibilities (they need to be based
on a read/write attribute protocol)

BLE devices operate under two main roles:

* central: a device with a central role is in charge of discovering
other BLE devices with which they want to interact (e.g. to collect data
from)
* peripheral: a device with a peripheral role advertizes its existence and
capabilities to be discovered by other devices

Some devices can operate under both roles, others under one of the two.

## Pairing
Before they can communicate, BLE devices (as classical bluetooth devices) need to associate one with another; this requires that they both have bluetooth turned on, that the peripheral device is advertizing in physical proximity to the central device, and that the central device scans for peripheral devices.

Classical bluetooth provides 4 mechanisms ("Numerical Comparison", "Just Works", "Passkey Entry", "Out of Band") for pairing devices; BLE does not support "Numerical Comparison", and neither "Just Works" and "Passkey Entry" provide proper protection against Man In the Middle attacks - in other words, there is no guarantee on the identity of the endpoint one communicates with over BLE.

(the 4th mechanism, "Out of Band" relies on an external mechanism for pairing)

## BLE profiles

All BLE profiles are based on GATT, a simple protocol to read/write properties (called attributes).

### Standard profiles
#### Health Care
* Blood Pressure
* Glucose
* Health Thermometer

#### Sport and fitness
* Cycling Power
* Cycling Speed and Cadence
* Heart Rate
* Running Speed and Cadence
* Location and Navigation

#### Proximity
* Find Me
* Proximity

#### Misc
* Alert Notification
* HID over GATT
* Phone Alert Status
* Scan Parameters
* Time

### Proprietary profiles
#### iBeacon (a properietary profile from Apple)
A specific profile developed by Apple to advertize unique identifiers for a given BLE peripheral as a way to facilitate proximity detection. Easily spoofable, but without central authority.

#### Paypal Beacon
Paypal Beacon similarly advertizes themselves, but their authenticity is verified through a Paypal server.

## Bluetooth services

## Lifecycle

## Using BLE devices from the Web
### Transport-neutral usage
(can't think of any at this time?)

### Specific bluetooth integration
#### Existing APIs
* FirefoxOS [Bluetooth Manager API](https://wiki.mozilla.org/WebAPI/WebBluetooth) does not support Bluetooth LE as of v1.3.
* [Chrome Apps Bluetooth API]() seems to support BLE in central role, but not in peripheral role.

#### Security and Privacy implications
iOS / Android lessons
#### Central mode
Foreground vs Background

#### Peripheral mode
Foreground vs Background