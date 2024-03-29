
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher group theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The notion of strict 2-group is a strict [[vertical categorification]] of that of [[group]].

A strict 2-group is a [[group object]] [[internalization|internal]] to the [[category]] [[Grpd]] of [[groupoid]]s (regarded as an ordinary category, not as a [[2-category]]). 

This means that it is a groupoid $G$ equipped with a product [[functor]] $\cdot : G \times G \to G$ that behaves like the product in a [[group]], in that it is unital and associative and such that there are inverses under multiplication.

More general [[2-group]]s correspond to group objects in the [[2-category]] incarnation of [[Grpd]]. For them associativity, inverses etc have to hold and exist only up to coherent natural isomorphism. So strict 2-groups are particularly rigid incarnations of [[2-group]]s. 

We may think of any 2-group $G$ in terms of its [[delooping]] $\mathbf{B}G$, a [[2-groupoid]] with a single object, with morphisms the objects of $G$ and [[k-morphism|2-morphism]]s the morphisms of $G$. If $G$ is a strict 2-group, then $\mathbf{B}G$ is a strict 2-groupoid. This is often a useful point of view. In particular, the general strictification result of [[bicategory|bicategories]] implies that any such 2-groupoid is equivalent to a strict one. So, up to the right notion of equivalence, strict 2-groups already exhaust all 2-groups; we just have to take care to allow for *homomorphisms* of these $2$-groups to be weak. (However, this theorem may not apply to structured $2$-groups, such as [[Lie 2-group]]s.)

Strict 2-groups are also equivalently encoded in terms of [[crossed module]]s $(G_2 \to G_1)$ of ordinary groups: $G_1$ is the group of [[object]]s of the groupoid $G$ and $G_2$ the group of [[morphism]]s in $G$ whose source is the neutral element in $G_1$. 

In applications it is usually useful to pass back and forth between the 2-groupoid incarnation of strict 2-groups and their incarnation as crossed modules. The first perspective makes transparent many constructions, while the second perspective gives a useful means to do computations with 2-groups. The translation between the two points of view is described in detail below.



##Definitions

A **strict [[2-group]]** is equivalently:

* an [[internal category]] in [[Grp]],
* an [[internal groupoid]] in [[Grp]],
* an internal [[group object]] in [[Cat]],
* an internal [[group object]] in [[Grpd]],
* a [[strict 2-groupoid]] with one object.


## Expanding the definition

We examine the first definition in more detail.

Copying and adapting from the entry on general internal categories we have:

A [[internal category]] in [[Grp]] is 

* a collection of group homomorphisms of the form
  $$
    C_1 \stackrel{s,t}{\to} C_0 \stackrel{i}{\to} C_1
  $$
such that the composites $s\cdot i$ and $t\cdot i$ are the identity morphisms on $C_0$, and
  such that, writing  $C_1 \times_{t,s} C_1$ for the pullback, 
  $$
    \array{
      C_1 \times_{t,s} C_1 &\to& C_1
      \\
      \downarrow && \downarrow^{t}
      \\
      C_1 &\stackrel{s}{\to}& C_0
    }
  $$
  there is, in addition,  a homomorphism
  $$
     C_1 \times_{t,s} C_1 \stackrel{comp}{\to} C_1
  $$
  "respecting $s$ and $t$";

 * such that the _composition_ $comp$ is associative
   and unital with respect to $i$ "in the obvious way".

### In terms of strict 2-groupoids

Every strict 2-group $G$ defines a strict [[2-groupoid]] $\mathbf{B}G$ -- called its [[delooping]] -- defined by the fact that

* $\mathbf{B}G$ has a single object $\bullet$;

* The [[hom-object|hom-groupoid]] $\mathbf{B}G(\bullet,\bullet) = G$ is the 2-group $G$ itself, regarded as a [[groupoid]];

* the horizontal composition in $\mathbf{B}G$ is given by the group product operation on $G$.

