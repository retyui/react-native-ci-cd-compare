# Compare CI\CD react native

I just create a black React Native 0.63.x Project and integrate CD/CI services

## Android builds

| CI | Status | Speed | Env |
|---|---|---|---|
| [AppCenter](https://appcenter.ms/) | ![appcenter](https://build.appcenter.ms/v0.1/apps/160707ba-61e6-4bca-a26c-a9e6927ae70a/branches/main/badge) | 3 min 25 sec | macOS Catalina 10.15 |
| [Travis CI](https://docs.travis-ci.com/user/languages/android/) | [![Build Status](https://travis-ci.org/retyui/react-native-ci-cd-compare.svg?branch=main)](https://travis-ci.org/retyui/react-native-ci-cd-compare) | 3 min 29 sec | Ubuntu 14 |
| [Circle CI](https://circleci.com/circleci-react/) | [![CircleCI](https://circleci.com/gh/retyui/react-native-ci-cd-compare.svg?style=svg)](https://circleci.com/gh/retyui/react-native-ci-cd-compare) | 2 min 22 sec | Docker, Debian GNU/Linux 10 (buster) |
| [GitHub Actions](https://github.com/features/actions) | [![Build Android](https://github.com/retyui/react-native-ci-cd-compare/workflows/Build%20Android/badge.svg)](https://github.com/retyui/react-native-ci-cd-compare/actions/) | 3 min 43 sec | Ubuntu 18.04 |
| [Bitrise](https://devcenter.bitrise.io/getting-started/getting-started-with-react-native-apps/) | [![Build Status](https://app.bitrise.io/app/6763bd2429233088/status.svg?token=4XQvHAYUO0CNdNq683DupA)](https://app.bitrise.io/app/6763bd2429233088) | 3 min 16 sec | Docker, Ubuntu 16.04 |


 
