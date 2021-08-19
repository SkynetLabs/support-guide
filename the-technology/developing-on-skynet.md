---
description: >-
  Developing on Skynet has plenty of advantages - learn how to do it on our
  decentralized app.
---

# Developing on Skynet

## Developing on Skynet

Skynet offers several advantages to developers:

* Developers don't have to manage or pay for any infrastructure
* Once deployed, applications are independent and need no further caretaking by the developer
* Application data is user-controlled and available across applications, so your application can utilize pre-existing user information instead of starting from scratch.
* You'll be able to monetize your application without the use of advertising

{% hint style="info" %}
Please see our new [Skynet Developer Guide](https://docs.siasky.net/) linked at the top of this page and available at [https://docs.siasky.net/](https://docs.siasky.net). If you haven't already, read through the [Getting Started](../getting-started/using-skynet-skapps.md) section to better understand how Skynet works.
{% endhint %}

{% embed url="https://docs.siasky.net/" caption="Skynet Developer Guide" %}

## Getting Started

To get started, create a folder with an `index.html` file in it and all css and javascript linked with relative paths. Visit [http://siasky.net/](http://siasky.net/), select "Do you want to upload an entire directory?" then upload the directory.

This works for static sites, along with client-side rendered Single Page Applications. Check out our [Skynet Workshop](https://github.com/SkynetHQ/skynet-workshop) for a more in-depth walkthrough.

{% hint style="info" %}
Using `create-react-app`? Add `"homepage": "."` to your `package.json` before you build, then just upload your build folder!
{% endhint %}

## Is Skynet the right platform for my website/app?

If your website is structured to be client-side, then hosting it on Skynet is straightforward. If not, it is likely your website will need to reconsider some parts of its architecture to be fully-functional on Skynet.

So, if you use Create React App or Gatsby, deploying to Skynet is as easy as uploading the folder of your production build. If you use a server-side backend like ExpressJS or a CMS like Django or Wordpress, these parts of your website cannot be run on Skynet. You can, however, host your html, css and javascript code on Skynet with your server API elsewhere, but that's not really a decentralized app and isn't what we'd call a skapp.

If you're considering developing on Skynet, take a look at the [Getting Started](../getting-started/using-skynet-skapps.md) section to learn some basics or reach out on our [Discord server](https://discord.gg/skynetlabs) in the `#skynet` or `#app-dev` channels.

