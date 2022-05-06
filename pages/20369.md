Rust is an efficient programming language with compile time memory safety model based on the innovative notion of ownership and borrows, small runtime, modern concurency, zero cost abstractions, both object oriented and functional programming model. Rust does not require garbage collector, hence it is useful for real time programming as garbage collectors periodically sweep the memory and typically stall the system for order of 100 ms. It compiles both to native code (LLVM compilers are commonly used) and to [[WebAssembly]]. It is particularly useful for real time programming, systems programming, embedded systems, web programming (via WebAssembly), concurrent systems and safety critical applications including [[blockchain]] and [[smart contract]]s. It easily links to the languages in C/C++ (ABI) linking model.
 
* [rust-lang.org](https://www.rust-lang.org), the official rust [book](https://doc.rust-lang.org/book), [reference](https://doc.rust-lang.org/reference/index.html)
* [what is rustdoc](https://doc.rust-lang.org/rustdoc/what-is-rustdoc.html#using-rustdoc-with-cargo)
* Jim Blandy, Jason Orendorff, _Programming Rust: fast, safe systems development_, O’Reilly Media 2017
* Rust crashcourse Rustlang (2hr) [yt](https://www.youtube.com/watch?v=zF34dRivLOw)
* yandex Rust course (in Russian, А. А. Кладов) [2019-spring](https://compscicenter.ru/courses/rustprogramming/2019-spring)
* double linked list in safe Rust [github](https://gist.github.com/pythonesque/5943252fb464b49123fa), std::collections::[LinkedList](https://doc.rust-lang.org/std/collections/struct.LinkedList.html), but use VectDeque and see Learn Rust With Entirely [Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists)
* _IOKH launches [[zoranskoda:Cardano]] Rust project_ [news](https://www.the-blockchain.com/2018/10/02/iohk-launches-cardano-rust-project) Feb 2018
* Rust can also compile to [RISC-V](https://en.wikipedia.org/wiki/RISC-V), see github/[riscv-rust](https://github.com/riscv-rust)

Rust is commonly compiled either to the native code or optionally to [[WebAssembly]].

* Rust & WebAssembly with Nick Fitzgerald [yt](https://www.youtube.com/watch?v=ZiiTRxWk8gA)

category: computer science

[[!redirects rust]]