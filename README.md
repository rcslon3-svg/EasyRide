# EasyRide
EasyRide - proximity Bluetooth ignition switch for motorcycle.

# EasyRide BLE Ignition Switch — Open Source

Keyless Bluetooth ignition system for motorcycles and scooters.  
Open hardware, firmware and documentation.

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

### Every day

1. Approach the scooter → system detects your phone → ignition unlocks
2. Double-press the starter button (or press killswitch on - depended of connection and setting) → beep + ignition turns on
3. Start the engine as usual (check your type - brake appied or not).
4. Stop → double-press the starter (check your type - brake appied or not) → ignition turns off
5. Walk away → after 5–7 metres the system locks automatically.

### PIN code (phone dead or unavailable)

1. Hold the starter for 3 sec until the beep → PIN entry mode active
2. Enter each digit by pressing the starter N times, wait 1 sec → confirmation beep
3. After the last digit hold the starter for 3 sec → ignition turns on
4. Wrong code → low beep, 15 sec lockout, retry
5. Mistake mid-entry → do nothing for 15 sec → auto-reset

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

## Note

If you ride off without your phone — the engine will not stall. Warning beeps at 5, 15 and 30 sec. Once stopped, enter your PIN.

---

## Repository structure

```
/
├── hardware/      # Schematics, PCB, BOM
├── firmware/      # Firmware source code
├── docs/          # Assembly and wiring guide
└── README.md
```
