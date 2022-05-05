# Audi Q3 (8U) AudiDriveSelect (ADS) activation
Enabling AudiDriveSelect in Audi Q3 (8U).

## What is ADS?
ADS is short for Audi Drive Select. It allows the driver to choose from different driving modes: comfort, normal, auto, dynamic, efficiency, individual. Depending on installed options, there are settings for engine, gearbox, suspension, exhaust, cornering lights.

## Tools required

## Procedure
### Gateway
* Parameterization required. Can be done with VCP or ODIS.
* Module `0x19`, address `0x1200`, upload data:
  * `0xB7, 0x38` - with AudiDriveSelect, no efficiency mode
  * `0x11, 0x00` - with AudiDriveSelect, with efficiency mode
  * `0x3A, 0x17` - no AudiDriveSelect

### Infotainment
#### Audi RMC2
* Parameterization required. Can be done with VCP or ODIS.
* Check this for more details: https://github.com/mrfixpl/audi-rmc-coding-adaptation-datasets

#### Audi RMC4
* Parameterization required. Can be done with VCP or ODIS.
* Check this for more details: https://github.com/mrfixpl/audi-rmc-coding-adaptation-datasets

#### Audi MMI 3G+ (HN+)
