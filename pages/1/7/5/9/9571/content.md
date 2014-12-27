


#Contents#
* table of contents
{:toc}

## Idea

The _Grothendieck-Teichm&#252;ller tower_ construction involves [[moduli spaces]] outlined in [[Grothendieck]]'s _[[Esquisse d'un programme]]_ and then developed by [[Vladimir Drinfel'd]] and others. It involves the [[Teichmüller groupoids]] which are the [[fundamental groupoids]] of [[moduli stacks]] of [[genus]] $g$ [[curves]] with $n$ points removed. It is a basis for the definition of the _Grothendieck-Teichm&#252;ller group_ which is by the definition inertia-preserving [[automorphism group]] of the Grothendieck-Teichm&#252;ller tower. 

## Definitions

...

### Grothendieck-Teichm&#252;ller Lie algebra

GT Lie algebra appears as the tangent Lie algebra to the GT group.

Drinfel'd defined it more explicitly as follows. 

Let $\mathfrak{lie}_n$ be the degree completion of the [[free Lie algebra]] on $n$-generators over a fixed ground field $K$ of characteristic $0$. 
Let $\mathfrak{der}_n$ be the space of $K$-linear derivations $\mathfrak{lie}_n\to
\mathfrak{lie}_n$. A derivation $u\in\mathfrak{der}_n$ is __tangential__ if there exist
$a_i\in\mathfrak{lie}_n$ for $i=1,\ldots,n$, such that $u(x_i)=[x_i,a_i]$. In particular, $u$ is determined by elements $a_1,\ldots,a_n$ and is below denoted
by $(a_1,\ldots,a_n)$. The tangential derivations form a Lie subalgebra
$\mathfrak{tder}_n\subset\mathfrak{der}_n$. The __GT Lie algebra__ is the subspace
$\mathfrak{grt}\subset\mathfrak{tder}_2$ consisting of the tangential derivations
of the form $(0,\psi)$, where the identities
$$
\psi(x,y)=-\psi(y,x),\,\,\,for\,\,\,all\,\,\,x,y,
$$
$$
\psi(x,y)+\psi(y,z)+\psi(z,x) = 0,\,\,\,whenever\,\,\,\,x+y+z=0,
$$
and the pentagon-type identity
$$
\psi(t^{1,2},t^{2,34})+\psi(t^{12,3},t^{3,4})=
\psi(t^{2,3},t^{3,4})+\psi(t^{1,23},t^{23,4})+\psi(t^{1,2},t^{2,3}),
$$
hold, and which is equipped with the __Ihara Lie bracket__
$$
[\psi_1,\psi_2]_{Ihara} = (0,\psi_1)(\psi_2)-(0,\psi_2)(\psi_1)+[\psi_1,\psi_2].
$$


## Properties

### Relation to Drinfeld associators

The GT group acts freely on the set of [[Drinfeld associators]].

### Relation to the absolute Galois group of the rational numbers

+-- {: .num_theorem}
###### Theorem 
**(Drinfeld, Ihara, Deligne)**

There is an inclusion of the [[absolute Galois group]] of the [[rational numbers]] into the Grothendieck-Teichm&#252;ller group (recalled e.g. [Stix 04, theorem 6](#Stix04)).

=--


### Relation to the motivic Galois group

The Grothendieck-Teichm&#252;ller group is supposed to be a [[quotient]] of the [[motivic Galois group]]. This is a conjecture due to ([Drinfeld 91](#Drinfeld91)). 



