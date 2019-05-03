See also [[virtual machine]], [[zoranskoda:hyperledger]], [[zoranskoda:EOS]], [[Rust]].

__WebAssembly__ (wasm) is a modern low level language (mimicking assembly code, but independent of a machine) intended for execution a [[virtual machine]]. It is represented in one of the three common forms. Virtual machine accepts the bytecode version. The corresponding assembly like representation is also used where the commands are given the names as usual. The third is lisp-like bracketed notation, the so called S-expression representation (which is complemented by a little bit of additional information not explicit in assembly like representation).
It is optimized for small compiling time and near native execution time, at least when implemented on a virtual machine on one of major [computer architectures](https://en.wikipedia.org/wiki/Instruction_set_architecture) (like the x86 or ARM series). It is created as a new VM standard for web browsers, backed by major internet companies; it is also used or planned on a number of [[blockchain]] projects, most notably Parity [[zoranskoda:substrate|Substrate]]. On web browsers it is highly interoperable with JavaScript.

* WebAssembly [wikipedia](https://en.wikipedia.org/wiki/WebAssembly), [spec](https://webassembly.github.io/spec), [webassembly.org](https://webassembly.org), [msdn](https://developer.mozilla.org/en-US/docs/WebAssembly) docs, [rust-to-wasm](https://developer.mozilla.org/en-US/docs/WebAssembly/Rust_to_wasm), [github](tps://github.com/WebAssembly)
* [WebAssembly-Links](https://wiki.parity.io/WebAssembly-Links) in Parity Tech Documentation
* AssemblyScript (maps a subset of javascript code to wasm) [github](https://github.com/AssemblyScript/assemblyscript), [news](https://www.infoworld.com/article/3224006/assemblyscript-compiles-typescript-to-webassembly.html)
* How does WASM get interpreted by the EOS virtual machine? [eosio.stackexchange](https://eosio.stackexchange.com/questions/167/how-does-wasm-get-interpreted-by-the-eos-virtual-machine)

[[Rust]] language has small runtime, which is desirable in common applications of WebAssembly. Thus Rust commonly compiles either to native code or to wasm.

* [www.rust-lang.org/what/wasm](https://www.rust-lang.org/what/wasm)
* Rust and wasm official [rustwasm.github.io/docs/book](https://rustwasm.github.io/docs/book)
* K. Hoffman, _Programming Webassembly with Rust_, book
* Nick Fitzgerald, _Rust & WebAssembly_, [yt](https://www.youtube.com/watch?v=ZiiTRxWk8gA)

General support for wasm outside of browsers is not yet standardized. One has to complement sandboxed wasm with some system calls to have reasonable functionality. WASI is a generic term for the wasm system interface.

* Lin Clark, _Standardizing WASI: A system interface to run WebAssembly outside the web_ [2019/03](https://hacks.mozilla.org/2019/03/standardizing-wasi-a-webassembly-system-interface); _WebAssembly’s post-MVP future: A cartoon skill tree_ [2018/10](https://hacks.mozilla.org/2018/10/webassemblys-post-mvp-future))
* wasmer is a standalone for wasm applications, see [github](https://github.com/wasmerio/wasmer), [wasmer.io](https://wasmer.io), [this](https://changelog.com/podcast/341) podcast of S. Akbary and article _WebAssembly & CloudABI_, [Medium](https://medium.com/wasmer/webassembly-cloudabi-b573047fd0a9)
* github/CraneStation/[wasmtime](https://github.com/CraneStation/wasmtime)
* medium/[running-webassembly-from-any-language](https://medium.com/wasmer/running-webassembly-from-any-language-5741f6320ccd)

Efficiency of wasm and its standardization and programming tools support make wasm VM ideal for distributed ledger applications. Ethereum flavoured version of wasm VM specification is at github/[ewasm](https://github.com/ewasm), see also github/[ewasm/design](https://github.com/ewasm/design). eWasm has a [testnet](http://ewasm.ethereum.org/explorer). According to article _[ewasm explained](https://www.mycryptopedia.com/ewasm)_, 

> The ewasm specification consists of a subset of WebAssembly components suitable for Ethereum’s needs, namely determinism and relevant features. It also includes a number of system smart contracts that provide access to Ethereum platform features.

[[zoranskoda:EOS]] is a [[high performance distributed ledger]] using wasm VM. 

* Shankar Nathan, _How to deploy and run a smart contract on the EOS blockchain_, [web](https://hackernoon.com/how-to-deploy-and-run-a-smart-contract-on-the-eos-blockchain-from-zero-to-hero-72ca592803ba)
* gurghet, [Write EOS contracts in Rust instead of C++](https://steemit.com/crypto/@gurghet/write-eos-contracts-in-rust-instead-of-c)


category: computer science