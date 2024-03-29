
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

The **quotient object** $Q$ of a [[congruence]] (an [[internalization|internal]] [[equivalence relation]]) $E$ on an [[object]] $X$ in a [[category]] $C$ is the [[coequalizer]] $Q$ of the induced pair of morphisms $E \,\rightrightarrows\, X$.  

If $E$ is additionally the [[kernel pair]] of the map $X \to Q$, then $Q$ is called an **effective quotient** -- and $E$ is called an **effective** congruence, with the map $X \to Q$ being an [[effective epimorphism]] (terminology as for _[[effective group action]]_).

Sometimes the term is used more loosely to mean an arbitrary [[coequalizer]].  It may also refer to a co-[[subobject]] of $X$ (that is, a subobject of $X$ in the [[opposite category]] $C^\op$), without reference to any congruence on $X$.  Note that in a [[regular category]], any [[regular epimorphism]] (i.e. a "regular quotient" in the co-subobject sense) is in fact the quotient (= coequalizer) of its [[kernel pair]] (actually, we can prove this under weaker hypotheses; see below).

## Galois connection between quotients and relations 

As we have said, there are various notions of quotient object. Let us consider the most general one, so that $Quot(X)$ of an object $X$ denotes the poset of co-subobjects of $X$, in other words the [[poset|posetal]] [[reflection]] of the [[preorder]] of epis $X \to Q$ which is a [[full subcategory]] of the [[co-slice category]] $X \downarrow \mathbf{C}$. A *regular quotient* then refers to a regular epi $X \to Q$. 

On the other hand, let $Rel(X)$ be the poset of [[relations]] on $X$, i.e., the 
poset of subobjects of $X \times X$, or in other words the posetal reflection of the preorder of monos $i = \langle e_1, e_2 \rangle: E \rightarrowtail X \times X$ which is a full subcategory of the [[slice category]] $\mathbf{C} \downarrow X \times X$. 

Between $Quot(X)$ and $Rel(X)$ there is a relation $\perp$ where $q \perp \langle e_1, e_2 \rangle$ means exactly $q \circ e_1 = q \circ e_2$. If the coequalizer $coeq(e_1, e_2)$ of the parallel pair $e_1, e_2: E \rightrightarrows X$ exists, then by definition we have $coeq(e_1, e_2) \leq q$ iff $q e_1 = q e_2$. On the other hand, if the [[kernel pair]] $\ker(q)$ of $q$ exists, then by definition we have $q e_1 = q e_2$ iff $\langle e_1, e_2 \rangle \leq \ker(q)$. 

This indicates in a category which admits coequalizers and kernel pairs, we have 

+-- {: .num_prop} 
###### Proposition 
$coeq: Rel(X) \to Quot(X)$ is [[left adjoint]] to $\ker: Quot(X) \to Rel(X)$. 
=-- 

Or, in other words, that $\ker$ and $coeq$ set up a [[Galois connection]] between $Quot(X)^{op}$ and $Rel(X)$. 

Restricting consideration to kernel pairs only of epis, or coequalizers only of jointly monic pairs, is no real restriction in the presence of epi-mono factorizations: 

