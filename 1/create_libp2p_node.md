Create a basic libp2p node
==========================
* As discussed, libp2p-core module is just a list of what jobs libp2p can perform. To actually be able to perform these jobs, other libp2p modules are necessary. There could be multiple modules that can provide implementations for these jobs but they do it in different ways. For every application built with libp2p a decision needs to be made on which modules are used to provide implementation for the desired tasks and our chat is nothing less!

* All modules could be added through options

* Examples of creating options and setting up config for each options (Refer: https://github.com/libp2p/js-libp2p/blob/8bed8f39ff3975850191cec93b7537d1428c8629/doc/CONFIGURATION.md#configuration-examples
)
* All the fields in the option also gives a brief overview of what libp2p is built of. 
* Tip: I use utils.promisify to convert the create p2p node into promise rather than callback. This makes the code look cleaner. The current latest version by default returns a promise. 
* Your Turn:
    - Include the libp2p core, and utils
    - Declare an empty option map for now. 
    - Create an async main, and inside main, call the create libp2p node and pass options
    - Call main



<!-- tabs:start -->

#### ** Template **

[embedded-code](./assets/1.2-template-code.js ':include :type=code embed-template')

#### ** Solution **

[embedded-code-final](./assets/1.2-finished-code.js ':include :type=code embed-final')

#### ** Previous Chapter Solution **

[embedded-code-previous](./assets/1.1-finished-code.js ':include :type=code embed-previous')

<!-- tabs:end -->