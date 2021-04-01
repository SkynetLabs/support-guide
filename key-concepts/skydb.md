# SkyDB

{% hint style="danger" %}
Our full documentation is still being worked on. In the meantime, here is a quick overview along with links to various resources. For a brief intro, see [Accessing Data on Skynet](../getting-started/accessing-data-on-skynet.md#skydb-and-the-registry).
{% endhint %}

SkyDB is a key-value store database building on Skynet's registry and skyfiles. By using the registry, users and applications are able to write JSON contents to a file that is accessed using their public key and a "data key" they assign the file to. Writes can only be made using the user's private key \(paired with the data key\).

By taking advantage of Skynet's system for rich, mutable data on the network, developers can build complex web applications where users can both store application data and share their data between applications.

SkyDB uses the registry for the mutable piece of its storage. The registry has limited data capacity, so instead of recording the JSON data directly, it stores a pointer to a skylink that contains the actual JSON data. Per byte, the registry is expensive to store and access when compared to typical Skyfiles, which is why they are heavily constrained. Developers should take this into consideration when designing their applications.

{% hint style="warning" %}
SkyDB is currently only implemented in our Javascript SDK. The code can be seen [here](https://github.com/NebulousLabs/skynet-js/blob/master/src/skydb.ts).
{% endhint %}

## Further Reading

{% embed url="https://blog.sia.tech/skydb-a-mutable-database-for-the-decentralized-web-7170beeaa985" caption="" %}

{% embed url="https://blog.sia.tech/mutating-the-immutable-behind-the-scenes-of-skydb-137df8105c17" caption="" %}

