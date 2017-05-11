+++
date = "2017-05-11T10:00:12+08:00"
draft = false
title = "修改 Grub2 開機順序"

+++

### Windows 10 First

<!--more-->

這是我的開機選單
```
*Ubuntu
 Advanced options for Ubuntu
 Windows 10 (loader) (on /dev/sda1)
```
- 如果你跟我一樣，裝了雙系統，但是大部分工作還是在 Windows 上完成  
- 覺得每次開機都要選很煩，想修改成從 Windows 開機

#### Steps
1. 打開 `Terminal`
2. 備份 `grub` 檔: 

    ```
    sudo cp /etc/default/grup /etc/default/grup.bak
    ```
3. 修改 Grub 設定

    ```
    sudo vim /etc/default/grup
    ```
4. 找到 `GRUB_DEFAULT=0`，索引是從 0 開始，以我的開機選單為例，0 就是 Ubuntu
5. 修改 `GRUB_DEFAULT` 的值 & 存檔。以我的開機選單為例，改成 `GRUB_DEFAULT=2`，就會從 Windows 10 開機
6. 最後不要忘記更新 Grub
    ```
    sudo update-grup
    ```
7. 重開機看是否有修改成功!

[Set the GRUB Default OS: Dual-boot Windows 7 and Ubuntu 14.04]: https://askubuntu.com/questions/485726/set-the-grub-default-os-dual-boot-windows-7-and-ubuntu-14-04