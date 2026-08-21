# [Padavan ng CAKE Linux 3.4 

## 🚀 Supported Devices (Kernel 3.4)

We support a massive array of **MT7620/MT7621** devices. Pick the one you love!
*(This list corresponds directly to the `target_select` menu in the build workflow.)*

| Brand | Supported Models |
| :--- | :--- |
| **TP-Link** | **Archer C2 (V1)**, C20 (V1/V4/V5), C5 (V4), C50 (V1/V3/V4), EC220-G5 (V2), MR200 (V1), MR3020 (V3), MR3420 (V5), WDR7300 (V5), WR840N (V4/V5/V6/RU), WR841N (V13/V14), WR842N (V5), WR845N (V3/V4) |
| **Xiaomi** | MI-3, MI-3C, MI-4 (A/C/SPI), MI-4A (100M), MI-MINI, MI-NANO, MI-R3G (v1/v2/SPI), MI-R3P (Pro), R2100 (AC2100), RM-AC2100 |
| **ASUS** | RT-AC1200 (GU/HP), RT-AC51U, RT-AC54U, RT-N10+, RT-N11P (B1), RT-N12+, RT-N13U (B1), RT-N14U, **RT-N56U (A1/B1/GE2)**, RP-AC56 |
| **ZyXEL** | Keenetic Series: **Giga III**, **Ultra II**, Extra (I/II), Lite (I/II/III/3B), Omni (I/II), Start II, Viva, 4G III (B) |
| **D-Link** | DIR-300 (B1/B7), DIR-320 (B1), DIR-620 (A1/D1), DIR-860L, **DIR-882** |
| **Newifi** | Newifi D1, Newifi D2, Newifi Mini, Newifi Y1S |
| **GL.iNet** | GL-MT300A, GL-MT300N (V1/V2) |
| **Phicomm** | K2P (PSG1218), 256PSG1218 |
| **ZBT** | WE1326, WE1626, WE826-T2, WG3526 (-32), WR8305RT |
| **Others** | **Ubiquiti** ER-X, **Linksys** EA-8100, **Belkin** F9K1103, **Totolink** A3004NS, **HiWiFi** HC5661A, **Youku** L1/L1C, **ZTE** E8820S |
| **OEM/Misc** | 5K-W20, A5-V11, ALR-U270, MQ-WITI, Nexx WT3020 (A/H), Samsung SWR1100, Sercomm (S1010/SmartBox), SNR (MD1/ME1/W4N), Tuoshi TS7620N, Unielec U7621, Wall-AP, Youhua WR1200JS |

---

## 🌐 Multi-Language Support

We believe in a borderless internet. The firmware now supports **14 Languages** out of the box!
*(Select your preferred language in the `language_select` menu.)*

* **English_Only** (Default)
* **CN (繁體中文)** - Traditional Chinese
* **RU (Pусский)** - Russian
* **ES (Español)** - Spanish
* **BR (Brazil)** - Portuguese
* **CZ (Česky)** - Czech
* **DA (Dansk)** - Danish
* **DE (Deutsch)** - German
* **FI (Finsk)** - Finnish
* **FR (Français)** - French
* **NO (Norsk)** - Norwegian
* **PL (Polski)** - Polish
* **SV (Svensk)** - Swedish
* **UK (Українська)** - Ukrainian

---

## ✨ Features (3.4 Edition)

* **Kernel**: Highly optimized **Linux 3.4.x** (Padavan-NG foundation).
* **Performance & Queue Management**:
    * **CAKE / FQ_CoDel** (The Dave Täht Special) - **Backported to 3.4** to mitigate bufferbloat on older devices!
    * Hardware NAT (PPE) support for gigabit speeds.
* **Wireless**: Optimized drivers for MT7603/MT7612/MT7620/MT7628.
* **Network**:
    * IPv6 support.
    * WireGuard support.
    * Hardware flow offloading.
* **Control**: LED & GPIO control via sysfs.

---

## 🛠️ Compilation Guide

We support both **GitHub Actions** (for ease of use) and **Manual Compilation**.

### Option A: GitHub Actions (Recommended)

Just go to the `Actions` tab in this repository, select `Build firmware (Ultimate Fix)`, and choose:

1.  **Target Model**: (e.g., `TL_C2-V1`, `MI-MINI`, `RT-N56U`...)
2.  **Language**: (e.g., `English_Only` or `CN (繁體中文)`)
3.  **Toolchain**: (Default or Padavan-NG)

The system will automatically apply the **CAKE Patch**, configure your language, and build your firmware.

### Option B: Manual Compilation

*Please see the original part of readme below!*

---

# Original README & Manual Compilation Instructions

# README #

