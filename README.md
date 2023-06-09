## Запись с помощью дополнительного ПО
1. скачайте файл образа [Pi400Packman.img.gz](https://drive.google.com/file/d/19Gx4Tzhd8SjY7VjmD3AxCg6GtPju0G8I/view?usp=sharing)
3. скачайте и установите [Etcher](https://www.balena.io/etcher)
4. Запустите **Etcher** и следуйте инструкциям на экране

## Запись SD-карты на MacOS:
1. Скачате файл [Pi400PackMan.img](https://drive.google.com/file/d/19Gx4Tzhd8SjY7VjmD3AxCg6GtPju0G8I/view?usp=sharing)
2. Подключите новую SD-карту к компьютеру Mac.
3. В терминале выполните:
```bash
 diskutil list
```
4. (не обязательно)
```
diskutil info diskN | grep "Block Size"
```
(где diskN - имя устройства соответствующего вашей SD-карте)
4. Вставьте SD-карту, затем:
```
diskutil unmountDisk /dev/diskN
```
(где diskN - имя устройства соответствующего вашей SD-карте)
5. Если не знаете размер блока:
```
gunzip -c /path/to/Pi400Packman.img.gz | sudo dd of=/dev/rdiskN bs=1m

```
если знаете размер блока (к примеру 512 Bytes)
```
sudo dd if=/path/to/Pi400Packman.img.gz of=/dev/rdiskN bs=512
```
***P.S. Требуемый размер SD-карты не менее 16ГБ.***

## Настройка среды
Неочевидные управляющие клавиши:
**Enter** - Вход/выход в/из меню настройки эмулятора
**D** - Настройка среды (она-же подтверждение выбора и вход в подпункты)
**S** - Аналог **Back** - Возврат в предыдущее меню

### P. S. Все кнопки могут быть переопределены

#### P. P. S. Запись на карту может потребовать времени.
Время затреченное на упаковку:
```
16106127360 bytes transferred in 1207.486882 secs (13338553 bytes/sec)
```
