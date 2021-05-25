

### Braid group cryptography
 {#BraidGroupCryptographyReferences}

Partly motivated by the possibility of [[quantum computation]] eventually breaking the security of [[cryptography]] based on [[abelian groups]], such as [[elliptic curves]], there are proposals to use [[non-abelian group|non-abelian]] [[braid groups]] for purposes of [[cryptography]] ("post-quantum cryptography").


#### Via Conjugacy Search

An early proposal was to use the _Conjugacy Search Problem_ in [[braid groups]] as a computationally hard problem for cryptography. This approach, though, was eventually found not to be viable.

Original articles:

* Iris Anshel, M. Anshel and D. Goldfeld, _An algebraic method for public-keycryptography_, Math. Research Letters 6 (1999), 287–291 ([pdf](https://www.intlpress.com/site/pub/files/_fulltext/journals/mrl/1999/0006/0003/MRL-1999-0006-0003-a003.pdf))

* K.H. Ko, S.J. Lee, J.H. Cheon , J.W. Han, J. Kang, C. Park , _New Public-Key Cryptosystem Using Braid Groups_, In: M. Bellare (ed.) _Advances in Cryptology — CRYPTO 2000_  Lecture Notes in Computer Science, vol 1880. Springer 2000 ([doi:10.1007/3-540-44598-6_10](https://doi.org/10.1007/3-540-44598-6_10))

Review:

* Karl Mahlburg, _An Overview of Braid Group Encryption_, 2004 ([pdf](http://www.math.wisc.edu/~boston/mahlburg.pdf))

* Parvez Anandam, _Introduction to Braid Group Cryptography_, 2006 ([pdf](https://courses.cs.washington.edu/courses/csep590/06wi/finalprojects/anandam.pdf))

* David Garber, _Braid Group Cryptography_, Lecture Notes Series, Institute for Mathematical Sciences, National University of Singapore ([arXiv:0711.3941](https://arxiv.org/abs/0711.3941), [doi:10.1142/9789814291415_0006](https://doi.org/10.1142/9789814291415_0006))

* Cryptowiki, _[Cryptosystems based on braid groups](http://cryptowiki.net/index.php?title=Cryptosystems_based_on_braid_groups)_


#### Via E-multiplication

A followup proposal was to use the problem of _reversing E-multiplication_ in braid groups, thought to remedy the previous problems.

Original article:

* Iris Anshel, Derek Atkins, Dorian Goldfeld and Paul E Gunnells, _WalnutDSA(TM): A Quantum-Resistant Digital Signature Algorithm_ ([eprint:2017/058](https://eprint.iacr.org/2017/058))

Review:

* Magnus Ringerud, _WalnutDSA: Another attempt at braidgroup cryptography_, 2019 ([pdf](https://ntnuopen.ntnu.no/ntnu-xmlui/bitstream/handle/11250/2622842/no.ntnu%3Ainspera%3A2452886.pdf?sequence=1&isAllowed=y))

But other problems were found with this approach, rendering it non-viable.

Original article:

* Matvei Kotov, Anton Menshov, Alexander Ushakov, _An attack on the Walnut digital signature algorithm_, Designs, Codes and Cryptography volume 87, pages 2231–2250 (2019) ([doi:10.1007/s10623-019-00615-y](https://doi.org/10.1007/s10623-019-00615-y))

Review:

*  José Ignacio Escribano Pablos, María Isabel González Vasco, Misael Enrique Marriaga and Ángel Luis Pérez del Pozo, _The Cracking of WalnutDSA: A Survey_, in: _Interactions between Group Theory, Symmetry and Cryptology_, Symmetry 2019, 11(9), 1072 ([doi:10.3390/sym11091072](https://doi.org/10.3390/sym11091072))

#### Further developments

The basic idea is still felt to be promising:

* Xiaoming Chen, Weiqing You, Meng Jiao, Kejun Zhang, Shuang Qing, Zhiqiang Wang, _A New Cryptosystem Based on Positive Braids_ ([arXiv:1910.04346](https://arxiv.org/abs/1910.04346))


* Garry P. Dacillo, Ronnel R. Atole,  _Braided Ribbon Group $C_n$-based Asymmetric Cryptography_, Solid State Technology Vol. 63 No. 2s (2020) ([JSST:5573](http://www.solidstatetechnology.us/index.php/JSST/article/view/5573))

But further attacks are being discussed:

* James Hughes, Allen Tannenbaum, *Length-Based Attacks for Certain Group Based Encryption Rewriting Systems* ([arXiv:cs/0306032](https://arxiv.org/abs/cs/0306032))

As are further ways around these:

* Xiaoming Chen, Weiqing You, Meng Jiao, Kejun Zhang, Shuang Qing, Zhiqiang Wang, *A New Cryptosystem Based on Positive Braids* ([arXiv:1910.04346](https://arxiv.org/abs/1910.04346))




