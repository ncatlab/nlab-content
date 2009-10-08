<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>


#Idea#

Universal bundles are intermediate steps in the computation of [[homotopy fiber]]s as [[mapping cone|cone]]s are intermedite steps in the computation of [[homotopy cofiber]]s.

It is familiar from topology that one can form the path fibration $P X \to X$ of a [[topological space]]. This can be understood as an example of a general construction where one computes [[homotopy pullback]]s of the [[point]] -- or, if things are not [[groupoid]]al, [[comma object]]s.

Since universal bundles are examples of this construction, we here speak of _generalized universal bundles_. Another appropriate term might be _generalized path fibrations_.

One generalizaton of "generalized universal bundles" is that the objects in question need not be groupoidal, i.e. they behave like [[directed space]]s. In this case the [[homotopy pullback]]s familiar from topology are replaced by [[comma object]] constructions. This is useful in various applications. For instance the constructions [[category of elements]] and [[Grothendieck construction]] can be understood as such directed homotopy pullbacks of the point.

See also

* [[fibration sequence]]

  * [[homotopy limit]]

  * [[homotopy pullback]]

* [[principal bundle]]

* [[principal 2-bundle]]

* [[principal infinity-bundle]]

#Definition#

Let $C$ be a [[closed monoidal category]] with [[interval object]] $I$. Then for any [[pointed object]] $pt \stackrel{pt_B}{\to}B$ in $C$ the **generalized universal $B$-bundle** is (if it exists) the morphism

$$
  p : \mathbf{E}_{pt} B \to B
$$

which is the total composite vertical morphism of the [[pullback]] diagram

$$
  \array{
    \mathbf{E}_{\mathrm{pt}}B
    &\to&
    pt
    \\
    \downarrow && \downarrow^{pt_B}
    \\
    [I,B]
    &\stackrel{d_1}{\to}&
    B
    \\
    \downarrow^{d_0}
    \\
    B
  }
  \,.
$$

So the object $\mathbf{E}_{pt} := [I,B]\times_{B} pt $ is defined to be the [[pullback]] of the diagram
$ [I,B] \stackrel{d_1}{\to} B \stackrel{pt_B}{\leftarrow} pt$ and the morphism $\mathbf{E}_{pt}B \to B$ is the composite of the left vertical morphism in the above diagram which comes from the definition of [[pullback]] and $d_0$.

Then a (generalized) "$B$-bundle" on some object $X$ is a morphism $P \to X$ which is the [[pullback]] of the generalized universal $B$-bundle $\mathbf{E}_{pt}$ along a "classifying morphism" $g : X \to B$

$$
  \array{
    P &\to& \mathbf{E}_{pt}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& B
  }
$$

This can be understood as a "(directed) [[homotopy pullback]]" of the point:

If one defines, as one does, a (possiby [[directed object|directed]]) homotopy between two morphisms $f,g : A \to B$ to be a morphism $\eta : A \to [I,B]$ such that $d_0^* \eta = f $ and $d_1^* \eta = g$, then $P$ is the "lax pullback" (really [[comma object]]) of the point along $g$ 

$$
  \array{
    P &\to& *
    \\
    \downarrow &\Downarrow& \downarrow^{pt_B}
    \\
    X &\stackrel{g}{\to}& B
  }
  \,.
$$



The fiber of the generalized universal bundle is the [[loop space object|loop monoid]] $\Omega_{pt} B$:

$$
  \array{
    \Omega_{pt} B &\to& P &\to& *
    \\
    \downarrow &\Downarrow& \downarrow &\Downarrow& \downarrow^{pt_B}
    \\
    * &\to& X &\stackrel{g}{\to}& B
  }
  \,.
$$


the sequence

$$
  \Omega_{pt}B \stackrel{i}{\to} \mathbf{E}_{pt} B \stackrel{p}{\to} B
$$

is exact in that $i$ is the kernel of $p$ in the sense of kernels of morphisms of [[pointed object]]s (see there).

#Examples#

## Groupoid incarnations of universal principal bundles ##

In (higher) categorical contexts, take the interval object to the the interval category $I := \{a \to b\}$. Then

### Ordinary $G$-principal bundles ###

For $C =$ [[Cat]], $B := \mathbf{B}G$ a one-object groupoid corresponding to a group $G$ with the unique point, $\mathbf{E}_{pt} \mathbf{B}G = \mathbf{E}G = G//G$ is the [[action groupoid]] of $G$ acting on itself. The sequence of groupoids is
$$
  G \to G//G \to \mathbf{B}G
  \,.
$$

This is the universal $G$-bundle in its groupoid incarnation. It is a theorem by Segal from the 1960s that indeed this maps, under [[geometric realization]] to the familiar universal $G$-bundle in $Top$. Moreover, it can be seen that every $G$-principal bundle $P \to X$ in the ordinary sense is the pullback of $\mathbf{E} G$ in the following sense:

the $G$-bundle $P \to X$ is classified by a nonabelian $G$-valued 1-cocycle (the transition function of any of its local trivializations), which is an [[anafunctor]]

$$
  \array{
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^\pi
    \\
    X
  }
  \,.
$$

(For instance $\hat X$ could be the &Ccaron;ech groupoid of a [[cover]] of $X$.)

The universal groupoid bundle $\mathbf{E}G \to \mathbf{B}G$ may now be pulled back along this anafunctor to yield the groupoid bundle $g^* \mathbf{E}G \to X$ given by the total left vertical morphism in 

