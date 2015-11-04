---
id: upgrading
title: Upgrading
layout: docs
category: Guides
permalink: docs/upgrading.html
next: native-modules-ios
---

Upgrading to new versions of React Native will give you access to more APIs, views, developer tools
and other goodies. Because React Native projects are essentially made up of an Android project, an
iOS project and a JavaScript project, all combined under an npm package, upgrading can be rather
tricky. But we try to make it easy for you. Here's what you need to do to upgrade from an older
version of React Native:

## 1. Upgrade the `react-native` dependency

Note the latest version of the `react-native` npm package from here:

* https://www.npmjs.com/package/react-native

Open your `package.json` file and update the version of `react-native` under `dependencies` to the
latest version. Now, in a terminal run:

```sh
$ npm install
```

## 2. Upgrade your project templates

> NOTE: This feature is available in version 0.14.0-rc and higher.

The new npm package will likely contain updates to the files that are normally generated when you
run `react-native init`, like the iOS and the Android sub-projects. To get these latest changes,
run this in a terminal:

```sh
$ react-native upgrade
```

This will check your files against the latest template and perform the following:

* If there is a new file in the template, it is simply created.
* If a file in the template is identical to your file, it is skipped.
* If a file is different in your project than the template, you will be prompted; you have options
  to view a diff between your file and the template file, keep your file or overwrite it with the
  template version. If you are unsure, press `h` to get a list of possible commands.