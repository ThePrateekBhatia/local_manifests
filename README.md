# local_manifests

This repository contains XML files that help in specifying custom repositories and projects for building Android ROMs.

## Instructions

1. **Fork this repo**: Fork this repository to your GitHub account.
2. **Clone this forked repo locally**: Clone the forked repository to your local machine.
3. **Create .xml file**: Create a new XML file with any name you prefer.
4. **Copy&Paste the following content into your XML file**:

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <manifest>
        <!-- remote source -->
        <remote name="Freaky"           fetch="https://github.com/ThePrateekBhatia/" />
        <remote name="Freaky-Gitlab"    fetch="https://gitlab.com/ThePrateekBhatia/" />
        <remote name="crDroid"          fetch="https://github.com/crdroidandroid/" />
        <remote name="KRISHNA"          fetch="https://github.com/pure-soul-kk/" />
        <remote name="Viper"            fetch="https://github.com/TogoFire/" />

        <!-- Device Tree -->
        <project name="android_device_xiaomi_veux"               path="device/xiaomi/veux"               remote="Freaky"   revision="fourteen" />
        <project name="proprietary_vendor_xiaomi_veux"           path="vendor/xiaomi/veux"               remote="Freaky"   revision="fourteen" clone-depth="1" />

        <!-- Kernel Tree -->
        <project name="android_kernel_oneplus_sm8350 "           path="kernel/xiaomi/sm6375"             remote="crDroid"  revision="14.0" clone-depth="1" />
        <project name="android_device_xiaomi_veux-kernel"        path="device/xiaomi/veux-kernel"        remote="crDroid"  rivision="14.0" clone-depth="1" />
    
        <!-- HALs -->
        <project name="android_hardware_xiaomi"                  path="hardware/xiaomi"                  remote="crDroid"  revision="14.0" clone-depth="1" />

        <!-- Google Camera -->
        <project name="vendor_xiaomi_veux-gcam"                  path="vendor/xiaomi/veux-gcam"          remote="KRISHNA"  revision="main" />

        <!-- ViPER4AndroidFX -->
        <project name="packages_apps_ViPER4AndroidFX"            path="packages/apps/ViPER4AndroidFX     remote="Viper"    revision="v4a" />
    </manifest>
    ```

5. **Replace everything with the remotes & repositories you need**: Customize the XML file according to your requirements by replacing the existing content with the remote sources and project details you want to include.
6. **Commit & push the changes to your forked repo**: Once you've made the necessary changes, commit and push the XML file to your forked repository on GitHub.
7. **Congratulations! Now you can start building your ROM**: With the local_manifests set up, you're ready to start building your custom Android ROM. Best of luck with your ROM-building endeavors!

Feel free to reach out if you have any questions or need further assistance. Happy ROM building!
