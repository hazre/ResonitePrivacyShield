# PrivacyShield

A [ResoniteModLoader](https://github.com/resonite-modding-group/ResoniteModLoader) mod for [Resonite](https://resonite.com/) that attempts to improve privacy slightly.

> Port of [PrivacyShield](https://git.ljoonal.xyz/ljoonal/Neos-Mods) mod by [ljoonal](https://github.com/ljoonal) for Neos to Resonite

The main feature is making all requests (excluding local:// and resdb://) require you granting permission to it, instead of just flux ones. It uses the same domain allowlist/blocklist as the normal logix requests. So no more tracking pixels!

The other semi-sensible feature is spoofing the local timezone. It's disabled by default, and any changes will require a restart.

Also includes a slightly questionable feature, FPS spoofing. Questionable as it might also just break some things, doesn't really protect you, and can be summarized as:

> Your scientists were so preoccupied with whether or not they could, they didn't stop to think if they should.

The FPS spoofing allows sensible values (so pick like between 30-60), and disables with anything else (so -1 for example). It doesn't spoof anything other than the Local User's FPS (so dT or the PerformanceMetrics component will leak your real FPS). But it does at least currently provide some privacy from some session user manager type of UIs. I'd kindly ask you to not to try to work around this if you're making tools, at least if your tool isn't opt-in. Since I think that this is a somewhat decent way to opt-out of FPS tracking.

## Installation

1. Install [ResoniteModLoader](https://github.com/resonite-modding-group/ResoniteModLoader).
1. Place [PrivacyShield.dll](https://github.com/hazre/PrivacyShield/releases/latest/download/PrivacyShield.dll) into your `rml_mods` folder. This folder should be at `C:\Program Files (x86)\Steam\steamapps\common\Resonite\rml_mods` for a default install. You can create it if it's missing, or if you launch the game once with ResoniteModLoader installed it will create the folder for you.
1. Start the game. If you want to verify that the mod is working you can check your Resonite logs.
