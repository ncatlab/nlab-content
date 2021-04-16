
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

The [[category]] $SimpSet$, or $sSet$ for short, is the category whose [[objects]] are [[simplicial sets]] and whose [[morphisms]] are [[simplicial maps]].

[[equivalence of categories|Equivalently]], this is the [[functor category]] from the [[opposite category]] $\Delta^{op}$ of the [[simplex category]] $\Delta$ to the [[category of sets]] [[Set]]:

$$
  SimpSet \simeq [\Delta^{op}, Set]
  \,.
$$

## Properties


Like all categories of [[presheaf|presheaves]] on a [[small category]], the [[category]] [[SimpSet]] of simplicial sets is complete and cocomplete (with [[limits]] and [[colimits]] constructed levelwise) and [[cartesian closed category|cartesian closed]]. In fact, like all [[presheaf|presheaf categories]], it is a [[topos]]. 

### Monoidal structure

As described at [[closed monoidal structure on presheaves]]
the cartesian tensor product $S \otimes T = S \times T$ of simplicial sets $S$ and $T$ is the simplicial set
$$
  (S \otimes T) : [n] \mapsto S_n \times T_n
  \,,
$$
where the product on the right is the cartesian product in [[Set]].

One central reason why simplicial sets are useful and important is that this simple monoidal structure ("disturbingly simple minded" in the words of [Friedman08, p. 24](http://arxiv.org/PS_cache/arxiv/pdf/0809/0809.4221v1.pdf#page=24)) actually does fully capture the standard monoidal structure on [[topological spaces]] under [[geometric realization]] $|\cdot| : SSet \to Top$

+-- {: .un_prop}
###### Proposition

For $S$ and $T$ simplicial sets, we have
$$
  |S \times T| \simeq |S| \times |T|
  \,,
$$
where on the right the cartesian product is in the [[nice category of spaces|nice category]] of compactly generated Hausdorff spaces.
=--


See also [[products of simplices]].


### Closed structure

As described at [[closed monoidal structure on presheaves]]
the [[internal hom]]  $[S,T]$ of simplicial sets is the simplicial set
$$
  [S,T] : [n] \mapsto Hom_{SSet}(S \times \Delta[n], T)
  \,,
$$
where $\Delta[n] = Hom_{\mathbf{\Delta}}(-,[n])$ is the standard simplicial $n$-[[simplex]], the image of $[n] \in \mathbf{\Delta}$ under the [[Yoneda embedding]]. This formula is clearly representing a Kan extension. 


### Adjunctions 

The maps $N: \Cat \rightarrow \Simp\Set$ and $S: \Top \rightarrow \Simp\Set$ described in the examples are actually functors, both of which have left adjoints. These adjoint pairs are examples of a very general sort of adjunction involving simplicial sets, of which there are many examples.

Let $E$ be any cocomplete category and let $F: \Delta \rightarrow E$ be a functor. We define the right adjoint $R : E \rightarrow \Simp\Set$ as follows. Given an object $e \in E$ the $n$-simplices of $Re$ are defined to be the set $E(F[n],e)$ of morphisms in $E$ from $F[n]$ to $e$. Face and degeneracy maps are given by precomposition by the appropriate (dual) maps in the image of $F$. $R$ is defined on morphisms by postcomposition. 

The left adjoint $L$ is defined to be the left [[Kan extension]] of $F$ along the Yoneda embedding $y: \Delta \rightarrow \Simp\Set$. Because the $y$ is full and faithful, we will have $Ly = F$, i.e., $L (\Delta[n]) = F[n]$. By specifying $F$, we have already defined a functor to $E$ on the represented simplicial sets; $L$ is the unique cocontinuous extension of this functor to $\Simp\Set$. It can be described explicitly on objects as a [[end|coend]], or as a [[weighted limit|weighted colimit]].

(Easy) [[category theory|abstract nonsense]] shows that $L$ and $R$ form an [[adjunction|adjoint pair]] $L \dashv R$.

Here are some examples:

* Let $E = \Cat$ and $F$ be the functor $[n] \mapsto [n]$ (the inclusion of posets into categories). The right adjoint is the nerve functor $N$ described above. The left adjoint ${\tau}_1$ takes a simplicial set to its **fundamental category**. 

* Let $E = \Top$ and $F$ be the functor $[n] \mapsto {\Delta}_n$. The right adjoint is the total singular complex functor $S$ described above. The left adjoint $|-|$ is called **[[geometric realization]]**.  As a consequence of the Kan extension construction, the geometric realization of the represented simplicial set $\Delta[n]$ is the standard $n$-simplex ${\Delta}^n$.

* (Barycentric) subdivision and extension $\sd: \Simp\Set \leftrightarrow \Simp\Set :\ex$.

* The [[homotopy coherent nerve]] functor and its left adjoint $\Simp\Set \leftrightarrow \Simp\Cat$ where [[SimpCat]] denotes the category of [[simplicially enriched category|simplicially enriched categories]], i.e., categories enriched in $\Simp\Set$.

* The adjunction $- \times X: \SimpSet \leftrightarrow \SimpSet :(-)^X$ between the product with a simplicial set $X$ and the internal-hom, which makes $\Simp\Set$ into a [[cartesian closed category]].

* Let $E$ be a [[Grothendieck topos]] equipped with an "interval" $I$, i.e. a [[total order|totally ordered object]] in the [[internal logic]] equipped with distinct top and bottom elements.  Then we have the functor $\Delta \to E$ sending $[n]$ to the subobject $ \{ (x_1,x_2,\dots,x_n) \;|\; x_1 \le x_2 \le \dots \le x_n \} \hookrightarrow I^n $ which gives rise to a [[geometric morphism]] $E\to \SimpSet$.  Therefore, $\SimpSet$ is the [[classifying topos]] of such "intervals".




### Model category structures

There are important [[model category]] structures on $sSet$.

* The standard [[model structure on simplicial sets]] [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoid]]s.

* The [[model structure for quasi-categories]] on $sSet$ presents the [[(∞,2)-category]] of [[(∞,1)-categories]] [[(∞,1)Cat]].

### Internal logic

Like any [[elementary topos]], $\SimpSet$ has an [[internal logic]].  Here we list some properties of this logic.

* It is a [[two-valued topos]], i.e. the only subobjects of $1 = \Delta^0$ are $0$ and $1$.  (This is not really a property of the internal logic, but we include it to contrast with the next point.)

* It is not [[Boolean topos|Boolean]].  In general, the [[complement]] of a simplicial subset $A\subseteq B$ is the *full* simplicial subset on the vertices of $B$ not contained in $A$ ("full" meaning it contains a simplex of $B$ as soon as it contains all its vertices).  Thus, $A\cup \neg A = B$ only if $A$ is a [[connected component]] of $B$, i.e. any simplex with at least one vertex in $A$ lies entirely in $A$.

* By [[Diaconescu's theorem]], $\SimpSet$ therefore does not satisfy the [[axiom of choice]].

* Like any presheaf topos, it satisfies the [[dependent choice]] (assuming
 it holds in the metatheory); see [Fourman and Scedrov](#FourmanScedrov). Moreover, [[natural numbers object]] is simply the discrete simplicial set of ordinary natural numbers.

* Similarly, it satisfies [[Markov's principle]].

* Less obviously, it satisfies the [[Kreisel-Putnam axiom]] that $(\neg p \to (q\vee r)) = ((\neg p \to q) \vee (\neg p \to r))$; see [this MO question](http://mathoverflow.net/questions/159989/internal-logic-of-the-topos-of-simplicial-sets/) and answers.

## Related concepts

* [[asSet]] ([[category]] of [[augmented simplicial sets]])

* [[Ho(sSet)]] (the [[homotopy category]] of [[simplicial sets]])

* [[dSet]] ([[category]] of [[dendroidal sets]])

## References
* {#FourmanScedrov} [[Mike Fourman]] and &#352;&#269;edrov, The "world's simplest axiom of choice" fails, manuscripta mathematica 1982, Volume 38, Issue 3, pp 325-332 [PDF](http://link.springer.com/content/pdf/10.1007%2FBF01170929.pdf)

category: category

[[!redirects SSet]]
[[!redirects sSet]]
[[!redirects Simp Set]]

[[!redirects category of simplicial sets]]
[[!redirects categories of simplicial sets]]

[[!redirects SimplicialSets]]