Conversely, every strict 2-groupoid with a single object $\bullet$ defines a 2-group this way. 

Beware, however, as discussed in detail at [[crossed module]], that (strict) 2-groups and (strict) one-object 2-groupoids, live is somewhat different 2-categories. If one wants to really _identify_ $\mathbf{B}G$ in a way that respects morphisms between these objects, one needs to think of $\mathbf{B}G$ as a [[pointed object]] equipped with its unique pointing ${*} \to \mathbf{B}G$.


### In terms of crossed modules {#InTermsOfCrossedModules}


We describe how a [[crossed module]]

$$
  [\mathbf{B}G] = (G_2 \stackrel{\delta}{\to} G_1) 
$$

with [[action]] 

$$
  \alpha 
  \,\colon\,
  G_1 
    \longrightarrow 
  Aut(G_2)
$$

encodes a strict one-object 2-groupoid $\mathbf{B}G$, and hence a strict 2-group $G$. 

There are four isomorphic but different ways to construct $\mathbf{B}G$ from $[\mathbf{B}G]$, which differ by whether the composition of 1-morphisms and of 1-morphisms with 2-morphisms in $\mathbf{B}G$ is taken to correspond to the product in the groups $G_1$ and $G_2$, respectively, or in their opposites. 

In concrete computations it happens that not all of these choices directly yield the expected formulas in terms of classical group theory from a given diagrammatics involving $\mathbf{B}G$. While all choices will be isomorphic, some will be more convenient. Therefore often it matters which one of the four choices below one takes in order to get a streamlined translation between diagrammatics and formulas. For concrete examples of this phenomenon in practice see [[nonabelian group cohomology]] and [[gerbe]].

We now define the one-object strict [[2-groupoid]] $\mathbf{B}G$ from the crossed module $(\delta : G_2 \to G_1)$ with action $\alpha : G_1 \to Aut(G_2)$.

* $\mathbf{B}G$ has a single [[object]] $\bullet$;

* The set of [[k-morphism|1-morphisms]] of $\mathbf{B}G$ is the group $G_1$:

  $$
    1Mor_{\mathbf{B}G}(\bullet, \bullet) := G_1
    \,.
  $$

  For $g \in G_1$ we write $\bullet \stackrel{g}{\to} \bullet$ for the corresponding 1-morphism in $\mathbf{B}G$;

* Composition of 1-morphisms is given by the product operation in $G_1$. There are two choices for the order in which to form the product.

  * **(convention F)** horizontal composition is given by

    $$
      (\bullet \stackrel{g_1}{\to} \bullet
      \stackrel{g_2}{\to} \bullet)
      \;\; 
      =
      \;\;
      (\bullet \stackrel{g_1 g_2}{\to} \bullet)
    $$

  * **(convention B)** horizontal composition is given by

    $$
      (\bullet \stackrel{g_1}{\to} \bullet
      \stackrel{g_2}{\to} \bullet)
      \;\; 
      =
      \;\;
      (\bullet \stackrel{g_2 g_1}{\to} \bullet)
    $$

* The [[set]] of [[k-morphism|2-morphism]]s of $\mathbf{B}G$ is the cartesian [[product]] $G_1 \times G_2$ where

  * the source operation is projection on the first factor

    $$
      s 
        \coloneqq
      p_1 
      \,\colon\,
      G_1 \times G_2 \to G_1
    $$

  * the target operation on morphisms starting at the identity morphism is the boundary map $\delta : G_2 \to G_1$ of the crossed module combined with the product in $G_1$

    $$
      t|_{{Id}\times G_2} = \delta
    $$

  So in diagrams this means that a 2-morphism 
  corresponding to $(Id, h) \in G_1 \times G_2$ is labelled as

  $$
    \array{
       &  \nearrow \searrow^{\mathrlap{Id}}
       \\
      \bullet &\Downarrow^{\mathrlap{h}}& \bullet
      \\
       &  \searrow \nearrow_{\mathrlap{\delta(h)}}
    }
    \,.
  $$

  The target of general 2-morphisms labeled by $h$ and starting at some $g$ is either $\delta(h)g $ or $g \delta(h)$, depending on the choice of conventions discussed in the following.

