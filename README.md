## Запись с помощью дополнительного ПО
1. скачайте файл образа
2. скачайте и установите [Etcher](https://www.balena.io/etcher)
3. Запустите **Etcher** и следуйте инструкциям на экране

## Запись SD-карты на MacOS:
1. Скачате файл **Pi400PackMan.img**
2. Подключите новую SD-карту к компьютеру Mac.
3. В терминале выполните:
```bash
 diskutil list
```
4.
```bash
diskutil info diskN | grep "Block Size"
``` (не обязательно)
(где diskN - имя устройства соответствующего вашей SD-карте)
4. Затем: ```bash
diskutil unmountDisk /dev/diskN
```
(где diskN - имя устройства соответствующего вашей SD-карте)
5. Если не знаете размер блока:
```bash
sudo dd if=/path/to/image.img of=/dev/rdiskN bs=1m
```
если знаете размер блока (к примеру 512 Bytes)
```bash
sudo dd if=/path/to/image.img of=/dev/rdiskN bs=512
```
***P.S. Требуемый размер SD-карты не менее 16ГБ.***