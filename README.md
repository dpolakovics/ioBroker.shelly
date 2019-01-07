![Logo](admin/shelly.png)
# ioBroker.shelly
=================

[![Build Status](https://travis-ci.org/schmupu/ioBroker.shelly.svg?branch=master)](https://travis-ci.org/schmupu/ioBroker.shelly)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/schmupu/ioBroker.shelly?branch=master&svg=true)](https://ci.appveyor.com/project/schmupu/ioBroker-shelly/)

[![NPM version](http://img.shields.io/npm/v/iobroker.shelly.svg)](https://www.npmjs.com/package/iobroker.shelly)
[![Downloads](https://img.shields.io/npm/dm/iobroker.shelly.svg)](https://www.npmjs.com/package/iobroker.shelly)

[![NPM](https://nodei.co/npm/iobroker.shelly.png?downloads=true)](https://nodei.co/npm/iobroker.shelly/)

Requires node.js 6.0 or higher and Admin v3!

The adapter communicates with Shelly devices by REST api and the CoAP protocol with the default Shelly firmware (no flashing of firmware needed!).
Because CoAP use multicast UDP packages, the Shelly devices has to be in the same subnet like ioBroker.
If you use ioBroker in a docker container, the container has to run in host or macvlan modus.  

You will find more and detailed information about the device here : [Shelly](https://shelly.cloud/)

## Installation

1. Install the adapter
2. No configuration needed. Shelly devices will be detected and added automatically. Sometimes you have to restart the shelly device or control it once using the app before it appear initially in ioBroker.

## Supported devices
* Shelly1 (SHSW-1, Verified)
* Shelly2 (SHSW-21/SHSW-22, Verified)
* Shelly4Pro (SHSW-44, not verified and tested)
* ShellyPlug (SHPLG-1, not verified and tested) 
* ShellyBulb (SHBLB-1, not verified and tested)
* Shelly2LED (SH2LED-1, not verified and tested)
* ShellyRGBW (SHRGBWW-01, not verified and tested)
* Shelly H&T (SHHT-1, verified)

## More details needed to implement (Debug log)
* Shelly Sense (SHSEN-1)

## Changelog

### 2.0.5 (07.01.2018)
* Fixing an error if Shelly device is not reachable (offline)

### 2.0.4 (04.01.2018)
* Support of js-controller compact mode and performance optimizing. Relay status changes will be shown much faster in ioBroker for Shelly 1, 2 and 4Pro

### 2.0.3 (02.01.2018)
* Shows RSSI Status for Shelly 1 & 2. You need Firmware 1.4.4 

### 2.0.2 (22.12.2018)
* Add Shelly H&T. 

### 2.0.1 (22.12.2018)
* Major update because of problems with CoAP messages. 

### 1.0.2 (17.12.2018)
* Work around for showing states in shutter/roller modus

### 1.0.1 (07.12.2018)
* Add shutter/roller position

### 1.0.0 (10.11.2018)
* Optimizations and Online status fixed

### 0.2.6 (31.10.2018)
* Two new datapoints (AutoTimerOn and AutoTimerOn) for Shelly 1/2

### 0.2.5 (13.10.2018)
* Hostname instead of ip address will be shown

### 0.2.4 (10.10.2018)
* Channel name can be overwrite with own name

### 0.2.3 (01.10.2018)
* Bugfixing, shutter status display

### 0.2.2 (30.09.2018)
* Bugfixing, on start default value of timer and duration of relay and shutter will be 0 sec

### 0.2.1 (28.09.2018)
* Username/Password supported

### 0.2.0 (28.09.2018)
* Roller / Shutter for Shelly2 supported

### 0.1.1 (21.09.2018)
* Bugfixing

### 0.1.0 (20.09.2018)
* First Version. Supports all Shelly switches like Shelly 1, Shelly 2, Shelly 4 and the power sockets.


## License
The MIT License (MIT)

Copyright (c) 2018 Thorsten Stueben <thorsten@stueben.de>, Apollon77 <iobroker@fischer-ka.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
