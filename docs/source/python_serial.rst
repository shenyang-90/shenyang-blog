
Serial
======


https://pyserial.readthedocs.io/en/latest/tools.html


`class` **serial.tools.list_ports.ListPortInfo**

This object holds information about a serial port. It supports indexed access for backwards compatibility, as in ``port, desc, hwid = info``.

**device**

Full device name/path, e.g. ``/dev/ttyUSB0``. This is also the information returned as first element when accessed by index.

**name**

Short device name, e.g. ``ttyUSB0``.

**description**

Human readable description or ``n/a``. This is also the information returned as second element when accessed by index.

**hwid**

Technical description or ``n/a``. This is also the information returned as third element when accessed by index.

USB specific data, these are all ``None`` if it is not an USB device (or the platform does not support extended info).

**vid**

USB Vendor ID (integer, 0…65535).

**pid**

USB product ID (integer, 0…65535).

**serial_number**

USB serial number as a string.

**location**

USB device location string (“<bus>-<port>[-<port>]…”)

**manufacturer**

USB manufacturer string, as reported by device.

**product**

USB product string, as reported by device.

**interface**

Interface specific description, e.g. used in compound USB devices.

Comparison operators are implemented such that the ``ListPortInfo`` objects can be sorted by ``device``. Strings are split into groups of numbers and text so that the order is “natural” (i.e. ``com1`` < ``com2`` < ``com10``).

