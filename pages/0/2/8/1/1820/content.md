
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A _combinatorial model catgeory_ is a particularly convenient [[model category]] structure.

## Definition ##

+-- {: .un_defn}
###### Definition
(Jeff Smith)

A [[model category]] $C$ is **combinatorial** if it is

* [[locally presentable category|locally presentable]]

and

* [[cofibrantly generated model category|cofibrantly generated]].

=--

Recall from the discussion at [[cofibrantly generated model category]] that this means that $C$ has a [[set]] (not a proper [[class]]) $I$ of generating cofibrations and and a set of trivial generating cofibrations in that

  $$ 
    cof = llp(rlp(I))
  $$
  
  $$
    fib = llp(rlp(J))
    \,.
  $$

Here $fib, cof \subset Mor(C)$ is the collection of fibrations and cofibration, respectively, and $llp(S), rlp(S)$ is the collection of morphisms satisfying the left or right, respectively, [[lifting property]] with respect to a collection of morphisms $S$. 

Jeff Smith's theorem, below, gives an equivalent characterization that is usually easier to handle.

## Characterization theorems ##

There are two powerful theorems that characterize combinatorial model categories in terms of data that is often easier to handle:

### Smith's theorem ###

A central theorem about combinatorial model categories is **Jeff Smith's theorem** which establishes the existence of model category structures from a comparatively small amount of input data.

+-- {: .num_theorem }
###### Theorem (Jeff Smith)

Let $C$ be a [[locally presentable category]], $W$ an accessibly embedded [[accessible category|accessible]] [[subcategory]] of the [[arrow category]] $Arr(C)$, and $I \subset Mor(C)$ a [[set]] (not a proper class) of morphisms of $C$ such that

* $W$ satisfies [[category with weak equivalences|2-out-of-3]];

* $inj(I) \subset W$

* $cof(I) \cap W$ is closed under [[pushout]] and [[transfinite composition]].

Then $C$ is a combinatorial model category with

* weak equivalences $W$;

* cofibrations $cof(I)$.

Conversely, every combinatorial model category is of this form.

=--

Here $inj(I) = rlp(I)$ and $cof(I) = llp(rlp(I))$.

This statement was announced by Jeff Smith in 1998 at a conference in Barcelona and appeared in print as theorem 1.7 in

* [[Tibor Beke]], _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0102087))

The above statement follows prop 2.2 in 

* [[Clark Barwick]], _On left and right model categories and left and right Bousfield localization_ ([pdf](http://www.math.harvard.edu/~clarkbar/complete.pdf))

+-- {: .proof}
###### Proof

For the proof of the first part, it is sufficent to exhibit a small set $J$ such that $cof(J) = W \cap cof(I)$. The construction of that is described in the following two lemmas.

The converse statement, that every combinatorial model category satisfies the assumptions of the theorem, is for instance corollary 2.6 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).

=--

+-- {: .un_lemma }
###### Lemma (Smith)

If a sub-set $J \subset cof(I) \cap W$ is such that every commutative square

$$
  \array{
    K &\to& X
    \\
    \downarrow^{\mathrlap{i \in I}} && 
    \downarrow^{\mathrlap{w \in W}}
    \\
    L &\to& Y
  }
$$

may be factored as

$$
  \array{
    K &\to& X' &\to& X
    \\
    \downarrow^{\mathrlap{i \in I}} && 
    \downarrow^{\mathrlap{j \in J}} && 
    \downarrow^{\mathrlap{w \in W}}
    \\
    L &\to& L' &\to& Y
  }
$$

then 

$$
  cof(j) = cof(I) \cap W
  \,.
$$


=--

+-- {: .proof}
###### Proof

(...)

=--


+-- {: .un_lemma }
###### Lemma (Smith)

Under the assumptions of Jeff Smith's theorem, a small set $J$ satisfying the condition of the above lemma can be found.

=--

+-- {: .proof}
###### Proof

(...)

=--

### Dugger's theorem ###

+-- {: .num_theorem }
###### Theorem (Dan Dugger)

Every combinatorial model category $C$ is [[Quillen equivalence|Quillen equivalent]] to a left [[Bousfield localization]] $L_S SPSh(K)_{proj}$ of the global projective [[model structure on simplicial presheaves]] $SPSh(K)_{proj}$ on a [[small category]] $K$

$$
  L_S SPSh(K)_{proj} \stackrel{\simeq_{Quillen}}{\to}
  C
  \,.
$$


=--

+-- {: .proof}
###### Proof

Recalled as theorem 4.32 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).

=--



### Tractable combinatorial model categories ###

