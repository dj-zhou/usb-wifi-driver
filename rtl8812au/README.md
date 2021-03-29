## USB WiFi Adapter for RTL8812AU

### Which USB WiFI Adapter

Run the command `lsusb`, and if see something like

```bash
Bus 003 Device 008: ID 0bda:8812 Realtek Semiconductor Corp. RTL8812AU 802.11a/b/g/n/ac 2T2R DB WLAN Adapter
```

then it is a RTL8812AU USB WiFi Adapter, then you can use this drive.

### Tested on

* Ubuntu 20.04.2 LTS, x86_64

### Code Original
https://github.com/aircrack-ng/rtl8812au.git, branch `v5.6.4.2`.

### Install
#### dkms
`dkms` is neded to install this driver. Download it from [here](http://archive.ubuntu.com/ubuntu/pool/main/d/dkms/dkms_2.8.1-5ubuntu1_all.deb), and install it byy

```bash
sudo dpkg -i dkms_2.8.1-5ubuntu1_all.deb
```

#### Compile and Install

```bash
cd rtl8812au
make
sudo make install
```