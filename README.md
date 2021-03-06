# TR-9
**Schematics are ready! We are working on PCBs now.**  
TR-9 is a handheld transceiver (HT) for the M17 standard. Its specification can be found [here](https://github.com/sp5wwp/M17_spec).

# Hardware  
The heart of TR-9 is STM32F777VI microcontroller. The handheld also contains:  
*  a **DEM 128128A TMH-PW-N** 1.44" 128x128px TFT display  
*  an **ESP8266-12F** WiFi module  
*  an **ADF7021** chip for the RF  
*  an **LSM9DS1** 9DoF sensor  
*  a USB-micro connector for firmware update (so-called *DFU mode*)  
*  an SD-micro card slot for codeplug and storage  
*  a connector for a GNSS module  
*  a Kenwood connector for external MIC/SPK  

RF output level can be regulated by the software. The maximum power output is 3 watts. The radio can work with both analog and digital modulation.  

# Software
M17 standard was designed having [Codec2](https://github.com/drowe67/codec2) vocoder in mind. TR-9 takes advantage of STM's internal Advanced Encryption Standard (AES) hardware for optional end-to-end encryption. There is a possibility of using other block ciphers and scrambling.  
  
This repo contains SW4STM32 project for the TR-9 board.
