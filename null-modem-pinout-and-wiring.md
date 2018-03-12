**Null modem cable: RS232 null modem pinout and wiring**
========================================================

**What is a null modem?**
------------------------

Using the RS232 protocol, null modems let you connect two computers that do not have modems. The RS232 protocol was developed to connect teletype machines and the modems they used for communication. Asymmetric connections employing RS232 needed a modem on one side and a data source or consumer at the other. Many wiring configurations are possible, as there is no standard null modem connection. Reception and transmission lines in null modem connections allow two-way data transmission by being connected crosswise.

Currently, the primary use of null modems is for data exchange between older laptops and computers that have no network card or USB port. An RS323 null modem is the only way to transfer data between these types of machine.

**Null modem pinout and wiring**
--------------------------------

It makes sense that null modem cables are required to make [null modem connections](https://www.eltima.com/article/what-is-null-modem-cable/). What exactly is a null modem cable? It is made up of three lines, one of which is the signal ground with the other two lines handling the data transmission. You may need an authenticating handshake depending in the software you use in this connection.

**Below are the most common schemes of null modem cables.**

![Null modem cable](https://www.eltima.com/images/upload/products/vspd/articles/null/Null_Modem.jpg)

Here is the RS232 cable wiring recommended by Microsoft that includes full authentication handshaking.

![Null modem cable - Handshake](https://www.eltima.com/images/upload/products/vspd/articles/null/Handshake.jpg)

The industry standard for RS232 employs a cable comprised of seven wires and was developed by Microsoft.

**Virtual null modem emulator**
-------------------------------

As previously mentioned, high-speed data transfer is not possible using a null modem cable. The theoretical top speed of a COM port is the limiting factor, and is capped at 115 kb/s. Cable length impacts transfer speed and the serial port’s maximum capacity is never approached.

You can effectively achieve higher data transfer speed by the use of a **[null modem emulator](https://www.eltima.com/products/virtual-null-modem/)**, which is an application that uses a virtual null modem cable to connect COM ports.

You are able to [create pairs of virtual COM ports](https://www.eltima.com/create-virtual-serial-port.html) using virtual null modem software. Two way communication is facilitated between the COM ports by the software and data transmitted to one COM port is available instantly at the paired port.

![Virtual Null Modem Emulator](https://www.eltima.com/imgnew/products/vspd/splash/splash-vspd.jpg)

Transmitting data trough a virtual cable by employing virtual null modem software is preferable to using a physical cable. Virtual Com Port Driver is a null modem emulator that supports the standard hardware line signals such as DRT/DSR, RTS/CTS, RING, ERROR, etc. This application supports strict baud rate emulation and full HandFlow control. You can also simulate a line break in you serial connection using this virtual null modem emulator.








