
#Contents#
* table of contents
{:toc}

## Idea

In [[computer science]], _cryptography_ is the art and science of securing communication and information through the use of [[mathematics|mathematical techniques]]. 

Its roots trace back to ancient civilizations where secret codes were employed to protect sensitive messages. The earliest known use of cryptography is attributed to the ancient Egyptians, who used [hieroglyphs to inscribe messages](https://www.redhat.com/en/blog/brief-history-cryptography) on monuments in a way that could only be understood by those with the knowledge of the secret key.

Today, cryptography relies on a wide variety of mathematical topics. Here is a non-exhaustive list of fields and topics that are particularly relevant to cryptography:

- **Number Theory** (modular arithmetic, prime numbers, and group theory in the context of modular arithmetic)

- **Abstract Algebra** (groups, rings, and fields such as Galois fields)

- **Algebraic Geometry** (elliptic curve cryptography and algebraic varieties over finite fields)

- **Combinatorics** (combinatorial designs and error-correcting codes)

- **Probability Theory** (randomized algorithms in cryptography and probability distributions relevant to cryptographic protocols

- **Graph Theory** (graph-based cryptographic algorithms
 and network flow algorithms in the context of network security)

- **Topology** (algebraic topology and homological algebra)

- **Logic** (in the context of formal verification and proof systems)

- **Complex Analysis** (analytic number theory)

- **Functional Analysis** (for signal processing and cryptographic protocols)


## Symmetric  and assymmetric cryptography

There are two fundamental types of cryptography: _symmetric_ and _asymmetric_. Symmetric cryptography involves the use of a single secret key $k$ for both encryption $E_k:M \to C$ and decryption $D_k:C \to M$. This key must be securely shared between the communicating parties. 

\[
\begin{array}{ccccc}
\mathsf{Bob} &\longrightarrow& \mathsf{Channel} & \longrightarrow &\mathsf{Alice}\\
m & \longrightarrow & E_k(m) & \longrightarrow & D_{k}(E_k(m)) = m
\end{array}
\]

On the other hand, asymmetric cryptography uses a pair of keys – a public key $k$ for encryption $E_k:M \to C$ and a private key $k'$ for decryption $D_{k'}:C \to M$. This asymmetric key pair allows for secure communication without the need for a shared secret, offering enhanced security in various scenarios.

\[
\begin{array}{ccccc}
\mathsf{Bob} &\longrightarrow& \mathsf{Channel} & \longrightarrow &\mathsf{Alice}\\
m & \longrightarrow & E_k(m) & \longrightarrow & D_{k'}(E_k(m)) = m
\end{array}
\]

In practice, Alice would generate both keys $k'$ and $k$ and would send the public key $k$ to Bob.

## Security and attacks

Security in cryptography is a constant battle against potential attacks. Common attacks include brute force, where an attacker systematically tries all possible keys, and cryptanalysis, which involves exploiting vulnerabilities in the cryptographic algorithm. 

Modern cryptographic systems aim to withstand these attacks, often relying on the complexity of mathematical problems, such as factoring large numbers or solving discrete logarithms, to ensure security.

### Complexity classes


[[complexity class|Complexity classes]] play a pivotal role in cryptography, providing a framework to analyze the efficiency and security of cryptographic algorithms. 

The study of computational complexity helps assess the computational resources required to break a cryptographic scheme, distinguishing between feasible and infeasible attacks. 


### Invertibility principle

In cryptography, the concept of invertibility is essential for ensuring secure decryption. When plaintext undergoes encryption through the encryption algorithm $E_k:M \to C$, the efficacy of the system depends on the ease of decryption for authorized users and the complexity it imposes on unauthorized attempts.

[[bijection|Bijections]] (or [[inverse|isomorphisms]]) $E:M \to C$ whose inverses $D = E^{-1}:C \to M$ are hard to compute provide practical examples of this principle. Such bijections $(E,D)$ establish a one-to-one relationship between plaintext $M$ and ciphertext $C$, enabling straightforward decryption given suitable information (constituting the potential private key $k$) while posing a significant challenge for unauthorized attempts.

Mathematically, we could imagine that Alice and Bob have access to a groupoid $\mathcal{G}$ and a category $\mathcal{C}$, respectively, such that $\mathcal{C}$ is embedded in $\mathcal{G}$ via an inclusion functor.
\[
\mathcal{C} \hookrightarrow \mathcal{G}
\]
The security of a cryptosystem would then rely on the difficulty of reconstructing this inclusion using an algorithmic completion procedure.

These mathematical principles form the foundation for secure cryptosystems, ensuring that only authorized users can successfully decrypt and access sensitive information.

\begin{remark}
Note that there is flexibility in considering weaker notions of isomorphisms, especially if Alice can employ these weaker isomorphisms effectively in the decryption of the message $m$ from the data $D_{k'}(E_k(m))$.
\[
D_{k'}(E_k(m)) \leftrightarrows m
\]
In category theory, examples of these weaker notions can be derived from higher category theory. This includes concepts such as [[adjoint equivalence|adjoint equivalences]], [[algebras for an endofunctor|algebras]], [[coalgebras|coalgebras]], and [[retractions|retractions]].
\end{remark}

## Post-quantum cryptography

With the advent of [[quantum computation|quantum computers]], there is growing concern about the potential threat they pose to existing cryptographic systems. Post-[[quantum cryptography]] is an evolving field that explores algorithms resistant to quantum attacks. 

Researchers are developing cryptographic schemes that rely on mathematical problems difficult for both classical and quantum computers to solve, ensuring the continued security of communication in the post-quantum era.

### Useful links

* [NTRU](https://en.wikipedia.org/wiki/NTRU)

* [LWE](https://en.wikipedia.org/wiki/Learning_with_errors) and [RLWE](https://en.wikipedia.org/wiki/Ring_learning_with_errors)

* [[braid group cryptography -- references|Braid group cryptography]]

## Homomorphic cryptography

[[homomorphism|Homomorphic]] cryptography takes a unique approach by allowing the processing of operations $\square$ on encrypted data without decrypting it first. 

\[
D(E(m_1) \square E(m_2)) = m_1 \square m_2
\]

This field aims to preserve privacy while still enabling meaningful computations on sensitive information. 

Fully homomorphic cryptography, [a subset of homomorphic cryptography](https://en.wikipedia.org/wiki/Homomorphic_encryption), extends this concept to support arbitrary computations on encrypted data, opening new possibilities for secure and privacy-preserving data processing in various applications, including cloud computing and data analytics.



### Related concepts

* [[group|Group]]-[[homomorphism|homomorphisms]]

* [[ring|Ring]]-[[homomorphism|homomorphisms]]

* [[functor|Functors]]

* [[monoidal functor|Monoidal functors]]


## Related entries

* [[arithmetic cryptography]]

* [[digital identity]], 

* [[information theory]], 

* [[quantum cryptography]], [[quantum information theory]]

* [[quantum computing]], 

* [[blockchain]]

* zoranskoda: [[zoranskoda:computer security]], [[zoranskoda:blockchain]], [[zoranskoda:blockchain security]], [[zoranskoda:digital identity]]


## References

### General

* Wikipedia, _[Outline of cryptography](https://en.wikipedia.org/wiki/Outline_of_cryptography)_, [public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography), [cryptographic protocol](https://en.wikipedia.org/wiki/Cryptographic_protocol), [authentication](https://en.wikipedia.org/wiki/Authentication), [zero-knowledge proof](https://en.wikipedia.org/wiki/Zero-knowledge_proof), [non-interactive zero-knowledge proof](https://en.wikipedia.org/wiki/Non-interactive_zero-knowledge_proof), [OAuth](https://en.wikipedia.org/wiki/OAuth), [homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption)

* post-quantum cryptography at [nist.gov](https://csrc.nist.gov/Projects/Post-Quantum-Cryptography)

[[probability theory|probabilistic]]:

* Shafi Goldwasser, Silvio Micali, _Probabilistic encryption_, Journal of Computer and System Sciences 28:2 (1984) 270-299


### Verified software
 {#VerifiedSoftwareReferences}

On [[verified software]] for cryptography:

* [[Mihhail Aizatulin]], Franccois Dupressoir, Andrew D. Gordon, Jan Jürjens, *Verifying Cryptographic Code in C: Some Experience and the Csec Challenge* ([pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/MSR-TR-2011-118.pdf)) 

* [[Mihhail Aizatulin]], Andy Gordon, Jan Jürjens, *Extracting and Verifying Cryptographic Models from C Protocol Code by Symbolic Execution*, CCS '11 Proceedings of the 18th ACM Conference on Computer and Communications Security 2011 ([pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/11/extracting.pdf))


* Matthias Berg, *Formal Verification of Cryptographic Security Proofs*, 20013 ([pdf](https://publikationen.sulb.uni-saarland.de/bitstream/20.500.11880/26584/1/thesis_berg.pdf), [doi:10.22028/D291-26528](http://dx.doi.org/10.22028/D291-26528))

* [[Adam Petcher]], *A Foundational Proof Framework for Cryptography*, 2014 ([pdf](https://dash.harvard.edu/bitstream/handle/1/17463136/PETCHER-DISSERTATION-2015.pdf), [harvard:17463136](https://dash.harvard.edu/handle/1/17463136))

* [[Adam Petcher]], Greg Morrisett, *The Foundational Cryptography Framework*,  In: R. Focardi, A. Myers (eds.) *Principles of Security and Trust* POST 2015. Lecture Notes in Computer Science, vol 9036. Springer, Berlin, Heidelberg ([doi:10.1007/978-3-662-46666-7_4](https://doi.org/10.1007/978-3-662-46666-7_4))

* Andrew W. Appel, *Verification of a Cryptographic Primitive: SHA-256*, ACM Transactions on Programming Languages and SystemsApril 2015 Article No.: 7 ([doi:10.1145/2701415](https://doi.org/10.1145/2701415), [pdf](https://www.cs.princeton.edu/~appel/papers/verif-sha.pdf))


* Andres Erbsen, Jade Philipoom, [[Jason Gross]], Robert Sloan, [[Adam Chlipala]], *Simple High-Level Code for Cryptographic Arithmetic - With Proofs, Without Compromises*, [2019 IEEE Symposium on Security and Privacy (SP)](https://ieeexplore.ieee.org/xpl/conhome/8826229/proceeding) $[$[doi:10.1109/SP.2019.00005](https://doi.org/10.1109/SP.2019.00005)$]$

* [[Mihhail Aizatulin]], *Verifying Cryptographic Security Implementations in C Using Automated Model Extraction* ([arXiv:2001.00806](https://arxiv.org/abs/2001.00806))



On [[type theory]] for [[verified programming|verified]] cryptography:

* Cédric Fournet, Karthikeyan Bhargavan, Andrew D. Gordon, *Cryptographic Verification by Typing for a Sample Protocol Implementation*, In: Aldini A., Gorrieri R. (eds) Foundations of Security Analysis and Design VI. FOSAD 2011. Lecture Notes in Computer Science, vol 6858. Springer (2011) ([doi:10.1007/978-3-642-23082-0_3]( https://doi.org/10.1007/978-3-642-23082-0_3))

* Cédric Fournet, Markulf Kohlweiss, [[Pierre-Yves Strub]], *Modular code-based cryptographic verification*, CCS '11: Proceedings of the 18th ACM conference on Computer and communications securityOctober 2011 Pages 341–350 ([doi:10.1145/2046707.2046746](https://doi.org/10.1145/2046707.2046746))


On [[homotopy type theory]] for [[verified programming|verified]] cryptography:

* [[Paventhan Vivekanandan]], *A Homotopical Approach to Cryptography*, talk at [FCS 2018](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf) ([pdf](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf), [easychair:GLtQ#](https://easychair.org/smart-slide/slide/GLtQ#)), In: Charles Morisset and Limin Jia (eds.) FCS Informal Proceedings  **[55](http://t-news.cn/Floc2018/FLoC2018-pages/volume55.html)** (2018) 

* [[Paventhan Vivekanandan]], *HoTT-Crypt: A Study in Homotopy Type Theory based on Cryptography*, Kalpa Publications in Computing Volume 9, 2018, Pages 75-90 ([doi:10.29007/tvpp](https://doi.org/10.29007/tvpp), [web slides](https://easychair.org/smart-slide/slide/WSST#), [[VivekanandanHoTTCryptography.pdf:file]])


category: applications, computer science


[[!redirects encryption]]

[[!redirects braid group cryptography]]

