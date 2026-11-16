## v4.0 (42)

### Changelog
**Nov 16, 2026**
- Updated the on-device APKEditor engine to 1.4.9 (more reliable, faster on-device patching).

### What's new
- Removes PowerKeeper's FPS limits in apps, video apps (YouTube and others) and games
- Removes Joyose's per-game frame caps (Xiaomi's game tuning app)
- Removes the refresh-rate drop when the phone heats up
- Battery saver no longer caps CPU speed (its other savings stay on)
- Unlocks PowerKeeper's hidden cloud info menu on stable ROMs: dial `*#*#76937#*#*`
- Closes a security hole: any app could point PowerKeeper's power policy to its own server
- Scheduler boost for system UI on devices that support it

### Improvements
- Module is now 3.8 MB (was 45 MB): no bundled Java, the phone's own Android runtime does the patching
- Patches the PowerKeeper and Joyose installed on your ROM, so it matches any version
- Works with Magisk, KernelSU and APatch
- Patching matches methods by name or content instead of fixed code positions, so it should keep working on newer versions
- If Joyose is missing or not supported, only that part is skipped
- Updating over an older version patches the original apps, not the old patched copies
- Fixes apps running slower after patching (old compiled files are now skipped)
- Clears only the patched apps' package cache, nothing else
- Clears a saved refresh-rate limit on first boot

### Notes
- Flash from the Magisk / KernelSU / APatch app, not recovery
- Android 13+: signature verification must be disabled
- Reflash after every ROM update
- Some games pick their own FPS limit per phone model (for example PUBG, Genshin); a system mod cannot change that
- Thermal safety limits are untouched (overheat protection still works)
- Report any issues or feedback in the [Support Group](https://t.me/bootloop_discussion)