$$
  \array{
    g^* \mathbf{E}G &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^\pi
    \\
    X
  }
  \,.
$$

This bundle of groupoids is weakly equivalent to the $G$-principal bundle we started with in that there is a morphism of bundles of groupoids (with $P$ regarded as a bundle of discrete groupoids)

$$
  \array{
     g^* \mathbf{E}G &&\stackrel{\simeq}{\to}&& P
     \\
     & \searrow && \swarrow
     \\  
     &&X
  }
  \,.
$$

In fact that horizontal morphism is an acyclic fibration in the [[folk model structure]], i.e. a  [[k-surjective functor]] for all $k$.

This is recalled in the following reference.

### $G$-principal 2-bundles

For $C = 2Cat$, strict 2-categories , $B := \mathbf{B}G$ a strict one-object 2-groupoid corresponding to a strict [[2-group]] $G$ with the unique point, $\mathbf{E}_{pt} \mathbf{B}G = \mathbf{E}G$ was described under the name $INN(G)$ in

* Urs Schreiber, David Roberts, _The inner automorphism 3-group of a strict 2-group_, Journal of Homotopy and Related Structures, Vol. 3(2008), No. 1, pp. 193-244
([arXiv](http://arxiv.org/abs/0708.1741v2))

This was shown to be _action bigroupoid_ of $G$ acting on itself in

* Igor Bakovi&ccaron;, _Bigroupoid 2-torsors _ PhD thesis, Munich (2008) ([pdf](http://edoc.ub.uni-muenchen.de/9209/)).

One can show that every $G$-principal 2-bundle as described in

* Toby Bartels, _2-Bundles_ ([arXiv](http://arxiv.org/abs/math.CT/0410328))

* Christoph Wockel, _..._

* Igor Bakovi&ccaron;, _Bigroupoid 2-torsors _ PhD thesis, Munich (2008) ([pdf](http://edoc.ub.uni-muenchen.de/9209/)).

indeed is recovered as the pullback of $\mathbf{E} G \to \mathbf{B}G$ along the corresponding cocycle, along the lines described above.

The way this works is indicated briefly in the last section of Roberts-Schreiber above. A more detailed description for the moment is in the notes

* Urs Schreiber: [[2bundrecon.pdf:file]]


## Universal $n$-category bundles: $n$-subobject classifiers ##

One can take $B$ to be something very different from the familiar classifying groupoids. Taking it to be $n Cat$ yields the [[subobject classifier]]s of higher [[topos|toposes]]:

* $\mathbf{E}_{pt} (-1)Cat \to (-1)Cat$ is $\{\top\} \to \{\top, \bottom\}$, the [[subobject classifier]] in [[Set]].

* $\mathbf{E}_{pt} 0Cat \to 0Cat$ is $Set_* \to Set$, the forgetful functor from [[pointed set]]s, which is the  2-[[subobject classifier]] in [[Cat]]. Pullback of this creates the [[category of elements]] of a [[presheaf]].

* $\mathbf{E}_{pt} Cat \to Cat$ is $Cat_* \to Cat$. Pullback of this is the [[Grothendieck construction]].

It was David Roberts in the blog comment

* David Roberts, [comment in: 101 things to do with a 2-classifier](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html#c014559)

who first pointed out that these (higher) subobject classifiers are just generalized universal bundles in the above sense.

These cases for $n= 0$ and $n=1$ have been considered in the context of universal category bundles in 

* Kathryn Hess, _[[HessLackBundCat.pdf:file]]_ .

The discussion there becomes more manifestly one of bundles if one regards all morphisms $C \to Set$ appearing there as being the right legs of [[anafunctor]]s. 

There is a well-understood version of this for $n = (\infty,1)$, i.e. for [[(infinity,1)-category|(∞,1)-categories]]. This is described at [[universal fibration of (∞,1)-categories]].

## Action groupoids as generalized bundles ##

A morphism $\rho : B \to F$ 
to a  [[pointed object]] $F$ (needs not be a basepoint preserving morphism!) can be regarded as a _representation_ of $B$ on the point of $F$. The pullback of the universal $F$-bundle along this morphism 

$$ \rho^* \mathbf{E}_{pt} F \to B$$

can be addressed as the _$F$-bundle **$\rho$-associated** to the universal $B$-bundle $\mathbf{E}_{pt}B$. 

If $B$ is a groupoid, then $\rho^* \mathbf{E}_{pt} F$ is the [[action groupoid]] of $B$ acting on the point of $F$.

Further pulling this back along a cocycle $g : \hat X \to B$
of a $B$-principal bundle yields the $\rho$-accociated bundle of that. 

For instance for $B = \mathbf{B}G$ and $F = Vect$ 
with $\rho : \mathbf{B}G \to Vect$ a [[representation]] of the group $G$ on a vector space $V$, the $\rho$-associated $\mathrm{Vect}$-bundle on $\mathbf{B}G$ is

$$
  V \to V//G \to \mathbf{B}G
  \,.
$$

Pulling that further back along the cocycle $g : \hat X \to \mathbf{B}G$ classifying a $G$-principal bundle $P \to X$, one obtains the familiar vector bundle $P \times_G V \to X$ which is $\rho$-associated to $P$, along the lines described above:

$$
  \array{
     g^* \rho^*\mathbf{E}_{pt}F 
    &&\stackrel{\simeq}{\to}&& P\times_G V
     \\
     & \searrow && \swarrow
     \\  
     &&X
  }
  \,.
$$



