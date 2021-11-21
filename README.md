# Compare CI\CD react native

I just create a black React Native 0.63.x Project and integrate CD/CI services

Then I add a lot of native libraries to check how it cause build time


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Environment information ENVINFO.md](#environment-information-envinfomd)
- [Builds speed](#builds-speed)
- [Limitations of CI/CD services](#limitations-of-cicd-services)
- [Questions](#questions)
    - [1 Seems Microsoft Corporation of Good?](#1-seems-microsoft-corporation-of-good)
    - [2 But limitation for the public repositories?](#2-but-limitation-for-the-public-repositories)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Environment information [ENVINFO.md](ENVINFO.md) 

## Builds speed

 `time 1 / time 2` where

 - **time 1** - is a build of the [`main`](https://github.com/retyui/react-native-ci-cd-compare) branch with cache
 - **time 2** - is a first build of the [`with-poplar-react-native-libraries`](https://github.com/retyui/react-native-ci-cd-compare/pull/1) branch 


| CI | Status | Android | iOS |
|---|---|---|---|
| [ExpoAS](https://expo.dev/eas) | [n/a](https://expo.dev/accounts/retyui/projects/react-native-ci-cd-compare/builds) | 04m55s / 04m32s | soon... |
| [AppCenter](https://appcenter.ms/) | [![appcenter](https://build.appcenter.ms/v0.1/apps/160707ba-61e6-4bca-a26c-a9e6927ae70a/branches/main/badge)](https://appcenter.ms/users/offantik/apps/Android-CI-CD-test/build/branches/main) | 03m25s / 06m22s | 19m21s / 22s12s |
| [Travis CI](https://docs.travis-ci.com/user/languages/android/) | [![Build Status](https://travis-ci.org/retyui/react-native-ci-cd-compare.svg?branch=main)](https://travis-ci.org/retyui/react-native-ci-cd-compare) | 03m29s / 06m38s | 35m41s / 41m28s |
| [Circle CI](https://circleci.com/circleci-react/) | [![CircleCI](https://circleci.com/gh/retyui/react-native-ci-cd-compare.svg?style=svg)](https://circleci.com/gh/retyui/react-native-ci-cd-compare) | **02m22s / 04m19s** 🚀 | - |
| [GitHub Actions](https://github.com/features/actions) | [![Build Android](https://github.com/retyui/react-native-ci-cd-compare/workflows/Build%20Android/badge.svg)](https://github.com/retyui/react-native-ci-cd-compare/actions/) | **02m44s / 04m56s** 🚀 | 13m53s / 26m58s |
| [Bitrise](https://devcenter.bitrise.io/getting-started/getting-started-with-react-native-apps/) | [![Build Status](https://app.bitrise.io/app/6763bd2429233088/status.svg?token=4XQvHAYUO0CNdNq683DupA)](https://app.bitrise.io/app/6763bd2429233088) | 03m16s / 10m57s | 32m36s / 39m/43s |
| [Codemagic](https://codemagic.io/react-native-continuous-integration/) | [n/a](https://codemagic.io/app/5f9d65de4758a77daf27b4d4) | 05m18s / 06m58s | 19m55s / 30m27s |
| [Buddy](https://buddy.works/docs/quickstart/react-native) | [n/a](https://app.buddy.works/offantik/react-native-ci-cd-compare/pipelines) | **01m32s / 04m20s** 🚀 | - |
| [appcircle](https://appcircle.io/blog/guide-to-automated-mobile-ci-cd-for-react-native-appcircle/) | [n/a](https://my.appcircle.io/build/detail/f552b6ad-96fd-43fe-bffc-55f4268ee0d4) | 07m16s / 10m53s | 20m05s / 15m44s |
| [Gitlab CI/CD](https://docs.gitlab.com/ee/ci/) | [![GitLab CI status](https://gitlab.com/retyui/react-native-ci-cd-compare/badges/main/pipeline.svg)](https://gitlab.com/retyui/react-native-ci-cd-compare/-/jobs) | 07m44s / 12m47s | - |
| [Bitbucket Pipelines](https://bitbucket.org/product/ru/features/pipelines) | [n/a](https://bitbucket.org/retyui/react-native-ci-cd-compare/addon/pipelines/home) | **01m53s / 03m28s** 🚀 | - |
| [Azure DevOps](https://techcommunity.microsoft.com/t5/windows-dev-appconsult/using-azure-devops-to-create-a-ci-cd-pipeline-for-an-android/ba-p/1094422) | [![Build Status](https://dev.azure.com/retyui/react-native-ci-cd-compare/_apis/build/status/retyui.react-native-ci-cd-compare?branchName=refs%2Fpull%2F1%2Fmerge)](https://dev.azure.com/retyui/react-native-ci-cd-compare/_build/latest?definitionId=1&branchName=refs%2Fpull%2F1%2Fmerge) | 04m04s / 06m26s | 16m19s / 20m20s |
| [Semaphore CI](https://semaphoreci.com/) | [![Build Status](https://retyui.semaphoreci.com/badges/iOS-react-native-ci-cd-compare/branches/main.svg)](https://retyui.semaphoreci.com/projects/react-native-ci-cd-compare) | **02m42s / 03m33s** 🚀 | 14m10s / 29m09s |

## Limitations of CI/CD services

- [App Center Pricing](https://docs.microsoft.com/en-us/appcenter/general/pricing#the-free-tier) **1 build** pipeline per organization or user account, **240 build minutes** per **month**, and up to 30 minutes per build

- [Limitations of Bitbucket Pipelines](https://support.atlassian.com/bitbucket-cloud/docs/limitations-of-bitbucket-pipelines/) build minutes: **50 min/month**, large file storage: 1 GB total, overage protection - not included

- [Gitlab shared runners](https://docs.gitlab.com/ee/user/gitlab_com/#shared-runners) **free** to use for **public open source projects** and limited to **2000 CI minutes per month** per group for **private projects**

- [CircleCI](https://circleci.com/pricing/) **2,500 free credits/week**, run 1 job at a time, build on Linux and Windows

- [Github Actions](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-billing-and-payments-on-github/about-billing-for-github-actions#about-billing-for-github-actions) GitHub Actions usage is **free for public repositories** 🚀 and self-hosted runners

- [Azure DevOps](https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/) 1 Microsoft-hosted job with **1,800 minutes per month** for CI/CD and 1 self-hosted job with unlimited minutes per month

- [Travis CI](https://travis-ci.com/account/plan?billingStep=1)  provide [5 concurrent builds](https://twitter.com/travisci/status/651856122559774722) for open source builds, 10000 Credits, Unlimited unique users, Private & Open-Source repos, Linux, Windows, macOS

- [Bitrise](https://www.bitrise.io/pricing) 1 concurrency, 200 builds / month, timeout at 30 min / build

- [Buddy](https://buddy.works/pricing) **120** pipeline runs / month, cache storage - 512 MB, RAM & vCPU - 1 GB RAM & 2 vCPU, concurrent pipelines - 1, parallel actions - 1, 

- [Codemagic](https://codemagic.io/pricing/) **500** macOS standard VM **minutes every month**, 1 build at a time

- [appcircle](https://appcircle.io/pricing/) 1 Concurrent Build, 20 minutes max build time per build, 25 Builds per Month

- [Semaphore CI](https://semaphoreci.com/blog/2014/08/14/semaphore-gets-free.html) becomes free for open source **(unlimited testing and deployment of open source projects)**

---


## Questions

#### 1 Seems Microsoft Corporation of Good?

Azure devops, GitHub Actions, Appcenter, Yes)))0

#### 2 But limitation for the public repositories? 

Pffff... 

Nobody limiting you!

How about clone a private repo inside your pipeline of the public repo!
