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
