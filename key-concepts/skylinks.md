# Skylinks

{% hint style="danger" %}
Our full documentation is still being worked on. In the meantime, here is a quick overview along with links to various resources. For a brief intro, see [Accessing Data on Skynet](../getting-started/accessing-data-on-skynet.md#handshake-names).
{% endhint %}

## Overview

Skylinks are unique identifiers that point to data on the Skynet network. They often look like this:`sia://CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg`

And their contents can be accessed through web portals using links like this:  
[https://siasky.net/CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg](https://siasky.net/CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg)

## Structure

Data on Skynet is "content-addressable" which means that Skylinks point to a file based on its content and not its name. This is why skyfiles are immutable -- if you change the data, you'd be changing the skylink.

The information needed by portals and hosts to locate the file on the network is encoded in the skylink. Skylinks strings are encoded in Base64 and are 46 characters long.

## Base32 Subdomains

Skylinks can also be modified for use as a subdomain of the portal domain.

This is useful in a variety of scenarios, but especially for web applications that need to secure their data from other skapps on Skynet. A skylink is typically encoded as a Base64 string, but when used for a subdomain, it must be re-encoded to Base32. \(Hostnames in URLs are not case-sensitive.\)

The widget below shows what this looks like. Here's a [link](https://siasky.net/CADIvje1Fdy2FP2TeBsYAbHfUsNug98wE7SYArdyczDaDg) to try.

{% embed url="https://codesandbox.io/s/skynet-guide-widgets-jp5wt?codemirror=0&view=preview&fontsize=12&hidenavigation=1&theme=light&hidedevtools=1&initialpath=%2F%23%2Fbase32-subdomain" caption="" %}

