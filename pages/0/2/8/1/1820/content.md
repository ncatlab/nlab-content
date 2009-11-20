
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

## Jeff Smith's theorem ##

The central theorem about combinatorial model categories is **Jeff Smith's theorem** which establishes the existence of model category structures from a comparatively small amount of input data.

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

The proof of the first part of the theorem proceeds in two lemmas, described below.

The converse statement, that every combinatorial model category satisfies the assumptions of the theorem, is for instance corollary 2.6 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).

=--

+-- {: .un_lemma }
###### Lemma (Smith)

If a sub-class $J \subset cof(I) \cap W$ is such that every commutative square

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

=--


+-- {: .un_lemma }
###### Lemma (Smith)

Under the assumptions of Jeff Smith's theorem, a small set $J$ satisfying the condition of the above lemma can be found.

=--

+-- {: .proof}
###### Proof

...

=--

## Tractable combinatorial model categories ##

A combinatorial model category is a [[tractable model category]] precisely if the set $I$ of generating cofibrations can be chosen such that all elements have a cofibrant object as domain.

A [[proper model category|left proper]] combinatorial model category precisely if the set $J$ of generating trivial cofibrations can be chosen with cofibrant domain.

This are corollaries 2.7 and 2..8 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).


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

* [[Jacob Lurie]], [[Higher Topos Theory]]

definition 1.3 in 

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

Smith's theorem is recalled as theorem xyz in [[Higher Topos Theory|HTT]], as proposition 1.7 in Barwick. After Smith presented it at a conference in Barcelona, its first appearance in a publication is apparently lemma 1.8 in 

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))


[[!redirects Smith's theorem]]
[[!redirects Smith theorem]]
[[!redirects Smith's theorem]]
[[!redirects Jeff Smith's theorem]]
[[!redirects Jeff Smith theorem]]
[[!redirects Jeff Smith's theorem]]