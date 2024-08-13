# Cell shield firmware update

Old cell shield firmware may be from 2017 or 2019.

```console
minicom -D /dev/ttyUSB2 -b 115200
AT+CVERSION
```

Press Ctrl A + X to leave the minicom connection.

If you need to update cell shield firmware version for ```EG25 modules``` (not EC25) just do:

```console
cd /home/pi/Downloads;
git clone https://github.com/lowellinstruments/ddt_quectel.git;
cd ddt_quectel;
unzip QFirehose_Linux_Android_V1.4.13.zip;
unzip EG25GGBR07A08M2G_30.007.30.007.zip;
cd QFirehose_Linux_Android_V1.4.13;
make;
sudo ./QFirehose -f ..
```

Instead, for ```EC25 modules``` do:

```console
cd /home/pi/Downloads;
git clone https://github.com/lowellinstruments/ddt_quectel.git;
cd ddt_quectel;
unzip QFirehose_Linux_Android_V1.4.13.zip;
unzip EC25AFAR05A07M4G_30.003.30.003.zip;
cd QFirehose_Linux_Android_V1.4.13;
make;
sudo ./QFirehose -f ..
```
