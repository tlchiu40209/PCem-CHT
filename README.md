# PCem vNEXT 繁體中文版

---

要下載預先編譯好 (For Windows x64) 的版本，請直接 [Release](https://github.com/tlchiu40209/PCem-CHT/releases) 下載。

解壓縮後即可使用。另外因各電腦廠商之 ROM 有其著作權，請不要詢問為什麼沒有 ROM。  
另外，使用該軟體需要具備對於各種舊 PC 的基本常識，此並非 VirtualBox 或是 VMware。

---

vNEXT 變更事項:
- ISA Sound Blaster 系列音效卡現在是不能調整 IRQ的，全部預設為: 位置 0x220, IRQ 7, DMA 1, High DMA 5。使用 DOS 作業系統時，請記得在 AUTOEXEC.bat 輸入 SET BLASTER = A220 I7 D1 Tx (T1 = SB 1.0，T3=SB 2.0, T4 = SB Pro, T6= SB16) 

---

PCem 是由 Sarah Walker 獨立維護的 x86 模擬器軟體  
目標為提供一個儘可能還原從 1981 到 Pentium II 時期的 x86 平台，從主機板，處理器到音效卡模擬等一應俱全。

目前 Sarah Walker 已將下一個版本的 PCem 開發交由 Michael Manley 帶領。

關於 PCem 更多的說明請見:
- [PCem](https://pcem-emulator.co.uk/)
- [PCem Github](https://github.com/sarah-walker-pcem/pcem)

本專案以中文化 PCem 介面為目的，無實質新增其他功能。  
由於為了讓程式能正常顯示中文，有一小部份的程式碼已經與原本的 PCem 不同。

請不要試圖 Merge ，否則會發生無法編譯等問題

---

中文化 PCem 參照版本: [PCem vNEXT (Apr. 17, 2022)](https://github.com/sarah-walker-pcem/pcem/commit/f4a1ab9c5193ebeaa5ab7da3b613dc78a5614550)  
編譯平台: Windows 10 x64

---

相較於 [Mar. 29, 2022](https://github.com/sarah-walker-pcem/pcem/commit/85e1ef3ee4b5b1598957bfa95312f42a1eaef6e6) 新增的功能:  
- 新增對這些機器的支援: Hyundai SUPER-16T, Hyundai SUPER-16TE, Commodore PC10C
- 新增對這些CD光碟機的模擬: Sony CDU311, Toshiba XM-5702B, GoldStar CRD-8160B, Creative CR-587-B/CR-588-B, BTC BCD36XH, Philips PCA403CD, Mitsumi CRMC-FX4820T

---

如果您要自行編譯這個專案，而不下載預先編譯版本:

Windows 作業系統 (MinGW)
1. 安裝 MSYS2，並啟動相對應環境 (如 MSYS2 MinGW x64)，第一次啟動時，請先進行更新 :
```sh
pacman -Syuu
```
2. 安裝基礎編譯環境 : 
```sh
pacman -Syu base-devel gcc
```
3. 安裝相關涵式庫 SDL2 / wxWidgets 3.x / OpenAL / CMake / Ninja (安裝時請注意對應)
```sh
pacman -Syu $MINGW_PACKAGE_PREFIX $MINGW_PACKAGE_PREFIX-ninja $MINGW_PACKAGE_PREFIX-cmake $MINGW_PACKAGE_PREFIX-gcc $MINGW_PACKAGE_PREFIX-pkg-config $MINGW_PACKAGE_PREFIX-openal $MINGW_PACKAGE_PREFIX-SDL2 $MINGW_PACKAGE_PREFIX-wxWidgets
```
4. 在 Source Code 根目錄執行:
```sh
cmake -G "Ninja" -DMSYS=TRUE -DCMAKE_BUILD_TYPE=Release -DUSE_NETWORKING=ON .
ninja
```

Linux 作業系統 (Debian-based 9+ / RedHat-based EL8+):
1. 安裝基本編譯環境 : 

```sh
[Debian-based] apt install build-essential
[RedHat-based] dnf install make automake gcc gcc-c++ kernel-devel
```

2. 安裝相關涵式庫 SDL2 / wxWidgets 3.x / OpenAL / CMake / Ninja (安裝時請注意對應)

```sh
[Debian-based] apt install libsdl2-dev libwxgtk3.0-gtk3-dev libopenal-dev cmake extra-cmake-modules pkg-config ninja-build
[RedHat-based] dnf install SDL2-devel wxGTK-devel wxGTK3-devel openal-soft-devel cmake ninja-build
```

3. 在 Source Code 跟目錄執行:
```sh
cmake -G "Ninja" -DCMAKE_BUILD_TYPE=Release -DUSE_NETWORKING=ON .
ninja
```

關於其他 CMake 選項與設定，請見 PCem Github 頁面。

---

原作者已使用 GPL v2.0 授權該軟體之使用，詳情請見 COPYING 檔案。  
另外也有參考其他相關專案之程式碼，詳情請見 NOTICE 檔案。