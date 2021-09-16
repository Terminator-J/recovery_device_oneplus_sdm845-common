## Hola amiguitos

This is my attempt to fix up and add a little crDroid customization flavor back into the sdm845-common device tree for OnePlus 6 & 6T (enchilada & fajita).
Moved a few things to common that don't make sense to be separate, and separated a few things that don't make sense to be commonized.
For the time being, the strategy is to move device-specific hardware features out of LiveDisplay/Lineage-SDK and into DeviceSettings,
to both be more consistent with sm8150 & sm8250 common trees, and because I don't know c++ and HIDL/AIDL well enough yet.

Rebased on the official lineage-18.1 branch of the LineageOS device tree as of September 2021.

* Please note that, for now, you'll need to add `pigz` to the allowed host tools paths in build/soong/ui/build/paths/config.go in order to compile the MCD-based kernel.
