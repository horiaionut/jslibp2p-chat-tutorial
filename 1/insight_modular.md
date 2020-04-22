## Insight into Libp2p
* The above problem of having multiple standards for the same job is prevalent all across network protocols like `peer-discover`, `pubsub`, `encryption`, etc. And this is one of the main problems that libp2p aims to solve. 
* It doesn't aims to create a *n+1th* protocol but to support all the previous *n* protocols in a standard way.
* This is why `libp2p` is mostly just a documentation/specification. Check it out [here](https://github.com/libp2p/specs). Every implementation (go, rust, js, python) would follow the same specification. 

* Thorough understanding the above specification gives a good brief about what libp2p is capable of doing and which are the APIs to use for a particular task. 
* The idea that it is completely a language or any specific protocol agnostics makes it highly modular (and also some times confusing).

## Understanding the Core libp2p-js Module
* The libp2p-js core module itself is nothing. It is just a skeleton with all the interfaces. You can easily plug all the modules that obey the interface. Libp2p already provides the implementation of a lot of modules which do so (check it out [here](https://libp2p.io/bundles/)) which you can easily plug.
* To better understand how the library works, let us talk about interfaces. An interface defines what functionalities exit. It defines what the input and output of these functions are. What is not in an interface is the implementations of these functions, the way they are carried out. A good example can be found [here](https://stackoverflow.com/questions/2866987/what-is-the-definition-of-interface-in-object-oriented-programming).
* Therefore libp2p-js core module is not enough since it does not provide any implementation. To use an interface provided by this module we need to add another module that implements the interface. For a given interface there could be multiple modules that provide different implementations and therefore an informed decision has to be made.

## Creating a simple bundle 
* First, install the libp2p dependency. We'll also need at least one transport module, so we'll pull in libp2p-tcp as well, and the @nodeutils/defaults-deep helper which we'll use when building the bundle.
```bash
    $ npm install libp2p@^0.26.2 libp2p-tcp@^0.13.2 @nodeutils/defaults-deep@^1.1.0 --save
```
* try it yourself 