+-- {: .num_lemma #image} 
###### Lemma 
In a category where every morphism $f: A \to B$ has an [[image|epi-mono factorization]] $f = i \circ q$, we have $\ker(f) = \ker(q)$. Similarly, for a pair $f, g: X \rightrightarrows Y$, we have $coeq(f, g) = coeq(e_1, e_2)$ where $\langle f, g \rangle: X \to Y \times Y$ factors as an epi $p: X \to E$ followed by a mono $\langle e_1, e_2 \rangle: E \to Y \times Y$. 
=-- 

+-- {: .proof} 
###### Proof 
We prove just the first statement; the second is proven similarly. It suffices to observe that the same class of jointly monic pairs $(e_1, e_2)$ are coequalized by $f$ as by $q$; the kernel pair is by definition the maximum of this class. If $q e_1 = q e_2$, then by applying $i$ to both sides we deduce $f e_1 = f e_2$. If $f e_1 = f e_2$, i.e., if $i q e_1 = i q e_2$, then $q e_1 = q e_2$ by monicity of $i$. 
=-- 

+-- {: .num_prop #galois} 
###### Proposition  
Suppose $\mathbf{C}$ is a category with coequalizers and kernel pairs and where every morphism has an epi-mono factorization. Then every regular epi $q$ is the coequalizer of its kernel pair: $q = coeq \circ \ker(q)$. And every kernel pair is the kernel pair of its coequalizer: $i = \ker \circ coeq(i)$. 
=-- 

+-- {: .proof} 
###### Proof 
We just prove the first statement; the second is proved similarly. We have of course a [[counit]] $coeq \circ \ker(q) \leq q$. On the other hand, if $q = coeq(f, g)$ (where we may assume $\langle f, g \rangle$ is monic by the lemma), then we have a unit $\langle f, g \rangle \leq \ker \circ coeq(f, g) = \ker(q)$; applying $coeq$ to each side, we have $q \leq coeq \circ \ker(q)$, as desired. 
=-- 

## In toposes 
 {#InToposes}

Constructing quotient objects in an [[elementary topos]] $\mathbf{E}$, starting from one or another standard definition (e.g., [[finitely complete category]] with [[power objects]]) that doesn't already mention colimits, is not trivial. 

The standard approach seen in textbooks (see for example _[[Sheaves in Geometry and Logic]]_), apparently first introduced by C.J. Mikkelsen but first published by [Par&#233;](#RP), is to prove that the contravariant [[power object]] functor $P \colon \mathbf{E}^{op} \to \mathbf{E}$ is [[monadic functor|monadic]]. It follows that $P$ [[reflected limit|reflects]] [[finite limits]] in $\mathbf{E}^{op}$ from limits in $\mathbf{E}$, but finite limits in $\mathbf{E}^{op}$ are of course finite colimits in $\mathbf{E}$. 

This elegant approach does involve a fair amount of categorical machinery (a [[monadicity theorem]], [[Beck-Chevalley conditions]], and consideration of up to six applications of the power object functor), making it a challenge to get across intuitively in say an undergraduate course. 

Other approaches that are closer to naive or common sense set-theoretic reasoning are possible. In the case of quotient objects, to form the coequalizer of a parallel pair $f, g: X \rightrightarrows Y$, we outline a possible path to take (see also at _[quotient type -- from univalence](quotient+type#FromUnivalence)_): 

* Construct enough of the [[internal logic]] to make available logical operators $\wedge, \Rightarrow, \forall$. 

* Construct an internal [[intersection]] operator $\bigcap: P P X \to P X$ via the formula $\bigcap \Phi = \{x: X\; |\; \forall_{S: P X} \Phi \ni S \Rightarrow S \ni x\}$. 

* Construct the [[image]] of a map $f: X \to Y$ by taking the internal intersection of all [[subobjects]] of $Y$ through which $f$ factors. 

* To construct the [[coequalizer]] of $f, g: X \rightrightarrows Y$: 
  * Take the image of $\langle f, g \rangle: X \to Y \times Y$ to get a relation $\langle p_1, p_2 \rangle: R \hookrightarrow Y \times Y$. According to Lemma \ref{image}, a coequalizer of $(p_1, p_2)$ is a coequalizer of $(f, g)$.  
  * Then take the equivalence relation $\langle e_1, e_2 \rangle: E \hookrightarrow Y \times Y$ generated by $R$, by taking the intersection of all equivalence relations containing $R$; a coequalizer of $(e_1, e_2)$ is a coequalizer of $(p_1, p_2)$ (akin to the fact that any coequalizer must be the coequalizer of its kernel pair, as in Proposition \ref{galois}). 
  * Take the image factorization of the map $\chi_E: Y \to P Y$ that classifies the relation $E \hookrightarrow Y \times Y$. That is, factor $\chi_E$ as an epi $q: Y \to Q$ followed by a mono $Q \to P Y$. Then $q$ is the desired coequalizer of $(e_1, e_2)$. 

Notice that what these steps collectively do is form the object $Q$ of equivalence classes of the equivalence relation generated by the relation $f(x) \sim g(x)$, which is exactly what we would do in ordinary set theory. Full details will appear elsewhere. 

## In higher category theory

These notions have generalizations when $C$ is an [[(∞,1)-category]]:

* an equivalence relation is then a [[groupoid object in an (∞,1)-category]]

* it has an "effective quotient" if it is [[delooping|deloopable]].

For instance an [[action groupoid]] is a quotient of a group action in 2-category theory.

## Examples

* [[quotient set]]

* [[quotient group]]

* [[quotient module]], [[quotient bimodule]]

* [[quotient ring]]

([[quotient norm]])

## Related concepts

* [[fraction]]

* [[subquotient]]

* [[quotient space]], [[geometric invariant theory]]

* [[quotient stack]]

* In [[type theory]]/[[homotopy type theory]] the analogous concept is that of [[quotient types]].

## References 

* {#Pare74} [[Robert Paré]], _Colimits in Topoi_, Bull. AMS 80 (1974) pp.556-561. ([pdf](http://www.ams.org/journals/bull/1974-80-03/S0002-9904-1974-13497-X/S0002-9904-1974-13497-X.pdf))
 {#RP}

[[!redirects quotient object]]
[[!redirects quotient objects]]
[[!redirects quotient]]
[[!redirects quotients]]

[[!redirects regular quotient]]
[[!redirects regular quotients]]

[[!redirects effective quotient]]
[[!redirects effective quotients]]

[[!redirects quotient map]]
[[!redirects quotient maps]]
[[!redirects quotient morphism]]
[[!redirects quotient morphisms]]
