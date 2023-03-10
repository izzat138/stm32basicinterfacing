# stm32basicinterfacing
This repository documents the details of the stm32basicinterfacing project on STM32F103C8T6 MCU together with the STM32CubeIDE, an open-source C/C++ development platform for STM32 microcontrollers and microprocessors.

We are required to program an STM32 MCU using open-source STM32CubeIDE in C language to print the sound intensity on the terminal. A C code is included in this repository for reference.

stm32basicinterfacing contains the project that uses pin GPIOA-PIN7 to input the sound sensor analog signal to the ADC and GPIOA-PIN9 and GPIOA-PIN10 as UART interface. Also, this project uses GPIOD-PIN0 and GPIOD-PIN1 for the RCC controller. In addtion, this project uses ADC to convert the analog signal from the sound sensor to digital signal.



## Group Members (Driven Raven)
1. Ashraf Aminin bin Arman Alim
2. Izzat bin Idris



## Project Prerequisites
1. STM32CubeIDE software
2. STM32 MCU
3. Putty



## Hardware Requirements
1. STM32F103C8T6 Board Blue Pill
2. ST-Link V2 Programming Unit
3. CH340 USB to TTL Converter UART Module 
5. KY-038 Sound Sensor



## Project Procedures
1. Start a new STM32 project on STM32CubeIDE and input part number according to the MCU being used.

![Semantic description of image](/image/pic1.jpg)


<br/>
<br/>


2. Input valid project name and click finish.

![Semantic description of image](/image/pic2.png)


<br/>
<br/>


3. Assign GPIOB-PIN12, GPIOB-PIN13, GPIOB-PIN14 and GPIOB-PIN15 as the GPIO input by clicking the pin in the pinout view. 

![Semantic description of image](/image/pic3.png)


<br/>
<br/>


4. Right-click the Connectivity > USART1 and set the mode as ‘Asynchronous’.

![Semantic description of image](/image/pic9.png)


<br/>
<br/>


5. Right-click the System Core > RCC and then click ‘Crystal/Ceramic Resonator’ in from the High Speed Clock feature. This will enable the RCC external clock source.

![Semantic description of image](/image/pic10.png)


<br/>
<br/>


6. Right-click the Clock Configuration found at the top and set HCLK to 72 MHz.

![Semantic description of image](/image/pic11.png)


<br/>
<br/>


7. Right-click the Analog > ADC1 and click the checkbox for IN7.

![Semantic description of image](/image/pic13.png)


<br/>
<br/>


8. Only a section of the generated code is modified. In this project, the executing loop is added with built-in functions to print the sound intensity on the terminal.

![Semantic description of image](/image/pic14.png)

<br/>
<br/>


9. Under project properties(Right click project, select properties), select to convert builds to binary and hex files under MCU Post build outputs. Apply the changes.

![Semantic description of image](/image/pic6.png)


<br/>
<br/>


10. Start building the debug for the current project.

![Semantic description of image](/image/pic5.png)


<br/>
<br/>


11. Connect the STM32 with all the components as shown below.

![Semantic description of image](/image/pic15.png)


<br/>
<br/>


12. STM32 ST-LINK Utility is utilized to program the SM32F103C8T6 MCU through an ST-LINK V2. The generated binary/hex files are opened through this application.

![Semantic description of image](/image/pic7.png)


<br/>
<br/>


13. Connect the STM32 MCU through the USB port with the ST-LINK V2. Then, connect with the MCU in the utility and start to program it.

Note: Move the BOOT jumper to the right to enable the microcontroller to go into programming mode.

![Semantic description of image](/image/pic8.png)


<br/>
<br/>


14. Use the CH340 USB to TTL Converter to connect the STM32 MCU through the USB port.

Note: Move the BOOT jumper to the left to enable the microcontroller to go into normal mode.


<br/>
<br/>


15. Open the device manager to check the COM port for the CH340 USB to TTL Converter. In our case, it is COM4.

![Semantic description of image](/image/pic12.png)

<br/>
<br/>


16. Open the Putty software and set the correct speed and COM port and then press Open to establish a connection. The message send from the STM32 MCU will be displayed throught the terminal.


<br/>
<br/>


# Project Demo

https://user-images.githubusercontent.com/106621749/211205508-ad10b29e-3684-4bad-b430-d556764d0871.mp4

*Youtube URL: https://www.youtube.com/watch?v=MvJmXh9NeRQ*


<br/>
<br/>


# Reflections

This STM32 project creation facilitates us in understanding the analog-to-digital converter (ADC) on STM32. An ADC converts an analog voltage to a digital value that a
microcontroller can use. In this project, we use the ADC to convert the analog signal from KY-038 Sound Sensor to 12-bit digital signal. 




# References
1. STM32CubeIDE Potentiometer ADC with STM32F103C8T6: https://youtu.be/oNiz5md51G4*