### Relation to the graph complex
 {#RelationToTheGraphComplex}

The Grothendieck-Teichm&#252;ller Lie algebra is isomorphic to the 0th cohomology of [[Kontsevich]]'s [[graph complex]] ([Willwacher 10](#Willwacher10)). 




### Relation to deformation quantization and the cosmic Galois group

[[Grothendieck]] predicted that the GT group is closely related to the absolute Galois group. [[Maxim Kontsevich]] later conjectured its [[action]] on certain space of [[quantum field theories]] and outlined its [[motivic cohomology|motivic]] aspects. 

This was later proven by [[Vasily Dolgushev]], see at _[formal deformation quantization -- Motivic Galois group action on the space of quantizations](deformation+quantization#MotivicGaloisGroup)_ for details and pointers.

For more see also at _[[cosmic Galois group]]_ for more on this.

## Related concepts

* [[stable symplectic category]],

* [[motivic Galois group]], [[cosmic Galois group]]

## References

### General

The Grothendieck-Teichm&#252;ller group $GRT$ was originally introduced in

* [[Vladimir Drinfel'd]], _On quasitriangular quasi-Hopf algebras and on a group that is closely connected with $Gal(\overline{\mathbb{Q}/\mathbb{Q}})$_, [abs](http://mi.mathnet.ru/aa199), Rossi&#301;skaya Akademiya Nauk. Algebra i Analiz (in Russian) 2 (4): 149&#8211;181, ISSN 0234-0852, MR1080203 translation in Leningrad Math. J. 2 (1991), no. 4, 829&#8211;860

inspired by

* [[Alexander Grothendieck]], _Sketch of a program_, London Math. Soc. Lect. Note Ser., 242, Geometric Galois actions, 1, 5&#8211;48, Cambridge Univ. Press, Cambridge, 1997.

See also

*  Leila Schneps, Pierre Lotchak, _Geometric Galois actions_, 1, London Math. Soc. Lecture Note Ser. 242 ([doi](http://dx.doi.org/10.1017%2FCBO9780511666124))-- it contains a reprint of Groethendieck's Esquisse and some surveys by contributors, including Leila Schneps, _The Grothendieck-Teichmueller group GT: a survey_, [pdf](http://www.math.jussieu.fr/~leila/SchnepsGT.pdf)

* [[Maxim Kontsevich]], _Operads and motives in deformation quantization_, Lett. Math. Phys. 48 (1999), 35-72,  [math.QA/9904055](http://arxiv.org/abs/math/9904055)

The following monograph is in progress:

* Benoit Fresse, _Operads and Grothendieck-Teichm&#252;ller groups_, [hal-00656333](http://hal.archives-ouvertes.fr/hal-00656333), [pdf](http://hal.archives-ouvertes.fr/docs/00/65/63/33/PDF/OperadGT-January2012Preprint.pdf) - extract for a school, Jan 2012 (200 pages); _Homotopy of operads and GT groups_, December draft [pdf](http://math.univ-lille1.fr/~fresse/OperadHomotopyBook/OperadGT-December2012Preprint.pdf) 317 pp. 

> The ultimate objective of this book is to prove that the Grothendieck-Teichm&#252;ller group is the group of homotopy automorphisms of a rational completion of the little 2-discs operad.

* Newton Instititute Programme Jan-April 2013: Grothendieck-Teichm&#252;ller Groups, Deformation and Operads, [seminars](http://www.newton.ac.uk/programmes/GDO/seminars/index.html) (some with videos)


## References

The Drinfeld conjeture is stated in

* [[Vladimir Drinfel'd]], _On quasi-triangular Quasi-Hopf algebras and a group closely related with $Gal(\overline{\mathbb{Q}/\mathbb{Q}})$, Leningrad Math. J., 2 (1991), 829 - 860.
 {#Drinfeld91}

Relation to the graph complex

* [[Thomas Willwacher]], _M. Kontsevich's graph complex and the Grothendieck-Teichmueller Lie algebra_ ([arXiv:1009.1654](http://arxiv.org/abs/1009.1654))
 {#Willwacher10}

* {#Stix04} [[Jakob Stix]], _The Grothendieck-Teichm&#252;ller group and Galois theory of the rational numbers_, 2004 ([[StiXGaloisAndGT.pdf:file]])

* [[Anton Alekseev]], Charles Torossian, _The Kashiwara-Vergne conjecture and Drinfeld's associators_, [arxiv/0802.4300](http://arxiv.org/abs/0802.4300)

[[!redirects Grothendieck-Teichmueller tower]]
[[!redirects Grothendieck-Teichmüller group]]
[[!redirects Grothendieck-Teichmuller tower]]
[[!redirects Grothendieck-Teichmuller group]]

[[!redirects Grothendieck-Teichmueller group]]

[[!redirects groupe de Grothendieck-Teichmüller]]
