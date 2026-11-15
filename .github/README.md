**[English](#english) | [中文](#中文)**

<a id="english"></a>

## 🚙 About
A personal fork of [sunnypilot](https://github.com/sunnypilot/sunnypilot) that brings sunnypilot's steering assist to the **2021–2022 Taiwan (Asia-Pacific spec) Subaru Outback** on the comma 4. sunnypilot is a fork of comma.ai's openpilot; this fork only adds the changes this car needs and is otherwise identical to sunnypilot.

> ⚠️ **Experimental. Use at your own risk.** This is not an officially supported sunnypilot or comma.ai release. Keep your hands on the wheel and your eyes on the road at all times. The system may disengage or steer unexpectedly at any moment.
>
> ⚠️ **EyeSight Automatic Emergency Steering (AES):** While this software is running, if EyeSight activates Automatic Emergency Steering (AES), the device may show an error and EyeSight may stop working. If this happens, pull over somewhere safe, then restart both the car and the device to restore normal operation. Do not rely on any EyeSight assistance until you have done so.

## 🚘 Supported vehicle & requirements
| Item | Requirement |
|---|---|
| Vehicle | 2021–2022 Subaru Outback, Taiwan / Asia-Pacific spec (angle-based EyeSight steering) |
| Device | comma 4 |
| Harness | Subaru D harness |

US-spec and 2020–2022 torque-steering Outbacks are **not supported** by this fork; please use [official sunnypilot](https://community.sunnypilot.ai/t/recommended-branch-installations/235). Other angle-steering Subarus (e.g. the 2025 Crosstrek) will only run in dashcam mode on this branch and will not steer.

## 📥 Installation
1. If other software is already installed: on the C4, go to **Settings → Device → Uninstall**. The device reboots into setup.
2. Choose **Custom Software**.
3. Enter:
   ```
   darwinchentw/22obtw
   ```
4. Wait for the download and first build (about 10–20 minutes). Installation is done once it boots to the home screen.
5. On your first drive, drive normally for a while so the device can finish calibrating.

**Install failed?** If you see "Incompatible openpilot version", first install stock openpilot by entering `openpilot.comma.ai` under Custom Software, let it fully boot, uninstall it, then enter the URL above again.

## 🔄 Updates
The C4 downloads updates from the `22obtw` branch automatically and applies them on the next reboot after the car is turned off. You can also check manually under **Settings → Software**.

## ✨ Differences from sunnypilot
- **Angle-based steering (LKAS angle)**: ported from comma.ai's not-yet-merged [commaai/opendbc#2864](https://github.com/commaai/opendbc/pull/2864), keeping sunnypilot's MADS
- **Fingerprinting**: adds a fingerprint for the Taiwan-spec 2022 Subaru Outback
- **MADS fixes**:
  - Fixes MADS lateral control failing to engage after turning ACC main off and back on
  - The LKAS button no longer affects MADS state

## 🐞 Reporting issues
Please report problems in this repo's [Issues](https://github.com/darwinchentw/openpilot/issues). Describe what happened and when, and include a [comma connect](https://connect.comma.ai/) route link.

**Car not recognized?** If the device says your car is not supported, or only runs in dashcam mode, your car's firmware versions may differ from the ones currently listed. Please open an issue with a route link so your firmware versions can be added.

---

<a id="中文"></a>

## 🚙 版本說明
這是 [sunnypilot](https://github.com/sunnypilot/sunnypilot) 的個人 fork，讓 **2021–2022 年式台灣（亞太規格）Subaru Outback** 能在 comma 4 上使用 sunnypilot 的轉向輔助。sunnypilot 是 comma.ai openpilot 的分支，本 fork 只加上這台車需要的修改，其餘功能與 sunnypilot 相同。

> ⚠️ **實驗性質，使用風險自負。** 這不是 sunnypilot 或 comma.ai 官方支援的版本。使用時請隨時手握方向盤、注意路況，系統隨時可能退出或做出非預期的轉向。
>
> ⚠️ **EyeSight 緊急轉向輔助（AES）注意事項：** 使用本軟體期間，若 EyeSight 啟動緊急轉向輔助（AES），裝置可能會出現錯誤，EyeSight 也可能因此失效。發生時請將車輛停到安全的地方，重新啟動車輛及裝置，即可恢復正常運作。恢復之前，請勿依賴 EyeSight 的任何輔助功能。

## 🚘 適用車型與需求
| 項目 | 需求 |
|---|---|
| 車型 | 2021–2022 年式 Subaru Outback，台灣／亞太規格（角度式 EyeSight 轉向） |
| 裝置 | comma 4 |
| 線組 | Subaru D 線組（Subaru D harness） |

美規、2020–2022 扭力式轉向的 Outback **不適用**，請使用[官方 sunnypilot](https://community.sunnypilot.ai/t/recommended-branch-installations/235)。其他使用角度式轉向的 Subaru（例如 2025 Crosstrek）在這個分支只會進入行車記錄器模式，不會控制轉向。

## 📥 安裝
1. 如果已經裝了其他軟體：C4 **設定 → 裝置 → 解除安裝**，重開機後會回到設定畫面
2. 選 **Custom Software（自訂軟體）**
3. 輸入：
   ```
   darwinchentw/22obtw
   ```
4. 等待下載及第一次編譯（約 10–20 分鐘），開機到主畫面即完成
5. 第一次上路需要正常行駛一段時間完成自動校正

**安裝失敗？** 如果出現「Incompatible openpilot version」，先在 Custom Software 輸入 `openpilot.comma.ai` 安裝官方 openpilot，等完整開機後解除安裝，再重新輸入上面的網址。

## 🔄 更新
C4 會自動從 `22obtw` 分支下載更新，熄火後重新開機時套用。也可以到 **設定 → 軟體** 手動檢查更新。

## ✨ 跟原版 sunnypilot 的差別
- **角度式轉向（LKAS angle）**：移植自 comma.ai 尚未合併的 [commaai/opendbc#2864](https://github.com/commaai/opendbc/pull/2864)，保留 sunnypilot 的 MADS
- **車型辨識**：新增台規 2022 年式 Subaru Outback fingerprint
- **MADS 修正**：
  - 修正 ACC 主開關關閉再打開後，MADS 橫向控制無法啟用的問題
  - LKAS 按鈕不會影響 MADS 狀態

## 🐞 問題回報
請在本 repo 的 [Issues](https://github.com/darwinchentw/openpilot/issues) 回報，說明發生的情況、時間，並附上 [comma connect](https://connect.comma.ai/) 的行程連結。

**車子辨識不到？** 開機後如果顯示「車型不支援」或只進入行車記錄器模式，可能是你的車韌體版本跟目前收錄的不同。請到 Issues 回報並附上行程連結，方便加入你的韌體版本。
