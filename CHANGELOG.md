# Changelog

All notable changes to the **InfiniteDropper** project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
