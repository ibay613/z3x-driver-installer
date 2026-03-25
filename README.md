# z3x-driver-installer


Z3X Driver Helper (AutoIt)
Overview
This script helps install Z3X Box / FTDI smart card drivers on Windows 10/11 x64 and optionally cleans problematic SCFILTER\CID_* smart card filter entries.
It is intended for fixing “smart card not found” and “this folder doesn’t contain a compatible driver” errors when installing Z3X drivers on Windows 11 21H2.

What It Does
Installs all matching .inf driver files in the script’s folder using pnputil /add-driver /install.

Optionally filters to specific driver files (e.g., ftdiport.inf, ftdibus.inf).

Enumerates SCFILTER\CID_* registry keys and deletes UpperFilters where present to repair broken smart card filter stacks.

The script does not patch or modify Z3X software itself; it only helps Windows bind the correct drivers.

Requirements
Windows 10/11 x64.

Administrator rights.

Driver signature enforcement disabled for the current boot (for unsigned Z3X drivers).