#### Please see the original part of readme below!

---

# README #

Welcome to the padavan-ng project

This project aims to improve the supported devices on the software part, allowing power user to take full control over their hardware.
This project was created in hope to be useful, but comes without warranty or support. Installing it will probably void your warranty.
Contributors of this project are not responsible for what happens next. Flash at your own risk!

### Contribution ###

Feel free to send in improvements/fixes. I'll keep the issue/pull request system open for that purpose.
NOTE: if and when a possible interesting change will get added depends on a verification/test of the particular change and if i have time to do it.

### Compilation Instructions ###

* Install dependencies

```shell
# I recommend building only on OS: Ubuntu Desktop 22.04.4 LTS (Jammy Jellyfish) and Before building the firmware, select "App Updates" and install them. Next, update the packages
sudo apt update
sudo apt upgrade
sudo apt install autoconf autoconf-archive automake autopoint bison build-essential ca-certificates cmake cpio curl dos2unix doxygen fakeroot flex gawk gettext git gperf help2man htop kmod libarchive-tools libblkid-dev libc-ares-dev libcurl4-openssl-dev libdevmapper-dev libev-dev libevent-dev libexif-dev libflac-dev libgmp3-dev libid3tag0-dev libidn2-dev libjpeg-dev libkeyutils-dev libltdl-dev libmpc-dev libmpfr-dev libncurses5-dev libogg-dev libsqlite3-dev libssl-dev libsystemd-dev libtool libtool-bin libudev-dev libunbound-dev libvorbis-dev libxml2-dev locales mc nano pkg-config ppp-dev python3 python3-docutils sshpass texinfo unzip uuid uuid-dev vim wget xxd zlib1g-dev

```
[Automatic Padavan firmware builds using GitHub servers](https://github.com/shvchk/padavan-builder-workflow)

[Автоматическая сборка прошивки Padavan на серверах GitHub](https://github.com/shvchk/padavan-builder-workflow/blob/main/README.ru.md)

### Firmware management ###
```shell 
Login details
IP: 192.168.1.1 or http://my.router
User: admin
Password: admin
WiFi name 2.4GHz: Padavan_2.4GHz
WiFi name 5GHz: Padavan_5GHz
WiFi Password 2.4/5GHz: 1234567890
```
# Для желающих поддержать проект #

Чтобы выразить благодарность и поддержать мою работу:

ЮMoney кошелёк 4100118647832050

Ссылка для быстрого пополнения https://yoomoney.ru/to/4100118647832050

ЮMoney виртуальная карта 5599 0020 6991 1404

Виртуальная карта Приват Банка гривна: 5169 3600 0910 4443

Виртуальная карта Приват Банка USD: 5169 3600 0910 4385

Большое спасибо вам за вашу поддержку!

Желаю всем добра, а так же Здоровья! Вы даёте мне возможоность жить и дышать! © by Sergey Hadzhioglu

# For those who want to support the project #

To express gratitude and support my work:

ЮMoney wallet 4100118647832050

Link for quick replenishment https://yoomoney.ru/to/4100118647832050

ЮMoney Virtual Card 5599 0020 6991 1404

Virtual Card Privat Bank UAH: 5169 3600 0910 4443

Virtual Card Privat Bank USD: 5169 3600 0910 4385

Thank you very much for your support!

I wish you all the best, and also Health! You give me the opportunity to live and breathe! © by Sergey Hadzhioglu

<a href="https://imgbb.com/"><img src="https://i.ibb.co/4KRbrfM/maxresdefault.jpg" alt="maxresdefault" border="0"></a>

# DISCLAIMER #
IMPORTANT NOTE!! PLEASE READ IT CAREFULLY!!
# NO WARRANTY OR SUPPORT
This product includes copyrighted third-party software licensed under the terms of the GNU General Public License. Please see The GNU General Public License for the exact terms
and conditions of this license. The firmware or any other product designed or produced by this project may contain in whole or in part pre-release, untested, or not fully tested works.
This may contain errors that could cause failures or loss of data, and may be incomplete or contain inaccuracies. You expressly acknowledge and agree that use of software or any part,
produced by this project, is at Your sole and entire risk.

ANY PRODUCT IS PROVIDED 'AS IS' AND WITHOUT WARRANTY, UPGRADES OR SUPPORT OF ANY KIND. ALL CONTRIBUTORS EXPRESSLY DISCLAIM ALL WARRANTIES AND/OR CONDITIONS, EXPRESS OR IMPLIED,
INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES AND/OR CONDITIONS OF SATISFACTORY QUALITY, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY, OF QUIET ENJOYMENT, AND NONINFRINGEMENT
OF THIRD PARTY RIGHTS.
