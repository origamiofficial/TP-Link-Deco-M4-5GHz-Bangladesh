# TP-Link Deco M4 5GHz Support in Bangladesh
Now Deco M4 users can upgrade to the stable version with 5 GHz band 4 support. Here we will discuss why this is happening & how do we go to a stable version & get future updates.

## Why It's Not Working In Bangladesh?
As you can see [this website](https://www.juniper.net/documentation/en_US/release-independent/junos/topics/reference/specifications/access-point-ax411-country-channel-support.html) shows the 2.4 GHz and 5 GHz channels supported for each country code. It also shows whether 802.11n and 40MHz channel width are supported or not. From table 1's 5th row Bangladesh only supports 149, 153, 157, 161, 165 channels for 5 GHz which are band 4 channels. So consumer devices that support wifi always try to find only band 4 channels. As they are smart enough to figure out where they are located & they avoid all other channels. So mobile devices only work with band 4 (channel 149-165) on 5 GHz in Bangladesh. But Deco devices are made for worldwide support. So they operate in all 5 GHz channels. And here is the problem, phones don't try to see on the other channels where they aren't supposed to see.

## Solution For the Problem
So after investigating the problem TP-Link Bangladesh came with a solution. They build a specific beta firmware [1.4.3 Build 20210324 Rel. 63599 for V2, 1.4.3 Build 20210317 Rel.03630 for V1] for Bangladesh users where they locked the 5 GHz channels on band 4. So that Deco never switches to other channels. Also if the Deco in the future detects an update & tries to upgrade to the latest version it will again unlock all bands for 5 GHz & cause the problem again, so they disabled the update option. The new shipping Deco devices to Bangladesh have a built-in band 4-supported firmware 1.4.1 Build 20200714 Rel. 47859 now.

## Side Effects Of The Solution
As you can already guess you won't get any future updates. Your update option is permanently blocked. This will create a security issue & you can't enjoy any additional features that TP-Link adds in the future. Also, the beta firmware is not so stable. It has some serious bug. Deco's system resources usages are high too. Also as for me, my Deco M4 units shows as V1 after upgrading to beta firmware but they are V2 units. So there are 2 options for the users. Either you upgrade the firmware of your Deco to fix the problems & lose 5 GHz access or you just stick with the beta firmware until it dies.

## Now Finally A Permanent Fix
You can now upgrade your Deco M4's firmware to the latest official firmware with 5Ghz Band 4 support. TP-Link at least realizes the problem & fix it after a long time. They locked 5 GHz on band 4 only in Bangladesh in their stable builds from version 1.5.0+. This feature will only work for Bangladeshi users. Other worldwide users can use as they are using from the first day. From now all Deco M4 units in Bangladesh will work on stable firmware & get firmware just link others.

## Steps To Go To Stable
First, you need to upgrade your Deco units to ["1.4.3 Build 20210324 REL 63599"](https://cutt.ly/DecoM4FixFirmware) This is a very important step otherwise your Deco can't upgrade to the latest official firmware!! This firmware fixes the hardware version conflict [V2 to V1] caused by beta firmware provided by TP-Link Bangladesh. After upgrading to this version you can finally upgrade through the Deco app or WebGUI online upgrade tool to the latest stable official firmware without any issue. I've uploaded the firmware file to this repository too.

## Things To Note
Do not try to manually flash the latest version. Use the Online Upgrade method ONLY after upgrading to the fixed firmware. Upgrading to fix firmware is necessary because after that the country code will be embedded. So that future Deco firmware will know they need to stick with band 4 channels. If your Deco units show as V1 then you can't upgrade to the latest version without upgrading to fix firmware first. It will never upgrade to the latest stable build. The app will show "Download > Install > Reboot". But they will never reboot actually. Again they will show the same previous version 1.4.3
1. For the products with 1.4.1 Build 20200714 Rel. 47859 or beta 1.4.3 Build 20210324 Rel. 63599, it is OK to update to the latest 1.5.0+ version, and it will keep supporting band 4, you will also get the new features supported on the latest version.
2. For the products with generic firmware 1.4.3 Build 20200918 Rel.74289, it is not recommended to update to the 1.5.0 directly after onboarding, please contact the local tech support to request the beta firmware that supports band 4 on 5 GHz first, then update to the latest 1.5.0+ version.
3. If you have updated to the 1.5.0 already from the generic 1.4.3 Build 20200918 Rel.74289 and noticed that the new 1.5.0 still does not support band 4 on 5 GHz, please email support@tp-link.com with [Forum ID 269484](https://community.tp-link.com/en/home/forum/topic/269484?page=1) Deco M4 supports Band 4 on 5 GHz for Bangladesh users.

## If I Reset My Deco Units, Do I Lost Access To Band 4 Again?
The answer is NO. You're safe. Ever since 1.5.2, the country code has been embedded into the firmware. So if the original firmware supported band 4, after the firmware upgrade, the new firmware will support band 4 as well. Even if you reset the Deco, it will still have band 4.

## [Advanced] Deco Firmware Recovery When Bricked
Never flash the latest version firmware via [recovery mode](https://www.tp-link.com/us/support/faq/2958/). You'll lose access to the band 4 5GHz network again. If you somehow bricked your Deco, flash the fixed firmware provided in this repository. After turning it on simply upgrade to the latest version again. If you mistakenly flashed the latest firmware via recovery mode, again go to recovery mode & flash the fixed firmware [untested].

## Some Info
[Fix Firmware](https://cutt.ly/DecoM4FixFirmware) means "1.4.3 Build 20210324 REL 63599" which is added in this repository.
[Dedicated Forum](https://community.tp-link.com/en/home/forum/topic/269484?page=1) on this topic.
