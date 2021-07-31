Rust is an efficient programming language with compile time memory safety model based on the innovative notion of ownership and borrows, small runtime, modern concurency, zero cost abstractions, both object oriented and functional programming model. It's speed is about the speed of comparable C programs. Rust does not require garbage collector, hence it is useful for real time programming as garbage collectors periodically stall the system for order of 100 ms. It compiles both to native code (LLVM compilers are commonly used) and to [[WebAssembly]]. It is particularly useful for real time programming, systems programming, embedded systems, web programming (via WebAssembly), concurrent systems and safety critical applications including [[blockchain]] and [[smart contract]]s. It easily links to the languages in C/C++ (ABI) linking model.

* [rust-lang.org](https://www.rust-lang.org), the official rust [book](https://doc.rust-lang.org/book), [reference](https://doc.rust-lang.org/reference/index.html), [crates.io](https://crates.io)
* [what is rustdoc](https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html#using-rustdoc-with-cargo)
* Jim Blandy, Jason Orendorff, _Programming Rust: fast, safe systems development_, O’Reilly Media 2017
* Steve Klabnik, Carol Nichols, _The rust programming language_, no starch press, xxvii+519 pp., 2018
* Rust crashcourse Rustlang (2hr) [yt](https://www.youtube.com/watch?v=zF34dRivLOw)
* yandex Rust course (in Russian, А. А. Кладов) [2019-spring](https://compscicenter.ru/courses/rustprogramming/2019-spring)
* double linked list in safe Rust [github](https://gist.github.com/pythonesque/5943252fb464b49123fa), std::collections::[LinkedList](https://doc.rust-lang.org/std/collections/struct.LinkedList.html), but use VectDeque and see Learn Rust With Entirely [Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists)
* _IOKH launches [[zoranskoda:Cardano]] Rust project_ [cardanorust.iohkdev.io](https://cardanorust.iohkdev.io), [news](https://www.the-blockchain.com/2018/10/02/iohk-launches-cardano-rust-project) Feb 2018
* Rust can also compile to [RISC-V](https://en.wikipedia.org/wiki/RISC-V), see github/[riscv-rust](https://github.com/riscv-rust)
* exonom[.com](https://exonum.com), [doc](https://exonum.com/doc/version/latest) -- extensible open-source framework for creating (permissioned) blockchain applications, smart contracts replaced by supposedly more flexible notion of [services](https://exonum.com/doc/version/latest/architecture/services) (see [comparision](https://exonum.com/doc/version/latest/architecture/services/#services-vs-smart-contracts)). Exonum services can be coded in Rust or Java.
* [rustsim](https://www.rustsim.org) numerical lib. and linear algebra for Rust
* list of crates on neural networks in Rust is [here](https://www.arewelearningyet.com/neural-networks)
* [[zoranskoda:Hyperledger]] Sabre is a transaction family/processor for Wasm on Hyperledger [Sawtooth](https://www.hyperledger.org/category/hyperledger-sawtooth) blockchain framework github/hyperledger/[sawtooth-sabre](https://github.com/hyperledger/sawtooth-sabre)

Linking to C/C++ is usually done via rust-bindgen 

* github/[rust-lang/rust-bindgen](https://github.com/rust-lang/rust-bindgen); user guide [rust-lang.github.io/rust-bindgen](https://rust-lang.github.io/rust-bindgen)

Rust is commonly compiled either to the native code or optionally to [[WebAssembly]].

* Rust & WebAssembly with Nick Fitzgerald [yt](https://www.youtube.com/watch?v=ZiiTRxWk8gA)

Parity supports [Kovan](https://kovan.etherscan.io) testnet for future candidate version of Ethereum which supports wasm (hence one can use Rust), see

* _Toward a brighter future for smart contracts_, at [troubles.md](http://troubles.md/posts/rust-smart-contracts)

Rust on Parity Substrate can be used for smart contracting via Ink eDSL package

* github/paritytech/[ink](https://github.com/paritytech/ink), [medium](https://medium.com/block-journal/introducing-substrate-smart-contracts-with-ink-d486289e2b59)
* Shawn Tabrizi, [substrate contracts workshop](https://shawntabrizi.com/substrate-contracts-workshop/#)

Some research papers

* Oxide: The Essence of Rust ([arXiv:1903.00982](https://arxiv.org/abs/1903.00982))
* _RustBelt: securing the foundations of the rust programming language_ [doi](https://doi.org/10.1145/3158154) (open access)
* B. Lamowski et al. _Sandcrust: automatic sandboxing of unsafe components in Rust_, [doi](https://doi.org/10.1145/3144555.3144562)
* Garming Sam, Nick Cameron, Alex Potanin, _Automated refactoring of rust programs_,  ACSW '17: Proceedings of the Australasian Computer Science Week Multiconference [doi](https://doi.org/10.1145/3014812.3014826)
* _POSTER: Rust SGX SDK: Towards Memory Safety in Intel SGX Enclave_ [doi](https://doi.org/10.1145/3133956.3138824)

category: computer science

[[!redirects rust]]