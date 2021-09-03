# FAQs

## How long does data remain on Skynet?

Files uploaded to Skynet will remain available as long as a portal pins the skyfile \(agrees to pay from it\). The rule-of-thumb for a minimum time is 3 months, but this will vary from portal to portal and could depend on if you have a user account with the portal. You can pin files yourself by running your own portal, and any portal can pin any file that already exists on the network.

## Is data uploaded and stored to Skynet encrypted?

By default, data stored on Skynet is stored in plain-text. Communications on the network are encrypted and applications and users can encrypt their data before uploading it to Skynet. Also, because files are broken into pieces and erasure-coded, even plain-text data becomes broken apart and obfuscated when distributed between hosts.

## Is Skynet free? Who pays for storage on Skynet?

* Accessing Skynet is free, but there are paid user accounts that allow prioritized access.
* Uploading files to Skynet is free, but without a user account, most portals will store your files for a minimum of 3 months.
* Storage expenses are paid by Skynet Portals, which use a cryptocurrency called Siacoin on the Sia network.
* Portal operating costs are paid by operators, but we encourage users to support portal operators, developers, and content creators by signing up for a user account.
* Skynet is open-source, so the code is available for anyone to freely use.

See [Webportals on Skynet](../getting-started/web-portals-on-skynet.md#portal-operating-costs).

## Is Skynet censorship-free?

Not really. We say "censorship-resistant," because the infrastructure makes it extremely difficult to censor or deplatform data and applications across the entirety of Skynet. That said, portals operate their own "blocklists." Users cannot download a file from a portal if it is on its blocklist. This helps to protect portal operators. The code for running a portal is free and open-source, so users can always run their own portal if they do not agree with the decisions made by another portal operator. See [Web Portals on Skynet](../getting-started/web-portals-on-skynet.md#blocklists) and [Running a Web Portal](../the-technology/running-a-web-portal.md).

## How fast is Skynet?

New download code released in `siad 1.5.5` still needs to be tested for real-world latency, but streaming throughput can reach speeds of 1 Gbps. It is competitive with centralized services and out-performs decentralized storage competitors. The team is regularly developing optimizations to further increase the speeds of uploads and downloads.

## Is my data on Skynet secure?

Skynet is secure because Sia is secure. Also, by designing our ecosystem around client-side applications, any data compromise doesn't affect the entire service, but rather just the user. For more information on Sia's data security see their support article [Is my data secure?](https://support.sia.tech/renting/is-my-data-secure) and see more about Failure modes for Decentralization in [A Deep Dive into Skynet](../the-technology/a-deep-dive-into-skynet.md#29e3).

## What is "pinning"?

When a portal "pins" a skyfile on Skynet, they are telling the network that they are willing to continue paying for the storage costs of that file. Any number of portals can pin the same skyfile, and as long as the file is pinned, it will be available on Skynet. See [Web Portals on Skynet](../getting-started/web-portals-on-skynet.md#file-pinning) for more.

## How does Skynet use Siacoins?

Skynet portals pay hosts on the Sia network in Siacoins. You do not need Siacoins or a wallet to use Skynet in your browser. For more information on costs, see [Is Skynet Free?](faqs.md#is-skynet-free-who-pays-for-storage-on-skynet) When monetization is released, developers and content creators will earn Siacoins, but payouts will be made by portals, not directly by Skynet users.

## Are there file size or bandwidth limits on Skynet?

Skynet Web Portals currently support uploads of up to 1GB. If you [run your own portal](skynet-portals/using-a-sia-node-as-a-portal.md), the limit is 400GB. If you want to send files larger than 1GB in your browser, look into skapps like [Skysend](https://skysend.hns.siasky.net/) which breaks up files into smaller chunks before uploading.

Portals pay for bandwidth costs, and your portal accounts will take bandwidth usage into consideration in your account's access tier. We do monitor to see if abuse is occurring on our web portal, and you can always [run your own portal](skynet-portals/using-a-sia-node-as-a-portal.md) if you're worried about bandwidth usage.

## Why did the skylink for my file change when I re-uploaded it?

If you are uploading a file you uploaded in the past, there are some cases in which you might get a different skylink. The file may have been altered, resulting in a new skylink. Additionally, the metadata in the upload affects the skylink. So, if your method of uploading has changed, or your uploader changes its default skyfile metadata settings, your skylink after uploading might be different too.

If your original file is still available on Skynet, we recommend "re-pinning" the file instead of trying to upload the file again.

