# EasyRide
EasyRide - proximity Bluetooth BLE ignition switch for motorcycle, based on Arduino board Supermini or Nice!Nano nRF52840.

# EasyRide BLE Ignition Switch — Open Source

Keyless Bluetooth ignition system for motorcycles and scooters.  
A Bluetooth-based start authorization unit wired into the motorbike ignition circuit. Your phone in the pocket replaces the physical key for daily riding. Turn ignition on by stock button (starter or killswitch).

Open hardware, firmware and documentation.

Compatible with motorbikes that have electric starter and NO factory keyless/keyfob or chip-key immobilizer.

Phone: Android and iOS with Bluetooth Low Energy support.

Not compatible with motorbikes that have factory keyless/keyfob or a chip-key immobilizer.

---

## What it does

- Unlocks the ignition when your phone with Bluetooth BLE enabled is nearby — no app required
- PIN code fallback via the starter button — if the phone is unavailable
- Standby current under 2 mA 
- Auto-locks after you walk 5–7 metres away

---

## How to use

Behavior will be changed by TYPE of your motorcycle and connection method.
1. Motorcycle witn killswitch. Ignition ON/OFF by killswitch.
2. Motorcycle only with starter button. Ignition ON/OFF by starter button. OFF - with brake pressed. Start - when brake released.
3. Scooter (variator transmission). Ignition ON/OFF by starter button. OFF - when brake released. Start - when brake pressed.

4. If you ride off without your phone — the engine will not stall. Warning beeps at 5, 15 and 30 sec. Once ignition OFF - enter your PIN.

### Every day

1. Approach the scooter → system detects your phone → ignition unlocks
2. Double-press the starter button (or press killswitch on - depended of connection and setting) → beep + ignition turns on
3. Start the engine as usual (check your type - brake appied or not).
4. Stop → double-press the starter (check your type - brake appied or not) → ignition turns off
5. Walk away → after 5–7 metres the system locks automatically.

### Specification

Supply voltage (nominal)	12 V

Supply voltage (operating)	5-24 V

Supply voltage (absolute max.)	30 V

Current on IGN output	7 A continuous, 10 A max

Current through ST1, ST2 contacts	0.5 A max

Standby current consumption	1.2 mA

Operating temperature	-20 to +80 degrees C

Dimensions	45 × 45 × 20 mm

Weight	25 g

### PIN code (phone dead or unavailable)

1. Hold the button (starter or killswitch - see above) for 3 sec until the beep → PIN entry mode active
2. Enter each digit by pressing the button N times, wait 1 sec → confirmation beep, next digit
3. After the last digit hold the button for 3 sec → ignition turns on
4. Wrong code → low beep, 15 sec lockout, retry
5. Mistake mid-entry → do nothing for 15 sec → low beep, auto-reset, try again

---

## Configuration

BLE device name, pairing code (6 digits) and PIN code (3 digits) are set by the user in the code before compiling and flashing.

---

## Pairing a new phone

1. Move the old phone out of range or turn it off
2. Enable Bluetooth on the new phone
3. Find the device name in the scan list and tap to pair
4. Enter the 6-digit pairing code

Only one phone can be paired at a time.

---

## How to get it.

You can assemble and program it yourself or buy it here https://www.smartmoto.asia 

---

## Repository structure

```
/
├── hardware/      # Schematics, PCB, BOM
├── firmware/      # Firmware source code
├── bootloader/    # BLE bootloader
├── docs/          # Picture, wiring guide, how to connect to motorcycle
└── README.md
```
