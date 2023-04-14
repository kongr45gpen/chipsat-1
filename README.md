# chipsat-1

Placeholder repository for the ChipSat-1 project.

Telemetry decoding information, and provisionally source code, to be uploaded here.

## Telemetry coding

| Parameter        | Value                   |
|------------------|-------------------------|
| Frequency        | TBD (UHF)               |
| Bandwidth        | 20 kHz                  |
| Modulation       | FSK                     |
| Error Correction | None                    |
| Chip Sequence    | DSSS with chip sequence |
| Bit rate         | 200 bits/s (raw data)   |

The mission uses the [STM32WL55CC](https://www.st.com/en/microcontrollers-microprocessors/stm32wl55cc.html) transceiver.

### Chip Sequence
The chip sequence used for the ChipSat consists of 63 (2^6-1) bits, and is defined as follows:
```
0: [1 0 0 0 0 0 1 1 1 1 1 1 0 1 0 1 0 1 1 0 0 1 1 0 1 1 1 0 1 1 0 1 0 0 1 0 0 1 1 1 0 0 0 1 0 1 1 1 1 0 0 1 0 1 0 0 0 1 1 0 0 0 0]
1: [1 0 0 0 1 0 1 1 1 1 0 0 1 0 1 0 0 0 1 1 0 0 0 0 1 0 0 0 0 0 1 1 1 1 1 1 0 1 0 1 0 1 1 0 0 1 1 0 1 1 1 0 1 1 0 1 0 0 1 0 0 1 1]
```

### Packet Structure

TBD
