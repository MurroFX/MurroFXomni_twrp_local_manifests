# Initialise the AOSP tree

  - In a terminal window, enter the following commands: 
```bash
mkdir ~/omni_9.0
cd ~/omni_9.0
repo init -u git://github.com/omnirom/android.git -b android-9.0
```

  - Clone the local_manifests from GitHub using the following commands:
```bash
cd .repo
git clone https://github.com/MartinX3sAndroidDevelopment/local_manifests.git
cd local_manifests
git checkout android-9.0
cd ../..
```

  - To download the code into the device repos created above, run the command:
```bash
repo sync
```

  - To build the TWRP bootimage ("-eng" build)
```bash
. build/envsetup.sh;
lunch;
make bootimage;
```
