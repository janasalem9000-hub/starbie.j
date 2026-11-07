# Starbie

Starbie is a small star-shaped PCB pet that I designed in KiCad. It uses a XIAO ESP32-C3 microcontroller, a small OLED screen to show the pet, two buttons to interact with it, an MPU6050 motion sensor so it reacts when you tilt or shake it, and a DHT11 sensor to read temperature and humidity.

## Why I made it
I wanted to understand how real circuit boards are designed and made, from the schematic all the way to factory files. I also just thought it would be fun to build my own little desk pet.

## How it works
- The ESP32-C3 is the brain and runs the Arduino firmware.
- Button 1 opens a menu, and tilting the board picks an option.
- Button 2 shows the pet's stats.
- The OLED and MPU6050 share the same I2C lines (SDA and SCL).
- A ground fill on both sides of the board connects all the ground pins.

## Bill of Materials
## Bill of Materials
| Part | Qty | Unit price (USD) | Link |
|---|---|---|---|
| Seeed XIAO ESP32-C3 | 1 | 4.99 | [Seeed Studio](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) |
| 0.96" SSD1306 OLED, 4-pin I2C | 1 | 6.89 | [ShillehTek](https://reach.dog/shop/shillehtek/products/0-96-i2c-white-oled-display-module-4-pin-ssd1306) |
| MPU6050 (GY-521) module | 1 | 7.37 | [Keszoox](https://keszoox.com/products/mpu-6050-gy-521-3-axis-accel-gryo-sensor-module) |
| DHT11 sensor | 1 | 2.49 | [Addicore](https://reach.dog/shop/addicore/products/dht11-temperature-and-humidity-sensor) |
| 10k resistor | 1 | ~0.10 | Any electronics store |
| 6x6 mm push button | 2 | ~0.20 | Any electronics store |
| Starbie PCB | 1 | ~2.00 (5 boards) | [JLCPCB](https://jlcpcb.com) |
## Pictures
![PCB layout](board.png)
![3D view](3d.png)

## Files
- `Starbie.kicad_sch`: schematic
- `Starbie.kicad_pcb`: PCB layout
- `bom.csv`: parts list
- `starbie.jver.zip`: Gerber and drill files for manufacturing
