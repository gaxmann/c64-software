# USERPORT NETWORK CABLE BUILD

## Purpose

Text-only build guide for a 4-node (or 2-node) Commodore 64 userport network (“NET'97”). The network is a shared bus with four conductors:

1. GND
2. CNT2 (CIA2 serial clock)
3. SP2  (CIA2 serial data)
4. PB7  (CIA2 port B bit 7) used as BUSY / bus arbitration line (active-low)

IDs are strapped via PB0/PB1 (two bits = 4 possible IDs). The plugs are labelled ID#1..ID#4 (this matches the internal numbering used by the network software).

## Safety / Power

Power off all machines before plugging/unplugging the userport cable. Power all computers on at the same!! time.

## Userport pin mapping (C64)

Signals used on each C64 userport connector:

- GND: userport 1 or 12 or A or N
- CNT2: userport 6
- SP2 : userport 7
- PB7 : userport L

- PB0 : userport C (ID bit 0)
- PB1 : userport D (ID bit 1)

## Cable (bus) wiring

Use one 4-core cable (approx. 3 m total). It is good to use a shielded data cable. Wire it as a daisy-chain physically, but electrically it is a bus: each conductor is continuous across all 4 plugs. (When you use only two plugs we tested cable length up to 20m with no problems, but when you have open unused plugs in the middle of the cable, you better only use 3m of cable.)

- BUS WIRE 1 (GND)  -> connect to GND pin on every plug
- BUS WIRE 2 (CNT2) -> connect to pin 6 on every plug
- BUS WIRE 3 (SP2)  -> connect to pin 7 on every plug
- BUS WIRE 4 (PB7)  -> connect to pin L on every plug

Text schematic (bus):

-   [C64 ID#1]---[C64 ID#4]---[C64 ID#3]---[C64 ID#2]
-   
-    GND------------GND----------GND----------GND
-    CNT2-----------CNT2---------CNT2---------CNT2
-    SP2------------SP2----------SP2----------SP2
-    PB7------------PB7----------PB7----------PB7

## Bill of materials (BOM)

(4 nodes; values in [brackets] are for 2 nodes)

- 9× 4.7 kΩ resistors [5× 4.7 kΩ]
- 1× 3.3 kΩ resistor (LED, optional; ID#1 only)
- 1× low-current LED (~2 mA), red or green (optional; ID#1 only)

- 4× C64 userport plugs [2×]
- 4× userport plug covers / housings [2×]

- 1× 4-core cable, shielded, approx. 3 m total [optionally up to 20 m]
- Heat-shrink tubing (assorted)
- Strain relief parts (cable clamp, cable ties or equivalent, depends on housing)
- An edding pen or labels: ID#1 … ID#4 [ID#1 … ID#2]

## BUSY line (PB7)

PB7 is active-low BUSY:
- PB7 HIGH = bus free
- PB7 LOW  = bus busy / claimed

## ID strapping (PB0/PB1): physical wiring vs logical meaning

Two inputs define the node ID:
- PB0 = ID bit 0 (LSB)
- PB1 = ID bit 1 (MSB)

Physical strap wiring (what you solder):
- You strap PB0 and PB1 via resistors either to GND or to +5 V (local +5 V on that machine).
- Recommended safe resistor value (also safe if a pin is accidentally configured as output): 4.7 kΩ.

The network software reads PB0/PB1 and maps the 2-bit value to the internal node number. The plugs were labelled ID#1..ID#4 and this mapping matches the software.

- ID#1: PB1 -> GND, PB0 -> GND
- ID#2: PB1 -> GND, PB0 -> +5 V
- ID#3: PB1 -> +5 V, PB0 -> GND
- ID#4: PB1 -> +5 V, PB0 -> +5 V
-  
- Strap to GND via 4.7 kΩ
- Strap to +5 V via 4.7 kΩ (local +5 V on that machine)

## Master node (ID#1) extras

Therefore, on the ID#1 plug (only!), add:

1) PB7 pull-up (necessary)
- 4.7 kΩ from PB7 (pin L) to local +5 V

2) Activity LED (optional)
- To show “network busy” when PB7 is pulled low (LOW = busy):
- local +5 V -> 3.3 kΩ -> LED (low-current!!, red or green, 2mA) -> PB7 (pin L) 

This makes the LED light when PB7 is LOW (bus in use). - **IMPORTANT:** you HAVE to use a low-current!! 2mA LED. The resistor is calculated for a red (or green) LED.

## Assembly steps (practical)

1. Prepare 4 (or 2) userport plugs and label them ID#1, ID#2, [ID#3, ID#4.]
2. Solder the 4-core bus cable through all plugs (GND, CNT2, SP2, PB7), mind the right order of the plugs: ID#1, [ID#4, ID#3,] ID#2
3. Add ID resistors on each plug:
   - PB0 strap
   - PB1 strap
4. On the ID#1 plug, add the PB7 pull-up and (optional) LED circuit.
5. Strain relief: add heat-shrink and cable clamps so solder joints are not load-bearing.

## Electrical checks (multimeter)

Before connecting to any C64:

- Continuity:
  - GND is continuous across all plugs.
  - CNT2 is continuous across all plugs and only on pin 6.
  - SP2 is continuous across all plugs and only on pin 7.
  - PB7 is continuous across all plugs and only on pin L.

- No shorts:
  - CNT2 not shorted to GND, SP2, PB7.
  - SP2 not shorted to GND, CNT2, PB7.
  - PB7 not shorted to GND.

- ID straps:
  - Each plug shows expected resistance from PB0/PB1 to GND or +5 V (4.7 kΩ nominal).

## Bring-up suggestion

1. Connect all four C64 machines (powered off).
2. Power on (at the same time!), load the original network software (master loads from disk "EMPIRE-NET" and runs "SD2.75", clients load from disk or tape "TRANSM 2.75").
3. Verify that PB7 activity (LED on ID#1) correlates with transfers.

