# Blocklisting Content on Your Portal

You can blocklist content on your Skynet portal. The blocklist will prevent skylinks from being downloaded. Since Skynet blocklist by merkleroot, this will also prevent uploads of the same underlying data \(and therefore pinning the files\) that would resolve to the same skylink and merkleroot.

## Command-Line

The command for blocking a file using `siac` is

```text
siac skynet blocklist [skylink] [flags]
```

For example, you want to blocklist`sia://ABCdefGHIjklMNOpqrSTUvwxYZ12345678901234567890` or its web-friendly form `https://siasky.net/ABCdefGHIjklMNOpqrSTUvxwYZ12345678901234567890` you would run the following:

```text
siac skynet blocklist ABCdefGHIjklMNOpqrSTUvxwYZ12345678901234567890
```

## Using the API

You can also use the Sia API to add or remove multiple links at a time. This is especially useful for portals that want to share blocklists with each other. For more examples, refer to the [Sia API Docs](https://sia.tech/docs/#skynet-blocklist-post).