A combinatorial model category is a [[tractable model category]] precisely if the set $I$ of generating cofibrations can be chosen such that all elements have a cofibrant object as domain.

A [[proper model category|left proper]] combinatorial model category precisely if the set $J$ of generating trivial cofibrations can be chosen with cofibrant domain.

This are corollaries 2.7 and 2..8 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).


## Properties ##

+-- {: .un_proposition }
###### Proposition

In a combinatorial model category, for every sufficiently large regular [[cardinal number|cardinal]] $\kappa$ the following holds:

* $\kappa$-[[filtered category|filtered]] [[colimit]]s preserve weak equivalences;

* hence $\kappa$-[[filtered category|filtered]] [[colimit]]s are [[homotopy colimit]]s.


=--

+-- {: .proof}
###### Proof

This appears as proposition 7.3 in [Dug00](http://arxiv.org/abs/math/0007068), reproduced for instance as prop. 2.5 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).


The point is to choose $\kappa$ such that all domains and codomains of the generating cofibrations are $\kappa$-[[compact object]]. This is possible since by assumption that $C$ is a [[locally presentable category]] all its objects are [[small object]]s, hence each a $\lambda$-[[compact object]] for some cardinal $\lambda$. Take $\kappa$ to be the maximum of these.

Let $F, G : J \to C$ be $\kappa$-filtered diagrams in $C$ and $F \to G$ a [[natural transformation]] that is degreewise a weak equivalence. Using the functorial factorization provided by the [[small object argument]] this may be factored as $F \to H \to G$ where the first transformation is objectwise an acyclic cofibration and the second objectwise an acyclic fibration, and by functoriality of the factorization this sits over a factorization

$$
  \lim_\to F \stackrel{\simeq}{\hookrightarrow} \lim_\to H \stackrel{}{\to}\lim_\to G
  \,.
$$

It remains to show that the second morphism is a weak equivalence. But by our factroization and by [[category with weak equivalences|2-out-of-3]] applied to our comoponentwise weak equivalences, we have that all its components $H(j) \to G(j)$ are acyclic fibrations .

At [[small object]] is is described in detail how $\kappa$-smallness of an object $X$ implies that morphisms from $X$ into a $\kappa$-filtered colimit lift to some component of the colimit

$$
  \array{
    \cdots&\to&H(j-1) &\to& H(j) &\to& H(j+1) &\to& \cdots
    \\
    &&&{}^{\mathllap{\exists \hat f}}\nearrow&\downarrow & \swarrow
    \\
    &&X& \stackrel{\forall f}{\to} &\lim_\to H
  }
  \,.
$$

So given a diagram

$$
  \array{
    X &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow
    \\
    Y &\to& \lim_\to G 
  }
$$

we are guaranteed, by the $\kappa$-[[small object|smallness]] of $X$ and $Y$ that we established above, a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
$$

into some component at $j \in J$ and hence a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} &
    \nearrow
    & \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
  \,.
$$

Thereby $\lim_\to H \to \lim_\to G$ is in $rlp(I) \subset W$.

=--





## Simplicial combinatorial model categories ##

Of interest are the combinatorial model categories that are at the same time [[simplicial model categories]]. These are precisely those that present [[presentable (∞,1)-categories]].

See [[combinatorial simplicial model category]].


## Combinatorial model categories from cofibrantly generated ones ##


Not every [[cofibrantly generated model category]] is also a combinatorial model category. 

For instance the standard [[model structure on topological spaces]] is cofibrantly generated, but not combinatorial. But it is [[Quillen equivalence|Quillen equivalent]] to a combinatorial model structure, namely to the standard [[model structure on simplicial sets]].

One might therefore ask which cofibrantly generated model categories are Quillen equivalent to combinatorial ones. See 

* J. Rosicky, _Are all cofibrantly generated model categories combinatorial?_ ([ps](http://www.math.muni.cz/~rosicky/papers/cof1.ps))



## References ##

Definition A.2.6.1 in 

* [[Jacob Lurie]], [[Higher Topos Theory]];

definition 1.3 in 

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

Smith's theorem appears as proposition A.2.6.8  in [[Higher Topos Theory|HTT]], as proposition 2.2 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf). After Smith presented it at a conference in Barcelona, its first appearance in a publication is apparently lemma 1.8 in 

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))


Dugger's theorem is in 

* [[Daniel Dugger]], _Combinatorial model categories have presentations_ ([arXiv](http://arxiv.org/abs/math/0007068))

[[!redirects Smith's theorem]]
[[!redirects Smith theorem]]
[[!redirects Smith's theorem]]
[[!redirects Jeff Smith's theorem]]
[[!redirects Jeff Smith theorem]]
[[!redirects Jeff Smith's theorem]]