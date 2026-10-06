# Curtain Opener PCB Plan

## Parts

- ESP32 C3 Supermini
- 2x 18650 cell holder
- 2x 18650 cells
- 20a 2s balanced bms
- 2s l-ion battery step up charger
- tmc2209
- temp/barometer sensor
- solar panel (5V one)

- THT Slide Switch or Toggle Switch
- 2.54mm Female Header Pins (2x8 for esp, 2x8 for stepper driver)
- Electrical tape

- N Channel MOSFET: 2N7000 (TO-92 package) - to pull second one low
- P Channel MOSFET: IRF9540N or NDP6020P - to stop charge input

- 2.54mm Screw Terminal Blocks (2-Pin) 1x for solar, 2x(2) for stepper, 2x(2) for i2c

- k7803 1000r3
- 10µF Electrolytic Capacitor (Radial THT, minimum 16V or 25V rating)
- 22µF or 47µF Electrolytic Capacitor (Radial THT, 10V or 16V rating)
- 0.1µF (100nF) Ceramic Disc Capacitor (Pitch 2.54mm)
- 100µF or 220µF Electrolytic Capacitor (Radial THT, Rated 16V or 25V) - for tmc2209 power absorbtion

#### Resistors
- 100Ω Resistor - Protects ESP32 from spikes turning on 2N7000 MOSFET
- 10kΩ Resistor - Pull up resistor that keeps P Channel mosfet off
- 1x 22kΩ and 1x 12kΩ - Battery Voltage Divider resistors.

#### Stepper motor choices
- Already have a Nicdec Nema 17 kv4239-t2b013 which I could use
- Could buy a Nema 17 pankake or a Nema 14, looking to be about £14
>e.g. [Nema 17 Pankake - Amazon £13](https://www.amazon.co.uk/STEPPERONLINE-Pancake-Stepper-Bipolar-Extruder/dp/B0B93PNYCP?th=1)


## Plan
ESP32, Stepper Driver and most components on one side. Battery holder solderd to other side. Detachable solar panel for upgradeability.

---

#### other
• 10µF Electrolytic Capacitor (Radial THT, minimum 16V or 25V rating) (C1: Input filter)
• 22µF or 47µF Electrolytic Capacitor (Radial THT, 10V or 16V rating) (C2: Output buffer)
• 0.1µF (100nF) Ceramic Disc Capacitor (Pitch 2.54mm) (C3: RF noise bypass)
• THT Slide Switch or Toggle Switch (To cut battery power completely)
• 2.54mm Female Header Pins (2 rows of 8-pins) (Optional: To socket the ESP32 instead of soldering it permanently)