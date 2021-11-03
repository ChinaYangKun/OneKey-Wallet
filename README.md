# OneKey-Wallet

### [IMPORTANT] 

### 🚧 This repo has been deprecated due to a lot of updates and changes, please go to OneKey [official project page](https://github.com/OneKeyHQ) to find the repo or code you need.


-------


Efficiency and secure crypto wallet for Bitcoin, Ethereum and more.

![git_hero_page.png](https://i.loli.net/2020/12/08/x2opCfVmEnK6XYq.png "OneKey Preview")

## 🔗 Links you may need
|  Target   | URL  |  Tips  |
|  ----  | ----  |  ----  |
| 🖥️ Official Web Site  | https://www.onekey.so/ | DO NOT visit other fishing sites |
| ⬇️ Download  | https://download.onekey.so/  | Both Android and iOS supported |
| 😊 Community | https://discord.com/invite/nwUJaTzjzv | Join us and talk! |

## 📱 OneKey App Works on
* iOS Device with system version **13.0 or above**
* Android Device with system version **8.0 or above**

## 📝 Translations
##### Wanna help us to make OneKey global?
* Please drop us an email (hi@onekey.so) so that we can put you in the translation team, or, go visit https://discord.com/invite/nwUJaTzjzv and say hi, we'll have you onboard.

## 🔋 Hardware
Not only is OneKey's software all open source, but the hardware is also completely open source, from the circuit boards to the 3D structures, and we've opened up all the information so you can print these enclosures and build your own OneKey if you're interested.

![3d_structure.png](https://i.loli.net/2020/12/08/S3FGmUyrVwToIJq.png)

Here is something you need to build your own OneKey:

|  Items   | URL  |  Tips  |
|  ----  | ----  |  ----  |
| 📕 Documents  | https://github.com/OneKeyHQ/doc | Grab whatever you need |
| 📦 3D File  | https://github.com/OneKeyHQ/doc/tree/master/docs/3d | Use it on your 3D Printer  |
| 📟 PCB File | https://github.com/OneKeyHQ/doc/tree/master/docs/pcb | / |
| 🧩 Secure Element | https://github.com/OneKeyHQ/doc/tree/master/docs/se| / |



## 🛠️ Build & Run Our Software


### For 🍎 iOS 

First, visit https://github.com/OneKeyHQ/electrum/tree/bixin_dev/ios

and then:

Quick Start Instructions
------------------------
1. Requirements:

   * Xcode 12.1 is required 
   * Python 3.8 must be installed
   * cookiecutter, briefcase, pbxproj, and setuptools python packages must be installed::

           python3.8 -m pip install 'setuptools==40.6.2' --user
           python3.8 -m pip install 'cookiecutter==1.6.0' --user
           python3.8 -m pip install 'briefcase==0.2.6' --user
           python3.8 -m pip install 'pbxproj==2.5.1' --user
2. ReSign the binary dependencies
        sh coderesign.sh

3. Generate the iOS project using the included shell script::

           ./make_ios_project.sh

App Store and Ad-Hoc Distribution
---------------------------------
For reasons that aren't entirely clear to me (but likely due to the way libPython.a and other libs are built), you need to do some special magic for the "Release" build to actually run properly. This means that if you want to compile for the App Store or for Ad-Hoc distribution, you need to disable symbol stripping of the compiled binary.  Make sure the following build settings for the "Release" build are as follows:

 - **Strip Debug Symbols During Copy** = NO
 - **Strip Linked Product** = NO
 - **Strip Style** = Debugging Symbols
 - **Enable Bitcode** = NO
 - **Valid Architectures** = arm64
 - **Symbols Hidden by Default** = NO

For more information, see this stackoverflow post: https://stackoverflow.com/questions/22261753/ios-app-wont-start-on-testflight-ad-hoc-distribution

Additional Notes
----------------
The app built by this Xcode project is a fully running standalone OneKey as an iPhone app.!

It uses the 'Briefcase' project to create an Xcode project which contains within it a Python interpreter, plus all scripts and dependent python packages. Python 3.6 or above is recommended.

- Rubicon-iOS Web Page: https://pybee.org/project/projects/bridges/rubicon/
- Briefcase Web Page: https://pybee.org/project/projects/tools/briefcase/


------------------------

### For 🤖 Android OS

First, visit https://github.com/OneKeyHQ/electrum/tree/bixin_dev/android

and then:

Quick Start Instructions
------------------------

The Android app can be built on any OS which can run the Android development tools. However,
the following automated process is available for Linux x86-64:

If necessary, install Docker using the [instructions on its
website](https://docs.docker.com/install/#supported-platforms).

Copy your release key to `keystore.jks` in this directory. It must contain a key with the
following configuration:

    keyAlias "key0"
    keyPassword "android"
    storePassword "android"

Run `build.sh`. The APK will be generated in `release` in this directory.

Between builds it may be helpful to free up disk space with the command `docker system prune`.


#### Development

To start developing the app, just open this directory in Android Studio.

#### Strings

For user interface text, the app uses the standard Android string resource system. The
`strings.xml` files are generated by the Gradle task `generateStrings`, which in turn calls the
script `contrib/make_locale` to obtain strings from elsewhere in the repository and Crowdin.

Android-specific strings should be added to
`app/src/main/python/electrum_gui/android/strings.py`.

`generateStrings` is run automatically the first time you build the app. If any of the source
strings change, you'll need to run it again manually to pick them up.

The Android string IDs are generated from the first 2 words of each string, plus as many more
words as necessary to make them unique. So if any of the source strings change, you may need to
update ID references in the code.

------------------------

## ⚖️ License 
* See [LICENSE](https://github.com/OneKeyHQ/electrum/blob/bixin_dev/LICENCE) 


## 💬 Contact
#### You can find us via these ways
* 🖥️ Website: https://www.onekey.so/
* 📮 E-mail: hi@onekey.so
* 🐦 Twitter: [@OneKeyHQ](https://twitter.com/OneKeyHQ "OneKey on twitter")
* 🧣 Weibo: [@OneKeyHQ](https://weibo.com/u/7503920127 "OneKey on Weibo")
* 👻 Discord: https://discord.com/invite/nwUJaTzjzv

TBD!....
