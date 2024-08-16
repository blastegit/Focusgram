<a name="haut"></a>
# 🎯Focusgram
![Dernier commit GitHub](https://img.shields.io/github/last-commit/blastegit/Focusgram?label=dernier%20d%C3%A9p%C3%B4t)
![Version Instagram supportée supérieur à 300](https://img.shields.io/badge/version_Instagram_supportée-<300-blue)

## Langues : [![Static Badge](https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7-anglais-white?style=plastic)](https://github.com/blastegit/Focusgram/blob/main/README.md)

Fatigué du défilement sans fin et des Reels qui font perdre du temps ? Découvrez l'Instagram d'antan. Notre application élimine les distractions, vous laissant avec un flux pure et concentré de photos époustouflantes des personnes qui vous intéressent.

📸 Du contenu purement photographique (avec seulement les Reels que l'on vous envoie)

⏱️ Économisez des heures de défilement inutile

🧘 Améliorez votre bien-être numérique

🔒 Conception axée sur la protection de la vie privée

Suivez ce guide et récupérez votre temps tout en restant connecté à ce qui compte vraiment. Votre futur vous remerciera.

⭐ Mettez-nous des étoiles pleins les yeux ⭐

[![Partager sur Facebook](https://img.shields.io/badge/partager-1877F2?logo=facebook&logoColor=white)](https://www.facebook.com/sharer/sharer.php?u=https://github.com/blastegit/Focusgram)
[![Partager sur Telegram](https://img.shields.io/badge/partager-0088CC?logo=telegram&logoColor=white)](https://t.me/share/url?url=https://github.com/blastegit/Focusgram&text=J%27ai+finallement+ma+vie+sous+contrôle+sur+Instagram.+Regardez+ce+dépôt+Github.)
[![Partager sur X](https://img.shields.io/badge/partager-000000?logo=x&logoColor=white)](https://x.com/intent/post?text=J%27ai+finallement+ma+vie+sous+contrôle+sur+Instagram.+Regardez+ce+dépôt+Github+%3A+https%3A%2F%2Fgithub.com%2Fblastegit%2FFocusgram)
[![Partager sur Reddit](https://img.shields.io/badge/partager-FF4500?logo=reddit&logoColor=white)](https://www.reddit.com/submit?title=J%27ai+finallement+ma+vie+sous+contrôle+sur+Instagram.+Regardez+ce+dépôt+Github+%3A+https%3A%2F%2Fgithub.com%2Fblastegit%2FFocusgram)
[![Partager sur LinkedIn](https://img.shields.io/badge/partager-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/sharing/share-offsite/?url=https://github.com/blastegit/Focusgram)

## Table des matières
- [🚨 Avant de commencer](#-avant-de-commencer)
- [📥 Etape 1 : Télécharger les fichiers](#-etape-1--télécharger-les-fichiers)
- [🔧 Etape 2 : Paramètrage](#-etape-2--paramètrage)
- [🗃️ Etape 3 : Décompilation](#%EF%B8%8F-etape-3--décompilation)
- [👷 Etape 4 : Modifications](#-etape-4--modifications)
- [🏗️ Etape 5 : Recompilation](#%EF%B8%8F-etape-5--recompilation)
- [✏️ Etape 6 : Signature](#%EF%B8%8F-etape-6--signature)
- [📱 Etape finale : Test](#-etape-finale--test)

## 🚨 Avant de commencer
> [!IMPORTANT]
> Pour des raisons juridiques, il n'est pas permis de modifier l'[APK](https://en.wikipedia.org/wiki/Apk_(file_format) "C'est le fichier utilisé pour exécuter une application Android.") d'Instagram et de le distribuer librement. C'est pourquoi ce guide vous permet d'effectuer facilement ces modifications vous-même.

Néanmoins, il est préférable d'avoir quelques connaissances en informatique pour pouvoir suivre et comprendre. Tout ceci afin que vous puissiez adapter ces changements aux vôtres et éventuellement contribuer à l'amélioration de ce dépôt Github. Au final, l'idée est d'automatiser l'ensemble du processus de modification des fichiers.

Comptez une bonne heure pour effectuer toutes les modifications de ce guide. Vous aurez besoin d'un ordinateur (Linux ou Windows) avec un accès internet et de votre téléphone portable Android pour installer l'application.

Enfin, pour faciliter la compréhension de ce guide, il vous suffit de passer votre souris sur les mots soulignés en bleu et une info-bulle apparaîtra.

## 📥 Etape 1 : Télécharger les fichiers

Commençons par télécharger les fichiers nécessaires : 
- l'APK original d'Instagram [ici](https://www.apkmirror.com/apk/instagram/instagram-instagram/#all_versions "APKMirror est un site donnant accès à l'APK d'un grand nombre d'applications du Play Store.")
- le jdk java [ici](https://www.oracle.com/java/technologies/downloads/ "Les outils de ligne de commande Android nécessitent l'installation du jdk java pour fonctionner.")
- et les outils de ligne de commande Android uniquement [ici](https://developer.android.com/studio#command-line-tools-only "Ici, il est plus pratique d'utiliser les outils de ligne de commande Android légers au lieu d'Android Studio complet. Cette approche permet d'économiser de l'espace et vous donne plus de contrôle sur votre environnement de développement. Ce paquetage contient sdkmanager, qui vous permet d'installer sélectivement des composants SDK supplémentaires selon vos besoins.").

Une fois téléchargé, créez un dossier avec le nom de votre choix et placez-le à l'endroit souhaité. Mettez-y ensuite tout ce que vous venez de télécharger dedans.

## 🔧 Etape 2 : Paramètrage

Commencez par lancer le programme d'installation de java jdk. Ensuite, créez un dossier appelé `android-utils`. A l'intérieur, créez un nouveau dossier appelé `cmdline-tools` et créez à l'intérieur un nouveau dossier appelé `latest`.

L'arborescence devrait ressembler à ceci : `votre-nom-de-dossier\android-utils\cmdline-tools\latest\` extrayez ici le contenu du dossier compressé "commandlinetools...".

Ouvrez le dossier bin et lancez votre terminal de commande ici. Exécutez ces lignes de code pour télécharger [2 paquets supplémentaires](https://developer.android.com/tools/sdkmanager "Android SDK Platform-Tools fournit des outils de ligne de commande essentiels pour communiquer directement avec le téléphone. Vous pouvez l'utiliser pour installer l'apk via votre ordinateur. Quant à Android SDK Build-Tools, il s'agit d'un composant du SDK Android nécessaire à la création d'applications Android. Il sera utile ici pour signer l'APK.") :
```bash
sdkmanager "platform-tools" "build-tools;34.0.0"
```

## 🗃️ Etape 3 : Décompilation

Ouvrez maintenant le terminal de commande dans le dossier `apktool` et exécutez cette commande :
```bash
apktool d -r -f -o instagram_decompile instagram_original.apk
```

## 👷 Etape 4 : Modifications

Ensuite, allez dans le dossier que vous avez créé contenant les fichiers apk décompilés et modifiez les lignes que vous souhaitez.

## 🏗️ Etape 5 : Recompilation

Maintenant, ouvrez le terminal de commande dans le dossier `apktool` et exécutez cette commande :
```bash
apktool b -r -f -c instagram_decompile
```
Le fichier APK compilé est situé dans le dossier `dist`.

## ✏️ Etape 6 : Signature
> [!NOTE]
> Il n'est pas nécessaire de répéter cette étape de génération de clé pour chaque signature d'APK. Vous pouvez utiliser la même clé de signature de façon illimité.

> Toutes les applications Android doivent être signées. Pour ce faire, nous allons commencer par générer notre signature. Exécutez cette commande dans le terminal de commande :
> ```bash
> keytool -genkeypair -alias key0 -keyalg RSA -keysize 4096 -validity 10000 -keystore cle_instagram.jks
> ```
>
> Il vous sera demandé de créer un mot de passe que vous devez sauvegarder quelque part. Le reste des informations demandées n'a pas d'importance, vous pouvez les laisser vides.

Enfin, exécutez cette commande, en remplaçant votre_mot_de_passe par le mot de passe que vous avez saisi à l'étape précédente :
```bash
echo votre_mot_de_passe | apksigner sign --ks cle_instagram.jks instagram.apk
```

## 📱 Etape finale : Test

Félicitations pour avoir terminé ! Il ne vous reste plus qu'à transférer l'apk Instagram modifiée sur votre téléphone et à l'installer.

[Retour en haut](#haut)
