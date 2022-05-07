
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
+ automatic table of contents goes here
{:toc}

## Idea

A [[geometric morphism]] is *locally connected* if it behaves as though its [[fiber]]s are [[locally connected space]]s.  In particular, a [[Grothendieck topos]] $E$ is [[locally connected topos|locally connected]] iff the unique [[geometric morphism]] to [[Set]] (the terminal Grothendieck topos, i.e. the [[point]] in the [[category]] [[Topos]] of toposes) is locally connected.

## Definition

A [[geometric morphism]] $ (f^* \dashv f_*) : F \underoverset{f_*}{f^*}{\leftrightarrows} E$ is **locally connected** if it satisfies the following equivalent conditions:

1. It is [[essential geometric morphism|essential]], i.e. $f^*$ has a [[left adjoint]] $f_!$, and moreover $f_!$ can be made into an $E$-[[indexed functor]].

1. For every $A\in E$, the functor $(f/A)^* \colon E/A \to F/f^*A$ is [[cartesian closed functor|cartesian closed]].

1. $f^*$ commutes with [[dependent products]] -- For any morphism $h\colon A\to B$ in $E$, the canonically defined [[natural transformation]] $(f/B)^* \circ \Pi_h \to \Pi_{f^*h} \circ (f/A)^*$ is an [[isomorphism]].

1. It is essential, and the counit $\varepsilon$ of  $f_!\dashv f^*$ is [[equifibered natural transformation|equifibered/cartesian]].


+-- {: .proof}
###### Proof of equivalence

