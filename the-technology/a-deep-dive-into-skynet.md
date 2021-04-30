# A Deep Dive into Skynet

_The following article was published by Sia co-founder and Skynet Labs CEO David Vorick in February 2021. It provides a great overview of Skynet, its technology, and its vision for the future._

{% embed url="https://blog.sia.tech/a-deep-dive-into-skynet-a0fa037feea" caption="" %}

## What is Skynet? <a id="1af0"></a>

Skynet is a collection of cryptographic protocols for storing and retrieving data over the Internet. In many senses, Skynet can be viewed as an alternative infrastructure for the Internet, providing much of the same functionality except that all data is user controlled instead of corporation controlled.

Like the Internet, most of the interesting applications on Skynet are web applications that can be viewed using a web browser. Skynet applications can be social media apps such as [https://skyfeed.hns.siasky.net](https://skyfeed.hns.siasky.net/)/, storage apps such as [https://marstorage.hns.siasky.net](https://marstorage.hns.siasky.net/)/, or nearly anything else that can be built on the traditional web. Skynet apps can also be normal desktop apps or mobile apps.

What sets Skynet apart from the rest of the Internet is the data model. On the traditional web, data is kept on centralized servers managed by the website operator. This means that if the website goes down, the data becomes unavailable. This also usually means that the website admins can see all of the data, and have the ability to change or delete the data at their discretion. Reading the data requires permission from the website operator, giving the operator control over what type of apps can be built that use the data.

On Skynet, data is controlled by the users. This means that a website only goes down if all of its users disappear, and any content creator with an active audience will be able to continue providing content to that audience, independent of the decisions of a website operator.

The biggest advantage to the Skynet data model is the way applications can make use of each other’s data. On the traditional web, each application has an isolated silo of data, and nobody can access that data without the permission of the website operator. This allows Facebook to guarantee that your list of friends exists only on Facebook, that your list of liked pages exists only on Facebook, and any work you’ve put into a profile can only be expressed using Facebook.

On Skynet, every application has \(with consent from the user\) full read-write access to the raw data of every other application. This means that alternatives to Facebook can import your list of friends, can show you all of the status updates that your friends are making, and can let you see and post in the same groups that you had on Facebook, all without any of your friends needing to know that you’ve left Facebook for another app.

## Centralization vs. Federation vs. Decentralization <a id="29e3"></a>

The words ‘centralization’, ‘federation’, and ‘decentralization’ are used in many communities, and each one tends to define the words differently. For clarity, I wanted to provide definitions for how we tend to use these words within the Skynet ecosystem.

When we talk about centralization, our focus tends to be on a source of control. If we say that a certain product or system is centralized, we generally mean that there is a single entity that has significant control over the ecosystem and its users. For example, Facebook is centralized because it can ban users at any time, delete posts at any time, replace moderators in groups, etc. Facebook the company is a single point of control over the Facebook ecosystem. Nearly every webapp on the Internet today is centralized.

When we talk about federation, we mean that there is a diverse set of participants that control a protocol, but the users themselves do not have any control. The classic example of a federated system is email. Most users access email through centralized services like Gmail —which have full control over a user’s account — but Gmail itself has limited ability to control what happens on other email providers such as Outlook or Proton Mail.

When we talk about decentralization, we mean that the user themselves has full control. Bitcoin is the canonical example of decentralization. In Bitcoin, every user has full administrative control over their wallet, and strong protocol-level protection against both theft and censorship. Every user also has full control over what protocol rules they follow, and a user can opt to change the rules they follow at any time.

One way we like to think about decentralization is in terms of failure modes. If an attacker could choose to take control of any single actor on a network, how much damage could they do? In centralized systems, the answer is typically “they can destroy everything.” In federated systems, the answer is typically “they can destroy a large percentage of users, but many users will still be okay.” And in decentralized systems, the answer is typically “they can only destroy the one user that they took control of.”

## How Do I Use Skynet? <a id="3d13"></a>

The most common way that people use Skynet is through the web browser, accessing Skynet applications the same way that you access other webapps like Facebook or YouTube. You can often tell that an application is a Skynet application \(also called a Skapp\) by the URL format, for example [https://hackerpaste.hns.siasky.net/](https://hackerpaste.hns.siasky.net/)

The URL is broken into 2 parts. The first is the application’s Skynet address, which is ‘hackerpaste.hns’. The second is the address of the portal that is being used to access the application, which is ‘siasky.net’. Skynet is a cryptographic protocol that makes use of cryptocurrency, and the portal is there to manage all of the heavyweight requirements such as running cryptocurrency nodes and making cryptocurrency transactions.

Data is not stored on the portal, data is stored on Skynet. The portal is merely an access point to Skynet, and can be swapped out at any time for another portal. For example, if you log into [https://hackerpaste.hns.siasky.net](https://hackerpaste.hns.siasky.net/) today, make some pastes, and then log into [https://hackerpaste.hns.skyportal.xyz](https://hackerpaste.hns.skyportal.xyz/) tomorrow, you will see all of the same pastes and data, despite accessing Skynet though a different portal. You can even change portals halfway through a session and still successfully pick up where you left off.

The best way to browse Skynet is with a custom Skynet browser. This is because all of the data being provided to the user by the portal can be cryptographically verified, ensuring that the user does not need to trust the portal at all. A custom Skynet browser can also handle portal selection for the user, allowing the user to use applications with their native Skynet URLs, such as [hackerpaste.hns](https://hackerpaste.hns.siasky.net/).

The only important difference between Firefox and a full Skynet browser is a handful of cryptographic verifications when browsing Skynet applications. Because the differences are minor, it’s reasonable to expect that after enough growth Firefox and other major web browsers will support verifiable Skynet browsing.

## Who Pays for Skynet? <a id="9b52"></a>

Just like on the traditional web, Skynet infrastructure costs money. The major resources that you pay for on Skynet are storage, bandwidth, and computation. In the traditional web, all costs are paid for by the website operator. The website operator typically recovers these expenses by either serving advertising, selling user data, charging a monthly premium, or all three.

On Skynet, infrastructure costs are paid for by the portal operator. And just like traditional websites, portal operators can recover expenses through ads, the sale of data, monthly premiums, or all three.

Most portals today leverage a freemium model to cover their costs. Freemium portals grant users universal access to Skynet, but constrain the speeds at which users are able to access Skynet based on their price tier. Free users can visit any page they want, but the page may load more slowly and files may take longer to download for free users than for paying users. Paying users are also usually able to upload larger files and store more data on Skynet.

## How Do I Make Money on Skynet? <a id="76ca"></a>

Just as Skynet charges for storage and bandwidth, Skynet can charge for content. For example, a photographer could add a price tag to a photo that says a user must pay the photographer $0.0001 before loading the image, which equates to $1 per 10,000 views.

From the perspective of the portal operator, this is analogous to paying a higher price for bandwidth. Skynet pages that have content fees are roughly cost equivalent to Skynet pages that require a large download before the page can be presented to the user. Because of this, portals can cleanly wrap paid content into their freemium models. Free users can still visit paid content, but it may load more slowly compared to premium users. Extremely expensive content may take a significant amount of time to load even for premium users.

When browsing, the user doesn’t need to worry about whether the pages they are visiting contain paid content or not. The user is on a fixed-price plan with a ratelimit. Expensive pages may be slower to load for the user, but they will not result in the user seeing a larger bill at the end of the month.

Monetization is not just for assets, but can also be added to code. For example, a developer could write an encryption library that charges a small fee every time something is encrypted using that library. Or a blogging platform could insert a fee for the developer that gets paid every time someone reads a blog post that was created using that platform.

A completed page on Skynet could be making payments to dozens or even hundreds of different parties. From the javascript libraries to the fonts to the icons to the actual media content itself, every piece of Skynet has the ability to be monetized.

All of the monetization on Skynet is permissionless. Nobody needs to ask the photographer before using a photo on their webpage because when that page is loaded by viewers, the photographer will receive payment even if they had no idea that the photo was being used. And the use of cryptocurrency means there’s no intermediary that can shut the payment down or rule the content in violation of some terms of service. Creators with happy users will have stable incomes.

## How is Money Paid Out on Skynet? <a id="ec7b"></a>

All content payments on Skynet are paid out over the Sia blockchain, which means that any content fee will be paid out to a Siacoin address. Because blockchain transactions are expensive, payouts are made using a lottery system rather than making a blockchain transaction every time someone loads an inexpensive piece of content.

For example, a photo that costs $0.01 might be entered into a 1-in-500 lottery to pay $5 to the photographer. If the photo is only viewed a few hundred times total, the photographer may get lucky and get overpaid or the photographer may go entirely unpaid. But if that photo is viewed tens of thousands of times, the photographer will get paid almost exactly as much money as they are supposed to make.

We use a lottery for two reasons: scalability and fairness. We need to pay larger sums infrequently to ensure that the Sia blockchain is not overwhelmed. And we use a random lottery because Skynet is decentralized and we don’t actually know if other users have viewed this content before. A lottery also has the benefit that no central manager ends up holding hundreds of millions of dollars of creator’s money from creators that never reached the payout threshold.

## Why Should Developers Builds Apps on Skynet? <a id="8808"></a>

Developers building on Skynet enjoy a feast of advantages over centralized developers. They don’t have server bills, they don’t need to worry about devops, developers make money every time someone uses the code and data from their application, and when building developers have access to all of the data that exists across the entire Skynet ecosystem.

On Skynet, all infrastructure is paid for by the portal operators, who then monetize from users. This means that none of the cost of running or maintaining an application is borne by the developer. Once an application is deployed, it exists sustainably so long as users are excited about using that application. The actual servers managing the data are operated and paid for by portals, and by the hosts on the Sia network.

Skynet’s monetization takes this even a step further. Developers can add a fee to their code that gets paid every time the app is used. Because there is zero marginal cost to the developer, this fee translates to directly to making the developer wealthy.

The developer fee doesn’t just need to exist at the application level either. For example, a decentralized YouTube could add the developer’s fee to every video that gets uploaded through the developer’s platform. If one of the videos is then used by another application, the YouTube developer will profit even though users aren’t actually using the developer’s original application.

The biggest advantage to developing on Skynet is the data access. Every piece of data that exists on Skynet across all applications is available for all developers to use. For example, when building a competitor to decentralized YouTube, the competitor has the ability to load all of the existing content, subscribe to all of the existing creators, and even write comments that appear on both the competitor and the original. New applications have the ability to fully and seamlessly integrate with existing applications, even without the permission of the existing application’s developers.

The final advantage is of course that the whole ecosystem is decentralized. The monetization model is not advertisement based, and therefore is not subject to advertisers withdrawing from the ecosystem and draining it of funding. The infrastructure is open access, and if a particular infrastructure provider refuses to serve your content, they can be seamlessly replaced with any other infrastructure provider. On Skynet, every application that has active users will be able to continue existing and serving those users.

## How Does Skynet Work? <a id="6498"></a>

Skynet is a composition of multiple decentralized technologies that have collectively been in development since 2013. The base component is a data storage blockchain called “Sia”, which gives users the ability to form data contracts with untrusted counterparties called “hosts” and verify that the data is being stored honestly.

The data contract itself is called the “Sia File Contract”, and contains a few elements. Cryptographically, the most important elements are the size of the data and the Merkle root of the data. These two fields define the data that the host is required to store. The renter puts money into the contract which gets held in escrow. The host _also_ puts money into the contract which gets held in escrow. There is a date which defines when the file contract expires, and on that date the host must prove that they are still holding the data in the contract. The blockchain chooses a random subset of the data that the host must reveal alongside a Merkle proof demonstrating that the data matches. If the host is successful in presenting the data and the proof, all of the escrowed money is given to the host as payment. If the host is not successful, the escrowed money is destroyed.

The Sia File Contract also contains a couple of elements that allow it to function as a state channel. It contains a list of pubkeys that are allowed to upgrade the contract in a multisig, and a revision number that allows external observers to determine which version of the file contract is the most recent. This state channel gets used heavily by other parts of the Skynet technology stack to make things scalable and high performance. Most importantly, users can update the data that they are storing the host and make payments to the host for resources like computation and bandwidth without needing to make new transactions on the blockchain.

The file contract and the payment system built on top of the file contract is the full extent of the reason that Skynet uses the Sia blockchain. Without the blockchain, we’d need to use trusted intermediaries to manage and move the money around, and those intermediaries would have the ability to interfere with the operation of the network.

A storage management engine called “the renter” will select hosts on the network and form file contracts with them. When data is uploaded to Sia, the renter will use erasure codes to spread the data reliably across a large number of hosts. The renter also monitors the health of the data, performing repairs as hosts go offline or otherwise experience failures.

Data on the Sia network is carved up into discreet 4 MiB pieces called “sectors”. Hosts keep an in-memory map of all the sectors that they are storing, allowing anyone to request a sector from a host if they know the Merkle root of the data that they want. This in-memory map forms the basis for Skynet requests. A Skylink is a sector Merkle root plus a tiny bit of extra information which contains hints about things like which hosts are storing the sector and which parts of the sector should be downloaded first.

A Skyfile is a static file stored on the Sia network that can be built from the metadata stored in a single sector. For small files, the single sector will contain the full file along with some metadata explaining what the file is and how to use it. For large files, the metadata will contain a longer list of sectors that the raw data of the file is stored in. This construction allows any file to be uploaded to the Sia network in a way that allows it to be fetched using nothing more than a 34 byte cryptographic link.

We call the static part of Skynet the ‘IGDL’, which is short for ‘Immutable Global Data Layer’. Because every file in the IGDL is indexed by a cryptographic hash, users can always verify the integrity of the data that they are retrieving from the IGDL.

The IGDL affords files a lot of flexibility. Entire web applications can be stored in the IGDL and loaded by web browsers the same way that any other website can be loaded, for example [Skylearn](https://0008fi4lv5gg4vqsal48nln5b9doa5c0qfg8j1btg9ptmjmls6p0be0.siasky.net/). The IGDL is also compatible with schemes like [HLS,](https://en.wikipedia.org/wiki/HTTP_Live_Streaming) which allows the same content to be streamed at different quality levels to users with different Internet speeds.

The final noteworthy aspect of the IGDL is the monetization: files in the IGDL can add monetization rules to their metadata which stipulate how much money must be paid to the file owner to load the file for a user. The monetization happens automatically, a developer embedding a file into their webpage from the IGDL does not need to worry about making payments, that will be handled by the Skynet portal when the user renders the final page. Skynet also provides an API that libraries can call out to to charge money to users, allowing code as well as objects to be monetized.

Sia hosts have a second storage mechanism called “the registry”. The registry exists as a key-value store for data, where the key is a public key and the value is a signed ~100 bytes. Most typically, the items in the registry entry are Skylinks that point to larger amounts of data. When the registry is used in combination with Skylinks, the result is called ‘SkyDB’. Sia hosts give observers the ability to subscribe to registry entries, such that the observers get notified immediately when a registry entry is updated.

SkyDB gives Skynet users the ability to update things in real time, and is a fundamental part of almost every interesting application on Skynet. It’s how a decentralized DropBox can know what files you’ve stored, it’s how you can see what your friends are posting on a decentralized Twitter, and beyond that it’s the fundamental technology that allows applications to interact with each other.

The final major technology used to build Skynet is Handshake. Handshake is a naming service that allows Skynet users to map human friendly names to Skylinks and SkyDB entries. Without Handshake, Skylinks and SkyDB entries would each contain at least 32 bytes of random data, which is typically rendered as 46 or more random-looking ascii characters. With Handshake, we can turn something like [https://8g012jcgk6dbfhorag…pu6qg.siasky.net/](https://8g012jcgk6dbfhoragieh3ahd52s5oio33dg3tkoj4qna7k2mfpu6qg.siasky.net/) into the much more readable [skydocs.hns](https://skydocs.hns.siasky.net/)

## What’s Finished and What’s Still Under Development <a id="6fc8"></a>

As of writing, most of the technology discussed today is finished. Sia is finished and works as described. The IGDL is finished and works as described. Handshake is finished and works as described. SkyDB is finished, and almost works as described. We have implemented and tested but not yet deployed the real time subscriptions to SkyDB entries. Everything else works as described.

The biggest thing that we are still working on is monetization. The designs are all complete, and implementation at the protocol level will be pretty simple, but a surprising challenge for us has been spinning up a traditional database to track user spending and implement ratelimits.

These days, AWS solves so many distributed database problems for you that the open source solutions to these problems \(if you constrain yourself to not using AWS\) are incomplete and overall very weak. And we’ve been further mired by the fact that most payment processors refuse to work with us because there is a cryptocurrency involved in our back-end processing \(even though the cryptocurrency never gets into the hands of our users\).

So our major slowdown at the moment is getting a traditional distributed database alive that can track users, accept payment from users, and ratelimit users based on their payment tier and current usage levels. We’ve solved most of the major issues at this point, and hope to have everything released shortly.

## Future Technological Direction <a id="d34f"></a>

Our main focus at the moment is performance and scalability. We want to reduce the latency that the end user experiences when interacting with Skynet and we want to increase the total number of users that Skynet can handle, and the cost which is required to reach that many users. Already today the numbers are very good. Supporting &gt;100,000 monthly active users on Skynet is costing us less than $5,000 per month in operational expenses, and we estimate that we can keep scaling Skynet out to 10 million or more users total with no upgrades to the codebase. Speeds are also pretty solid today already, with the average download going as fast as 100 megabits per second, and the average latency on the time-to-first-byte being under 200ms. To the best of our knowledge, these numbers **significantly** outperform all other decentralized storage platforms. Still, we think all of these numbers can easily be pushed another order of magnitude.

A second focus for us currently is building out the toolchains and SDKs that exist on top of Skynet. We believe that there is a significant amount of latent power in the protocol that has already been deployed, including improved global identity solutions, improved social network solutions, among other ideas that we have for making the lives of developers significantly easier. In many senses, it is already easier to deploy complex applications on Skynet than it is to deploy them on AWS, however like the scalability and performance, we believe that there is at least an order of magnitude — if not two — of room for improvement here.

Finally, in the research department we’ve got a lot of eyes on privacy. We’ve mostly held off on incorporating privacy technology into Sia and Skynet thus far because we’ve felt that privacy technology as a whole was not yet at the point where we could reasonably give users strong privacy assurances. But a lot has changed on the privacy front in the past 5 years, and our patience has been bearing fruit. It is my current belief that in the next 5 to 10 years we will be able to upgrade Skynet to make it fully private, exceeding the privacy capabilities of systems like Tor and Freenet while maintaining the same performance that Skynet enjoys today. There are a substantially nontrivial number of privacy technologies and techniques that we would need to deploy to make this possible, but at the very least it does seem to be actually possible.

## Diving Deeper <a id="d64e"></a>

The best way to learn about Skynet is to join our [Discord server](https://discord.gg/skynetlabs) and start asking questions. If you want to learn more on your own, you can browse our [growing body of support documents](https://skynet-labs.gitbook.io/skynet-guide/the-technology/developing-on-skynet). And if you want to get started with Skynet in general, you can checkout our homepage at [https://siasky.net/](https://blog.sia.tech/siasky.net).

