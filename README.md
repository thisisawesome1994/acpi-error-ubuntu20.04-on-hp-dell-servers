# acpi-error-ubuntu20.04-on-hp-dell-servers
How to fix issue with HP servers giving acpi (ipmi) error when using ubuntu 20.04

Getting this error?
```
Nov  2 17:30:25 host kernel: ACPI: No handler for Region [POWR] (ffff8820538672b8) [IPMI]
Nov  2 17:30:28 host kernel: ACPI: No handler for Region [POWR] (ffff8820538672b8) [IPMI]
Nov  2 17:30:31 host kernel: ACPI: No handler for Region [POWR] (ffff8820538672b8) [IPMI]
Nov  2 17:30:34 host kernel: ACPI: No handler for Region [POWR] (ffff8820538672b8) [IPMI]
```

Fix it by these commands:
```
modprobe ipmi_si
modprobe acpi_ipmi
modprobe acpi_power_meter
```
