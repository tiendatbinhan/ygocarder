> **This is a fork of [lauqerm/ygocarder](https://github.com/lauqerm/ygocarder) with self-hosted support.**

If you are looking for V1, please visit [ygocarder-v1 repo](https://github.com/lauqerm/ygocarder-v1).

## YGO Carder

* Template provided by: [Grezar](https://www.deviantart.com/grezar), [9558able](https://www.deviantart.com/9558able), [SlackerMagician](https://www.deviantart.com/slackermagician) and [icycatelf](https://www.deviantart.com/icycatelf).
* GUI by [@lauqerm](https://github.com/lauqerm)
* Self-hosted features by [@tiendatbinhan](https://github.com/tiendatbinhan)

### What's different in this fork?

This fork extends the original app with **self-hosted support**, allowing you to deploy YGO Carder on your own infrastructure with full control over your data and assets.

### Thank you

My deepest gratitude goes to [@lauqerm](https://github.com/lauqerm) for creating and maintaining the original YGO Carder.

Once again, big thanks to [Grezar](https://www.deviantart.com/grezar), [9558able](https://www.deviantart.com/9558able), [SlackerMagician](https://www.deviantart.com/slackermagician) and [icycatelf](https://www.deviantart.com/icycatelf), for allowing the use of their templates. Their hard work is the reason this project is possible in the first place.

### My goal

Create an easy-to-use GUI to make Yu-Gi-Oh! cards, for anyone who cannot afford Photoshop or the skill needed to use it.

Even though the app supports conversion between cards made by this app and cards made by other vendors such as YGOPro, Dueling Nexus and Neo Card Maker, there is no affiliation with them.

### What does it provide?

To put it more correctly: what advantage does this app offer over a dozen Yu-Gi-Oh! card-maker apps out there? In short, there are just 2 things:
* The UI - Most of the changes can be made with just a single click or keystroke. Other apps will need you to constantly cycle through multiple dropdowns.
* Automatic text compression - You may notice modern Yu-Gi-Oh! cards try to compress words to avoid using smaller font sizes. YGO Carder can replicate that behavior rather automatically, while other apps will just simply keep reducing font size and adding new lines, or provide you with a manual slider without solving any edge cases.

Other advantages such as foils and additional card frames come from the template of use, so again, big shout out to template owners who put their time and effort into creating them.

### What does it NOT provide?

The app of course has multiple shortcomings, many of them are by design, while others may become future plans:
* No template for Rush Duel - Template for Rush Duel is already available, so maybe it will be revisited in the future by [@lauqerm](https://github.com/lauqerm).
* No "ultra" card size - While some apps may offer 4K resolution for their card, this app does not. While the current card resolution is decently enough, you can always seek for professional up-scale method. Up-scaling is a resource-intense operation that requires a powerful server to do, while most of the user devices will hang for a good few minutes trying to run it, so there is no out for this problem in the near future.
* No remote saving - This app currently does not have a dedicated server for such a feature, but thanks to that it can serve the app for a long time completely free without the need for any financial support. The app only provides very simple card information export and import, and your card art should come from online links. However, if you self-host this service, you can also self-host an image server yourself for full control over your assets.

### Can I use your source code in my site?

Yes, you are free to fork it and do whatever, just don't claim it is yours. Also, it will be extra thankful if you keep the credit for [@lauqerm](https://github.com/lauqerm) and the template makers.

If you want to modify the app's assets, better contact template makers and ask for permission yourself.

You may also contact [@lauqerm](https://github.com/lauqerm) through [Reddit](https://www.reddit.com/user/lauqerm/).

### How to run

#### Local development

##### Preparation

If you want to deploy the app elsewhere, you will need to prepare your own `.env.production` file, which the following attributes:
```env
### Template file used for batch import function
VITE_TEMPLATE_FILE="https://drive.google.com/file/d/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/view?usp=sharing"
### Sentry DSN Link if you want to use the feedback function
VITE_SENTRY_DSN="https://32e20d849c5724b2e63eab9d0a57c165@o4508424630697984.ingest.us.sentry.io/xxxxxxxxxxxxxxxx"
```
It's okay to leave the file empty, it will simply disable features related to them.

Prerequisites:
* [Node](https://nodejs.org/) version: 22.12+ (I'm using v24.15.0)
* Package manager such as [yarn](https://yarnpkg.com/) (my recommendation) or [npm](https://www.npmjs.com/).

##### Start working

If you are already familiar with a React app, you can run the app with the following steps:
* Install all the package: `yarn install` or `npm install`
* Run the app: `yarn start` or `npm start`
* Build the app: `yarn build` or `npm run build`

#### Using Docker

Check [README.Docker.md](README.Docker.md)
