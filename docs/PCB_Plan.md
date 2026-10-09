# Curtain Opener PCB Plan

## Parts

- ESP32 C3 Supermini
- 2x 18650 cell holder
- 2x 18650 cells (already have)
- 20a 2s balanced bms
- 2s l-ion battery step up charger (usb5v)
- tmc2209
- temp/barometer sensor - likely BME280

- 12mm Panel Mount Metal Momentary Push Button
- THT Slide Switch or Toggle Switch
- 2.54mm Female Header Pins (2x8 for esp, 2x8 for stepper driver)
- 2.54mm Male Pin Headers. Just get a couple sets of 40.
- Electrical tape

- 2.54mm Screw Terminal Blocks (2-Pin) 1x for spare power, 2x(2) for stepper, 2x(2) for i2c, 2x(2) for batt, 1x for button

- k7805 1000r3
- 10µF Electrolytic Capacitor (Radial THT, minimum 16V or 25V rating)
- 22µF or 47µF Electrolytic Capacitor (Radial THT, 10V or 16V rating)
- 0.1µF (100nF) Ceramic Disc Capacitor (Pitch 2.54mm)
- 100µF or 220µF Electrolytic Capacitor (Radial THT, Rated 16V or 25V) - for tmc2209 power absorbtion

#### Resistors
- 100Ω Resistor - Protects ESP32 from spikes turning on 2N7000 MOSFET
- 10kΩ Resistor - Pull up resistor that keeps P Channel mosfet off
- 1x 220kΩ and 1x 120kΩ - Battery Voltage Divider resistors. (equally can do 22k and 12k, but has more current loss)

#### Stepper motor choices
- Using a Nema 17 pancake


## Plan
ESP32, Stepper Driver and most components on one side. Battery holder solderd to other side.
Will only be opening a curtain periodically, so does not need high voltages etc.
All things avaliable as modules will be on pin headers. or attached with wires etc. Will have minimal on pcb components, and all should preferably be tht.

At some point will design and 3D print a case.

## Removed
- Solar panel circuitry as overcomplicated things
- All Mosfets for Charging toggling - too complex
- Nicdec kv4239-t2b013 in favour of Nema 17 pancake