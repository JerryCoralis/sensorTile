# Internet of Things - progress log
## Jargon
STM32

|                      |                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------|
| **BLE**              | blue tooth low energy                                                                   |
| **STM32**            | family of 32-bit microcontroller integerated circuits based around 32-bit ARM processor |
| **STEVAL-STLKT01V1** | mini square sensor board                                                                |
| **STLCR01V1**        | cradle board (current attached tile)                                                    |
| **STLCX01V1**        | expansion board (current attached tile)                                                 |

## Raspberry pi
issues with formatting usb in linux
issues using NOOBS to install raspbian, tarball was corrupt even though sha256sum showed valid file integrity

resolved by flashing raspbian stretch image file


formating usb: http://qdosmsq.dunbar-it.co.uk/blog/2013/06/noobs-for-raspberry-pi/
https://www.garron.me/en/go2linux/format-usb-drive-fat32-file-system-ubuntu-linux.html

flashing stretch:
https://www.youtube.com/watch?v=ana7uz0l728

## challenges
1. [ssh the raspberry pi. How to use laptop to interface with it](https://www.raspberrypi.org/documentation/remote-access/ssh/)
1. how to get sensor tile to talk with RaspPi using bluetooth
2. how to access that data from sensor tile
3. how to get that data to cloud

## connecting R\pi to sensor tile via bluetooth
---
**problem: pairing pi and St**
- pairing via Raspbian GUI and Terminal initially connects then disconnects
  terminal command: `$ bluetoothctl`
  
  abandoning GUI as per online resources

> terminal
- ensured the bluetooth daemon is running and working `$ sudo systemctl start bluetooth`
- GUI sometimes prompts error: Paring failed - GDBus.Error.bluez.Eroror.AuthenticationFailed:Authentication Failed
- terminal: trust: BD address prompts for passkey, not default 0000

ST address: C0:7A:31:30:18:4D
[this seems like what we need](https://github.com/STMicroelectronics-CentralLabs/BlueSTSDK_Android)
Bluetooth low energy connectivity based on BlueNRG-MS

> too triggered by bluetooth shienangians, going straight from ST to cloud
[follow this tutorial: IBM Watson x ST](https://www.hackster.io/taifur/sensortile-data-monitoring-with-ifttt-notification-e43365)
- using IBM cloud to as IoT viusalization medium 
- [ibm data viusalization](https://console.bluemix.net/docs/services/IoT/data_visualization.html#boards_and_cards)
- [initalize testing of IoT data transmition via IBM IoT quickstart](https://developer.ibm.com/recipes/tutorials/connect-st-sensor-tile-to-ibm-watson-iot-platform/)
Great success! It works.
- [IBM IoT board guide](https://console.bluemix.net/services/iotf-service/38d36e95-8aba-48b7-a638-941136f1242a/?paneId=manage&new=true&env_id=ibm:yp:us-south&org=3d3e67b7-554f-431b-ad02-d32a92b1f0dd&space=2dd9c759-376e-4ff2-9490-3b5b4be54687)
very helpful
- using IBM IoT because of amazing company & community documentation



## R\pi to server IoT
[promising for IoT using Azure](https://docs.microsoft.com/en-us/azure/iot-suite/iot-suite-v1-raspberry-pi-kit-c-get-started-basic)
[industrial IoT](http://wizzilab.com/)
[what the final product might look like](https://www.youtube.com/watch?v=KyS2gNLurKU)







