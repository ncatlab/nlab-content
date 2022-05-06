In [[computer science]], a virtual machine is a simulation of a fixed architecture executing some sort of signaling or software. It can abstract an entire or part of hardware,  firmware, a file system with some ports, devices and/or CPU and installed operating system, but it can be simply an isolated environment executing some specified class of software, or simply any installation in hardware or in another virtual machine of a specified execution model. For example, Java Virtual Machine executes formally specified "bytecode" to ensure identical execution on all hardware.

See also [[certified programming]], [[WebAssembly]]

## Virtual machines for cloud

### Virtual machine simulating machine with operating system

...

### Containers

...

### Blockchain runtimes for multiple blockchains

Microsoft Azure develops a runtime framework intended to work on various blockchains. This is the CoCo project (see whitepaper 2017 at github [pdf](https://github.com/Azure/coco-framework/blob/master/docs/Coco%20Framework%20whitepaper.pdf), [announcement](https://azure.microsoft.com/en-us/blog/announcing-microsoft-s-coco-framework-for-enterprise-blockchain-networks) and a presentation on [Medium](https://medium.com/@jrodthoughts/with-coco-framework-microsoft-wants-to-become-the-redhat-of-the-blockchain-5b35f8ac8707)).


## Languages for simulation of devices

...

## Bytecode virtual machines


### Java Virtual Machine

Java VM has a specification which executes Java bytecode. Several languages compile to JVM including Java, Kotlin and Scala.

* [java (language)](http://en.wikipedia.org/wiki/Java_%28programming_language%29), [java (platform)](http://en.wikipedia.org/wiki/Java_%28software_platform%29)
* [kotlin](https://kotlinlang.org)
* [scala](http://en.wikipedia.org/wiki/Scala_%28programming_language%29)
* [scalaz](https://github.com/scalaz/scalaz) - library for functional programming in scala

### WebAssembly VM

WebAssembly is optimized for small compiling time and near native execution time on major architectures (like 86 series). It appeared first as new VM standard
on web browsers, backed by major internet companies; it is also used or planned on a number of [[blockchain]] projects.

* WebAssembly [wikipedia](https://en.wikipedia.org/wiki/WebAssembly), [spec](https://webassembly.github.io/spec), [webassembly.org](https://webassembly.org), [msdn](https://developer.mozilla.org/en-US/docs/WebAssembly) docs, [rust-to-wasm](https://developer.mozilla.org/en-US/docs/WebAssembly/Rust_to_wasm), [github](tps://github.com/WebAssembly)
* [WebAssembly-Links](https://wiki.parity.io/WebAssembly-Links) in Parity Tech Documentation
* AssemblyScript (maps a subset of javascript code to wasm) [github](https://github.com/AssemblyScript/assemblyscript), [news](https://www.infoworld.com/article/3224006/assemblyscript-compiles-typescript-to-webassembly.html)

[[Rust]] has small runtime, which is desirable in common applications of WebAssembly. Thus Rust commonly compiles either to native code or to wasm.

* Rust & WebAssembly with Nick Fitzgerald [yt](https://www.youtube.com/watch?v=ZiiTRxWk8gA)

Ethereum flavoured version of wasm VM specification is at github/[ewasm](https://github.com/ewasm), see also github/[ewasm/design](https://github.com/ewasm/design). eWasm has a [testnet](http://ewasm.ethereum.org/explorer). According to article _[ewasm explained](https://www.mycryptopedia.com/ewasm)_, 

> The ewasm specification consists of a subset of WebAssembly components suitable for Ethereum’s needs, namely determinism and relevant features. It also includes a number of system smart contracts that provide access to Ethereum platform features.

### IELE

Part of [[zoranskoda:Cardano]] project, IELE executes and verifies [[smart contract]]s as well as providing a human-readable language for blockchain developers.

* IELE, _Semantics based compilation_, at [iohkdev.io](https://testnet.iohkdev.io/iele/about/semantics-based-compilation)

### Ethereum VM

Primarily used for smart contract execution on Ethereum blockchain (and some others blockchains, like [[zoranskoda:Hyperledger]] Fabric). Ethereum community has plans to supercede it with Ethereum version of wasm VM (ewasm).

### TON VM

Used for executing smart contracts on [[Telegram Open Network]]. See

* [[Nikolai Durov]], _Telegram Open Network Virtual Machine_, Sep. 2018, 148 pp. [pdf](https://www.docdroid.net/R3vEKBY/telegram-open-network-virtual-machine-september-5-2018.pdf)

### CKB VM (Nervos)

This is a [RISC-V](https://en.wikipedia.org/wiki/RISC-V) VM for a Nervos blockchain design.  "Uses rv64imc architecture: it is based on core RV64I ISA with M standard extension for integer multiplication and division, and C standard extension for RCV(RISC-V Compressed Instructions)." No floating point.

* github [mb](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0002-ckb/0002-ckb.md), [code](https://github.com/nervosnetwork/ckb)

[[!redirects Virtual Machine]]
