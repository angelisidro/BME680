# Documentación BME680

![](/Img/BME680.jpeg)

Este es un sensor creado por el fabricante de dispositivos electronicos BOSCH, es capas de hacer lecturas ambientales en un pequeño empaquetado. Este pequeño sensor tiene la capacidad de leer las siguientes variables:
- Temperatura
- Humedad 
- Presión Barometrica
- VOC gases.
- CO2 Equivalente

## Protocolos de comunicación

- I2C
- SPI 

## Voltajes de alimentación

- 3V3
- 5V

## Erroes 

### BME680 error code : -2
![](/Img/error1.PNG)

Para solucionar este error debemos hacer algunos cambios en nuestro codigo, si estas utilizando la libreria ***wire.h*** este es el codigo que debes modificar para que tu sensore BME680 Funcione adecuadamente.
Busca en tu codigo la linea que contenga ```Wire.begin();``` y reemplazala por la siguiente linea de código:
```cpp
Wire.begin( SCL_#PIN , SDA_#PIN );
```
