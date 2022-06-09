
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

An **[[H-monoid|$H$-monoid]]** is a [[monoid object]] in [[Ho(Top)]], hence an $H$-space is an $H$-monoid if the product of the magma is [[associativity|associative]] up to [[homotopy]]. 

An __$H$-group__ is a [[group object]] in [[Ho(Top)]], so an $H$-monoid is an $H$-group if it also has [[inverses]] up to homotopy.

An **$H$-ring** is a [[ring object]] in (pointed) [[Ho(Top)]].

To continue in this pattern, one could say that an **[[H-category]]** is a category internal to [[Ho(Top)]].

Notice that here the homotopies for units, associativity etc. are only required to _exist_ for an H-space, not required to be equipped with higher [[coherence|coherent]] homotopies. An $H$-monoid equipped with such higher and coherent homotopies  is instead called a _strongly homotopy associative_ space or  _$A_\infty$-[[A-infinity space|space]]_ for short.  If it has only higher homotopies up to level $n$, it is called an $A_n$-[[A-n space|space]].

A better name for an $H$-space might be be $H$-[[unitoid]], but it is rarely used. The $H$ stands for [[Heinz Hopf]], and reflects the sad fact that the natural name 'homotopy group' was [[homotopy group|already occupied]]; Hopf and A. Borel found necessary algebraic conditions for a space to admit an $H$-space structure.

There are dual notions of $H$-counitoid (or $H'$-space, or [[co-H-space]]), $H$-comonoid (or $H'$-monoid) and $H$-[[cogroup]] (or $H'$-group) having co-operations with the usual identities up to homotopy. 

## Examples

### Loop spaces

The main example of an $H$-group is the [[loop space]] $\Omega X$ of a space $X$, which however is naturally even an [[A-infinity space]]. 

### Suspensions

The main example of an [[co-H-space|H-cogroup]] in $Top_*$ is the [[suspension]] $S X= S^1\wedge X$ of a pointed topological space $X$. 

### Spheres

The only [[n-spheres]] $S^n$ which have $H$-space structure are those for $n = 0,1,3,7$, and their H-space structure is given by identifying them as the unit spheres in one of the four [[normed division algebras]] ([[real numbers]], [[complex numbers]], [[quaternions]], [[octonions]]) and taking the product to be that induced by the algebra product. 

An example of an H-space that does not lift to an [[A-infinity space]] is the [[7-sphere]] $S^7$. It can't be delooped because its [[delooping]] would have [[cohomology group]] a [[polynomial ring]] on a generator in degree 8, and this is impossible by mod $p$ [[Steenrod operations]] for any odd $p$, see [Lemma 2, Adams61](#Adams61). The 7-sphere is also not an $H$-group.

### Mapping spaces into H-groups

If $K$ is an $H$-group then for any topological space $X$, the set of [[homotopy classes]] $[X,K]$ has a natural group structure in the strict sense; analogously if $K'$ is an $H$-cogroup then $[K',X]$ has a group structure. If there is more than one $H$-group structure on a space, then the induced group structures on the set of homotopy classes coincide. 

If an $H$-space is equivalent to a [[delooping|deloopable one]], then it is a [[groupoid object in an (infinity,1)-category|group object in the (∞,1)-category]] [[Top]]. In other words, in that case, the associativity and other axioms hold up to **coherent homotopy**. 

### K-Theory space


The [[classifying space]] $B U \times \mathbb{Z}$ for (complex) [[topological K-theory]] is an H-ring space (p. 205 (213 of 251) in _[[A Concise Course in Algebraic Topology]]_.)

### Dwyer-Wilkerson space

See at _[[Dwyer-Wilkerson H-space]]_


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

## H-Spaces in homotopy type theory

In [[homotopy type theory]], an *H-Space* consists of

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

* {#Arkowitz11} [[Martin Arkowitz]], _H-Spaces and Co-H-Spaces_, chapter 2 in _Introduction to homotopy theory_, Springer 2011 ([pdf](file:///C:/Users/Sony/Downloads/9781441973283-c1.pdf))

The terminology "$H$-space" is a definition in a Chapter IV, Section 1 (dedicated to loop spaces) of 

* [[Jean-Pierre Serre]], _Homologie singuli&#232;re des espaces fibr&#233;s. Applications._, Ann. Math. __54__ (1951), 425--505. 

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

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

See also

* [[John Adams]], _Finite $H$-Spaces and Lie groups_, Journal of Pure and Applied Algebra 19 (1980) 1-8 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamse8.pdf))

* {#Adams61} [[John Adams]], _The sphere, considered as an $H$-space mod $p$_, Quart. J. Math. Oxford. Ser. (2) vol 12 52-60 ([pdf](http://qjmath.oxfordjournals.org/content/12/1/52.citation))

[[!redirects H-spaces]]

[[!redirects homomorphism of H-spaces]]
[[!redirects homomorphisms of H-spaces]]
[[!redirects H-space homomorphism]]
[[!redirects H-space homomorphisms]]

[[!redirects H-group]]
[[!redirects H-groups]]

[[!redirects H-ring]]
[[!redirects H-rings]]


[[!redirects H-unitoid]]
[[!redirects H-cogroup]]
[[!redirects H-comonoid]]


