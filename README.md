# TWRP Device configuration for Motorola Moto Z4

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core (2x2.0 GHz Kryo 460 Gold & 6x1.7 GHz Kryo 460 Silver)
CHIPSET | Qualcomm SDM675 Snapdragon 675
GPU     | Adreno 612
Memory  | 4GB
Shipped Android Version | 9 (Pie)
Storage | 128GB
Battery | 3600 mAh
Dimensions | 158 x 75 x 7.4 mm
Display | 1080 x 2340 pixels, 6.4" OLED
Rear Camera  | 48 MP (f/1.7) (PDAF, OIS)
Front Camera | 25 MP (f/2.0)

<!--- ![Device Picture](https://fdn2.gsmarena.com/vv/bigpic/motorola-moto-z4-r.jpg) --->
![Device Picture](https://phonesdata.com/files/models/Motorola--Moto-Z4-302.png)

### Kernel Source

Check here: https://github.com/Fazwalrus/android_kernel_motorola_sm6150

### How to compile

```sh
. build/envsetup.sh
export LC_ALL=C
lunch omni_foles-eng
make -j4 recoveryimage
```

To automatically make the twrp installer, you need to import this commit in the build/make path: https://gerrit.omnirom.org/#/c/android_build/+/33182/
and add @osm0sis' standard twrp_abtemplate repo to a local manifest as indicated below (followed by another `repo sync` to download the repo):

```xml
<project name="osm0sis/twrp_abtemplate" path="bootable/recovery/installer" remote="github" revision="master"/>
```

### Copyright
 ```
  /*
  *  Copyright (C) 2013-21 The OmniROM Project
  *
  * This program is free software: you can redistribute it and/or modify
  * it under the terms of the GNU General Public License as published by
  * the Free Software Foundation, either version 3 of the License, or
  * (at your option) any later version.
  *
  * This program is distributed in the hope that it will be useful,
  * but WITHOUT ANY WARRANTY; without even the implied warranty of
  * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  * GNU General Public License for more details.
  *
  * You should have received a copy of the GNU General Public License
  * along with this program.  If not, see <http://www.gnu.org/licenses/>.
  *
  */
  ```
