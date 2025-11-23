<!-- buton ve batarya eklenmis devre semasi -->

## 👀 esp32-cam_webserver Overview  
<h1 align="center">A handmade webcam</h1>  


![Image](https://github.com/user-attachments/assets/4ce4f88f-1948-4605-b5d2-8e3a560e5176)
![Image](https://github.com/user-attachments/assets/f7362817-596c-4757-8a26-0679a51139fc)


## 🚀 Features  
<h1 align="center">This a portable webcam.It has also a flash.If you want, you can record stream in the OBS application, or create a virtual camera in OBS and use it with applications like Zoom or Teams.</h1>  


## 🔎 Preparation
<details>
<summary>1. Components</summary>
'1' ESP32-CAM<br>
'1' FT232RL USB to UART Converter<br>
</details>


## 📦 Setup 
1. `Refer to the circuit diagram`
2. `File>Preferences>Additional Boards Manager URLs:(Click the double window button)`
>Paste this code  
```bash
https://dl.espressif.com/dl/package_esp32_index.json
```
3. `Click 'OK'`
4. `Install the 'Arduino IDE' software and open 'Examples>ESP32>Camera>CameraWebServer' file`
5. `Open the 'board_config.h' and add '//' at the beginning to turn your default camera module line for change into a comment line then, remove the '//' in front of #define CAMERA_MODEL_AI_THINKER.`
6. `Tools>Board>Boards Manager...`  
7. `Search 'esp32' by Espressif Systems, and install it` 
> ⚠️ **Warning:** Make sure you have installed the correct USB driver (CH340, CH341, FT232R / FTDI Driver, CP2102) before connecting the ESP32CAM to your computer.
7. `Plug the ESP32CAM into your computer`
8. `Tools>Board>esp32>'AI Thinker ESP32-CAM'`
9. `Tools>Port>'Select the esp's port'`

<details>
<summary>Apply these changes:</summary>

- CPU Frequency: 240MHz (WiFi/BT)
- Core Debug Level: None
- Erase All Flash Before Sketch Upload: Disabled
- Flash Frequency: 80MHz
- Flash Mode: QIO
- Partition Scheme: Huge APP (3MB No OTA/1MB SPIFFS)
- *115200 baud*

</details>

10. `Tools>Manage Libraries...>Install the libraries used in the code`
11. `Click the 'upload ➡️' button`  
✅ **To make sure it has been uploaded successfully, you should see the message 'Done uploading'** 


## 🎉 Run  
1. `Disconnect the IO0-GND connection(disable programming mode)`
2. `Connect your esp32cam to your pc`
3. `Press the reset button on the esp32cam`
<details>
<summary>Open 'OBS' app and follow these steps:</summary>

1. Sources(Kaynaklar)>Click +>Media Source(Ortam kaynağı)>Click OK>Deselect the 'Local File'
  - Network Buffering: 16MB(max)
  - Input: esp32cam's last stream ip + (gate 81) + '/stream' --> "http://192.168.1.63:81/stream"
  - Reconnect Delay: 5S
  - !Keep the other settings as default!


</details>

5. `You are ready to use your mini webcam`  
6. `You can access the camera settings from esp32cam's ip --> "http://192.168.1.63"`


## 🔒 License  
<h1 align="center">📜 GPL-3.0 License</h1>
