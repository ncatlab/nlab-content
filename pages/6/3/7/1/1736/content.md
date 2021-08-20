
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

A [[model category]] is a context in which we can do  [[homotopy theory]] or some generalization thereof; two model categories are 'the same' for this purpose if they are Quillen equivalent.  For example, the classic version of homotopy theory can be done using either [[topological space|topological spaces]] or [[simplicial sets]].  There is a model category of topological spaces, and a model category of simplicial sets, and they are Quillen equivalent.

In short, Quillen equivalence is the right notion of [[equivalence]] for [[model category|model categories]] --- and most importantly, this notion is weaker than [[equivalence of categories]].  The work of Dwyer--Kan, Bergner and others has shown that Quillen equivalent model categories [[presentable (infinity,1)-category|present]] equivalent [[(infinity,1)-category|(infinity,1)-categories]].


## Definition

Let $C$ and $D$ be [[model category|model categories]] and let

$$
  (L \dashv R) 
  \;\colon\; 
  C 
    \stackrel{\overset{R}{\leftarrow}}{\underset{L}{\to}}
  D
$$

be a [[Quillen adjunction]] with $L$ [[left adjoint]] to $R$.

Write $Ho C$ and $Ho D$ for the corresponding [[homotopy category of a model category|homotopy categories]].

By the discussion there, $Ho C$ may be regarded as obtained by first passing to the full [[subcategory]] on cofibrant objects and then [[localization|inverting]] [[weak equivalences]], and $L$ (being a left Quillen adjoint) preserves weak equivalences between cofibrant objects.  Thus, $L$ induces a functor 

$$
  \mathbb{L} : Ho C \to Ho D
$$ 