The equivalence of 1,2,3 is shown in [Johnstone (2002)](#elephant), C3.3.1.

The equivalence of 1 and 4 can be easily deduced from the fact that the functors

$$(f/A)_{!} : F/f^*A\to E/A$$ 

are given by $(h:X\to f^*A)\mapsto (\varepsilon_A\circ f_!(h))$.

=--


## Properties


### Relation to connectedness

If $f$ is locally connected, then it makes sense to think of the left adjoint $f_!$ as assigning to an object of $F$ its "set of connected components" in $E$.  In particular, if $f$ is locally connected, then it is moreover [[connected geometric morphism|connected]] if and only if $f_!$ preserves the [[terminal object]].  However, not every connected geometric morphism is locally connected. {#connect}

### Over $Set$

Over the [[base topos]] $E = $ [[Set]] every [[connected topos]] which is [[essential geometric morphism|essential]] is automatically locally connected.

This is because the required [[Frobenius reciprocity]] condition 

$$
  f_!(A \times f^* (B)) \simeq f_!(A) \times B
$$

is automatically satisfied, using that [[cartesian product]] with a [[set]] is equivalently a [[coproduct]]

$$
  A \times B = \coprod_{a \in A} B
  \,,
$$

that the [[left adjoint]] $f_!$ preserves coproducts, and that for $f^*$ [[full and faithful]] we have $f_! f^* \simeq Id$. 

### Strong adjunctions
 {#StrongAdjunctions}

The pair of [[adjoint functors]] $(f_! \dashv f^*)$ in a locally connected geometric morphisms forms a "strong adjunction" in that it holds also for the [[internal homs]] in the sense that there is a [[natural isomorphism]]

$$
  [f_!(X), A] \simeq f_* [X, f^* A]
$$

for all $X, A$. This follows by duality from the [[Frobenius reciprocity]] that characterizes $f^*$ as being a [[cartesian closed functor]]:

by the [[Yoneda lemma]], the morphism in question is an [[isomorphism]]
if for all objects $A,B, X$ the morphism

$$
  Hom(X, [f_!(A), B]) 
   \stackrel{}{\to}
  Hom(X,f_*[A,f^*(B)])
$$

is a bijection. By [[adjunction]] this is the same as

$$
  Hom(X \times f_!(A), B) \stackrel{\simeq}{\to}
  Hom(f_!(f^*(X) \times A), B)
  \,.
$$

Again by Yoneda, this is a bijection precisely if

$$
  f_!(f^*(X) \times A) \to X \times f_!(A)
$$

is an [[isomorphism]]. But this is the [[Frobenius reciprocity]] condition on $f^*$.

### Coreflectivity

Locally connected toposes are [[coreflective subcategory|coreflective]] in [[Topos]]. See ([Funk (1999)](#Funk)).

### Other characterizations

* Let $(\mathcal{C}, J)$ be a [[site]] and $S$ be a [[sieve]] on the object $U$. $S$ is called _connected_ when $S$ viewed as a full subcategory of $\mathcal{C}/U$ is connected. The **site** is called _locally connected_ if every sieve is connected. For a [[bounded geometric morphism]] $p:\mathcal{E}\to\mathcal{S}$ the following holds:
_$p$ is locally connected iff there exists a locally connected internal site in $\mathcal{S}$ such that $\mathcal{E}\simeq Sh(\mathcal{C},J)$._ (cf. [Johnstone (2002)](#elephant), pp.656-658)

* [Caramello (2012)](#Cara12) gives syntactic characterizations of [[geometric theories]] whose [[classifying topos]] is locally connected.

The same paper also contains the following characterization:

* A Grothendieck topos is locally connected iff it has a [[separator|separating set]] of (coproduct) indecomposable objects.


### Variations in the context of the Nullstellensatz

[Johnstone (2011)](#JS11) studies several subclasses of locally connected geometric morphisms in the context of [[William Lawvere|Lawvere]]'s theory of [[cohesion]] and the [[Nullstellensatz]]. He calls a locally connected morphism $p$ _stably locally connected_ if $p_!$ preserves finite products. According to the [above remark](#connect) this implies that $p$ is connected. Slightly stronger is the preservation of all finite limits by $p_!$: these $p$ are called [[totally connected geometric morphisms]].


## Examples

* If the terminal [[global section]] geometric morphism $E \to Set$ is locally connected, one calls $E$ a [[locally connected topos]].  More generally, if $E\to S$ is locally connected, we may call $E$ a *locally connected $S$-topos*.

* Let $X$ be a [[topological space]] (or a [[locale]]) and $U\subseteq X$ an [[open subset]], with corresponding [[geometric embedding]] $j\colon Sh(U)\to Sh(X)$.  Then any $A\in Sh(X)$ can be identified with a space (or locale) $A$ equipped with a [[local homeomorphism]] $A\to X$, in such a way that $Sh(X)/A \simeq Sh(A)$.  Moreover, $j^*A \in Sh(U)$ can be identified with the pullback of $A\to X$ along $U$, and so $Sh(U)/j^*A \simeq Sh(j^*A)$ similarly.  Noting that $j^*A \to A$ is again the inclusion of an open subset, and using the fact that the inverse image part of any open [[geometric embedding]] is cartesian closed, we see that $(j/A)^*\colon Sh(X)/A \to Sh(U)/j^*A$ is cartesian closed for any $A$.  Hence $j$ is locally connected.

## Related entries

* [[connected geometric morphism]]

* [[local geometric morphism]]

* [[totally connected geometric morphism]]

## References

The case of $Sh(X)$ for a topological space $X$ was an exercise (p.417) in [[SGA4]]:

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, Springer LNM vol.269 (1972).

The concept relative to other bases was introduced in the following paper:

* [[Michael Barr]], [[Robert Paré]], _Molecular Toposes_ , JPAA **17** (1980) pp.127-152.

The standard reference is section C3.3 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ , Oxford UP 2002. {#elephant}

Further references include

* [[Olivia Caramello]], _Syntactic Characterizations of Properties of Classifying Toposes_ , TAC **26** no.6 (2012) pp.176-193. ([pdf](http://www.tac.mta.ca/tac/volumes/26/6/26-06.pdf))
  {#Cara12}

* [[Jonathon Funk]], _The locally connected coclosure of a Grothendieck topos_, JPAA **137** (1999) pp.17-27.
  {#Funk}

* {#JS11} [[Peter Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* [[Ieke Moerdijk]], _Continuous fibrations and inverse limits of toposes_ , Comp. Math. **58** (1986) pp.45-72. ([pdf](http://archive.numdam.org/article/CM_1986__58_1_45_0.pdf))

* [[Ieke Moerdijk]], [[Gavin Wraith]], _Connected and locally connected toposes are path connected_ , Trans. AMS **295** (1986) pp.849-859. ([pdf](http://www.ams.org/journals/tran/1986-295-02/S0002-9947-1986-0833712-3/S0002-9947-1986-0833712-3.pdf))


[[!redirects locally connected geometric morphisms]]
