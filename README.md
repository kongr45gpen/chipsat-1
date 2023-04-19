# chipsat-1

Placeholder repository for the ChipSat-1 project.

Telemetry decoding information scripts, and provisionally spacecraft source code, to be uploaded here.

## Telemetry coding

| Parameter        | Value                   |
|------------------|-------------------------|
| Frequency        | TBD (UHF)               |
| Bandwidth        | 20 kHz                  |
| Modulation       | FSK                     |
| Error Correction | None                    |
| Chip Sequence    | DSSS with chip sequence |
| Frequency Deviation | TBD                  |
| Bit rate         | 200 bits/s (raw data)   |

The mission uses the [STM32WL55CC](https://www.st.com/en/microcontrollers-microprocessors/stm32wl55cc.html) transceiver.

### Chip Sequence
The chip sequence used for the ChipSat consists of 31 (2^5-1) bits, and is defined as follows:
```
0: [0 1 1 1 1 1 0 0 1 1 0 1 0 0 1 0 0 0 0 1 0 1 0 1 1 1 0 1 1 0 0]
1: [0 0 0 1 0 1 0 1 1 1 0 1 1 0 0 0 1 1 1 1 1 0 0 1 1 0 1 0 0 1 0]
```

### Packet Structure

TBC (To Be Confirmed)
```
| callsign (LX~~~~) | packet #no  |   data type   |  boot cnt |  temperature | data 1 | data 2 | data 3 | crc |
|      6 bytes      |   2 bytes   |     2 bit     |   6 bit   |    float     | float  | float  | float  | TBD |
```
where `data` can be:
- If `data type == 0`, ambient light sensor data
- If `data type == 1`, gyroscope data for each axis
- If `data type == 2`, accelerometer data for each axis

## GNURadio Decoding Tree

Under construction...
