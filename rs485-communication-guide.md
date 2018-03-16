**RS485 communication guide**
=============================

**What is RS485?**
------------------
Many electronic devices and pieces of equipment use serial ports to communicate with computers. A widely used, legacy serial interface is the RS-485 protocol. Used extensively in industrial automation, the protocol is used in many industrial networks. Examples are Modbus, Profibus, DP, ARCNET, BitBus, WorldFip, LON, Interbus, and other non-standard networks. A serial RS-485 port is currently seen as the most efficient implementation of serial communication. Let’s see why the RS-485 protocol is so popular and look at a simple way to test and monitor the interface.

**What is RS-485?**
-------------------

The legacy name RS-485 is now known as EIA/TIA-485. It is a standard interface of the 1st level of the Open System Interconnection (OSI) model. It is a signal transmission method that deals with the physical layer of communication and was developed to expand RS-232’s capabilities.

A cable of two or three wires is used in a serial EIA-485 connection. The cable will always have a data wire, and an inverted data wire. Additionally the cable often has a zero or ground wire. Twisted-pair cables comprised of 22 0r 24 AWG solid wires are used to exchange data between transmitters and receivers. The goal is to use two wires to transport one signal, with the original signal on one wire and its inverse on the other, making the transmission highly resistant to interference. Both shielded and unshielded twisted-pair cables can be used as the transmission line.

**[RS-485 communication: main features](https://www.eltima.com/article/rs485-communication-guide/)**
---------------------------------------

RS-485 technology is still the basis of many communication networks despite the availability of numerous alternatives. This is due to its major advantages, which are:

* Using one twisted-pair of wires to enact two-way data exchange;
* The ability to build networks by connecting several transceivers to the same line;
* Communication lines can be long;
* High transmission speed.

**Let’s examine the main characteristics of RS-485 communication:**

1. Bi-directional half-duplex data transmission. A serial stream of data can be transmitted in one direction with a transceiver required for data transfer on the receiving end. The transceiver, or driver, is an electrical circuit or device on the transmitter side that forms a physical signal.

2. Symmetrical communication channel. A pair of equivalent single wires are needed to receive or transmit data. This allows data exchange to alternately travel in both directions. The twisted-pair cable forms a symmetrical channel that suppresses the signal’s electromagnetic radiation, thereby increasing its stability.

3. Multi-pointing. The ability to work with multiple receivers and transceivers connected is part of the RS-485 protocol. One transmitter and several receivers can be attached at together to one communication line at a time. If other transmitters need to be connected they need to wait until the communication line is free for data transmission.

**How to test RS-485 ports with RS485 Protocol Analyzer**
---------------------------------------------------------

The EIA/TIA-485 standard is used extensively with industrial applications. Many of these applications require high data transmission speeds to be maintained over long distances. The RS-485 interface has proved robust in noisy, industrial environments such as factories, utilities, and process control plants.

Many devices have an RS-485 port embedded in them. Some of these devices include programmable logic controllers (PLCs), point-of-sale terminals, low-speed modems, industrial monitoring instruments, and scientific lab equipment to name a few.

It is evident that technicians working with RS-485 networks may need to test the serial interfaces when attempting to identify and resolve network problems. Additionally, developers working on industrial serial applications will need to test and monitor serial ports as they develop their apps.

There is a solution that makes it easy to monitor and analyze RS-485 port activity. Thus medicated RS-485 test software is call **[RS485 Protocol Analyzer](https://www.eltima.com/rs485-analyzer.html)**. It’s main function is to monitor, log, and display serial data traveling through your system’s RS-485 ports. It comes with many advanced features that allow you to track and record all data transmitted through the monitored serial ports without any additional hardware.

**Core functionality of RS485 Analyzer:**

 * Ability to connect to any COM port immediately even in the port is in use. All data transmitted through a monitored RS-485 interface is shown in real time, to facilitate fast diagnosis of problems in your serial communication network.

 * Monitoring multiple COM ports at a time in one monitoring session. You can now consolidate your output and all data will be saved to the same log for later review.

 * Simulating serial communication. The software’s Terminal mode option enables you to emulate the sending of data in different formats, including (string, binary, octal, decimal, hexadecimal, mixed). Session comparison is made simple with the software’s RS-485 loopback feature.
 
 ![RS485 Analyzer](https://www.eltima.com/imgnew/products/spm/splash/screen.png)

























