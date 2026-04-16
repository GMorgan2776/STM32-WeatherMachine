# STM32-WeatherMachine
STM32 NucleoF446RE Project that uses I2C to read data from a BME280 sensor, prints all of the information through UART, and displays the information one sensor at a time on a basic 16x2 LCD using the onboard button to cycle through the three sensor readings.

**This project does NOT use an I2C LCD, it only uses I2C for the BME280 sensor.**

# This Project Requires/Uses The Following Libraries:
* [Sayid Hosseini's Liquid Crystal Library for STM32](https://github.com/SayidHosseini/STM32LiquidCrystal)
* [Afebia's BME280 Library for STM32](https://github.com/Afebia/BME280-STM32-V2)
