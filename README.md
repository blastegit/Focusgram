<a name="top"></a>
# 🎯Focusgram
![GitHub last commit](https://img.shields.io/github/last-commit/blastegit/Focusgram)
![Static Badge](https://img.shields.io/badge/supported_Instagram_version-<300-blue)

## Languages : [![Static Badge](https://img.shields.io/badge/%F0%9F%87%AB%F0%9F%87%B7-french-blue?style=plastic)](https://github.com/blastegit/Focusgram/blob/main/README.fr.md)

Tired of endless scrolling and time-wasting reels? Experience Instagram as it was meant to be. Our app strips away the distractions, leaving you with a clean, focused feed of stunning photos from the people you care about.

📸 Pure photo content (with just the reels we send you)

⏱️ Save hours of mindless scrolling

🧘 Boost your digital well-being

🔒 Privacy-focused design

Follow this guide and reclaim your time while staying connected to what truly matters. Your future self will thank you.

⭐ Give us stars in our eyes ⭐

[![Share](https://img.shields.io/badge/share-1877F2?logo=facebook&logoColor=white)](https://www.facebook.com/sharer/sharer.php?u=https://github.com/blastegit/Focusgram)
[![Share](https://img.shields.io/badge/share-0088CC?logo=telegram&logoColor=white)](https://t.me/share/url?url=https://github.com/blastegit/Focusgram&text=I%27ve+finally+got+my+life+back+under+control+on+Instagram.+Check+it+out+on+Github.)
[![Share](https://img.shields.io/badge/share-000000?logo=x&logoColor=white)](https://x.com/intent/post?text=I%27ve+finally+got+my+life+back+under+control+on+Instagram.+Check+it+out+on+Github%3A+https%3A%2F%2Fgithub.com%2Fblastegit%2FFocusgram)
[![Share](https://img.shields.io/badge/share-FF4500?logo=reddit&logoColor=white)](https://www.reddit.com/submit?title=I%27ve+finally+got+my+life+back+under+control+on+Instagram.+Check+it+out+on+Github%3A+https%3A%2F%2Fgithub.com%2Fblastegit%2FFocusgram)
[![Share](https://img.shields.io/badge/share-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/sharing/share-offsite/?url=https://github.com/blastegit/Focusgram)

## Table of Contents
- [🚨 Before you begin](#-before-you-begin)
- [📥 Step 1 : Downloading files](#-step-1--downloading-files)
- [🔧 Step 2 : Setting up](#-step-2--setting-up)
- [🗃️ Step 3 : Decompilation](#%EF%B8%8F-step-3--decompilation)
- [👷 Step 4 : Modifications](#-step-4--modifications)
- [🏗️ Step 5 : Recompilation](#%EF%B8%8F-step-5--recompilation)
- [✏️ Step 6 : Signature](#%EF%B8%8F-step-6--signature)
- [📱 Final step : Test](#-final-step--test)

## 🚨 Before you begin
> [!IMPORTANT]
> For legal reasons, it is not permitted to modify the Instagram [apk](https://en.wikipedia.org/wiki/Apk_(file_format) "This format is used to run an Android application") and distribute it freely. That's why this guide makes it easy to make these changes yourself.

Nevertheless, it is preferable to have some knowledge of computers to be able to follow and understand. All this so that you can adapt these changes to your own and possibly contribute to improving this repo. Ultimately, the idea is to automate the entire file modification process.

Allow around an hour to make all the changes to the guide. You will need a computer (Linux or Windows) with internet access and your mobile phone to install the application.

Finally, to make this guide easier to understand, simply point your mouse over the words underlined in blue and an tool-tip will appear.

## 📥 Step 1 : Downloading files

Let's start by downloading the necessery files : 
- the original Instagram APK [here](https://www.apkmirror.com/apk/instagram/instagram-instagram/#all_versions "APKMirror is a site giving access to the APK of a large number of Play Store applications.").
- the java jdk [here](https://www.oracle.com/java/technologies/downloads/ "Android command line tools require the java jdk to be installed in order to run.").
- and the Android command line tools only [here](https://developer.android.com/studio#command-line-tools-only "Here it is more practical to use the lightweight Android command-line tools instead of full Android Studio. This approach saves space and gives you more control over your development environment. This package includes sdkmanager, which allows you to selectively install additional SDK components as required. ").

Once downloaded, create a folder with the name of your choice and place it wherever you like. Then put in everything you've just downloaded.

## 🔧 Step 2 : Setting up

Start by running the java jdk installer.
Then create a folder called `android-utils`. Inside, create a new folder called `cmdline-tools` and create inside a new folder called `latest`.

The tree structure should look like this : `your-folder-name\android-utils\cmdline-tools\latest\` extract here the contents of the "commandlinetools..." compressed folder.

Open the bin folder and launch your command terminal here. Run these lines of code to download [2 additional packages](https://developer.android.com/tools/sdkmanager "Android SDK Platform-Tools provides essential command-line tools for communicating directly with the phone. You can use it to install the apk via your computer. As for Android SDK Build-Tools, it is a component of the Android SDK needed to create Android applications. It will be useful here for signing the apk.") :
```bash
sdkmanager "platform-tools" "build-tools;34.0.0"
```

## 🗃️ Step 3 : Decompilation

Now open the command terminal in the `apktool` folder and execute this command :

```bash
apktool d -r -f -o decompiled_instagram instagram_original.apk
```

## 👷 Step 4 : Modifications

Next, go to the folder you created containing the decompiled apk files and modify the lines you want.

## 🏗️ Step 5 : Recompilation

Now open the command terminal in the `apktool` folder and execute this command :
```bash
apktool b -r -f -c decompiled_instagram
```
The compiled APK file is located in the `dist` folder.

## ✏️ Step 6 : Signature
> [!NOTE]
> It is not necessary to repeat this key generation step for each APK signature. You can use the same signing key over and over again.

> All Android applications must be signed. To do this, we're going to start by generating our signature. Run this command in the command terminal :
> ```bash
> keytool -genkeypair -alias key0 -keyalg RSA -keysize 4096 -validity 10000 -keystore instagram_key.jks
> ```
> You will be asked to create a password that you will need to register somewhere. The rest of the information doesn't matter, you can leave it blank.

Finally, run this command, replacing your_password with the password you entered in the previous step :
```bash
echo your_password | apksigner sign --ks instagram_key.jks instagram.apk
```

## 📱 Final step : Test

Congratulations on finishing! Now all you have to do is transfer the modified Instagram apk to your phone and install it.

[Back to top](#top)
