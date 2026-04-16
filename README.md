# STM32-WeatherMachine
STM32 NucleoF446RE Project that uses I2C to read data from a BME280 sensor, prints all of the information through UART, and displays the information one sensor at a time on a basic 16x2 LCD using the onboard button to cycle through the three sensor readings.

## This project uses two FreeRTOS tasks and one FreeRTOS queue:
* BME280Task : Initializes BME280 and rapidly sends sensor data to the queue (High Priority)
* LCDTask : Initializes the LCD and continuously reads data from the queue to display it on the LCD and print to console using UART. (Low Priority)
* DataQueue : Size 5 Queue of datatype SensorData_t

**This project does NOT use an I2C LCD, it only uses I2C for the BME280 sensor.**

# This Project Requires/Uses The Following Libraries:
* [Sayid Hosseini's Liquid Crystal Library for STM32](https://github.com/SayidHosseini/STM32LiquidCrystal)
* [Afebia's BME280 Library for STM32](https://github.com/Afebia/BME280-STM32-V2)
