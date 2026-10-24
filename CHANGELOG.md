# Changelog

All notable changes to the **InfiniteDropper** project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.2] - 2026-10-24

### Added
- **Official Developer Credit:**
  - Formally credited developer **Smitronix** across `plugin.yml`, the `/id help` command menu, and the server startup banner.
- **Server Console Plugin Startup Banner:**
  - Beautiful formatted console banner displayed upon startup with ASCII typography, developer attribution (**Smitronix**), server platform diagnostics, and active feature verification indicators (Auto-Clock, Direct Container Injection, Underwater Kelp & Crop Fertilization, 54-Slot GUI Item Selector, Modrinth & GitHub Async Update Checker).
- **Console Shutdown Diagnostics:**
  - Added clean shutdown logging confirming all active infinite blocks are safely persisted to world NBT data before container stops.

---

## [1.0.1] - 2026-10-24

### Added
- **Interactive In-GUI Item Selector:**
  - Added a dedicated 54-slot visual Item Selection Menu accessible by clicking Slot 10 in the Settings GUI.
  - Displays all server-allowed farm items (Bone Meal, Wheat Seeds, Carrots, Potatoes, Melon/Pumpkin Seeds, Arrows, Saplings, Buckets) with Bone Meal conveniently pinned at Slot 0.
  - Fully supports multi-page browsing and instant item selection with a single click.
- **Dedicated Underwater Kelp Growth Engine:**
  - Dispensing Bone Meal directly into `KELP` or `KELP_PLANT` water columns now actively grows the kelp upward stage by stage.
  - Spawns green happy villager particles and plays bone meal crunch sound effects.
- **Enhanced Multi-Crop Fertilization:**
  - Added automatic growth stage advancing for Sugar Cane, Bamboo, and ageable crops (Wheat, Carrots, Potatoes, Beetroots).
- **In-World Shift + Right-Click Auto-Conversion:**
  - Server administrators can now Sneak + Right-Click **any** vanilla Dropper or Dispenser in the world to automatically convert it into an Infinite Dropper/Dispenser and open the GUI immediately.
- **Automatic Update Alert System:**
  - Added an asynchronous update checking engine that queries Modrinth and GitHub for new releases without impacting server TPS.
  - Automatically notifies server operators in chat upon joining with clickable update links and plays an alert chime.
- **Instant Inventory Selection:**
  - Clicking any allowed item in your player inventory while inside the Settings GUI now instantly selects and locks it in as the infinite supply.

---

## [1.0.2] - 2026-10-24

### Added
- **Official Developer Credit:**
  - Formally credited developer **Smitronix** across `plugin.yml`, the `/id help` command menu, and the server startup banner.
- **Server Console Plugin Startup Banner:**
  - Beautiful formatted console banner displayed upon startup with ASCII typography, developer attribution (**Smitronix**), server platform diagnostics, and active feature verification indicators (Auto-Clock, Direct Container Injection, Underwater Kelp & Crop Fertilization, 54-Slot GUI Item Selector, Modrinth & GitHub Async Update Checker).
- **Console Shutdown Diagnostics:**
  - Added clean shutdown logging confirming all active infinite blocks are safely persisted to world NBT data before container stops.

---

## [1.0.0] - 2026-10-24

### Added
- **Infinite Dropper & Dispenser Blocks:**
  - Added custom glowing `Infinite Dropper` and `Infinite Dispenser` items with PersistentDataContainer (PDC) tags.
  - Paper native `TileState` persistence: Survives world saves, server reboots, and chunk unloads with zero external database requirements.
- **Unlimited Supply & Auto-Replenish:**
  - Placed infinite items are automatically locked and replenished at a full stack (64), ensuring farm supplies like bone meal never deplete.
- **Internal Auto-Clock (Zero Redstone Lag):**
  - Toggleable internal pulsing engine with sub-second tick intervals (5 to 100+ ticks).
  - Eliminates the need for noisy comparator or repeater redstone loops, preserving server TPS.
- **Direct Container Injection:**
  - When facing a Chest, Hopper, or Barrel directly, items are injected straight into the container inventory.
  - Skips floating item entities in the world to eliminate entity lag and prevent despawn loss.
- **Smart Farming / Dispenser Support:**
  - Dispensers loaded with bone meal can directly fertilize crops, saplings, and sugarcane without spilling items.
- **Interactive Configuration GUI:**
  - Sneak + Right-Click with an empty hand opens a custom 27-slot menu.
  - Configure the infinite item, toggle Auto-Clock, adjust pulse speed, and cycle batch sizes (1, 4, 16, 64).
- **Security & Restriction System:**
  - Configurable `WHITELIST` and `BLACKLIST` in `config.yml`.
  - Disallows duplication of high-value items (Diamonds, Netherite, Shulkers, TNT).
  - Piston and explosion immunity (immune to Creepers, TNT, and Withers).
  - Admin permission gates (`infinitedropper.admin`, `infinitedropper.give`, `infinitedropper.place`, `infinitedropper.break`, `infinitedropper.gui`).
- **Modrinth Integration:**
  - Published release v1.0.0 on Modrinth under developer SmitroniX: [https://modrinth.com/plugin/infinite-dropper](https://modrinth.com/plugin/infinite-dropper).
