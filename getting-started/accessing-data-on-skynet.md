# Accessing Data on Skynet

## Beyond the File Upload

Now that you have uploaded a file to Skynet, you'll see some of the ways you can use the network to access data, taking a closer look at skylinks before learning about SkyDB and HNS domains.

## Skylinks

In the last section, you learned that you can't edit skyfiles \(files hosted on Skynet\). It's important to know that this is not a limitation, but a design feature! Data that cannot change is called _immutable_, and in this section, we'll see how that helps power Skynet.

### Anatomy of a Skylink

Remember, when we uploaded a file to Skynet, we got back a wild-looking URL. Here's an example: [https://siasky.net/CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg](https://siasky.net/CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg)

This URL has two distinct parts:

1. The Portal URL, which points to the portal you're using to access Skynet: `https://siasky.net/`
2. The information needed to locate and pull your file from Skynet -- its _skylink:_ `CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg`

{% hint style="info" %}
Skylinks are usually written with `sia://` at the beginning. A skylink will point to the same file, no matter what portal you use, so the portal is not included. For the link above, we'd write the skylink as`sia://CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg`
{% endhint %}

### How Skylinks are Generated \(and Why They're So Strange Looking\)

Although skylinks can look random, their structure is essential to the security of Skynet.

When a file is put on Skynet, the data in the file is hashed using a cryptographic function. This hash, along with some additional info, is used to generate the skylink. Because of this process, Skynet portals can always confirm that the file they receive from hosts hasn't been altered, because a different file would result in a different hash! This is also why you can't edit files on Skynet -- if you try to change a file's contents, its hash changes, and so the skylink would have to change too.

{% hint style="info" %}
If "hashing" is unfamiliar to you, just imagine it as doing some math to make a fingerprint for a file. The fingerprint remains small, even if the file is quite large, and if the file changes, its fingerprint changes.
{% endhint %}

### Skylink Alternatives

Some sites and applications will put a modified version of the skylink before the portal domain. We'll walk through how to do this \(and why you might want to\) on the [Skylinks](../key-concepts/skylinks.md) page.

### Skylink Limitations

You don't always want cryptic URLs for data you can't edit. Sometimes you want data to be _mutable_ or URLs that are human-readable. Let's take a look at how SkyDB and Handshake Names solve these issues.

## SkyDB & The Registry

Skynet uses registry entries and SkyDB entries to enable mutable content on the network. Most users won't directly interact with these, but they're what powers content-rich web applications on Skynet.

### Registry Entries

Registry entries are a special type of content that can be updated. Registry entries are very, very small -- just big enough to point to a Skyfile and keep track of how many times they've been updated. They also use cryptography that lets anyone with the right info to read an entry while only those with a special key can update it.

### SkyDB

Used alone, registry entries aren't that exciting for the average user since you can't fit much information in such a small space. What they power though is our database solution called SkyDB. SkyDB uses the registry entries to make powerful web applications possible. By taking advantage of the registry's mutability at a consistent URL, SkyDB can create updatable data by updating registry entries to point at the skylink of newly created data.

SkyDB entries themselves take the form of JSON files, a standard format used across the web for storing information and sharing data between applications. With SkyDB, you can store info like a follower-list or a user profile and take it with you from skapp to skapp. This is a crucial piece of building Web3 -- you control your data and which apps get to access it.

{% hint style="info" %}
You won't usually see them typed out, but when typed as URLs, registry entries look like this: `https://siasky.net/skynet/registry?publickey=ed25519%3Ab4f9e43178222cf33bd4432dc1eca49499397ecd1f7de23b568f3fa1e72e5c7c&datakey=79c05b4b67764ad99a7976a7d2fb1cfce4f196ea217ef0356af042cb5492bd5d`
{% endhint %}

## Handshake Names

If you'll remember back to [Using Skynet](using-skynet.md#starting-with-skapps), none of the skapps had strange URLs. That's because they use something called Handshake Names \(or _HNS_\).

Handshake is a decentralized domain name project that Skynet Portals support out-of-the-box. Developers can bid on and purchase domain names and then link them to data and applications on Skynet. Let's look quickly at what this means for Skynet users.

{% hint style="info" %}
As we saw in [Using Skynet](using-skynet.md#starting-with-skapps), you'll typically see HNS links look like this:  
`https://<hns-name>.hns.siasky.net`
{% endhint %}

{% hint style="info" %}
For more in-depth details about the Handshake and how it interacts with Skynet, see [Handshake Names](../key-concepts/handshake-names.md).
{% endhint %}

### Benefits

When you own a handshake name, you're not "leasing" it like with `.com` names -- you own the name and gain censorship resistance beyond what traditional domains can give you. If Mr. GoDaddy gets cross with you, you won't have to worry about your access to your domain names being revoked.

Skynet Portals take care of figuring out where on Skynet an HNS name points. Handshake names can point to applications, user profiles, and more.

{% hint style="info" %}
One great use-case for HNS names is the fully decentralized profile platform [dLinks](https://www.namebase.io/dlinks). Hosted using Skynet, this service lets you use your Handshake name to host a simple profile full of links that your friends and community can always trust to be available and under your control.
{% endhint %}

### Trade-offs

With Handshake names, you gain access to a URL that's easy to remember \(not to mention keeps developers from having to update the links to their skapp every time they want to make a small update\). The trade-off to keep in mind is that, as a user, you may not want an app's underlying code to change!

By using HNS, we re-introduce an issue to Skynet that we claimed was a benefit over the traditional web. When going to a site using HNS, you can't guarantee the data or code hasn't changed, unless you can confirm that the skyfile that the name points to has the same skylink as before. And immutable data was our major feature! It's a trade-off of convenience, and, for most user-facing applications, it's best to prioritize making content convenient and accessible.

{% hint style="info" %}
As we get deeper into the design and functions of Skynet, you'll see there are often multiple ways of achieving a similar result. It's important to realize that this flexibility is necessary because there are trade-offs when choosing one option over another, especially when designing applications.
{% endhint %}