between the [[homotopy category|homotopy categories]], called its (total) left [[derived functor]].  Similarly (but dually), $R$ induces a (total) right derived functor $\mathbb{R} : Ho D \to Ho C$. See at _[homotopy category of a model category -- derived functors](homotopy+category+of+a+model+category#DerivedFunctors)_ for more.

+-- {: .num_defn}
###### Definition

A [[Quillen adjunction]] $(L \dashv R)$ is a **Quillen equivalence** if the following equivalent conditions are satisfied.

* The total left [[derived functor]] $\mathbb{L} : Ho(C) \to Ho(D)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* The total right [[derived functor]] $\mathbb{R} : Ho(D) \to Ho(C)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* {#AdjunctOfWeakEquivalence} For every cofibrant object $c \in C$ and every fibrant object $d \in D$, a morphism $c \to R(d)$ is a weak equivalence in $C$ precisely when the [[adjunct]] morphism $L(c) \to d$ is a weak equivalence in $D$.

* The following two conditions hold:

  1. The [[derived adjunction unit]] is a weak equivalence, in that for every cofibrant object $c\in C$, the composite $c \overset{\eta_c}{\to} R(L(c)) \to R(L(c)^{fib})$ (of the [[adjunction unit]] with a [[fibrant replacement]] $R(L(c) \stackrel{\simeq}{\to} L(c)^{fib})$) is a weak equivalence in $C$, 

  1. The [[derived adjunction counit]] is a weak equivalence, in that for every fibrant object $d\in D$, the composite $L(R(d)^{cof}) \to L(R(d)) \overset{\epsilon_d}{\to} d$ (of the [[adjunction counit]] with [[cofibrant replacement]] $L(R(d)^{cof} \stackrel{\simeq}{\to} R(d))$) is a weak equivalence in $D$.

=--

+-- {: .num_remark}
###### Remark

Not every equivalence between homotopy categories of model categories lifts to a Quillen equivalence. An interesting counterexample is given for instance in ([Dugger-Shipley 09](#DuggerShipley09)).

=--

Here are further characterizations:

+-- {: .num_prop #InCaseTheRightAdjointCreatesWeakEquivalences}
###### Proposition

If in a [[Quillen adjunction]]  $ \array{\mathcal{C} &\underoverset{\underset{R}{\to}}{\overset{L}{\leftarrow}}{\bot}& \mathcal{D}}$ the [[right adjoint]] $R$ "[[created limit|creates]] weak equivalences" (in that a morphism $f$ in $\mathcal{C}$ is a weak equivalence precisely if $R(f)$ is) then $(L \dashv R)$ is a Quillen equivalence precisely already if for all cofibrant objects $c \in \mathcal{C}$ the plain [[adjunction unit]]

$$
  c \overset{\eta}{\longrightarrow} R (L (c))
$$

is a weak equivalence.

=--

(e.g. [Erdal-Ilhan 19, Lemma 3.3.](#ErdalIlhan19))

+-- {: .proof}
###### Proof

Generally, $(L \dashv R)$ is a Quillen equivalence precisely if

1. for every cofibrant object $d\in \mathcal{D}$, the "derived adjunction unit", hence the composite 

   $$
     d 
       \overset{\eta}{\longrightarrow} 
     R(L(d)) 
       \overset{R(j_{L(d)})}{\longrightarrow}
     R(P(L(d)))
   $$ 

   (of the [[adjunction unit]] with image under $R$ of any fibrant replacement $L(d) \underoverset{\in W}{j_{L(d)}}{\longrightarrow} R(P(L(d)))$) is a weak equivalence;

1. for every fibrant object $c \in \mathcal{C}$, the "derived adjunction counit", hence the composite 
  
   $$
     L(Q(R(c))) 
       \overset{L(p_{R(c)})}{\longrightarrow} 
     L(R(c)) 
       \overset{\epsilon}{\longrightarrow}
     c
   $$ 

   (of the [[adjunction counit]] with the image under $L$ of any cofibrant replacement $Q R(c)\underoverset{\in W}{p_{R(c)}}{\longrightarrow} R(c)$  is a weak equivalence in $D$.

Consider the first condition: Since $R$ preserves the weak equivalence $j_{L(d)}$, by [[two-out-of-three]] the composite in the first item is a weak equivalence precisely if $\eta$ is.

Hence it is now sufficient to show that in this case the second condition above is automatic.

Since $R$ also reflects weak equivalences, the composite in item two is a weak equivalence precisely if its image 

$$
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow} 
  R(L(R(c))) 
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
$$ 

under $R$ is.

Moreover, assuming, by the above, that $\eta_{Q(R(c))}$ on the cofibrant object $Q(R(c))$ is a weak equivalence, then by [[two-out-of-three]] this composite is a weak equivalence precisely if the further composite with $\eta$ is

$$
  Q(R(c))
    \overset{\eta_{Q(R(c))}}{\longrightarrow}
  R(L(Q(R(c))))
    \overset{R(L(p_{R(c))})}{\longrightarrow} 
  R(L(R(c))) 
    \overset{R(\epsilon)}{\longrightarrow}
  R(c)
  \,.
$$ 

But by the formula for [[adjuncts]], this composite is the $(L\dashv R)$-adjunct of the original composite, which is just $p_{R(c)}$

$$
  \frac{
     L(Q(R(c))) 
       \overset{L(p_{R(c)})}{\longrightarrow} 
     L(R(c)) 
       \overset{\epsilon}{\longrightarrow}
     c
  }{
     Q(R(C)) \overset{p_{R(c)}}{\longrightarrow} R(c)
  }
  \,.
$$

But $p_{R(c)}$ is a weak equivalence by definition of cofibrant replacement.


=--


## Properties

### 2-out-of-3 
  {#TwoOutOfThree}


Since [[equivalence of categories|equivalences of categories]] enjoy the [[category with weak equivalences|2-out-of-3-property]], so do Quillen equivalences.

### Presentation of equivalence of $(\infty,1)$-categories

[[sSet]]-[[enriched functor|enriched]] Quillen equivalences between [[combinatorial model categories]] present equivalences between the corresponding [[locally presentable (infinity,1)-categories]]. And every equivalence between these is presented by a Zig-Zag of Quillen equivalences. See there for more details.

## Examples
 {#Examples}


+-- {: .num_example #TrivialQuillenEquivalence}
###### Example
**(trivial [[Quillen equivalence]])**

Let $\mathcal{C}$ be a [[model category]]. Then the [[identity functor]] on $\mathcal{C}$ constitutes a [[Quillen equivalence]] from $\mathcal{C}$ to itself:

$$
  \mathcal{C}  
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu}}
  \mathcal{C}
$$

=--

+-- {: .proof}
###### Proof

From [this prop.](geometry+of+physics+--+categories+and+toposes#ComputationOfLeftRightDerivedFunctorsViaResolutions) it is clear that in this case the [[derived functors]] $\mathbb{L}id$ and $\mathbb{R}id$ both are themselves the [[identity functor]] on the [[homotopy category of a model category]], hence in particular are an [[equivalence of categories]].

=--



\begin{prop}\label{LeftBaseChangeQuillenEquivalence}
**([[left base change Quillen equivalence]])** \linebreak

Let $\mathcal{C}$ be a [[model category]], 
and $\phi \colon S \overset{ \in \mathrm{W} }{\longrightarrow} T$ be a [[weak equivalence]] in $\mathcal{C}$.

Then the [left base change Quillen adjunction](slice+model+structure#BaseChangeQuillenAdjunction) along $\phi$ is a Quillen equivalence

$$
  \mathcal{C}_{/T}
    \underoverset
      {\underset{\phi^*}{\longrightarrow}}
      {\overset{\phi_!}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu}}
  \mathcal{C}_{/S}  
$$

if and only if $\phi$ has this property:

$(\ast)$ *The [[pullback]] ([[base change]]) of $\phi$ along any [[fibration]] is still a [[weak equivalence]].*
\end{prop}
Notice that the property $(\ast)$ of $\phi$ is implied as soon as either:

* $\mathcal{C}$ is [[right proper model category|right proper]], or

* $\phi$ is an [[acyclic fibration]], or

* both $S$ and $T$ are [[fibrant objects]]

(for the first this follows by definition; for the second by the fact that $\phi^\ast$ is a [[right Quillen functor]] by [this Prop.](slice+model+structure#LeftBaseChangeQuillenAdjunction); for the third by [this Prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback) on recognizing [[homotopy pullbacks]]).
\begin{proof}
Using the characterization of Quillen equivalences by derived adjuncts ([here](#AdjunctOfWeakEquivalence)), the base change adjunction is a Quillen equivalence iff for 

* any [[cofibrant object]] $X \to S$ in the slice over $S$ (i.e. $X$ is cofibrant in $\mathcal{C}$) 

* and a [[fibrant object]] $p \colon Y \to T$ in the slice over $T$ (i.e. $p$ is a [[fibration]] in $\mathcal{C}$), 

we have that 

(1) $X \to \phi^*(Y) = S \times_T Y$ is a weak equivalence 

iff 

(2) $\phi_!(X) \to Y$ is a weak equivalence.

But the latter morphism is the top composite in the following [[commuting diagram]]:

$$
  \array{
    X 
      &\longrightarrow& 
    S \times_T Y 
      &\overset{p^\ast \phi}{\longrightarrow}& 
    Y
    \\
    &\searrow& 
    \big\downarrow 
    &{}^{_{(pb)}}& 
    \big\downarrow {}^{\mathrlap{p \in Fib}}
    \\
    && S &\underset{\phi \in \mathrm{W} }{\longrightarrow}& T
  }
$$

Hence the [[two-out-of-three]]-property says that (1) is equivalent to (2) if $p^\ast \phi$ is a weak equivalence.

Conversely, taking $X \to \phi^\ast(X)$ to be a weak equivalence (hence a [[cofibrant resolution]] of $\phi^\ast(X)$), [[two-out-of-three]] implies that if $(\phi_! \dashv \phi^\ast)$ is a Quillen equivalence, then $p^\ast \phi$ is a weak equivalence.

\end{proof}


## Related concepts

* [[Quillen adjunction]]

* [[Quillen reflection]]

* [[simplicial Quillen adjunction]]

* **Quillen equivalence**

* [[monoidal Quillen adjunction]]

## References

For standard references see at _[[model category]]_.

An example of an equivalence of [[homotopy categories]] of model categories which does not lift to a Quillen equivalence is in 

* {#DuggerShipley09} [[Daniel Dugger]], [[Brooke Shipley]], _A curious example of triangulated-equivalent model categories which are not Quillen equivalent_, Algebraic & Geometric Topology 9 (2009) ([pdf](http://homepages.math.uic.edu/~bshipley/dugger.shipley.curious.example.pdf))
 
The characterization of Quillen equivalences in the case that one of the adjoints creates equivalences appears for instance in 

* {#ErdalIlhan19} Mehmet Akif Erdal, Aslı Güçlükan İlhan, _A model structure via orbit spaces for equivariant homotopy_, Journal of Homotopy and Related Structures volume 14, pages 1131–1141 (2019) ([arXiv:1903.03152](https://arxiv.org/abs/1903.03152), [doi:10.1007/s40062-019-00241-4](https://doi.org/10.1007/s40062-019-00241-4))


[[!redirects Quillen equivalences]]
[[!redirects Quillen equivalent]]
[[!redirects Quillen equivalent model categories]]