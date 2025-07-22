# Custom crDroid `frameworks_base` Fork

This fork includes overlay modifications to the Android framework and SystemUI components.

## Goals
- Override stock configuration values via overlay XML
- Tune SystemUI behavior (e.g. QS layout, nav bar, screenshot toggle)
- Test and maintain clean base modifications for my custom crDroid builds

## Modified Paths
- `overlay/frameworks/base/core/res/res/values/config.xml`
- `overlay/frameworks/base/packages/SystemUI/res/values/config.xml`

## Sample Changes
```xml
<bool name="config_showNavigationBar">false</bool>
<integer name="config_maxQsColumns">3</integer>
<bool name="config_enableScreenshot">true</bool>

---

## 🧾 If You Use This in `local_manifest.xml`
Inside `~/.repo/local_manifests/crdroid.xml`, description not needed per se, but you can still comment it:

```xml
<!-- Custom frameworks_base with personalized overlays -->
<project name="yourgithub/android_frameworks_base"
         path="frameworks/base"
         remote="github"
         revision="15.0" />
# frameworks_base of the 🧠

This ain't your grandma’s Android base.

Features:
- Kicked out the nav bar
- Gave QS tiles a haircut (fewer columns)
- SystemUI now obeys MY config.xml

Built for:
- Instantnoodle (OnePlus 8)
- Instant fun. Instant regret. Instant rollback if it breaks.

Enjoy responsibly. 🍻

# CincaiAndroid Frameworks Base

This is a modified fork of the `android_frameworks_base` repository, originally from the crDroid project.

This fork was made as part of the **CincaiAndroid** ROM project — a playful and experimental Android ROM built with learning, simplicity, and flexibility in mind.

## Collaboration

Development and modifications are done with occasional technical and creative input from **ChatGPT** by OpenAI. The AI serves as a co-pilot, advisor, and... sometimes, comic relief.

## Credits

- **crDroid Android**: For the original and outstanding base sources
- **OpenAI**: For ChatGPT’s guidance throughout this journey
- **Android Open Source Project (AOSP)**: For the foundation of all custom ROMs
- ...and all upstream contributors

## License

Follows the original licensing of the AOSP and crDroid base, unless explicitly stated otherwise.

