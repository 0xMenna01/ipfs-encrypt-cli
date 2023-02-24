# ipfs-encrypt-cli

This is a cli application that implements content encryption on top of IPFS.

IPFS is a desentralised file system that uses content-addressing for retrieving 
files rather then location addressing.
This protocol hardly relies on cryptograpghic principles.
Full description about IPFS here: https://docs.ipfs.tech/

Since IPFS relies on a garbage collector to free memory, files are not permanenlty stored.
To solve this problem the application uses a decentralised pinning service of Crust Network.
Full details about Crust can be found here: https://wiki.crust.network/docs/en/build101

For it to be fully decentralised and IPFS content identifiers easily accessible
the application relies on the usage of ink smart contracts.
The smart contracts are responsible of storing all content identifiers and
an access control list of the owners that have the priviledges to access the 
encrypted files, thus mantaining encryption keys.

Read about ink! here: https://use.ink/

NOTE: IPFS is a publicly avaliable network, content is encrypted but can be read by anyone.
It would be more secure to use a private IPFS network that is publicly avaliable,
where peers return the content only to the owners returned by the smart contracts.
