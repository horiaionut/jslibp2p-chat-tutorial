What is transport?
==================
TODO: Add a cool gif about transports
lets break it!

## What does transport means in p2p system?
As the word transport says it does transportation, but of data between two peers. Currently our internet supports multiple standards of communication. Eg. [tcp](https://www.avast.com/c-what-is-tcp-ip), [websockets](https://blog.teamtreehouse.com/an-introduction-to-websockets), [mqtt](https://github.com/mqtt/mqtt.github.io/wiki), etc. Every standard is just a set of rules that both communicating parties have to follow in order for a successful communication.
>TODO: Verify and add transports.

In a p2p system it might be not clear which of these standards does the other party supports. As the standards are drastically different it would be hard for a p2p system to implement each one from scratch. 

## This is where transports of libp2p comes
One thing which is very clear though every transport is very different in the core implementation it has certain operations in common eg. dialing other user, sending/receiving packets and listening for connections.

[`libp2p`](https://docs.libp2p.io/) uses these similarities to build an interface (a set of functions) that every module needs to follow in order to be used in a transport. In addition, libp2p provides implementations of some of the important [transport protocols](https://libp2p.io/implementations/).

Now anyone can plug in any of the transport implementations and use the common interface to work with it. One can also come up with it's own transport implementation, and, as long as they follow the interface, it would work with any system that uses libp2p.

## Use of transport in our awesome-p2p-chat-system
>TODO: explain that in the end you would have a way to communicate with other peers for out chat system

A chat application needs to make use of communication protocols to deliver messages from one user to another. To decide which protocol fits best our chat, we need to consider their different features and filter out the ones that don't provide the functionalities that our chat requires. For example, the UDP protocol does not guarantee that messages even arrive at the destination, which is clearly unacceptable for a chat.

## Additional Reference
[simpleaswater/transport](https://simpleaswater.com/transport/)