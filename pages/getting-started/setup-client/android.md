---
layout: page
title: Android
permalink: /android
nav_order: 1
parent: Setup Client
grand_parent: Getting Started
---
# Android Instructions

Our Android application is available to download on Google Play.

[![Download at https://play.google.com/store/apps/details?id=com.geeksville.mesh](https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png)](https://play.google.com/store/apps/details?id=com.geeksville.mesh&referrer=utm_source%3Dgithub-homepage)

The application may not be found if your phone/Android version are too old. The minimum Android version is 5.0 (Lollipop 2014, first BLE support). However Android 6, Marshmallow 2015, is recommended as the Bluetooth is more stable.

On installing the Meshtastic app, load it and navigate to the settings page. Here you will ba able to select a nearby Meshtastic node, which you then need to pair with using your phone's operating system. Some nodes have buttons allowing you to change the page displayed on the nodes screen. If you double click this button, it will set the pairing code to `123456`

[![Messages page](img/messages_sm.png)](img/messages_sm.png) [![Nodes page](/assets/nodes_sm.png)](/assets/nodes.png) [![Channel page](/assets/channel_sm.png)](/assets/channel.png) [![Settings page](/assets/settings_sm.png)](/assets/settings.png) [![Debug page](/assets/debug_sm.png)](/assets/debug.png)

The app will ask you to give it permissions to access your location. This is needed for any app to use bluetooth, as the app is then able to scan the local area for bluetooth devices and, in theory, could triangulate your location based the devices it sees. If you give location permissions "only while using the app", the app will only be able to use bluetooth while it is open and visible to the user. This means if the screen is locked, or you are using another app, Meshtastic will not be able to use bluetooth, and will not be able to receive any messages from the node.

There is a beta program for the app, which will let you test the cutting edge changes, though this may come with extra bugs. You can join this via Google Play. It is recommended that you follow the [Meshtastic Discourse Alpha Testers](https://meshtastic.discourse.group/c/development/alpha-testers) channel if you decide to join this.

The app uses anonymous usage statistics and crash reports to allow us to catch problems with Meshtastic and fix them. You can disable this by unticking the checkbox on the settings page.

[![Settings page with statistics consent box highlighted](/assets/stats_consent_sm.png)](/assets/stats_consent.png)

For more information on using the Meshtastic Android App, please see the [software documentation page](/pages/software_docs/meshtastic-android.md).
  
  
  
Google Play and the Google Play logo are trademarks of Google LLC.
=======

