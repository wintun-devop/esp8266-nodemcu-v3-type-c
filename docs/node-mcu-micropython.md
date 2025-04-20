### Virtual Env Setup
```
python -m venv iot-env
```
```
iot-env/Script/activate
```
### Installin Necessary Tools
```
pip install esptool
```
### Check the Chip ID 
```
esptool --port COM3 chip_id
```

### Erase Flash and Upload Micropython
```
esptool --chip esp8266 --port COM3 erase_flash
```
###
```
esptool --port COM3 erase_flash
```
```
esptool --port COM3 --baud 460800 write_flash --flash_size=detect 0x00000 ESP8266_GENERIC-20240602-v1.23.0.bin
```
```
esptool --port COM3 --baud 115200 write_flash --flash_size=detect 0x00000 ESP8266_GENERIC-20250415-v1.25.0.bin

```

```
esptool --port COM3 --baud 115200 write_flash --flash_size=detect 0x00000 ESP8266_GENERIC-FLASH_512K-20250415-v1.25.0.bin

```
###
```
esptool --port COM3 --baud 460800 write_flash --flash_size=detect -fm dout 0 ESP8266_GENERIC-20250415-v1.25.0.bin
```
###
```
esptool.py --port <serial-port-of-ESP8266> write_flash -fm <flash-mode> 0x00000 <nodemcu-firmware>.bin
```
```
esptool --port com3 write_flash -fm qio 0 ESP8266_GENERIC-20250415-v1.25.0.bin
```
```
esptool --chip esp8266 --port COM3 --baud 460800 write_flash -fm qio 0 ESP8266_GENERIC-20250415-v1.25.0.bin
```
```
esptool --port com3 --baud 115200 write_flash --flash_size=detect -fm qio 0 ESP8266_GENERIC-20250415-v1.25.0.bin
```
```
esptool --port COM3 --baud 115200 write_flash --flash_size=detect -fm dio 0 ESP8266_GENERIC-20250415-v1.25.0.bin
```
```
esptool -p COM3 write_flash --flash_size=detect -fm dio 0  ESP8266_GENERIC-20240602-v1.23.0.bin
```