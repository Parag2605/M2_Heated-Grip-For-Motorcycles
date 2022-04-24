# Introduction
Now-days everyone is looking for automation and advancements in all the sectors. The Heated Grip For Motorcycles System is capable of maintaining of heat in the vehicles Handlebars. In European countries, the temperature is very low and any electronic designer should make sure that his equipment should work efficiently in that whether. 

When rider of the motorcycle rides the motorcycle, the button sensor gets trigger after that heater empowered. The temperature sensor keeps monitoring the temperature and sends analog value of temperature to the microcontroller. The microcontroller alters analog to digital values using ADC and show the numerical value of temperature.

Based on the controller it will set the temperature and it is capable of upholding of heat in the vehicles seats. And whatever the warmness is generated that fact it will be showing on displays.

![image](https://user-images.githubusercontent.com/101051467/164626150-ac18a773-f9f4-4a5a-8fa4-0884ab2e5206.png)


# Features
- The System will sense is rider is riding or not.
- Rider has the access to modify the temperature in the vehicle grips.
- As per Riders request, Heater will generate the heat accordingly.
- Low cost and robust system.

# SWOT Analysis
![image](https://user-images.githubusercontent.com/101051467/164614917-95dcb8ff-70b3-4f4a-901f-9d8075d87535.png)

## Strenghts
- User Friendly
- Easy to alter the temperature on the handlebar.
- Low cost and Robust system.

## Weakness
- Its only applicable for those countries which are having low temperature and on hilly areas.

## Opportunities
- It can be implemented on any of the motorcycles.

## Threats
- Not suitable for average or high temperature places.

# 4'W and 1'H
- WHY - Well-being for user.

- WHAT - Heated Grip For Motorcycles System.

- WHEN - Winter seasons and according to user.

- WHERE - Used in Motorcycles.

- HOW - Operates by Temperature Sensor and Microcontroller.

# Requirements

## High Level Requirements
| High Level Requirements  | Description |
| ------------- | ------------- |
| HLR1  | Microcontroller |
| HLR2  | Temperature Sensor |
| HLR3  | Heat Generation |
| HLR4  | Display |
| HLR5  | Software used |

## Low Level Requirements
| Low Level Requirements	  | Description |
| ------------- | ------------- |
| HLR1_LLR1 | ATmega328  |
| HLR2_LLR1 | ADC  |
| HLR2_LLR2 | ADC with PWM-fast  |
| HLR3_LLR1 | Thermoelectric module  |
| HLR4_LLR1 | CRO and LED  |
| HLR5_LLR1 | Code Blocks with AVR GCC compiler  |
| HLR5_LLR2 | SimulIDE  |

## Block Diagram
![Block Diagram](https://user-images.githubusercontent.com/101051467/164991899-4a3922db-cbfe-4a07-86bf-a34d4342bf5a.png)

## Flow Chart
![Flow Chart (1)](https://user-images.githubusercontent.com/101051467/164991913-3298a7a0-7cd8-4a37-8a03-4eedd684e036.png)

# Test Plan
# High Level Test Plan
| Test ID  | Description | Exp I/P | Exp O/P | Actual O/P | Type of Test |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
| H_01  | System Testing  | Blink the LED when the rider is riding and the heater is pressed  | Pass  | Pass  | Requirement Based  |
| H_02  | System Testing  | Convert the analog signal from the temperature sensor to the digital value | Pass  | Pass  | Boundary Based  |
| H_03  | System Testing  | Generate the PWM signal according to the converted digital value  | Pass  | Pass  | Scenario Based  |
| H_04  | System Testing  | Send the temperature value to the serial monitor using UART protocol  | Pass  | Pass  | Boundary Based  |

# Low Level Test Plan
| Test ID  | Description | I/P | O/P | Status |
| ------------- | ------------- | ------------- | ------------- | -------------
| H_01  | If person riding  | Push button=1  | Push button=1  | Pass  |
| H_02  | If person not riding  | Push button=0  | Push button=0  | Pass  |
| H_03  | Temperature Request  | Temp=0  | Heater=Off  | Pass  |
| H_04  | Temperature Request  | Temp=20  | Heater=20 degree generation | Pass  |
| H_05  | Temperature Request  | Temp=25  | Heater=25 degree generation  | Pass  |
| H_06  | Temperature Request  | Temp=29  | Heater=29 degree generation  | Pass  |
| H_07  | Temperature Request  | Temp=33  | Heater=33 degree generation  | Pass  |
| H_08  | LED ON | Button=1 && Heater=1 | LED=1  | Pass  |
| H_08  | LED OFF | Button=0 && Heater=0  | LED=0  | Pass  |
| H_08  | Display | Temperature :- 20 deg Cel  | Temperature :- 20 deg Cel  | Pass  |

