
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An __$H$-space__ ("H" for [[Heinz Hopf|Hopf]], as in _[[Hopf construction]]_) is a [[magma]] [[internalization|internal to]] the [[classical homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category $Ho(Top)_*$ of [[pointed topological spaces]],  which has a [[unit]] up to [[homotopy]]. 

Similarly:

* An **[[H-monoid|$H$-monoid]]** is a [[monoid object]] in [[Ho(Top)]], hence an $H$-space is an $H$-monoid if the product of the magma is [[associativity|associative]] up to [[homotopy]]. 

* An __$H$-group__ (or *grouplike space*) is a [[group object]] in [[Ho(Top)]], so an $H$-monoid is an $H$-group if it also has [[inverses]] up to homotopy (cf. [Arkowitz 2011 Def. 2.2.1](#Arkowitz11)).

* An **$H$-ring** is a [[ring object]] in (pointed) [[Ho(Top)]].

To continue in this pattern, one could say that an **[[H-category]]** is a category internal to [[Ho(Top)]].

Notice that here the homotopies for units, associativity etc. are only required to _exist_ for an H-space, not required to be equipped with higher [[coherence|coherent]] homotopies. An $H$-monoid equipped with such higher and coherent homotopies  is instead called a _strongly homotopy associative_ space or  _$A_\infty$-[[A-infinity space|space]]_ for short.  If it has only higher homotopies up to level $n$, it is called an $A_n$-[[A-n space|space]].

A better name for an $H$-space might be $H$-[[unitoid]], but it is rarely used. The $H$ stands for [[Heinz Hopf]], and reflects the sad fact that the natural name 'homotopy group' was [[homotopy group|already occupied]]; Hopf and A. Borel found necessary algebraic conditions for a space to admit an $H$-space structure.

There are dual notions of $H$-counitoid (or $H'$-space, or [[co-H-space]]), $H$-comonoid (or $H'$-monoid) and $H$-[[cogroup]] (or $H'$-group) having co-operations with the usual identities up to homotopy. 

## Examples

\begin{example}
**(topological groups)** \linebreak
  The [[topological groups]] are the $H$-groups where all the [[axioms]] ([[unitality]], [[associativity]] and [[inverses]]) hold even as [[equalities]] and not just as [[homotopies]].
\end{example}

\begin{example}
**(loop spaces)** \linebreak
For $X$ a [[pointed topological space]] its based [[loop space]] is an $H$-group under concatenation and reversal of loops.  

Of course, loop groups have a much more structured grouplike structure: They are grouplike [[A-infinity spaces|$A_\infty$-spaces]] also called *[[infinity-groups|$\infty$-groups]]*.

Generally, if an $H$-space is equivalent to a [[delooping|deloopable one]], then it is a [[groupoid object in an (infinity,1)-category|group object in the (∞,1)-category]] [[Top]]. In other words, in that case, the associativity and other axioms hold up to [[coherence|coherent]] [[higher homotopy]]. 
\end{example}

 

\begin{example}
**(suspensions)** \linebreak
The main example of [[co-H-space|H-cogroups]] in $Top_*$ are [[reduced suspensions]] $S X= S^1\wedge X$ of [[pointed topological spaces]] $X$. 
\end{example}

\begin{example}
**(sphere)**
\linebreak
The only [[n-spheres]] $S^n$ which have $H$-space structure are those with $n = 0, 1, 3, 7$. Their H-space structure is given by identifying them as the [[unit spheres]] in one of the four [[normed division algebras]] ([[real numbers]], [[complex numbers]], [[quaternions]], [[octonions]]) and taking the product to be that induced by the algebra product.

The [[7-sphere]] $S^7$ is an example of an H-space that does not lift to an [[A-infinity space|$A_\infty$-space]]. It can't be delooped because its would-be [[delooping]] would have [[cohomology group]] a [[polynomial ring]] on a generator in degree 8, and this is impossible by mod $p$ [[Steenrod operations]] for any odd $p$ (cf. [Adams 1961 Lemma 2](#Adams61). The 7-sphere is also not an $H$-group.
\end{example}

\begin{example}
**(Mapping spaces into H-groups)**
If $K$ is an $H$-group then for any topological space $X$, the set of [[homotopy classes]] $[X,K]$ of [[maps]] $X \to K$ has a natural group structure in the strict sense. Analogously, if $K'$ is an $H$-cogroup then $[K',X]$ has a group structure. 

If there is more than one $H$-group structure on a space, then the induced group structures on the set of homotopy classes coincide. 
\end{example}


\begin{example}
**(K-Theory classifying space)** \linebreak
The [[classifying space]] $B U \times \mathbb{Z}$ for (complex) [[topological K-theory]] is an H-ring space (cf. p. 205 (213 of 251) in _[[A Concise Course in Algebraic Topology]]_.)
\end{example}

\begin{example}
  The _[[Dwyer-Wilkerson H-space]]_, see there for more.
\end{example}



## Properties

Let $A$ be a [[connected]] H-space. Then for every $a:A$, the [[maps]] $\mu(a,-),\mu(-,a):A \to A$ are [[homotopy equivalences]].

### Nilpotency

Every [[connected topological space|connected]] H-space is [[nilpotent topological space|nilpotent]] (see [there](nilpotent+topological+space#Properties)).

### Relation to $A_\infty$-spaces

Given an [[A-∞ space]] in the [[(∞,1)-category]] [[∞Grpd]]/[[Top]], its image in the corresponding [[homotopy category of an (∞,1)-category]] [[Ho(Top)]] in an $H$-space. Conversely, refining an H-space to a genuine $A_\infty$-space means lifting the structure of a [[monoid object in an (∞,1)-category]] from the [[homotopy category of an (∞,1)-category|homotopy category]] [[Ho(Top)]] to the genuine [[(∞,1)-category]] [[∞Grpd]]/[[Top]].

Further discussion of this is also at _[loop space -- Homotopy associative structure](loop+space#AInfinityStructure)_.

### Ring structure on homology
 {#RingStructureOnHomology}

The operations on an [[H-space]] $X$ equip its [[homology]] with the [[mathematical structure|structure]] of  [[ring]]. At least for [[ordinary homology]] this is known as the _[[Pontrjagin ring]]_ $H_*(X)$ of $X$.

### Rational homotopy
 {#RationalHomotopy}

Every [[connected topological space|connected]] H-space of rational [[finite type]] (i.e., whose [[rational cohomology]] in each degree is a [[finite-dimensional vector space|finite-dimensional]] [[rational vector space]]) is [[rational homotopy equivalence|rationally homotopy equivalent]] to a [[product space|product]] of [[Eilenberg-MacLane spaces]] (e.g. [May & Ponto 2011, Thm. 9.1.1](#MP11concise)). This means equivalently that its minimal [[Sullivan model]] has vanishing [[differential]], see for instance the example of [[Sullivan models of based loop spaces]].

If such an H-space in addition admits the structure of a [[finite CW-complex]] then it has the [[rational homotopy equivalence|rational homotopy type]] of a finite [[product topological space|product]] of [[odd number|odd]]-[[dimension of a manifold|dimensional]] [[rational n-sphere|rational spheres]] (Cor. 9.1.2. of [May & Ponto 2011](#MP11concise)). 

For example, since [[smooth manifolds]] have CW-complex structure (see [there](CW+complex#SmoothManifoldsAdmitCWComplexStructure)) this  is the case for all [[Lie groups]] (e.g. [Lin 1995](#Lin95)). 

## H-Spaces in homotopy type theory

In [[homotopy type theory]], *H-spaces* may be axiomatized as  consists of

* A type $A$,
* A basepoint $e:A$
* A binary operation $\mu : A \to A \to A$
* A left unitor 
$$\lambda:\prod_{(a:A)} \mu(e,a)=a$$ 
* A right unitor 
$$\rho:\prod_{(a:A)} \mu(a,e)=a$$

A __homomorphism of H-spaces__ between two H-spaces $A$ and $B$ consists of 

* A function $\phi:A \to B$ such that 
  * The basepoint is preserved
$$\phi(e_A) = e_B$$
  * The binary operation is preserved
$$\prod_{(a:A)} \prod_{(b:A)} \phi(\mu_A(a, b)) = \mu_B(\phi(a),\phi(b))$$

* A function 

$$\phi_\lambda:\left(\prod_{(a:A)} \mu(e_A,a)=a\right) \to \left(\prod_{(b:B)} \mu(e_B,b)=b\right)$$

such that the left unitor is preserved:

$$\phi_\lambda(\lambda_A) = \lambda_B$$

* A function 

$$\phi_\rho:\left(\prod_{(a:A)} \mu(a, e_A)=a\right) \to \left(\prod_{(b:B)} \mu(b, e_B)=b\right)$$

such that the right unitor is preserved:

$$\phi_\rho(\rho_A) = \rho_B$$


### Examples 
 {#Examples}

* There is a H-space structure on the [[circle]]. See Lemma 8.5.8 of the [[HoTT book]]. 

\begin{proof}
We define $\mu : S^1 \to S^1 \to S^1$ by circle induction:
$$\mu(base)\equiv id_{S^1}\qquad ap_{\mu}\equiv funext(h)$$
where $h : \prod_{x : S^1} x = x$ is defined in Lemma 6.4.2 of the [[HoTT book]]. We now need to show that $\mu(x,e)=\mu(e,x)=x$ for every $x : S^1$. Showing $\mu(e,x)=x$ is quite simple, the other way requires some more manipulation. Both of which are done in the book.
\end{proof}

* Every [[loop space]] is naturally a [[H-space]] with [[path]] concatenation as the operation. In fact every [[loop space]] is a [[group]].

* The type of [[maps]] $A \to A$ has the structure of a H-space, with basepoint $id_A$, operation function composition.

* An [[A3-space]] $A$ is an H-space with an equality $\mu(\mu(a, b),c)=\mu(a,\mu(b,c))$ for every $a:A$, $b:A$, $c:A$ representing associativity up to homotopy. 

* A unital magma is a 0-truncated H-space. 

## Related concepts

* [[topological monoid]]

* [[Pontrjagin ring]]

* [[group completion]]

* [[H-space ring spectrum]], [[H-group ring spectrum]]

* [[H-spaceoid]]

* [[A3-space]]

* [[H-spatial groupoid]]

* [[k-tuply associative n-groupoid]]


## References

Introduction and survey:


* {#Hatcher02} [[Allen Hatcher]], §3.C in: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#Arkowitz11} [[Martin Arkowitz]], *H-Spaces and Co-H-Spaces*, chapter 2 in: *Introduction to homotopy theory*, Springer (2011) 37-70 &lbrack;[doi:10.1007/978-1-4419-7329-0_2](https://doi.org/10.1007/978-1-4419-7329-0_2)&rbrack; 

The terminology "$H$-space" appear sin  

* [[Jean-Pierre Serre]], Chapter IV, Section 1 of: _Homologie singuli&#232;re des espaces fibr&#233;s. Applications._, Ann. Math. __54__ (1951), 425--505. 

Early discussion:

* [[William Browder]], *Torsion in H-Spaces*, Annals of Mathematics, Second Series **74** 1 (1961) 24-51  &lbrack;[jstor:1970305](https://www.jstor.org/stable/1970305)&rbrack;



More general notion of [[internalization|internal]] H-objects:

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories I multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories III primitive categories_,  Math. Ann. **150** 165–187 (1963) ([doi:10.1007/BF01470843](https://doi.org/10.1007/BF01470843)) 




Original articles:

* [[Edwin Spanier]], [[Henry Whitehead]], _On fibre spaces in which the fibre is contractible_, Comment. Math. Helv. __29__, 1955, 1--8.

* Arthur H. Copeland, _On $H$-spaces with two nontrivial homotopy groups_, Proc. AMS __8__, 1957, 109--129.

* [[Masahiro Sugawara]]:
  * _$H$-spaces and spaces of loops_, Math. J. Okayama Univ, __5__, 1955, 5--11;
  * _A condition that a space is an $H$-space_, Math. J. Okayama Univ. __6__, 1957, 109--129; ([pdf](https://ousar.lib.okayama-u.ac.jp/files/public/3/33737/20160528030627675220/fulltext.pdf))
  * _A condition that a space is group-like_, Math. J. Okayama Univ. __7__, 1957, 123--149.

* F. I. Karpelevi&#269;, A. L. Oni&#353;&#269;ik, _Algebra of homologies of space of paths_, Dokl. Akad. Nauk. SSSR, (N.S.), 106 (1956), 967--969. MR0081478

The theory of $H$-spaces was widely established in the 1950s and studied by Serre, Postnikov, Spanier, Whitehead, Dold, Eckmann and Hilton and many others. 

The deloopable case has more coherent structure which has been discovered few years later in J. Stasheff's thesis and published in

* [[Jim Stasheff]], _Homotopy associative $H$-spaces I, II_, Trans. Amer. Math. Soc. 108, 1963, 275-312 

For a historical account see

* [[John McCleary]], _An appreciation of the work of Jim Stasheff_ ([pdf](http://www.math.unc.edu/Faculty/jds/jds.pdf))

The description in terms of [[groupoid object in an (∞,1)-category]] is due to 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

see last remark of section 6.1.2 .

Wikipedia\'s definition (at time of this writing, and phrased in the language of [[homotopy theory]]) is rather a [[unitoid]] object in the $(\infty,1)$-category [[Top]].

* MathOverflow: [homotopy-associative-h-space-and-coh-space](http://mathoverflow.net/questions/16711/homotopy-associative-h-space-and-coh-space)

For H-spaces in [[homotopy type theory]]:

* [[Univalent Foundations Project]], [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* [[Ulrik Buchholtz]], [[J. Daniel Christensen]], [[Jarl G. Taxerås Flaten]], [[Egbert Rijke]], *Central H-spaces and banded types* &lbrack;[arXiv:2301.02636](https://arxiv.org/abs/2301.02636)&rbrack;

See also

* [[John Adams]], _Finite $H$-Spaces and Lie groups_, Journal of Pure and Applied Algebra 19 (1980) 1-8 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamse8.pdf))

* {#Adams61} [[John Adams]], _The sphere, considered as an $H$-space mod $p$_, Quart. J. Math. Oxford. Ser. (2) vol 12 52-60 ([pdf](http://qjmath.oxfordjournals.org/content/12/1/52.citation))

* {#MP11concise} [[Peter May]], [[Kate Ponto]]. *[[More Concise Algebraic Topology]]*, University of Chicago Press (2011). &lbrack;[doi:10.7208/chicago/9780226511795.001.0001](https://www.doi.org/10.7208/chicago/9780226511795.001.0001), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf)&rbrack

* {#Lin95} James P. Lin. "H-spaces with Finiteness Conditions". In: *Handbook of Algebraic Topology*
(1995), pp. 1095, 1097-1141. ([doi](https://doi.org/10.1016/B978-044481779-2/50023-7))

[[!redirects H-spaces]]

[[!redirects homomorphism of H-spaces]]
[[!redirects homomorphisms of H-spaces]]
[[!redirects H-space homomorphism]]
[[!redirects H-space homomorphisms]]

[[!redirects H-group]]
[[!redirects H-groups]]

[[!redirects grouplike space]]
[[!redirects grouplike spaces]]
[[!redirects group-like space]]
[[!redirects group-like spaces]]

[[!redirects H-monoid]]
[[!redirects H-monoids]]

[[!redirects H-ring]]
[[!redirects H-rings]]


[[!redirects H-unitoid]]
[[!redirects H-cogroup]]
[[!redirects H-comonoid]]

