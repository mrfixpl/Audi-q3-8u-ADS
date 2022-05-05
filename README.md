# Audi Q3 (8U) AudiDriveSelect (ADS) activation
Enabling AudiDriveSelect in Audi Q3 (8U).

![Audi RMC with AudiDriveSelect screen option](https://github.com/mrfixpl/Audi-q3-8u-ADS/blob/main/images/RMC-AudiDriveSelect.jpg?raw=true)

## What is ADS?
ADS is short for Audi Drive Select. It allows the driver to choose from different driving modes: comfort, normal, auto, dynamic, efficiency, individual. Depending on installed options, there are settings for engine, gearbox, suspension, exhaust, cornering lights.

## Tools required

## Procedure
### Gateway
* Parameterization required. Can be done with VCP or ODIS.
* Module `0x19`, address `0x1200`, upload data:
  * `B7 38 A8 6A` - with AudiDriveSelect (comfort, auto, dynamic)
  * `11 00 97 60` - with AudiDriveSelect (comfort, auto, dynamic, efficiency)
  * `3A 17 73 E5` - no AudiDriveSelect

### Infotainment
#### Audi RMC2
* Parameterization required. Can be done with VCP or ODIS.
* Check this for more details: https://github.com/mrfixpl/audi-rmc-coding-adaptation-datasets

#### Audi RMC4
* Parameterization required. Can be done with VCP or ODIS.
* Check this for more details: https://github.com/mrfixpl/audi-rmc-coding-adaptation-datasets

#### Audi MMI 3G+ (HN+)

## Research
* Last 4 bytes in gateway dataset is CRC-32 checksum,
* Last 2 bytes in RMC dataset is CRC-16/CCITT-FALSE checksum,
* Modes in order: Individual, Comfort, Auto, Dynamic, Offroad, Efficiency, Race.
* Individual settings in order: engine/transmission, suspension, steering, 4x4, exhaust, belt tensioner, ACC. Additionally: contour seats, cornering lights.

## Credits, reference, links
* Huge thanks to everyone involved in this research!
* Checksum calculator: https://crccalc.com/
* OBDeleven diagnostic interface (ref link): http://obdeleven.com/?src=link&ref=Zy245Iacqc6bMTHh
