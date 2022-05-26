# android_vendor_losppOTA
# lospp OTA repo
In order for a device to be officially supported by lospp, OTA information needs to be added.
Please refer to the following "Readme" to get started

## 1. Introduction ##
In order for a device to be OTA compliant, there are a few things to know.

### 1.1 JSON structure ###
```
{
  "response": [
    {
        "maintainer": "Name (nickname)",
        "oem": "OEM",
        "device": "Device Name",
        "filename": "lospp-12.1-<date>-<device codename>-v<ppversion>.zip",
        "download": "https://sourceforge.net/projects/lospp/files/<device codename>/<crversion>/lospp-12.1-<date>-<device codename>-v<ppversion>.zip/download",
        "timestamp": 0000000000,
        "md5": "abcdefg123456",
        "sha256": "abcdefg123456",
        "size": 123456789,
        "version": "<ppversion>",
        "buildtype": "Testing/Alpha/Beta/Weekly/Monthly",
        "forum": "https://forum link",
        "gapps": "https://gapps link",
        "firmware": "https://firmware link",
        "modem": "https://modem link",
        "bootloader": "https://bootloader link",
        "recovery": "https://recovery link",
        "paypal": "https://donation link",
        "telegram": "https://telegram link",
        "dt": "https://github.com/lospp/android_device_<oem>_<device_codename>",
        "common-dt": "https://github.com/lospp/android_device_<orm>_<SOC>-common",
        "kernel": "https://github.com/lospp/android_kernel_<oem>_<SOC>"
    }
  ]
}
```

### 1.2 changelog.txt structure ### 
```
Highlights & Device Specific Changes:
Build type: Testing/Alpha/Beta/Weekly/Monthly
Device: Device name (<device codename>)
Device maintainer: Name (nickname)
Required firmware: add if any else remove this line

===== <date> =====
- change 1
- change 2
- change 3
```

## 2 Guidelines ##
* Check if manufacturer already exists
* Check if published link is official
* Check if JSON is intact with help of online validator tools like [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com) or [https://jsonformatter.org](https://jsonformatter.org)
* Check if no extra / missing spaces
