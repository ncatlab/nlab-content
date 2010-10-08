
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

A [[monomorphism]] is _regular_ if it behaves like an [[embedding]].

* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .

The universal factorization through an embedding is the [[image]].


## Definition

A **regular monomorphism** is a [[morphism]] $f : c \to d$ in some [[category]] which occurs as the [[equalizer]] of _some_ parallel pair of morphisms $d \stackrel{\to}{\to} e$, i.e. for which a [[limit]] diagram

$$
  c \stackrel{f}{\to} d \stackrel{\to}{\to} e
$$

exists.

From the defining universal property of the [[limit]] it follows directly that a regular monomorphism is automatically a [[monomorphism]].

The dual concept is that of a [[regular epimorphism]].


## Properties

### Relation to effective monomorphisms 

A monomorphism $i: A \to B$ is an [[effective monomorphism]] if it is the [[equalizer]] of its [[cokernel pair]]: if the [[pushout]]

$$\array{
A & \stackrel{i}{\to} & B \\
i \downarrow & & \downarrow i_1 \\
B & \underset{i_2}{\to} & B +_A B
}$$ 

exists and $i$ is the equalizer of the pair of coprojections $i_1, i_2: B \stackrel{\to}{\to} B +_A B$. Obviously effective monomorphisms are regular. 

+-- {: .un_prop} 
######Proposition
In a category with [[finite limit]]s and [[finite colimit]]s, every regular monomorphism $i: A \to B$ is effective. 
=-- 

+-- {: .proof} 
######Proof 
Suppose $i: A \to B$ is the equalizer of a pair of morphisms $f, g: B \to C$, and with notation as above, let $j: E \to B$ be the equalizer of the pair of coprojections $i_1, i_2$. Since $f \circ i = g \circ i$, there exists a unique map $\phi: B +_A B \to C$ such that $\phi \circ i_1 = f$ and $\phi \circ i_2 = g$. Then, since 
$$f j = \phi i_1 j = \phi i_2 j = g j$$ 
and since $i: A \to B$ is the equalizer of the pair $(f, g)$, there is a unique map $k: E \to A$ such that $j = i k$. Since $i_1 i = i_2 i$, there is a unique map $l: A \to E$ such that $i = j l$. The maps $k$, $l$ are mutually inverse. 
=-- 

