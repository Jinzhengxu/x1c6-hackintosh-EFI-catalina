# x1c6-hackintosh-EFI-catalina
This is Clover and BOOT folder work in my ThinkPad X1Carbon 6th MacOS 10.15 Catalina.



### Hardware

|   CPU    |      SSD       |   Memory   | Graphic Card |         Display          |
| :------: | :------------: | :--------: | :----------: | :----------------------: |
| i7-8650U | 256G PCIe-NVME | 16G LPDDR3 |   UHD 620    | 14'' HDR WQHD(2560x1440) |



+ New device need to add 

|        Bluetooth         |  Wireless Card   |
| :----------------------: | :--------------: |
| CSR 4.0 Bluetooth Dongle | COMFAST CF-811AC |



### Usage

Open your EFI partition and replace the CLOVER and BOOT floder.

ThinkPad wireless card and bluetooth can't work in MacOS. You can chose BCM943602z or DW1820A(with block stitch). But I recommend use Bluetooth dongle and USB wireless card, they won't disturb your when work in Linux or Win.

+ Bluetooth

  Please chose a Bluetooth dongle which doesn't need driver. 

  1. Block your System bluetooth

     You should use [MACiASL](https://github.com/acidanthera/MaciASL/releases) to edit `EFI/CLOVER/ACPI/orgin/SSDT-UIAC.asl`,remove all entries which contain `HS07`.(If your use my CLOVER floder you don't need do this step, just put dongle in your PC). For more information about edit SSDT, please refer to [this Guide](https://github.com/tylernguyen/x1c6-hackintosh/blob/master/4_README-ACPIpatching.md).

  2. Put the USB dongle in 

+ Wireless 

  I chose the COMFAST CF-811ac, you should download dirver [there](https://github.com/chris1111/Wireless-USB-Adapter-Clover/releases), I use V9 and it work well, you can chose the lastest version to downloads. 