* Horizontal composition of 1-morphisms with 2-morphisms ("whiskering") is determined by the rule

  * **(convention R)

    $$
      \array{
        & \nearrow \searrow^{Id}  
        \\
        \bullet &\Downarrow^h& \bullet 
        &\stackrel{g}{\to}&
        \bullet
        \\
        & \searrow \nearrow
      }
      \;\;
      :=
      \;\;
      \array{
        & \nearrow \searrow^{g}
        \\
        \bullet &\Downarrow^h& \bullet
        \\
        & \searrow \nearrow
      }
    $$

    $$
      \array{
       && & \nearrow \searrow^{Id}  
        \\
        \bullet
        &\stackrel{g}{\to}&
        \bullet &\Downarrow^h& \bullet 
        \\
        && & \searrow \nearrow
       }
      \;\;
      :=
      \;\;
      \array{
        & \nearrow \searrow^{g}
        \\
        \bullet &\Downarrow^{\alpha(g)(h)}& \bullet
        \\
        & \searrow \nearrow
      }
    $$


  * **(convention L)

    $$
      \array{
       && & \nearrow \searrow^{Id}  
        \\
        \bullet
        &\stackrel{g}{\to}&
        \bullet &\Downarrow^h& \bullet 
        \\
        && & \searrow \nearrow
       }
      \;\;
      :=
      \;\;
      \array{
        & \nearrow \searrow^{g}
        \\
        \bullet &\Downarrow^h& \bullet
        \\
        & \searrow \nearrow
      }
    $$

    $$
      \array{
        & \nearrow \searrow^{Id}  
        \\
        \bullet &\Downarrow^h& \bullet 
        &\stackrel{g}{\to}&
        \bullet
        \\
        & \searrow \nearrow
      }
      \;\;
      :=
      \;\;
      \array{
        & \nearrow \searrow^{g}
        \\
        \bullet &\Downarrow^{\alpha(g)(h)}& \bullet
        \\
        & \searrow \nearrow
      }
    $$


* Horizontal composition of 2-morphisms 
  starting at the identity 1-morphism is fixed by the
  convention chosen for composition of 1-morphisms

  * in **convention F**

    $$
      \array{
        & \nearrow \searrow^{\mathrlap{Id}} & 
        &
         \nearrow \searrow^{\mathrlap{Id}}
        \\
        \bullet &\Downarrow^{h_1}&
        \bullet
        &\Downarrow^{h_2}&
        \bullet
        \\
        & \searrow \nearrow && \searrow \nearrow
      }
      \;\;\;
      =
      \;\;\;
      \array{
        & \nearrow \searrow^{\mathrlap{Id}}
        \\
        \bullet &\Downarrow^{h_1 h_2}&
        \bullet
        \\
        & \searrow \nearrow
      }
    $$
   
  * in **convention B**

    $$
      \array{
        & \nearrow \searrow^{\mathrlap{Id}} & 
        &
       \nearrow \searrow^{\mathrlap{Id}}
        \\
        \bullet &\Downarrow^{h_1}&
        \bullet
        &\Downarrow^{h_2}&
        \bullet
        \\
        & \searrow \nearrow && \searrow \nearrow
      }
      \;\;\;
      =
      \;\;\;
      \array{
        & \nearrow \searrow^{\mathrlap{Id}}
        \\
        \bullet &\Downarrow^{h_2 h_1}&
        \bullet
        \\
        & \searrow \nearrow
      }
    $$

  Notice that this is compatible with the source-target maps due to the fact that that $\delta$ is a group homomorphism.

* With these choices made, all other compositions are now fixed by use of the exchange law:


