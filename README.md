# Automotive Door Control System
In this project I have designed automotive door control system (Static and Dynamic Design) schematic diagrams, Layer Architecture, APIs , State machines, Sequence Diagrams and CPU load calculations.

## System Design
![](https://github.com/mohamed-elsayed13/Automotive-Door-Control-Design-egFWD/blob/master/1.system%20schematic.png)

## MCAL Layer
1- GPIO Layer
This module will be responsible for interfacing between 1/0 devices and MCIJ.
This module will consist of the following APIs:
```
/ *Initialize GPIO direction* /
void portnumber, uint8_t direction);
/ *write data to GPIO*/
void GPIO_write(uint8_t portnumber,uint8_t pinnumber,uint8_t value);
/ *toggle GPIO*/
void GPIO_togg1e(uint8_t portnumber, uint8_t pinnumber);
/*Read GPIO*/
void GPIO_read(uint8_t portnumber,uint8_t pinnumber,uint8_t* value);
```

2-Timer Module
This module will be responsible for Timing delays and functions in the system.
This module will consist of the following APIs:
```
/ *Initialize Timer*/
void
/ * Turn on Timer* /
void TIMER_on(void);
/ *Turn off Timer * /
void TIMER_off(void);
```

3-ADC Module
This module will be responsible for reading values analog values from sensors.
This module will consist of the following APIs:
```
/ *Initialize ADC*/
void ADC_init(void);
/*Read ADC*/
Uint16_t ADC_read(uint8_t Channelnumber);
```
4-CAN Module
This module will be responsible for communications with other ECUs.
This module will consist of the following APIs:
```
/ *Initialize CAN* /
void CAN_init(void);
/ *Initialize CAN* /
void CAN_send(uint8_t Data);
```
