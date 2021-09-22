# macpro-quickstart-serverless-support

<!-- Add badges later -->
<!-- ![Build](https://github.com/CMSgov/macpro-quickstart-serverless-support/workflows/Deploy/badge.svg?branch=master) [![Maintainability](https://api.codeclimate.com/v1/badges/1449ad929006f559756b/maintainability)](https://codeclimate.com/github/CMSgov/macpro-quickstart-serverless-support/maintainability) [![CodeQL](https://github.com/CMSgov/macpro-quickstart-serverless-support/actions/workflows/codeql-analysis.yml/badge.svg?branch=master)](https://github.com/CMSgov/macpro-quickstart-serverless-support/actions/workflows/codeql-analysis.yml) [![Dependabot](https://badgen.net/badge/Dependabot/enabled/green?icon=dependabot)](https://dependabot.com/) [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier) [![Test Coverage](https://api.codeclimate.com/v1/badges/1449ad929006f559756b/test_coverage)](https://codeclimate.com/github/CMSgov/macpro-quickstart-serverless-support/test_coverage) -->

A support repository for [macpro-quickstart-serverless](https://github.com/cmsgov/macpro-quickstart-serverless). This repository builds appliances and systems that support the [macpro-quickstart-serverless](https://github.com/cmsgov/macpro-quickstart-serverless) product, but are not directly related to the application and/or are not bound to the application code's lifecycle. Things of this nature are frequently centered on AWS account level maintenance and configuration.

## Release

Our product is promoted through branches. Master is merged to val to affect a master release, and val is merged to production to affect a production release. Please use the buttons below to promote/release code to higher environments.<br />

\*\* The quickstart only has one backing AWS account, so master/val/production all deploy to the same account. As such, there is no need for promotion in the support repository. The master branch will control the one and only AWS account. However, since forks of this project will likely support 3 AWS accounts - one for master/dev, one for val, and one for production - this blurb about release, the table below, and the pull request templates for val/production will all remain. We simply won't use val/production branches or tooling for this support repository, because we only have the one account.

| branch     | status                                                                                                                     | release                                                                                                                                                                                                                                                           |
| ---------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| master     | ![master](https://github.com/CMSgov/macpro-quickstart-serverless/workflows/Deploy/badge.svg?branch=master)                 | [![release to master](https://img.shields.io/badge/-Create%20PR-blue.svg)](https://github.com/CMSgov/macpro-quickstart-serverless-support/compare?quick_pull=1)                                                                                                   |
| val        | ![val](https://github.com/CMSgov/macpro-quickstart-serverless-support/workflows/Deploy/badge.svg?branch=val)               | [![release to val](https://img.shields.io/badge/-Create%20PR-blue.svg)](https://github.com/CMSgov/macpro-quickstart-serverless-support/compare/val...master?quick_pull=1&template=PULL_REQUEST_TEMPLATE.val.md&title=Release%20to%20Val)                          |
| production | ![production](https://github.com/CMSgov/macpro-quickstart-serverless-support/workflows/Deploy/badge.svg?branch=production) | [![release to production](https://img.shields.io/badge/-Create%20PR-blue.svg)](https://github.com/CMSgov/macpro-quickstart-serverless-support/compare/production...val?quick_pull=1&template=PULL_REQUEST_TEMPLATE.production.md&title=Release%20to%20Production) |

## Usage

See master build [here](https://github.com/CMSgov/macpro-quickstart-serverless-support/actions?query=branch%3Amaster)

This application is built and deployed via GitHub Actions.

Want to deploy from your Mac? Well, word of warning... this repository contains things and ideas that are typically bound to an account, not a stage. So if deploying a stage (mystagename for example), you may well step on another stage if you're both deploying to the same AWS account. If that's confusing, don't deploy from your mac.

- Create an AWS account
- Install/configure the AWS CLI
- brew install yarn
- source set.env.sh
- sh deploy.sh mystagename

## Requirements

Node - we enforce using a specific version of node, specified in the file `.nvmrc`. This version matches the Lambda runtime. We recommend managing node versions using [NVM](https://github.com/nvm-sh/nvm#installing-and-updating).

Serverless - Get help installing it here: [Serverless Getting Started page](https://www.serverless.com/framework/docs/providers/aws/guide/installation/)

Yarn - in order to install dependencies, you need to [install yarn](https://classic.yarnpkg.com/en/docs/install/).

AWS Account: You'll need an AWS account with appropriate IAM permissions (admin recommended) to deploy this app in Amazon.

## Dependencies

None.

## Examples

None.

## Contributing / To-Do

See current open [issues](https://github.com/CMSgov/macpro-quickstart-serverless-support/issues) or check out the [project board](https://github.com/CMSgov/macpro-quickstart-serverless-support/projects/1).

Please feel free to open new issues for defects or enhancements.

To contribute:

- Fork this repository
- Make changes in your fork
- Open a pull request targeting this repository

Pull requests are being accepted.

## License

[![License](https://img.shields.io/badge/License-CC0--1.0--Universal-blue.svg)](https://creativecommons.org/publicdomain/zero/1.0/legalcode)

See [LICENSE](LICENSE.md) for full details.

```text
As a work of the United States Government, this project is
in the public domain within the United States.

Additionally, we waive copyright and related rights in the
work worldwide through the CC0 1.0 Universal public domain dedication.
```

### Contributors

| [![Mike Dial][dial_avatar]][dial_homepage]<br/>[Mike Dial][dial_homepage] |
| ------------------------------------------------------------------------- |

[dial_homepage]: https://github.com/mdial89f
[dial_avatar]: https://avatars.githubusercontent.com/mdial89f?size=150
