# Web Portals on Skynet

## Types of Portals

As you first saw in [Skynet Basics](skynet-basics.md#skynet-is-built-on-top-of-sia), Skynet Portals are fundamental to Skynet. They're the piece that communicates and interacts with the Sia network, and they allow users to access Skynet from any device with an internet connection.

Portals can be set up in different ways to serve different functions. In this article, you'll learn about "public web portals." These are portals that are available for anyone to use \(public\) and that are accessed over the internet.

{% hint style="info" %}
Does this imply that there are private portals and ones that aren't accessed through the web? Yes! See our more-comprehensive [Portals](../key-concepts/skynet-portals/) page to learn more about other types of portals.
{% endhint %}

## Public Web Portals

As you've gone through the previous sections of this guide, you've actually been learning about and using web portals in each section. Let's recap some of what you've already seen about portals.

In [Using Skynet](using-skynet.md#file-sharing-with-skynet-send), you saw that you could access skapps at URLs like [https://skynet-send.hns.siasky.net/](https://skynet-send.hns.siasky.net/) through your normal internet connection, with no sign-up or special software. You were accessing the app through the [https://siasky.net](https://siasky.net) portal.

In [Skynet Basics](skynet-basics.md#skynet-is-built-on-top-of-sia), you learned that one job of a portal is to act as a renter on the Sia network, which it uses for decentralized file storage. You [also saw](skynet-basics.md#skynet-in-action) that you could upload a file to one portal \(Siasky.net, which is owned and operated by Skynet Labs\) and instantly download that same file from any other portal on Skynet.

Finally, in [Accessing Data](accessing-data-on-skynet.md#anatomy-of-a-skylink) on Skynet, you saw that Skynet URLs have a portal domain name, and by changing this domain, you are able to access the content on Skynet but using a completely different portal -- one not controlled by or moderated by Skynet Labs.

## What to Know When Using a Portal

### File Pinning

When you upload a file to Skynet, it gets broken up and stored across hosts on the Sia network. Portals are responsible for sending out that data, but also for making sure that Sia hosts hold on to the data and keep it online. This process is called "pinning" the file and is done by the portal.

Pinning is a portal's way of saying it will pay to keep a file on the network, and if any hosts go offline, the portal will find new ones to make sure it's always available. Portals set their own policies about how long they will pin a file, so some files may only be pinned for 3 months, while others might be pinned indefinitely.

In [Skynet Basics](skynet-basics.md#change-the-file-and-delete-the-file), you saw that you can't delete a skyfile from the network. A file only leaves the network when it is no longer pinned by any portal.

{% hint style="info" %}
Once a skyfile is on the network, any portal can pin it. So, if a file seems at risk of being removed, another portal can agree to pay for its storage, assuring that the file remains available.
{% endhint %}

### Portal Operating Costs

When it comes to accessing the Sia network, Portals act on behalf of their users. That means that web portals pay for all of the storage and bandwidth costs used to incentivize the hosts on the Sia network. This payment is done using a cryptocurrency called Siacoins.

How much this will cost depends on how many files the portal pins and how fast and often it needs to access content on Skynet. If you're running your own portal, the cost and necessary hardware can be minimal. That said, running a public web portal, like running any server, has other costs associated with it as well. To service hundreds of users all storing and accessing data on the Sia network, the portal will require fast internet, powerful hardware, and some love and care in the form of maintenance. Running a web portal isn't always cheap, and portals may ask users to help to cover these operating costs.

### User Accounts

User Accounts let users signup for a membership with a specific portal. This accomplishes many things, but most importantly:

* It lets users keep track of what skyfiles a portal is pinning for them.
* It lets portals generate revenue by charging a fee to users who want upgraded service.
* It lets users who wish to pay extra have extended file pinning and increased speeds.
* It helps reduce spam and abuse of the network.
* And it provides the foundation for an alternative economy where users support Skynet, developers, and content creators without needing to worry about how to obtain cryptocurrency and without introducing advertisers into the mix.

User accounts follow a "freemium" model, where anyone can access any of the content on Skynet for free, but users putting money into the network get a better experience. By choosing a paid tier, you're not only speeding up your own access, but also participating in an economy that can support the content creators, portal operators, and developers trying to build a better future for the internet.

{% hint style="info" %}
Not everyone will have or need a paid account! Every file on Skynet is still available to any user. Speeds may be slowed down a little, but a bit of a delay still beats an ad-break -- and that's if the user even notices.
{% endhint %}

### Blocklists

Another crucial function of portals is maintaining a blocklist. **Just because something is uploaded to Skynet doesn't mean it can't or won't be blocked by a portal!** A portal can choose to add skylinks to their blocklist. Once on the blocklist, no one can download the file from that portal. This helps protect our portal operators no matter their legal jurisdictions or obligations.

Blocklists don't remove files from Skynet though. If the file is still pinned \(and paid for\) by any portal on the network, then the file is still available on Skynet. Being blocked by one portal doesn't mean that the file is unavailable through any other portal, it just means that users can't access the file through portals that have blocked the file.

If you can't find a portal that hasn't blocklisted your skyfile \(_what did you upload?!_\) and are worried you'll lose access to your data, you can always set up your own portal to pin or download the file.

{% hint style="info" %}
Skynet Labs operates [https://siasky.net](https://siasky.net), which regularly gets DMCA takedown notices. We happily comply with these in order to remain compliant with US and EU legal requirements.
{% endhint %}

## The Future Portal Ecosystem

In [Skynet Basics](skynet-basics.md#download-the-file), you saw a few different portals where you could download your file. We don't have a complete list of public web portals, but we do encourage other portal operators to join the network!

Currently, much of our engineering effort is on making web portals robust and self-sustaining. A large number of portals on the network is an essential step for Skynet to become truly decentralized. With each release, we aim to make the process for setting up and running a portal easier and expect a robust ecosystem of portals to emerge that benefits the entire Skynet ecosystem.

Since portals are open-source, we also expect to see them be modified and customized. Some may charge different rates, some might only allow users in countries with lenient copyright laws, some may work together to share blocklists or provide unique portal features, and some may be run by local and university libraries, accessible to patrons free of charge.

If you want to dive deeper into portals, how they work and how to run your own, see [Portals](../key-concepts/skynet-portals/).

## Congratulations!

You made it through our Getting Started guide! Hopefully, you have a better grasp on Skynet, how it works, and why we're so excited about the future of the web.

If you want to talk to other folks in the community or to get more involved, come introduce yourself on our [Discord Server](http://discord.gg/sia)! If you want to dive deeper into the details and philosophy of Skynet, check out the articles in **Key Concepts**.

