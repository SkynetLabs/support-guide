# Portals

{% hint style="danger" %}
This documentation is still being worked on. For a brief introduction, see [Web Portals on Skynet](../../getting-started/web-portals-on-skynet.md).
{% endhint %}

## Overview

Portals serve many functions on Skynet, but put simply, they do the work to serve content to users from Sia and store content from users on Sia. Different type of portals serve different functions in the ecosystem, as you'll see below.

## Portals and The Sia Network

Much of the work that a Portal does is interacting with the Sia network. Describing the details of Sia is beyond the scope of this documentation, but for further reading, start with Sia Support's [Sia 101](https://support.sia.tech/get-started-with-sia/sia-101).

Portals act on behalf of Skynet users on the Sia network. They run full blockchain nodes and act as special "Renters" on the network. They hold Siacoins in a wallet, and they create file contracts and pay hosts for their storage and bandwidth.

### Uploading Files with a Portal

When you upload files to Skynet using a portal, the portal creates a contract with several hosts, committing to pay them to store the file for a period of time. For more info on the specifics of how files are treated on Sia, see the Sia Support article for [Uploading](https://support.sia.tech/renting/managing-your-files#uploading).

Currently, there are two main differences for how Skynet handles uploads compared to Sia's default behavior:

1. Uploads on Skynet use 1-to-10 Reed-Solomon encoding for extra-high redundancy, but at additional cost to the portals. _\(Setting this to a custom value will be possible in the near future.\)_ 
2. Files on Skynet are not encrypted before being erasure-coded and sent across the network. Encryption for skyfiles is the responsibility of the application. 

### Downloading Files with a Portal

When you download files from Skynet using a portal, the portal finds the pieces it needs to reconstruct the file from hosts across Sia. It reconstructs the file and streams it to you with minimal lag or latency. For more information on how Skynet can do this in a performant way, see the [Skyrocket](../../the-technology/skyrocket.md) page.

### Pinning Files with a Portal

When you "pin" a file on Skynet using a portal, the portal is creating file contracts with hosts and committing to pay for the storage of that file on the Sia network. You don't need to be the original uploader to pin a file -- as long as you have access to the file when you pin it, portals take care of the process needed to keep the file alive on the network and "repairing" it if hosts cannot prove they're still storing the data.

## Web Portals

Portals at their most basic are a special type of renter on the Sia network. If you run a Sia node, you can easily upload files to Skynet or pin files you find on the network. See [Using a Sia node as a Portal](using-a-sia-node-as-a-portal.md) for more information.

Web Portals enable much of the functionality that make Skynet accessible on the web for users and developers. In addition to the work that all portals do on the Sia network, Web Portals allow:

* Uploading and Downloading by using standard HTTP requests
* Interacting with Web Apps
* Full Handshake node for trustlessly hosting web apps and files at human-readable URLs

Skynet Web Portals that are available to any user are called public web portals. Skynet Labs operates the public web portal hosted at [http://siasky.net/](http://siasky.net/).

For more information on the technology stack that makes this work, see [Running a Web Portal](../../the-technology/running-a-web-portal.md#web-portal-components).

## Portal Responsibilities

Portals can be used to access any data uploaded to Skynet. This creates certain difficulties, as portal operators cannot control what data may have been uploaded to the network by other portals.

Web portals, by virtue of being open to the public, have to contend with data that may put them in danger of legal consequences or with data they do not want to serve.

### Blocklists

Portals maintain a list of "blocklisted" files that are not downloadable through their portal. Blocklisted files will also not be uploaded to the Sia network if a user tries to upload the file to the portal.

Blocklists are an important way for portals to remain compliant with legal obligations. Blocklists are also saved in an obfuscated format to allow portals to share blocklists without publishing the skylinks of the material they've chosen to block.

Skynet Labs cannot give legal advice in any jurisdiction, so please operate public web portals with extreme caution. We do believe that code is speech and that free software, open access, and user-control are key to a better, freer internet.

## Running a Web Portal

See [Running a Web Portal](../../the-technology/running-a-web-portal.md).

