# GamePanelHUD (SPT 4.1.x Edition)

**GamePanelHUD** is an all-in-one modular HUD and tactical UI expansion for **Escape from Tarkov (Single Player Tarkov - SPT)**.

Inspired by RPG-style compass and heads-up displays, it brings dynamic navigation, extraction tracking, quest objectives, and customizable raid panels into Tarkov without breaking immersion.

---

## ✨ Features

* 🧭 **Raid Compass (Top / Bottom Bar)**:
  * Horizontal compass displaying cardinal directions (N, S, E, W) and bearing degrees.
  * **Real-time Extracts**: Visual indicators of active and available map extraction points with distance in meters.
  * **Airdrop Tracking**: Alerts and compass markers pointing directly toward dropped supply crates.
  * **Quest Objectives**: Real-time markers pointing toward quest targets and task locations.
* 📍 **Player Coordinates**:
  * Live `X, Y, Z` coordinate display in the lower corner for easy map navigation.
* 🎯 **Modular HUD Components** (All independently toggleable):
  * **Compass HUD**: Compass strip and POI markers.
  * **Health HUD**: Minimalist vitals, stamina, and body part status.
  * **Weapon HUD**: Ammo counters and firing mode indicator.
  * **Grenade HUD**: Trajectory / grenade awareness.
  * **Hit & Kill HUD**: Hit feedback and kill notifications.
* ⚙️ **In-Game Configuration**:
  * Press the **`Home`** key (or **`F12`** via BepInEx Configuration Manager) in raid to customize positions, sizes, opacities, and toggles in real time.

---

## 🚀 Enhancements in this Fork (`rauldzmartin / f4taL`)

1. **SPT 4.1.x Compatibility**:
   * Merged community migration fixes for **SPT 4.1.x (SP-Tushonka / EFT 0.15+)**.
   * Updated internal API calls, removed deprecated references, and aligned with `KmyTarkovApi v3.5.0`.
2. **Hide Completed Quest Conditions** (`feat: compass`):
   * Added a dedicated setting to automatically filter out and hide completed sub-conditions on active quest markers from the compass.
   * Drastically reduces on-screen clutter during multi-stage quests.

---

## 📦 Requirements & Installation

### Requirements
* **SPT 4.1.x** (SP-Tushonka or modern SPT 4.1+ release)
* **BepInEx 5.x** (Included with standard SPT installations)
* **[KmyTarkovApi (v3.5.0+)](https://github.com/Hazeofdream/KmyTarkovApi/releases)** (Required core dependency)

### Installation
1. Download the release archive (`GamePanelHUD` and `KmyTarkovApi`).
2. Extract both archives into your game root directory:
   ```text
   <Your-SPT-Folder>/
   └── BepInEx/
       └── plugins/
           ├── kmyuhkyuk-GamePanelHUD/
           └── kmyuhkyuk-KmyTarkovApi/
   ```
3. Launch the game and press **`Home`** in raid to configure the HUD overlay.

---

## 🛠️ Building from Source

1. Clone this repository:
   ```bash
   git clone https://github.com/rauldzmartin/GamePanelHUD.git
   ```
2. Open `GamePanelHUD.sln` in **Visual Studio 2022** or **JetBrains Rider**.
3. Ensure reference DLLs are available from your SPT / EFT installation:
   * `EscapeFromTarkov_Data/Managed/` (Assembly-CSharp.dll, UnityEngine*.dll, etc.)
   * `BepInEx/core/` (BepInEx.dll, 0Harmony.dll)
   * `BepInEx/plugins/kmyuhkyuk-KmyTarkovApi/` (KmyTarkovApi.dll and dependencies)
4. Build `GamePanelHUD.sln` using the `Release` configuration.

---

## 🤝 Credits & Acknowledgments

* **Original Creator**:
  * [**kmyuhkyuk**](https://github.com/kmyuhkyuk/GamePanelHUD) — Architect and creator of **GamePanelHUD** and **KmyTarkovApi**.
* **SPT 4.1 Port & Community Contributors**:
  * [**dustinmoon78**](https://github.com/dustinmoon78/GamePanelHUD) — Initial port and migration patches to SPT 4.1 framework.
  * [**Hazeofdream**](https://github.com/Hazeofdream/GamePanelHUD) — Assembly cleanups, reference fixes, and `4.1-fixed` / `v3.5.0` releases.
  * [**slpf**](https://github.com/slpf/GamePanelHUD) — Community contributions and SPT 4.1 build maintenance.
* **Fork Maintenance & Feature Additions**:
  * [**rauldzmartin (f4taL)**](https://github.com/rauldzmartin/GamePanelHUD) — Completed quest condition filtering, documentation, and unified integration.