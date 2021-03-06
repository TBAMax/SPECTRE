# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit board TjeeRdiE). This is a PCB with the hardware to run speeduino on a STM32F407VE6T daugther board from ebay. (Or a STM32 BLACK_F407VE as it is sometimes called). Schematics and more information on the cpu board can be found here: (https://github.com/mcauser/BLACK_F407VE) 

This is a design in Kicad so to open the files use Kicad. The philosophy of the V0.3 board is to use minimal hardware next to the board and casing. So fuse protected injector power, MAP power IGN power etc are all available from the connector directly. For a 4 cylinder NA engine with wasted spark and full seqential fuel injection you would only need a relay for the fuel pump and a relay for the cooling Fan if needed. The board with MCU board fits inside the ebay ECU housing with 48pin connector.

From version V0.4 and on the idea is to use more pins for other functions. like CAN bus and RS232 more ignition/injection outputs. So now a fuse/relay box is needed to connect it to the car. (or the orginal can be used)

From version V0.5 and onwards 4/8 injector outputs are designed for PWM peak and hold drivers. This is usefull for low-z injectors. The idea is to use 4 drivers for petrol injection normal saturated mode and 4 drivers for LPG vapour injection with a second fuel table. LPG vapour injectors are normally low-z (between 2.5 to 4 Ohm). The necessary changes in speeduino software are not developed yet. No worries until that time it will work as normal injector drivers. 

A stand alone Peak and Hold driver board is now in a seperate repo. See my other repository for this. 


##Photos
Check out the SPECTRE_V0.3\photos folder to see the real thing! For version V0.5 there are some 3d renders in the folder.

## Getting Started
Well there is no getting started because this board is not fully tested and debugged yet. Current status of design mistakes and fixes for V0.4 and V0.5 can be found in TODOfixes file. Version 0.3 is now fully tested on a real engine and this works as expected! So version 0.5 has been produced and is up for testing next. 

## Tested on V0.3
The following functions have been tested and confirmed to be working with real under the bonnet hardware and provide good results.<br/> 
VR1 input (Trigger 1) [OK] <br/> 
VR2 input (Trigger 2) [OK]<br/> 
Halleffect trigger input (Trigger 1) [OK]<br/>
Halleffect trigger input (Trigger 2) [OK]<br/>
Inlet Air Temperature (IAT) [OK]<br/>
Manifold Absolute pressure (MAP) [OK]<br/>
Injector outputs [OK]<br/>
Lambda sensor (O2) [OK]<br/>
Throttle position input [OK]<br/>
Bluetooth module (PD8,PD9) [OK]<br/>
Ignition outputs [OK]<br/> 
TACHO out [OK]<br/>
Fuel pump relay [OK]<br/>
FAN relay [OK]<br/>

## Tested and working with modifcations on V0.3
Coolant temperature (CLT) [OK]<br/>
PWM idle output [OK]<br/>
Battery voltage reading [OK]<br/> 

## Not tested on V0.3
Stepper idle output<br/> 
BARO <br/>
FLEX fuel <br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>

## Tested on V0.5
The following functions have been tested and confirmed to be working with real under the bonnet hardware and provide good results.<br/> 

VR1 input (Trigger 1) [OK] <br/> 
Manifold Absolute pressure (MAP) [OK]<br/>
Injector outputs [OK]<br/>
Lambda sensor (O2) [OK]<br/>
Throttle position input [OK]<br/>
Bluetooth module (PA9,PA10) [OK]<br/>
Battery voltage reading [OK]<br/> 
Ignition outputs [OK]<br/> 

## To be tested on V0.5
VR2 input (Trigger 2)<br/> 
Halleffect trigger input (Trigger 1)<br/>
Halleffect trigger input (Trigger 2)<br/>
Fuel pump relay<br/>
FAN relay<br/>
PWM idle output<br/>
TACHO out<br/>
BOOST output<br/>
Stepper idle output<br/> 
BARO <br/>
CAN bus<br/>
RS232 on connector<br/>
FLEX fuel input<br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>
Inlet Air Temperature (IAT)<br/>
Coolant temperature (CLT)<br/>

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


