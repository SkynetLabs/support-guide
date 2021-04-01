# Using a Sia node as a Portal

## Accessing Skynet using a Sia Node

If you are running a fully-synced Sia node on your machine, you can download, upload and pin files to Skynet by using the command-line tool `siac` or using its API. This page will get you started using `siac` but Sia also provides [API documentation](https://sia.tech/docs/#skynet).

If you need help getting Sia up and running, see the [Sia Support](https://support.sia.tech/your-sia-wallet/sia-ui-faqs/how-to-download-and-install-sia-ui) page.

{% hint style="warning" %}
This documentation is intended for Advanced users with experience using the Sia network.
{% endhint %}

{% hint style="info" %}
The location of `siac` depends on your OS and installation method. For Sia-UI users on Windows, try `%APPDATA%\Local\Programs\Sia-UI\resources\bin`
{% endhint %}

## Pre-Requisites

You'll need:

* A running, fully-synced [Sia](https://sia.tech/get-started) blockchain 
* [Siacoins](https://support.sia.tech/get-started-with-sia/how-to-buy-siacoins) in your wallet
* An [allowance set](https://support.sia.tech/renting/how-to-rent-storage-on-sia) for your Renter

{% hint style="info" %}
By default, node renters do not try to create contracts with all hosts. To configure your renter as a Skynet portal, follow these instructions for [configuring siad](https://github.com/NebulousLabs/skynet-webportal/tree/master/setup-scripts#step-3-configuring-siad).
{% endhint %}

## Skynet Commands

To see all the commands available, see the [Sia Repository on Gitlab](https://gitlab.com/NebulousLabs/Sia/-/tree/master/cmd/siac#skynet-tasks) or run:

```bash
siac skynet --help
```

### Uploading to Skynet

To upload a file or directory to Skynet, use this command, where `source` is the location on your local filesystem and `destination` is the siapath to use for saving renter data locally.

```bash
siac skynet upload [source] [destination]
```

For any of the commands, use `--help` for a thorough explanation of how it works. For example, for s`siac skynet upload --help` we see:

> After it runs, a skylink will be produced which can be shared and used to retrieve the file. If the given path is a directory it will be uploaded as a single skylink unless the `--separately` flag is passed, in which case all files under that directory will be uploaded individually and an individual skylink will be produced for each. All files that get uploaded will be pinned to this Sia node, meaning that this node will pay for storage and repairs until the files are manually deleted. Use the `--dry-run` flag to fetch the skylink without actually uploading the file.

### Additional Commands

Here are some other important commands along with their help instructions to get you started.

#### Download

> Download a file from skynet using a skylink. The download may fail unless this node is configured as a skynet portal. Use the --portal flag to fetch a skylink file from a chosen skynet portal.

```bash
siac skynet download [skylink] [destination]
```

#### Pin

> Pin the file associated with this skylink by re-uploading an exact copy. This ensures that the file will still be available on skynet as long as you continue maintaining the file in your renter.

```bash
siac skynet pin [skylink] [destination]
```

#### Unpin

> Unpin one or more pinned skyfiles or directories at the given siapaths. The files and directories will continue to be available on Skynet if other nodes have pinned them.

```bash
siac skynet unpin [siapath]
```

#### Blocklist

> Add space separated skylinks to the blocklist.

```bash
siac skynet blocklist add [skylink]
```