* Vertical composition of composable 2-morphisms is given, on the labels, by the product in $G_2$, in the following order

  **(in convention L B)**

  $$
    \array{
       & \nearrow &\Downarrow^{\mathrlap{h_1}}& \searrow
       \\
       \bullet &&\to&& \bullet
       \\
       & \searrow &\Downarrow^{\mathrlap{h_2}}& \nearrow
    }
    \;\;\;
    =
    \;\;\;
    \array{
      & \nearrow \searrow
      \\
      \bullet
      &\Downarrow^{\mathrlap{h_2 h_1}}& \bullet
      \\
      & \searrow \nearrow
    }   
    \,.
  $$



## Examples

### From crossed modules

By the above, every [[crossed module]] gives an example of a 2-group. 

But the nature of some strict 2-groups is best understood by genuinely regarding them as 2-categorical structures. This is true notably for the example of the automorphism 2-groups, discussed below. These, too, of course are equivalently encoded by crossed modules, but that may hide their structural meaning a little.

### Automorphism 2-groups

For $a$ any [[object]] in a [[strict 2-category]] $C$, there is the strict **automorphism 2-group** $Aut_C(a)$ whose 

* objects are 1-[[isomorphism]]s $a \to a$ in $C$;

* morphisms are 2-isomorphisms between these 1-isomorphisms.

In particular, for $K$ a [[group]] and $\mathbf{B}K$ its [[delooping]] [[groupoid]], we have the automorphism 2-group of $\mathbf{B}K$ in the 2-category [[Grpd]]. This is usually called the **automorphism 2-group of the group $K$**

$$
  AUT(K) := Aut_{Grpd}(\mathbf{B}K)
  \,.
$$

Its objects are the ordinary [[automorphism]]s of $K$ in [[Grp]], while its morphisms go between two automorphisms that differ by an inner automorphism.

Accordingly, the [[crossed module]] corresponding to the 2-group $AUT(K)$ is

$$
  [AUT(K)] =
  \left(
    \array{
      K &\stackrel{Ad}{\to}& Aut(K)
      \\
    }
  \right)
  \,,
$$

where the boundary map is the one that sends each element $k \in K$ to the inner automorphism given by conjugation with $k$:

$$
  Ad(k) : q \mapsto k q k^{-1}
  \,.
$$


### From congruence relations

Perhaps the _simplest example_ of such a structure is a 
[[congruence|congruence relation]] on a group $G$. If $\sim$ is a congruence relation on $G$, then we form the 2-group by setting $C_0 = G$ and $C_1$ to be the group of pairs $(a,b)$ with $a\sim b$.  That this is a group follows from the definition of congruence given in the above reference. The two maps $s$ and $t$ are defined by $s(a,b) = a$, $t(a,b) = b$, whilst $i(a) = (a,a)$. The pullback is a subgroup of $C_1\times C_1$ given by all 'pairs of pairs' $((a,b),(b,c))$ and the composition homomorphism sends such a pair to $(a,c)$.  The other properties are easy to check.

Any congruence relation corresponds to a [[normal subgroup]], given by those elements $a$ that are congruent to the identity element of $G$, so that $e\sim a$. Likewise given a normal subgroup $N$ of $G$ you get a congruence, with $a \sim b$ iff $b^{-1} a$ (or equivalently, $a b^{-1}$) belongs to $N$.


## Related concepts

* [[2-group]]

* [[strict 2-category]], [[strict 2-groupoid]]

## References

For more see the references at *[[2-group]]* and at *[[crossed module]]*.

The equivalence between strict 2-groups and [[crossed modules]]:

* [[Ronnie Brown]] and C. Spencer, _G-groupoids, crossed modules and the fundamental groupoid of a topological group_, Proc. Kon. Ned. Akad. v. Wet **79** (1976) 296-302. 

Textbook account:

* [[Saunders MacLane]], §XII.8 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

[[!redirects strict 2-groups]]
