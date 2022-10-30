

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **pro-object** of a category $C$ is a "formal [[filtered category|cofiltered]] limit" of objects of $C$.  The category of pro-objects of $C$ is written $pro$-$C$. Such a category is sometimes called a 'pro-category', but notice that that is *not* the same thing as a pro-object in [[Cat]].

"Pro" is short for "projective". (A 'projective limit' was an older term for a [[limit]].) It is contrasted with "ind" in the [[ind-object|dual notion]], standing for "inductive", (and corresponding to "inductive limit," the old term for [[colimit]]).  In some (often older) sources, the term 'projective system' is used more or less synonymously for pro-object.

## Definition 

The objects of $pro$-$C$ are diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|cofiltered]] category.  The set of morphisms between $F:D\to C$ and $G:E\to C$ is 

\[pro\text{-}C(F,G) = lim_{e\in E} colim_{d\in D} C(F d, G e)\]

The limit and colimit is taken in the category of sets; we know that cofiltered limits there are [[thread]]s and filtered colimits are germs (classes of equivalences). Thus a representative of $s\in\mathrm{pro}C(F,G)$ is a thread whose each component is a germ:  
$s = (germ_e(s))_{e\in E}$ which can be more concretely written as $([s_{d_e,e}])_e$; thus $[s_{d_e,e}]\in colim_{d\in D} C(F d, G e)$ where $s_{d_e,e}\in C(F d_e, G e)$ is some representative of the class; there is at least one $d_e$ for each $e$; if the domain $E$ is infinite, we seem to need an axiom of choice in general to find a function $e\mapsto d_e$ which will choose one representative in each class $germ_e(s)$. Thus $s$ is given by the (equivalence class) of the following data

* function $e\mapsto d_e$ 

* correspondence $e\mapsto s_{d_e,e}\in C(F d_e, G e)$ 

such that $([s_{d_e,e}])_e$ is a thread, i.e. for any $\gamma: e\to e'$ we have an equality of classes (germs) $[G(\gamma)\circ s_{d_e,e}] = [s_{d_{e'},e'}]$. This equality holds if 
there is a $d'$ and morphisms $\delta_e: d'\to d_e$, 
$\delta_{e'}: d'\to d_{e'}$ such that $G(\gamma)\circ s_{d_e,e}\circ F\delta_e = s_{d_{e'},e'}\circ F\delta_{e'}$. (Usually in fact people consider the dual of $D$ and the dual of $C$ as filtered domains). Now if we chose a different function $e\mapsto\tilde{d}_e$ instead then,  $([s_{d_e,e}])_e = ([s_{\tilde{d}_e,e}])_e$, hence by the definition od classes, for every $e$ there is a $d''\in D$ and morphisms $\sigma_e : d''\to d_e$, $\tilde\sigma_e:d''\to \tilde{d}_e$ such that $s_{\tilde{d}_e,e}\circ F(\tilde\sigma_e) = s_{d_e,e}\circ F(\sigma_e)$.

This definition is perhaps more intuitive in the dual case of [[ind-object|ind-objects]] (pro-objects in $C^{op}$), where it can be seen as stipulating that the objects of $C$ are [[finitely presentable object|finitely presentable]] in $ind$-$C$.

#### Definition of $\mathrm{pro}C$ as a subcategory of functors

Another, equivalent, definition is to let $pro$-$C$ be the [[full subcategory]] of $[C,Set]^{op}$ determined by those functors which are cofiltered limits of representables. This is reasonable since the [[presheaf category|copresheaf category]] $[C,Set]^{op}$ is the [[free completion]] of $C$, so $pro$-$C$ is the "free completion of $C$ under cofiltered limits."

## Examples

* [[profinite group]]

* [[progroup]]

* [[profinite space]]

## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* **pro-object** / [[pro-object in an (∞,1)-category]]

## References

* (SGA4-1) _Th&#233;orie des topos et cohomologie &#233;tale des sch&#233;mas. Tome 1: Th&#233;orie des topos_, S&#233;minaire de G&#233;om&#233;trie Alg&#233;brique du Bois-Marie 1963&#8211;1964 ([[SGA 4]]). Dirig&#233; par M. Artin, A. Grothendieck, et J. L. Verdier. Avec la collaboration de N. Bourbaki, P. Deligne et B. Saint-Donat. Lecture Notes in Mathematics __269__, Springer 1972. 
* [[J.-M. Cordier]], [[Tim Porter]],  _Shape Theory_ , categorical methods of approximation, Dover (2008) (It is a reprint of the 1989 edition without amendments.)
* [[Masaki Kashiwara]], [[Pierre Schapira]], [[Categories and Sheaves]]
* [[Peter Johnstone]], _[[Stone Spaces]]_.
* [[S. Marde?i?]], J. Segal, _Shape theory_, North Holland 1982

[[!redirects pro-objects]]
[[!redirects pro object]]