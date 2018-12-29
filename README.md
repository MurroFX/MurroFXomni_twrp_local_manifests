# XDA Thread

https://forum.xda-developers.com/xperia-xz2/development/recovery-twrp-3-2-2-0-touch-recovery-t3821597

# Initialise the omnirom tree

  - In a terminal window, enter the following commands: 
```bash
mkdir omni_9.0
cd omni_9.0
repo init -u git://github.com/omnirom/android.git -b android-9.0
```
###### or for the minimal TWRP build environment
```bash
mkdir omni_9.0
cd omni_9.0
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
```

  - Clone the local_manifests from GitHub using the following commands:
```bash
cd .repo
git clone https://github.com/MartinX3sAndroidDevelopment/omni_twrp_local_manifests.git local_manifests
cd ..
```
###### or for the minimal TWRP build environment
```bash
cd .repo
git clone https://github.com/MartinX3sAndroidDevelopment/omni_twrp_local_manifests.git local_manifests
rm local_manifests/twrp.xml
cd ..
```

  - To download the code into the device repos created above, run the command:
```bash
repo sync
```

  - To build the TWRP bootimage ("-eng" build)
```bash
. build/envsetup.sh;
export ALLOW_MISSING_DEPENDENCIES=true # Only if you use minimal omnirom twrp tree.
lunch;
make bootimage;
```
