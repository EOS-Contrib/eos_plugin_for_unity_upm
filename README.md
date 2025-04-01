<div align="center"> <img src="/Documentation~/images/EOSPluginLogo.png" alt="EOS Plugin for Unity" /> </div>

<br />

<div align="left">
  
<a href="">[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)</a>
<a href="">![Unity](https://img.shields.io/badge/Unity-2021.3.16f1-blue)</a>
<img src="/tools/coverage/results/Report/badge_linecoverage.svg" />

</div>

# YOUVE BEEN SLIMED

I'm really struggling to understand the maintainers choice to close the github issues on play everyware's eos unity plugin. We had a major bug silently solved in a release, news to us! If only we had a place to publish an issue, and discuss, maybe we could ask a developer to add a fix to the release notes? Nevermind lets just use this hideous, proprietary forum instead. 🤢

I can at least try to post here in case anyone else is getting a timeout around the hour mark, Your auth is expiring, and the listener to the notification used to be a NOOP!

https://github.com/EOS-Contrib/eos_plugin_for_unity/commit/47bd72feb3bee79fd7daff6d74e0f02bdfe5d3a4 

https://eoshelp.epicgames.com/s/article/Why-am-I-being-logged-out-after-1-hour-of-EOS

LogEOSP2P(Warning): Attempted to get next received packet size with a LocalUserId that did not validate correctly. LocalUserId=[000...417] Result=[EOS_InvalidAuth]

![image](https://github.com/user-attachments/assets/5d4de389-c64f-48b4-a42a-47cba3d353e3)


# Overview

The EOS Plugin for Unity brings the free services from Epic that connect players across all platforms and all stores to Unity in an easy-to-use package. Find more information on what services Epic Online Services encompasses at [https://dev.epicgames.com/en-US/services](https://dev.epicgames.com/en-US/services) and read the developer documentation at [https://dev.epicgames.com/docs/epic-online-services](https://dev.epicgames.com/docs/epic-online-services).

This repository contains the source code for development of the [EOS Plugin for Unity (UPM Package)](https://github.com/EOS-Contrib/eos_plugin_for_unity_upm).

Out of the box, this project demonstrates (through a collection of sample scenes) each feature of the Epic Online Services SDK[^1]. The sample scenes (coupled with accompanying documentation) can be used to get an idea of how you can implement the online features you want in your game.

See [this](/com.playeveryware.eos/Documentation~/plugin_advantages.md) for a more complete overview of the advantages of using EOS with Unity.

[^1]: See the [supported-eos-sdk-features](#supported-eos-sdk-features) section for which SDK features specifically are demonstrated.

> [!NOTE]
> If you are **not** interested in the _development_ of the EOS Plugin for Unity project (and instead just want to get to using it) you can follow our guide on [Importing the Plugin Package](#importing-the-plugin-package) to start using the most recently released version of the EOS Plugin for Unity.

# Getting Started

## Prerequisites

* [An Epic Games account](https://www.epicgames.com/id/register) (_although, most [features](#exploring-supported-eos-features) do not require your users to have an Epic Games account, you must have one to configure your game in the Epic Games Developer Portal_).
* A product configured on the [Epic Games Developer Portal](https://dev.epicgames.com/portal/).
* A Unity project to integrate the plugin into.

> [!NOTE]
> Your system should also satisfy [Unity's system requirements](https://docs.unity3d.com/2021.3/Documentation/Manual/system-requirements.html) as well as the [EOS system requirements](https://dev.epicgames.com/docs/epic-online-services/eos-get-started/system-requirements)

# Supported EOS SDK Features

Below is a table summarizing the features the EOS Plugin for Unity supports. Most features are demonstrated via sample scenes provided in the project, and links to the guide for each corresponding sample scene are listed below. In some cases (such as Anti-Cheat) the feature is not able to be demonstrated well with a scene. In those cases, a link to information about how the plugin utilizes the feature is provided. In some cases (such as logging and overlay) the features are not implemented in any one scene specifically, but in all of them.

Use the "Select Demo Scene" dropdown in the application to select the sample scene that corresponds with the walkthrough. 

There are many EOS features that do not require your player to have an Epic Games account - such features are also marked accordingly in the following table.

| Feature | Status | Sample Scene Walkthrough | Requires Epic Games account |
| :-- | :-: | :-- | :-: |
|[Achievements](https://dev.epicgames.com/docs/game-services/achievements)                 | ✅ | ["Achievements"](/Documentation~/scene_walkthrough/achievements_walkthrough.md)                                                  |   |
|[Anti-Cheat](https://dev.epicgames.com/docs/game-services/anti-cheat)                     | ✅ | ["Information"](/Documentation~/easy_anticheat_configuration.md)                                                                             |  |
|[Authentication](https://dev.epicgames.com/docs/epic-account-services/auth-interface)     | ✅ | ["Auth & Friends"](/Documentation~/scene_walkthrough/auth&friends_walkthrough.md), [Information](/Documentation~/player_authentication.md) | ✔️ |
|[Custom Invites](https://dev.epicgames.com/docs/game-services/custom-invites-interface)   | ✅ | ["Custom Invites"](/Documentation~/scene_walkthrough/customInvites_walkthrough.md)                                               |  |
|[Connect Interface](https://dev.epicgames.com/docs/game-services/eos-connect-interface)   | ✅ | ["Auth & Friends"](/Documentation~/scene_walkthrough/auth&friends_walkthrough.md)                                                               |   |
|[Ecommerce](https://dev.epicgames.com/docs/epic-games-store/tech-features-config/ecom)[^2]    | ✅ | ["Store"](/Documentation~/scene_walkthrough/store_walkthrough.md), [Information](/com.playeveryware.eos/Documentation~/ecom.md)                                        | ✔️ |
|[Friends](https://dev.epicgames.com/docs/epic-account-services/eos-friends-interface)     | ✅ | ["Auth & Friends"](/Documentation~/scene_walkthrough/auth&friends_walkthrough.md)                                                               | ✔️ |
|[Leaderboards](https://dev.epicgames.com/docs/game-services/leaderboards)                 | ✅ | ["Leaderboards"](/Documentation~/scene_walkthrough/leaderboards_walkthrough.md)                                                               |   |
|[Lobbies](https://dev.epicgames.com/docs/game-services/lobbies)                             | ✅ | ["Lobbies"](/Documentation~/scene_walkthrough/lobbies_walkthrough.md)                                                                    |  |
|[Logging Interface](https://dev.epicgames.com/docs/game-services/eos-logging-interface)   | ✅ | NA                                                                                                                               |  |
|[Metrics](https://dev.epicgames.com/docs/game-services/eos-metrics-interface)             | ✅ | ["Metrics"](/Documentation~/scene_walkthrough/metrics_walkthrough.md)                                                                    |  |
|[Epic Games Store Mods](https://dev.epicgames.com/docs/epic-games-store/tech-features-config/mods)      | ❌ | NA                                                                                                                               | ✔️ |
|[NAT P2P](https://dev.epicgames.com/docs/game-services/p-2-p)                                               | ✅ | ["Peer 2 Peer"](/Documentation~/scene_walkthrough/P2P_walkthrough.md), ["P2P Netcode"](/com.playeveryware.eos/Documentation~/scene_walkthrough/P2P_netcode_walkthrough.md) |  |
|[Platform Interface](https://dev.epicgames.com/docs/game-services/eos-platform-interface)                   | ✅ | NA |   |
|[Player Data Storage](https://dev.epicgames.com/docs/game-services/player-data-storage)                     | ✅ | ["Player Data Storage"](/Documentation~/scene_walkthrough/player_data_storage_walkthrough.md)                                                        |   |
|[Presence](https://dev.epicgames.com/docs/epic-account-services/eos-presence-interface)                     | ✅ | ["Auth & Friends"](/Documentation~/scene_walkthrough/auth&friends_walkthrough.md)                                                               | ✔️ |
|[Progression Snapshot Interface](https://dev.epicgames.com/docs/epic-account-services/progression-snapshot) | ❌ | NA                                                                                                             | ✔️ |
|[Reports](https://dev.epicgames.com/docs/game-services/reports-interface)                 | ✅ | ["Player Reports & Sanctions"](/Documentation~/scene_walkthrough/player_reports_and_sanctions_walkthrough.md)                                               |  |
|[Sanctions](https://dev.epicgames.com/docs/game-services/sanctions-interface)             | ✅ | ["Player Reports & Sanctions"](/Documentation~/scene_walkthrough/player_reports_and_sanctions_walkthrough.md)                                               |  |
|[Sessions](https://dev.epicgames.com/docs/game-services/sessions)                         | ✅ | ["Sessions & Matchmaking"](/Documentation~/scene_walkthrough/sessions_and_matchmaking_walkthrough.md)                                                   |  |
|[Social Overlay](https://dev.epicgames.com/docs/epic-account-services/social-overlay-overview)[^2] / [UI Interface](https://dev.epicgames.com/docs/epic-account-services/eosui-interface) | ✅ | [Information](/Documentation~/overlay.md)        | ✔️ |
|[Stats](https://dev.epicgames.com/docs/game-services/eos-stats-interface)                 | ✅ | ["Leaderboards"](/Documentation~/scene_walkthrough/leaderboards_walkthrough.md)                                                               |  |
|[Title Storage](https://dev.epicgames.com/docs/game-services/title-storage)               | ✅ | ["Title Storage"](/Documentation~/scene_walkthrough/title_storage_walkthrough.md)                                                              |  |
|[User Info Interface](https://dev.epicgames.com/docs/epic-account-services/eos-user-info-interface) | ✅ | NA                                                                                                                     | ✔️ |
|[Voice with Lobbies](https://dev.epicgames.com/docs/game-services/voice#voicewithlobbies)   | ✅ | ["Lobbies"](/Documentation~/scene_walkthrough/lobbies_walkthrough.md), [Information](/Documentation~/enabling_voice.md)                            |  |
|[Voice Trusted Server](https://dev.epicgames.com/docs/game-services/voice#voicewithatrustedserverapplication) | ❌ | NA                                                                                                           |  |

Efforts will be made to add corresponding support to features as they are added to the Epic Online Services SDK. The table above reflects the features as of November 2023.

[^2]: Overlay features aren't supported yet on mobile devices as of EOSSDK 1.17. That includes Social Overlay and Store Overlay.

## Supported Platforms

We currently support the following platforms, details of each can be found on our [Supported Platforms](/Documentation~/supported_platforms.md) document:

* Windows
* Linux
* macOS
* Android
* iOS
* Nintendo Switch™
* Xbox One
* Xbox Series X|S
* PlayStation®4
* PlayStation®5

## Importing the Plugin Package

There are two options to install the package:
* Via a [UPM tarball](/Documentation~/add_plugin.md#adding-the-package-from-a-tarball) _(easiest to get started quickly)_.
* From a [git url](/Documentation~/add_plugin.md#adding-the-package-from-a-git-url) _(this method has the possible advantage of keeping the plugin up-to-date, if that's something that you would prefer)_.

Once imported into your project, be sure to [Configure the Plugin](/Documentation~/configure_plugin.md) to work with your game.

## Exploring Supported EOS Features

### [Supported Epic Online Services Features](/Documentation~/eos_features.md)
### [How to import sample scenes into your project](/Documentation~/samples.md)

# Support / Contact

EOS Plugin for Unity [documentation](/Documentation~) can be found here on GitHub.

For questions or issues related to integration or usage of Epic Online Services, Epic Games Developer Portal, or the EOS Plugin for Unity, please create a discussion on the [EOS Developer Community](https://eoshelp.epicgames.com).

Detailed descriptions and usage for EOS SDK Interfaces can be found on [Epic Developer Resources Documentation](https://dev.epicgames.com/docs/).

For issues of a confidential nature (including support using this plugin on console platforms), please create a private discussion on the [EOS Developer Community](https://eoshelp.epicgames.com).

# Contributor Notes

This is an open source project! We welcome you to make contributions. See our [Contributions](/Documentation~/contributions.md) document for more information.

# FAQ

To disable the plugin for specific platforms, see [this](/Documentation~/disable_plugin_per_platform.md) (which also explains why you might want to do this).

See [our guide](/Documentation~/command_line_export.md) on how to export the plugin from the command line. 

For issues of API Level compatibility, please read our [document](/Documentation~/dotnet_quirks.md) on .NET Quirks and Unity compatibility.

For more FAQs see [Frequently Asked Questions](/Documentation~/frequently_asked_questions.md).
