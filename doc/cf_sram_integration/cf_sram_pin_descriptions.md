

| Unique Spec ID | Pin Name (all pins) | Type | Direction | Relative Power | Relative Ground | Level | Always On? | Description |
|---|---|---|---|---|---|---|---|---|
| Pin 47 | AD[9:0] | digital | In | vpwrtp | vgnd | LV | No | Address, sampled on rising edge of CLKin |
| Pin 48 | EN | digital | In | vpwrtp | vgnd | LV | No | Ram Enable, sampled on rising edge of CLKin. Low=macro disabled (internal macro clock held LOW for Normal operation). High=macro enabled. (Internal macro clock switches for Normal operation) |
| Pin 49 | CLKin | digital | In | vpwrtp | vgnd | LV | No | Clock Input |
| Pin 50 | D[31:0] | digital | In | vpwrtp | vgnd | LV | No | Data In, sampled on rising edge of CLKin, ignored during read cycle |
| Pin 51 | DQ[31:0] | digital | Out | vpwrtp | vgnd | LV | No | Data out |
| Pin 52 | BEN[31:0] | digital | In | vpwrtp | vgnd | LV | No | Data bit enables, sampled on rising edge of CLKin. Allow/block writing to a memory bit Low=bit disabled, High=bit enabled |
| Pin 53 | WL/OFF | digital | In | vpwrtp | vgnd | LV | No | Wordline off for test if vpwrtp not driven - e.g. vpwrmcT when power switch is used to power vpwrtp) For WLBH-0, WLOFF=0: Normal operation. For WLBH-0, WLOFF=1: all wordlines clamped to vgnd, and READand WRITE disabled. For WLBH=1, WLOFF=0: WLBI testmode. For WLBI=1, WLOFF=1: illegal state |
| Pin 54 | WLBI | digital | In | vpwrtp | vgnd | LV | No | DISABLED (Wafer Level Burn In test mode. WLBI=1 All wordlines are ON. WLBI=0: Normal operation) |
| Pin 55 | R_WB | digital | In | vpwrtp | vgnd | LV | No | Read High, Write Low |
| Pin 56 | vpwrpc | digital | In | vpwrtp | vgnd | LV | Yes | Periphery Power switch control Low: power switch from vpwrtp to vpwrtp is ON (conducting) High: power switch from vpwrtp to vpwrtp is OFF (non-conducting) |
| Pin 57 | vpwrac | digital | In | vpwrm | vgnd | LV | Yes | Array Power switch control Low: power switch from vpwrm to vpwra is ON (conducting) High: power switch from vpwrm to vpwra is OFF (non-conducting) |
| Pin 58 | vpwrm | power | In | vpwr | vgnd | LV | Yes | Nominal 1.8V power supply. Gated to vpwrp and vpwra by vpwrtpc and vpwrac |
| Pin 59 | vpwrp | power | Inout | vpwr | vgnd | LV | Yes | Nominal 1.8V power supply for periphery. Connection to vpwrm controlled by vpwrtpc |
| Pin 60 | vpwra | power | Inout | vpwr | vgnd | LV | Yes | Nominal 1.8V power supply for array. connection to vpwrm controlled by vpwrac |
| Pin 61 | vnb | bulk | In | vpwr | vgnd | LV | Yes | Bulk supply for Nfets |
| Pin 62 | vpb | bulk | In | vpwr | vgnd | LV | Yes | Bulk supply for Pfets |
| Pin 63 | vgnd | ground | In | vgnd | vgnd | LV | Yes | Nominal 0V power supply return |
| Pin 64 | TM | digital | In | vpwrtp | vgnd | LV | No | Scan Test mode Enable. For TME1: Memory in scan test mode. For TME0: Normal operation |
| Pin 65 | SM | digital | In | vpwrtp | vgnd | LV | No | Scan Shift Enable (SSE) For TME1, SME1: Scan shift mode, shift on rising CLKin. For TME1, SME0: parallel load scan registers on rising edge of CLKin. For TME0, SME1: illegal state. For TME0, SME0: Normal operation |
| Pin 66 | ScanInCC | digital | In | vpwrtp | vgnd | LV | No | Input to the control or address scan chain |
| Pin 67 | ScanInDL | digital | In | vpwrtp | vgnd | LV | No | Input to the data scan chain on the left side of the macro (LSBs of the data bus) |
| Pin 68 | ScanInDR | digital | In | vpwrtp | vgnd | LV | No | Input to the data scan chain on the right side of the macro (MSBs of the data bus) |
| Pin 69 | ScanOutCC | digital | Out | vpwrtp | vgnd | LV | No | Output of address & control scan chain (Note: Polarity is inverse of ScanInCC) |
