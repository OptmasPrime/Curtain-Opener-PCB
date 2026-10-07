# Curtain Opener PCB Plan

## Parts

- ESP32 C3 Supermini
- 2x 18650 cell holder
- 2x 18650 cells (already have)
- 20a 2s balanced bms
- 2s l-ion battery step up charger (usb5v)
- tmc2209
- temp/barometer sensor
- solar panel (5V one)

- THT Slide Switch or Toggle Switch
- 2.54mm Female Header Pins (2x8 for esp, 2x8 for stepper driver)
- 2.54mm Male Pin Headers. Just get a couple sets of 40.
- Electrical tape

- N Channel MOSFET: 2N7000 (TO-92 package) - to pull second mosfet low
- P Channel MOSFET: NDP6020P - to stop charge input (changed by n channel)

- 2.54mm Screw Terminal Blocks (2-Pin) 1x for solar, 2x(2) for stepper, 2x(2) for i2c, 2x(2) for batt

- k7803 1000r3
- 10µF Electrolytic Capacitor (Radial THT, minimum 16V or 25V rating)
- 22µF or 47µF Electrolytic Capacitor (Radial THT, 10V or 16V rating)
- 0.1µF (100nF) Ceramic Disc Capacitor (Pitch 2.54mm)
- 100µF or 220µF Electrolytic Capacitor (Radial THT, Rated 16V or 25V) - for tmc2209 power absorbtion

- Some sort of diode for reverse voltage protection

#### Resistors
- 100Ω Resistor - Protects ESP32 from spikes turning on 2N7000 MOSFET
- 10kΩ Resistor - Pull up resistor that keeps P Channel mosfet off
- 1x 220kΩ and 1x 120kΩ - Battery Voltage Divider resistors. (equally can do 22k and 12k, but has more current loss)
- 10kΩ or 100k tht potentiometer (could use to set current on stepper driver)

#### Stepper motor choices
- Already have a Nicdec Nema 17 kv4239-t2b013 which I could use
- Could buy a Nema 17 pankake or a Nema 14, looking to be about £14
>e.g. [Nema 17 Pankake - Amazon £13](https://www.amazon.co.uk/STEPPERONLINE-Pancake-Stepper-Bipolar-Extruder/dp/B0B93PNYCP?th=1)


## Plan
ESP32, Stepper Driver and most components on one side. Battery holder solderd to other side. Detachable solar panel for upgradeability.
Will only be opening a curtain periodically, so does not need high voltages etc.
All things avaliable as modules will be on pin headers. or attached with wires etc. Will have minimal on pcb components, and all should preferably be tht.

At some point will design and 3D print a case.