{#RegEquEff}
+-- {: .un_lemma}
###### Lemma
In a [[category]] with [[equalizer]]s and [[cokernel pair]]s, a regular monomorphism is precisely an effective monomorphism.
=--





## Examples {#Examples}

* In [[Set]], or more generally in any [[pretopos]], every [[monomorphism]] is regular.

* Similarly, in [[Ab]], and more generally any [[abelian category]], every monomorphism is regular.

+-- {: .un_prop}
###### Proposition

In [[Top]], the monics are the injective functions, while the regular monos are the embeddings (that is, the injective functions whose sources have the [[induced topology|topologies induced]] from their targets); these are in fact all of the [[extremal monomorphism]]s.
=--

+-- {: .proof}
###### Proof

Use the [above lemma](#RegEquEff).

If $i: X \to Y$ is a subspace embedding, then we form the cokernel pair $(i_1, i_2)$ by taking the [[pushout]] of $i$ against itself (in the category of sets, and using the quotient topology on a disjoint sum). The equalizer of that pair is the set-theoretic equalizer of that pair of functions endowed with the subspace topology. Since monos in $Set$ are regular, we get the function $i$ back with the subspace topology. This completes the proof. 
=--

+-- {: .un_prop}
###### Proposition

In [[Grp]], the monics are (up to [[isomorphism]]) the inclusions of [[subgroup]]s, and every monomorphism is regular
=--

In contrast, the [[normal monomorphisms]] (where one of the morphisms $d \to e$ is required to be the [[zero morphism]]) are the inclusions of [[normal subgroups]].

+-- {: .proof}
###### Proof

We follow [exercise 7H](http://katmat.math.uni-bremen.de/acc/acc.pdf#page=129) of ([AdamekHerrlichStrecker](#AdamekHerrlichStrecker)).

Let $K \hookrightarrow H$ be a subgroup. We 
need to define another group $G$ and group homomorphisms 
$f_1, f_2 : H \to G$ such that

$$
  K = \{h \in H  | f_1(h) = f_2(h)\}
  \,.
$$

To that end, let 

$$
  X  := H/K  \coprod  \{\hat K\}  := \{ h K | h \in H \}  \coprod  \{\hat K\} 
$$

be the set of [[coset]]s together with one more element $\hat K$.

Let then

$$ 
  G = Aut_{Set}(X)
$$

be the [[permutation group]] on $X$. 

Define $\rho \in G$ to be the permutation that exchanges the coset $e K$ with the extra element $\hat K$ and is the identity on all other elements.

Finally define group homomorphism $f_1,f_2 : H \to G$ by

$$
  f_1(h) : x \mapsto 
  \left\{
     \array{
        h h' K & if x = h' K
        \\
        \hat K & if x = \hat K
     }
  \right.
$$

and

$$
  f_2(h) = \rho \circ f_1(h) \circ \rho^{-1}
  \,.
$$

It is clear that these maps are indeed group homomorphisms.

So for $h \in H$ we have that 

$$
  f_1(h) : \hat K \mapsto \hat K
  \,,
$$

and

$$
  f_1(h) : e K \mapsto h K
$$

and

$$
  f_2(h) 
  : 
  \hat K 
   \mapsto 
  e K 
    \mapsto 
   h K 
   \mapsto 
  \left\{
    \array{
     \hat K & if h \in K
     \\
     h K & otherwise
   }
   \right.
  \,.
$$

$$
  f_2(h) : e K \mapsto \hat K \mapsto \hat K \mapsto e K
  \,.
$$

So we have $f_1(h) = f_2(h)$ precisely if $h \in K$.

=--


## In an $(\infty,1)$-category {#Infty1Version}

In the context of [[higher category theory]]
the ordinary [[limit]] diagram $c \stackrel{f}{\to} d \stackrel{\to}{\to} e $ may be thought of as the beginning of a [[homotopy limit]] diagram over a [[cosimplicial object|cosimplicial]] diagram

$$
  c \stackrel{f}{\to} d_0 \stackrel{\to}{\to} d_1
  \stackrel{\to}{\stackrel{\to}{\to}}
  d_2
  \cdots
  \,.
$$

Accordingly, it is not unreasonable to define a regular monomorphism for instance in an [[(∞,1)-category]], to be a morphism which is the [[limit in a quasi-category]] of a cosimplicial diagram.

In practice this is of particular relevance for the $\infty$-version of [[regular epimorphism]]s: with the analogous definition as described there, a morphism $f : c \to d$ is a [[regular epimorphism]] in an [[(∞,1)-category]] $C$ if for all objects $e \in C$ the induced morphism $f^* : C(d,e) \to C(c,e)$ is a [[regular monomorphism]] in [[∞Grpd]] (for instance [[model structure on simplicial sets|modeled]] by a [[homotopy limit]] over a cosimplicial diagram in [[SSet]]).

**Warning.** The same warning as at [[regular epimorphism]] applies: with this definition of regular monomorphism in an [[(∞,1)-category]] these may fail to satisfy various definitions of plain monomorphisms that one might think of. 

## References

* [[Jiri Adamek]], [[Horst Herrlich]], and [[George Strecker]], _Abstract and concrete categories: the joy of cats_. ([pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf))
{#AdamekHerrlichStrecker}


[[!redirects regular monomorphism]]
[[!redirects regular monomorphisms]]
[[!redirects regular mono]]
[[!redirects regular monos]]
[[!redirects regular monic]]
[[!redirects regular monics]]

[[!redirects regular subobject]]
[[!redirects regular subobjects]]
