# Compare CI\CD react native

I just create a black React Native 0.63.x Project and integrate CD/CI services

## Android builds

| CI | Status | 🚀 Speed | Env |
|---|---|---|---|
| [AppCenter](https://appcenter.ms/) | ![appcenter](https://build.appcenter.ms/v0.1/apps/160707ba-61e6-4bca-a26c-a9e6927ae70a/branches/main/badge) | 3 min 25 sec | macOS Catalina 10.15 |
| [Travis CI](https://docs.travis-ci.com/user/languages/android/) | [![Build Status](https://travis-ci.org/retyui/react-native-ci-cd-compare.svg?branch=main)](https://travis-ci.org/retyui/react-native-ci-cd-compare) | 3 min 29 sec | Ubuntu 14 |
| [Circle CI](https://circleci.com/circleci-react/) | [![CircleCI](https://circleci.com/gh/retyui/react-native-ci-cd-compare.svg?style=svg)](https://circleci.com/gh/retyui/react-native-ci-cd-compare) | 2 min 22 sec | Debian GNU/Linux 10 (buster) |
| [GitHub Actions](https://github.com/features/actions) | [![Build Android](https://github.com/retyui/react-native-ci-cd-compare/workflows/Build%20Android/badge.svg)](https://github.com/retyui/react-native-ci-cd-compare/actions/) | 3 min 43 sec | Ubuntu 18.04 |
| [Bitrise](https://devcenter.bitrise.io/getting-started/getting-started-with-react-native-apps/) | [![Build Status](https://app.bitrise.io/app/6763bd2429233088/status.svg?token=4XQvHAYUO0CNdNq683DupA)](https://app.bitrise.io/app/6763bd2429233088) | 3 min 16 sec | Ubuntu 16.04 |
| [Codemagic](https://codemagic.io/react-native-continuous-integration/) | n/a | 5 min 18 sec | macOS |
| [Buddy](https://buddy.works/docs/quickstart/react-native) | ![buddy pipeline](https://app.buddy.works/offantik/react-native-ci-cd-compare/pipelines/pipeline/288914/badge.svg?token=9bd6b8cc4ce0b2090330d0df656e566da6899dab5dc97c8312335ef9180cf9a2 "buddy pipeline") | 1 min 32 sec | linux | 
| [Nevercode](https://nevercode.io/blog/continuous-integration-for-react-native/) | ![Nevercode build status](https://app.nevercode.io/api/projects/8b869647-61e1-43bf-bc3e-c630f6099205/workflows/b81b5cb7-0ebe-43d1-92e0-81261d790fcc/status_badge.svg?branch=main) | 11 min 4 sec | ? |
| [appcircle](https://appcircle.io/blog/guide-to-automated-mobile-ci-cd-for-react-native-appcircle/) | n/a | 7 min 16 sec | ? | 
| [Gitlab CI/CD](https://docs.gitlab.com/ee/ci/) | [![GitLab CI status](https://gitlab.com/retyui/react-native-ci-cd-compare/badges/main/pipeline.svg)](https://gitlab.com/retyui/react-native-ci-cd-compare/-/jobs) | 7 min 44 sec | linux |


## iOS builds (TODO)
