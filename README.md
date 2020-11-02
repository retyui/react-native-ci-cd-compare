# Compare CI\CD react native

I just create a black React Native 0.63.x Project and integrate CD/CI services (see column: Speed #1)

Then I add a lot of native libraries to check how it cause build time (see column: [Speed #2](https://github.com/retyui/react-native-ci-cd-compare/pull/1))  


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Environment information ENVINFO.md](#environment-information-envinfomd)
- [Builds speed](#builds-speed)
- [Limitations of CI/CD services](#limitations-of-cicd-services)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Environment information [ENVINFO.md](ENVINFO.md) 

## Builds speed

| CI | Status | Android | iOS |
|---|---|---|---|
| [AppCenter](https://appcenter.ms/) | [![appcenter](https://build.appcenter.ms/v0.1/apps/160707ba-61e6-4bca-a26c-a9e6927ae70a/branches/main/badge)](https://appcenter.ms/users/offantik/apps/Android-CI-CD-test/build/branches/main) | 3m25s / 6m22s | 19m21s / 22s12s |
| [Travis CI](https://docs.travis-ci.com/user/languages/android/) | [![Build Status](https://travis-ci.org/retyui/react-native-ci-cd-compare.svg?branch=main)](https://travis-ci.org/retyui/react-native-ci-cd-compare) | 3m29s / 6m38s | 35m41s / |
| [Circle CI](https://circleci.com/circleci-react/) | [![CircleCI](https://circleci.com/gh/retyui/react-native-ci-cd-compare.svg?style=svg)](https://circleci.com/gh/retyui/react-native-ci-cd-compare) | 2m22s / 4m19s 🚀 | - |
| [GitHub Actions](https://github.com/features/actions) | [![Build Android](https://github.com/retyui/react-native-ci-cd-compare/workflows/Build%20Android/badge.svg)](https://github.com/retyui/react-native-ci-cd-compare/actions/) | 2m44s / 4m56s 🚀 | 13m53s / |
| [Bitrise](https://devcenter.bitrise.io/getting-started/getting-started-with-react-native-apps/) | [![Build Status](https://app.bitrise.io/app/6763bd2429233088/status.svg?token=4XQvHAYUO0CNdNq683DupA)](https://app.bitrise.io/app/6763bd2429233088) | 3m16s / 10m57s | |
| [Codemagic](https://codemagic.io/react-native-continuous-integration/) | [n/a](https://codemagic.io/app/5f9d65de4758a77daf27b4d4) | 5m18s / 6m58s | 19m55s / |
| [Buddy](https://buddy.works/docs/quickstart/react-native) | [![buddy pipeline](https://app.buddy.works/offantik/react-native-ci-cd-compare/pipelines/pipeline/288914/badge.svg?token=9bd6b8cc4ce0b2090330d0df656e566da6899dab5dc97c8312335ef9180cf9a2 "buddy pipeline")](https://app.buddy.works/offantik/react-native-ci-cd-compare/pipelines) | 1m32s / 4m20s 🚀 | - |
| [Nevercode](https://nevercode.io/blog/continuous-integration-for-react-native/) | [![Nevercode build status](https://app.nevercode.io/api/projects/8b869647-61e1-43bf-bc3e-c630f6099205/workflows/b81b5cb7-0ebe-43d1-92e0-81261d790fcc/status_badge.svg?branch=main)](https://app.nevercode.io/#/project/8b869647-61e1-43bf-bc3e-c630f6099205) | 11m4s / 13m22s | |
| [appcircle](https://appcircle.io/blog/guide-to-automated-mobile-ci-cd-for-react-native-appcircle/) | [n/a](https://my.appcircle.io/build/detail/f552b6ad-96fd-43fe-bffc-55f4268ee0d4) | 7m16s / 10m53s | |
| [Gitlab CI/CD](https://docs.gitlab.com/ee/ci/) | [![GitLab CI status](https://gitlab.com/retyui/react-native-ci-cd-compare/badges/main/pipeline.svg)](https://gitlab.com/retyui/react-native-ci-cd-compare/-/jobs) | 7m44s / 12m47s | - |
| [Bitbucket Pipelines](https://bitbucket.org/product/ru/features/pipelines) | [n/a](https://bitbucket.org/retyui/react-native-ci-cd-compare/addon/pipelines/home) | 1m53s / 3m28s 🚀 | - |
| [Azure DevOps](https://techcommunity.microsoft.com/t5/windows-dev-appconsult/using-azure-devops-to-create-a-ci-cd-pipeline-for-an-android/ba-p/1094422) | [![Build Status](https://dev.azure.com/retyui/react-native-ci-cd-compare/_apis/build/status/retyui.react-native-ci-cd-compare?branchName=refs%2Fpull%2F1%2Fmerge)](https://dev.azure.com/retyui/react-native-ci-cd-compare/_build/latest?definitionId=1&branchName=refs%2Fpull%2F1%2Fmerge) | 4m4s / 6m26s | 16m19s / |


## Limitations of CI/CD services

- [App Center Pricing](https://docs.microsoft.com/en-us/appcenter/general/pricing#the-free-tier) **1 build** pipeline per organization or user account, **240 build minutes** per **month**, and up to 30 minutes per build

- [Limitations of Bitbucket Pipelines](https://support.atlassian.com/bitbucket-cloud/docs/limitations-of-bitbucket-pipelines/) build minutes: **50 min/month**, large file storage: 1 GB total, overage protection - not included

- [Gitlab shared runners](https://docs.gitlab.com/ee/user/gitlab_com/#shared-runners) **free** to use for **public open source projects** and limited to **2000 CI minutes per month** per group for **private projects**

- [CircleCI](https://circleci.com/pricing/) **2,500 free credits/week**, run 1 job at a time, build on Linux and Windows

- [Github Actions](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-billing-and-payments-on-github/about-billing-for-github-actions#about-billing-for-github-actions) GitHub Actions usage is **free for public repositories** and self-hosted runners

- [Azure DevOps](https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/) 1 Microsoft-hosted job with **1,800 minutes per month** for CI/CD and 1 self-hosted job with unlimited minutes per month

- [Travis CI](https://travis-ci.com/account/plan?billingStep=1)  provide [5 concurrent builds](https://twitter.com/travisci/status/651856122559774722) for open source builds, 10000 Credits, Unlimited unique users, Private & Open-Source repos, Linux, Windows, macOS


- [Bitrise](https://www.bitrise.io/pricing) 1 concurrency, 200 builds / month, timeout at 30 min / build

- [Buddy](https://buddy.works/pricing) **120** pipeline runs / month, cache storage - 512 MB, RAM & vCPU - 1 GB RAM & 2 vCPU, concurrent pipelines - 1, parallel actions - 1, 

- [Nevercode](https://nevercode.io/pricing/) is transitioning to Codemagic January 1, 2021

- [Codemagic](https://codemagic.io/pricing/) **500** macOS standard VM **minutes every month**, 1 build at a time

- [appcircle](https://appcircle.io/pricing/) 1 Concurrent Build, 25 minutes max build time per build
