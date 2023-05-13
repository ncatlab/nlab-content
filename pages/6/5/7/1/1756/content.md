
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Quillen adjunctions are one convenient notion of [[morphisms]] between [[model categories]].  They present [[adjoint (∞,1)-functors]] between the [[(∞,1)-category|(∞,1)-categories]] [[presentable (infinity,1)-category|presented]] by the model categories.


## Definition 
 {#Definition}

+-- {: .num_defn #QuillenAdjunction}
###### Definition

For $C$ and $D$ two [[model category|model categories]], a pair $(L,R)$

$$
  (L \dashv R) : C \stackrel{\overset{R}{\leftarrow}}{\underset{L}{\to}}
  D
$$

of [[adjoint functors]] (with $L$ [[left adjoint]] and $R$ [[right adjoint]]) is a **Quillen adjunction** if the following equivalent conditions are satisfied:

1. $L$ preserves [[cofibrations]] and [[acyclic cofibrations]];

1. $R$ preserves [[fibrations]] and [[acyclic fibrations]];

1. $L$ preserves [[cofibrations]] and $R$ preserves [[fibrations]];

1. $L$ preserves [[acyclic cofibrations]] and $R$ preserves [[acyclic fibrations]].

=--

+-- {: .num_prop}
###### Proposition

The conditions in def. \ref{QuillenAdjunction} are indeed all equivalent.

=--

+-- {: .proof}
###### Proof

Observe that

* (i) _A [[left adjoint]] $L$ between [[model categories]] preserves acyclic cofibrations precisely if its [[right adjoint]] $R$ preserves fibrations.

* (ii) _A [[left adjoint]] $L$ between [[model categories]] preserves cofibrations precisely if its [[right adjoint]] $R$ preserves acyclic fibrations.

We discuss statement (i), statement (ii) is [[formal dual|formally dual]].  So let $f\colon A \to B$ be an acyclic cofibration in $\mathcal{D}$ and $g \colon X \to Y$ a fibration in $\mathcal{C}$. Then for every [[commuting diagram]] as on the left of the following, its $(L\dashv R)$-[[adjunct]] is a commuting diagram as on the right here:

$$
  \array{
    A &\longrightarrow& R(X)
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{R(g)}}
    \\
    B &\longrightarrow& R(Y)
  }
  \;\;\;\;\;\;
  \,,
  \;\;\;\;\;\;
  \array{
    L(A) &\longrightarrow& X
    \\
    {}^{\mathllap{L(f)}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    L(B) &\longrightarrow& Y
  }
  \,.
$$

If $L$ preserves acyclic cofibrations, then the diagram on the right has a [[lift]], and so the $(L\dashv R)$-[[adjunct]] of that lift is a lift of the left diagram. This shows that $R(g)$ has the [[right lifting property]] against all acylic cofibrations and hence is a fibration. 
Conversely, if $R$ preserves fibrations, the same argument run from right to left gives that $L$ preserves acyclic fibrations.

Now by repeatedly applying (i) and (ii), all four conditions in question are seen to be equivalent.

=--

+-- {: .num_remark}
###### Remark

Quillen adjunctions that are analogous to an [[equivalence of categories]] are called _[[Quillen equivalences]]_.

In an [[enriched model category]] one speaks of _[[enriched Quillen adjunction]]_.

=--


## Properties

### Derived adjunction

+-- {: .num_prop}
###### Proposition
**([[Ken Brown's lemma]])**

Given a [[Quillen adjunction]] $(L \dashv R)$ (def. \ref{QuillenAdjunction}), then

* the [[left adjoint]] $L$ preserves weak equivalences between cofibrant objects;

* the [[right adjoint]] $R$ preserves weak equivalences between fibrant objects.

=--


+-- {: .proof}
###### Proof

To show this for instance for $R$, we may argue as in a 
[[category of fibrant objects]] and apply the _[[factorization lemma]]_
which shows that every weak equivalence between fibrant objects may be
factored, up to [[homotopy]], as a [[span]] of acyclic fibrations.

These weak equivalences are preserved by the right Quillen property of $R$ and hence the claim follows by [[category with weak equivalences|2-out-of-3]]. 

For $L$ we apply the [[formal dual|formally dual]] argument.

=--

+-- {: .num_prop #QuillenAdjunctionInducesAdjunctionOnHomotopyCategories}
###### Proposition
**([[derived adjunction]])**

For $\mathcal{C} \underoverset{\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{{}_{\phantom{Qu}}\bot_{Qu}}\mathcal{D}$ a [[Quillen adjunction]] between [[model categories]], also the corresponding left and right [[derived functors]] form a pair of [[adjoint functors]]

$$
  Ho(\mathcal{C})
    \underoverset
      {\underset{\mathbb{R}}{\longrightarrow}}
      {\overset{\mathbb{L}}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{D})
$$

between the corresponding [[homotopy category of a model category|homotopy categories]].

Moreover, the [[adjunction unit]] and [[adjunction counit]] of this derived adjunction are the images of the [[derived adjunction unit]] and [[derived adjunction counit]] of the original [[Quillen adjunction]].


=--

([Quillen 67, I.4 theorem 3](model+category#Quillen67))


### Behaviour under Bousfield localization
 {#BehaviourUnderLocalization}

+-- {: .num_prop #DescendToLeftBousfieldLocalization}
###### Proposition

Given a [[Quillen adjunction]]

$$
  (L \dashv R) 
  \;\;\;\colon\;\;\; 
  \mathcal{C}
  \underoverset
     {\underset{\;\;\;\;\;\; R \;\;\;\;\;\;}{\longrightarrow}}
     {\overset{\;\;\;\;\;\; L \;\;\;\;\;\;}{\longleftarrow}}
     {\bot_{\mathrlap{{}_{Qu}}}}
  \mathcal{D}
$$ 

and $S \subset Mor(\mathcal{D})$ is a [[set]] of [[morphisms]] such that 

1. the [[Bousfield localization of model categories|left Bousfield localization]] of $\mathcal{D}$ at $S$ exists, 

1. the [[derived functor|derived]] image $\mathbb{L}L(S)$ of $S$ lands in the [[weak equivalences]] of $\mathcal{C}$, 

then the Quillen adjunction descends to the [[Bousfield localization of model categories|Bousfield localization]] $\mathcal{D}_S$

$$
  (L \dashv R) 
  \;\;\;\colon\;\;\; 
  \mathcal{C}
  \underoverset
     {\underset{\;\;\;\;\;\; R \;\;\;\;\;\;}{\longrightarrow}}
     {\overset{\;\;\;\;\;\; L \;\;\;\;\;\;}{\longleftarrow}}
     {\bot_{\mathrlap{{}_{Qu}}}}
  \mathcal{D}_S
  \,.
$$ 

=--

This appears as ([Hirschhorn, prop. 3.3.18](#Hirschhorn))


### Of $sSet$-enriched adjunctions {#sSet}

Of particular interest are [[SSet]]-[[enriched category theory|enriched]] adjunctions between [[simplicial model categories]]: [[simplicial Quillen adjunctions]]. 

These present [[adjoint (∞,1)-functors]], as the first proposition below asserts.


+-- {: .num_prop}
###### Proposition

Let $C$ and $D$ be [[simplicial model categories]] and let 

$$
  (L \dashv R) : C \stackrel{\overset{R}{\leftarrow}}{\underset{L}{\to}} D 
$$

be an [[sSet]]-[[enriched category theory|enriched]] [[adjunction]] whose underlying ordinary adjunction is a Quillen adjunction. Let $C^\circ$ and $D^\circ$ be the [[(∞,1)-categories]] presented by $C$ and $D$ (the [[Kan complex]]-enriched full [[sSet]]-subcategories on fibrant-cofibrant objects). Then the Quillen adjunction lifts to a pair of [[adjoint (∞,1)-functors]] 

$$
  (\mathbb{L} \dashv \mathbb{R}) : C^\circ \stackrel{\leftarrow}{\to} D^{\circ}
  \,. 
$$

On the [[decategorification|decategorified]] level of the [[homotopy category|homotopy categories]] these are the total left and right [[derived functors]], respectively, of $L$ and $R$.

=--

+-- {: .proof}
###### Proof

This is proposition 5.2.4.6 in [[Higher Topos Theory|HTT]].

=--


The following proposition states conditions under which a Quillen adjunction may be detected already from knowing of the right adjoint only that it preserves fibrant objects (instead of all fibrations).


+-- {: .num_prop #RecognitionOfSimplicialQuillenAdjunctions}
###### Proposition
**(recognition of [[simplicial Quillen adjunctions]])**

If $C$ and $D$ are [[simplicial model categories]] and $D$ is a left [[proper model category]], then an [[sSet]]-enriched adjunction

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

is a Quillen adjunction already if $L$ preserves cofibrations and $R$ just fibrant objects.

=--

This appears as [[Higher Topos Theory|HTT, cor. A.3.7.2]].

See [[simplicial Quillen adjunction]] for more details.

### Associated (infinity,1)-adjunction
 {#AssociatedInfinityAdjunction}

+-- {: .un_theorem}
###### Theorem
Let $F : C \rightleftarrows D : G$ be a Quillen adjunction between [[model categories]] (which are not assumed to admit functorial factorizations or infinite (co)limits).  Then there is an induced [[adjunction of (infinity,1)-categories]]
  $$ F : C[W_C^{-1}] \rightleftarrows D[W_D^{-1}] : G $$
where $C[W_C^{-1}]$ and $D[W_D^{-1}]$ denote the respective [[simplicial localizations]] at the respective classes of [[weak equivalences]]. 
=--

See ([Mazel-Gee 16](#MazelGee16), Theorem 2.1).  (This is also asserted as ([Hinich 14](#Hinich14), Proposition 1.5.1), but it is not completely proved there -- see ([Mazel-Gee 16](#MazelGee16), Remark 2.3).)

For [[simplicial model categories]] with [[sSet]]-[[enriched functor|enriched]] [[Quillen adjunctions]] between them, this is also in ([Lurie, prop. 5.2.4.6](#Lurie)).

See also at _[derived functor -- As functors on infinity-categories](derived%20functor#OnInftyCats)_

## Related concepts

* [[Quillen reflection]]

* [[Quillen adjoint triple]]

* [[simplicial Quillen adjunction]]

* [[Quillen equivalence]]

* [[monoidal Quillen adjunction]]


## References

See the references at _[[model category]]_. For instance

* [[Philip Hirschhorn]], _Model categories and their localization_
 {#Hirschhorn}

* [[Peter May]], [[Kate Ponto]], Section 16.2 of: _[[More concise algebraic topology]]_,   University of Chicago Press (2012) ([ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf))

The proof that a Quillen adjunction of [[model categories]] induces an [[adjunction of (infinity,1)-categories]] is recorded in

* {#MazelGee16} [[Aaron Mazel-Gee]], _Quillen adjunctions induce adjunctions of quasicategories_, New York Journal of Mathematics Volume 22 (2016) 57-93 ([arXiv:1501.03146](https://arxiv.org/abs/1501.03146), [publisher](http://nyjm.albany.edu/j/2016/22-4.html))

and this question is also partially addressed in

* {#Hinich14} [[Vladimir Hinich]], *Dwyer-Kan Localization Revisited*, Homology, Homotopy and Applications Volume 18 (2016) Number 1 ([arXiv:1311.4128](https://arxiv.org/abs/1311.4128), [doi:10.4310/HHA.2016.v18.n1.a3](https://dx.doi.org/10.4310/HHA.2016.v18.n1.a3))

The case for [[simplicial model categories]] is also in 

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects Quillen adjunctions]]

[[!redirects right Quillen functor]]
[[!redirects left Quillen functor]]
[[!redirects right Quillen functors]]
[[!redirects left Quillen functors]]

[[!redirects Quillen functor]]
[[!redirects Quillen functors]]
[[!redirects Quillen pair]]
[[!redirects Quillen pairs]]
