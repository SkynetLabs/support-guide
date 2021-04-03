# Understanding Data Usage

## Upload Usage

It's important to know that upload sizes won't always match the size of the files you're uploading.

The reason comes down to how files are stored on the Sia network and how much redundancy your data has. For more info on how Skynet uses Sia, see [Skynet Basics](../getting-started/skynet-basics.md).

### Upload Calculations

Skyfiles stored on Sia have a base sector size of 4MB. For speed and reliability, base sectors are stored with 10x redundancy. Any data beyond this initial 4MB is divided into 40MB "chunks" which are stored with redundancy that requires 3x their storage size. For more info on Sia uploads, see the [Sia Documentation](https://support.sia.tech/renting/managing-your-files#uploading).

So, we're currently rating storage usage at 1/3 of the storage it uses on the Sia network, which for larger files means you don't need to worry about the cost of redundancy toward your quota. For small files, this can be quite surprising, since even a 1 byte file will appear as 14MB \(roughly 4MB \* 10x redundancy / 3\).

{% hint style="info" %}
We're aware of the confusion users are facing with these numbers and plan to find better solutions that better explain how we arrive at our numbers. Expect these numbers to change.
{% endhint %}

### Application Uploads

When using Skynet applications, they will often save data to Skynet in the background. This usually takes the form of formatted text \(called JSON\) and it might be a post you made, your friend list, or your user profile. The files are important data for the Skynet apps and will be attached to your portal account so that they remained pinned and available on Skynet.

## Download Usage

Download usage is much more straight-forward than uploads. The files you access are listed as downloads.

### Application Downloads

When using Skynet applications, they may load data in the background. Just like on the traditional web, this happens very often while browsing a website. Some of the loaded material may never even show up in your web browser.

