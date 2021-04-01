---
description: The resources can get you started developing with Skynet.
---

# Developing on Skynet

## Why Develop on Skynet?

Skynet offers several advantages to developers:

* Developers don't have to manage or pay for any infrastructure
* Once deployed, applications are independent and need no further caretaking by the developer
* Application data is user-controlled, available across applications, so your application can utilize pre-existing user information instead of starting from scratch.
* You'll be able to monetize your application without the use of advertising

{% hint style="danger" %}
Our proper "Developer's Guide" is still being worked on. In the meantime, here is a quick overview along with links to various resources. If you haven't already, read through the [Getting Started](../getting-started/using-skynet.md) section to better understand how Skynet works.
{% endhint %}

## Getting Started

To get started, create a folder with an `index.html` file in it and all css and javascript linked with relative paths. Visit [http://siasky.net/](http://siasky.net/), select "Do you want to upload an entire directory?" then upload the directory.

This works for static sites, along with client-side rendered Single Page Applications. Check out our [Skynet Workshop](https://github.com/SkynetHQ/skynet-workshop) for a more in-depth walkthrough.

{% hint style="info" %}
Using `create-react-app`? Add `"homepage": "."` to your `package.json` before you build, then just upload your build folder!
{% endhint %}

## Tools and Resources

Official Documentation and SDKs

* [**Skynet SDK Docs**](https://siasky.net/docs) – Documentation for all the SDKs
* **SDKs** –
  * Browser JS: [skynet-js](https://github.com/NebulousLabs/skynet-js)
  * NodeJS: [nodejs-skynet](https://github.com/SkynetHQ/nodejs-skynet)\*
  * Python: [python-skynet](https://github.com/SkynetHQ/python-skynet)\*
  * GoLang: [go-skynet](https://github.com/SkynetHQ/go-skynet)\*
  * CLI: [skynet-cli](https://github.com/SkynetHQ/skynet-cli)\*

{% hint style="warning" %}
SDKs marked with \* above are not fully implemented – only `skynet-js` implements SkyDB and is our recommended SDK for the time being.
{% endhint %}

### Guides and Walkthroughs

* [**Skynet Workshop**](https://github.com/SkynetHQ/skynet-workshop) – A workshop that builds on skills showing various parts of developing with Skynet. Watch Daniel [walk through the workshop](https://www.youtube.com/watch?v=3VlQQDPkTPk) for the ENCODE Hackathon or visit the [companion skapp](https://encode-skynet.hns.siasky.net/) which includes code samples and interactive widgets.
* [**Automated Deployments on Skynet**](https://blog.sia.tech/automated-deployments-on-skynet-28d2f32f6ca1) – Blog post walking through how to use Github for automated build uploads and HNS updates
* [**SkyDB Example: A Note-to-Self App**](https://blog.sia.tech/skydb-example-a-note-to-self-app-ccd4e7ba31ba) – A tutorial showing SkyDB usage with React. [Code here](https://github.com/kwypchlo/skydb-example).

### Deployment Tooling

* [**skynet-cli**](https://github.com/SkynetHQ/skynet-cli) – Great tool for uploading directories from the command line.
* [**Deploy to Skynet Github Action**](https://github.com/kwypchlo/deploy-to-skynet-action) – Github action that deploys a directory to Skynet and comments on pull request with a skylink url. See [Automated deployments on Skynet](https://blog.sia.tech/automated-deployments-on-skynet-28d2f32f6ca1) for using with Handshake.
* [**Upload2Cloud**](https://github.com/cycleworm/Upload2Cloud) – Windows Explorer integration for sending files and directories to Skynet. Python script available.
* [**Vue CLI Deployment Plugin**](https://github.com/Delivator/vue-cli-plugin-skynet) – Vue UI based tool for site upload with auto Namebase/Handshake updates
* [**SkyDeploy**](https://github.com/redsolver/skydeploy) – Command-Line Tool for easily deploying web apps on Skynet and setting the skyns records to point your HNS domain to the new version

### Community SDKs & Initiatives

* [**py-skydb**](https://github.com/PowerLoom/py-skydb) – Python Wrapper that you can use to interact with SkyDB portals
* [**Skynet SDK for Dart**](https://github.com/redsolver/skynet) – Use Sia Skynet and SkyDB in your Dart and Flutter projects
* [**Skystandards**](https://github.com/SkynetHQ/skystandards) – a proposal for data standards to be adopted in Skynet applications in such a way that users can share and use their data in different Skynet apps

## Is Skynet the right platform for my website/app?

If your website is structured to be client-side, then hosting it on Skynet is straightforward. If not, it is likely your website will need to reconsider some parts of its architecture to be fully-functional on Skynet.

So, if you use Create React App or Gatsby, deploying to Skynet is as easy as uploading the folder of your production build. If you use a server-side backend like ExpressJS or a CMS like Django or Wordpress, these parts of your website cannot be run on Skynet. You can, however, host your html, css and javascript code on Skynet with your server API elsewhere, but that's not really a decentralized application and isn't what we'd call a skapp.

If you're considering developing on Skynet, take a look at the [Getting Started](../getting-started/using-skynet.md) section to learn some basics or reach out on our [Discord server](http://discord.gg/sia) in the `#skynet` or `#app-dev` channels.

## Best Practices

Many of these will be incorporated into our Developer Guide, but in the meantime, some things to keep in mind:

* For skapps, it's best to use and link URLs that are a subdomain of the portal domain. That means either using an HNS name as a subdomain like `<skapp>.hns.siasky.net` or a [Base32-encoded subdomain](../key-concepts/skylinks.md#base32-subdomains). 
* If linking to code on Skynet, you should use immutable skylinks when possible so that later updates don't risk breaking your code.
* To be a proper "skapp," your application shouldn't be relying on external, centralized services to function. This means external requests to APIs for on-network storage or computation that would make your skapp's data not interoperable with other skapps.
* Do not hardcode a specific portal domain into your code! This can be helpful for local development, but be sure to remove this before deploying to Skynet, so that the code isn't forced to use a portal other than the one it is being served from.

