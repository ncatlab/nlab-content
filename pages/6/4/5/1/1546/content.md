<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **Atiyah Lie groupoid** $At(P)$ of a $G$-[[principal bundle]] $P \to X$ is the [[Lie groupoid]] whose objects are the fibers of the bundle, and whose morphisms are the $G$-equivariant morphisms between the fibers. Schematically:

$$
  At(P)
  = 
  \left\{
     P_x \stackrel{\alpha}{\to} P_y
     | x,y \in X
  \right\}
  \,.
$$

Its [[Lie algebroid]] is the [[Atiyah Lie algebroid]] $at(P)$ of $P$.

Both the Atiyah Lie groupoid and its Lie algebroid are used to characterize and are characterized by [[connection on a bundle|connections]] on $P$.



## Definition

As generally for every [[Lie algebroid]], there are different [[Lie groupoid]]s [[Lie integration|integrating]] the [[Atiyah Lie algebroid]]. We describe two of them.

The Aityah Lie algebroid $at(P)$ of the [[principal bundle]] $P \to X$ comes canonically with a morphism $at(X) \to T X$ to the [[tangent Lie algebroid]].

The simplest [[Lie integration]] of the tangent Lie algebroid is the [[codiscrete groupoid]] $X \times X$ of $X$. On the other hand, the universal integration is the [[fundamental groupoid]] $\Pi(X)$ (both coincide precisey if $X$ is a [[simply connected space]]). 

Accordingly, there is a version of the Atiyah Lie groupoid over $X \times X$, and a richer version over $\Pi(X)$. 

### Over the pair groupoid

For $G$ a Lie group and $P \to X$ a $G$-principal bundle, the **Atiyah groupoid** $At(P)$ -- also called the **gauge groupoid** or **transport groupoid** -- of $P$ is the [[Lie groupoid]] with

* $Obj(At(P)) = X$;
* $Mor(At(P)) = (P \times P)/G$, where the [[quotient object|quotient]] is taken with respect to the [[diagonal action]] of $G$ on $P \times P$.

The Atiyah groupoid sits in an sequence of groupoids

$$
  Ad(P) \to At(P) \to Codisc(X)
$$

where

* $Ad(P) = P \times_G G$ is the **adjoint bundle** of groups associated via the adjoint action of $G$ on itself; regarded as a smooth union $\coprod_{x \in X} \mathbf{B} P_x \times_G G$ of one-object groupoids coming from [[group]]s;

* $Codisc(X) = (X \times X \rightrightarrows X)$ is the [[codiscrete groupoid]] of $X$

* the [[functor]] $Ad(P) \to At(P)$ is the identity on objects and on morphisms given by the canonical identification $P_x \times_G G \stackrel{\simeq}{\to} (P_x \times P_x) G$, where again we use the diagonal action of $G$ on $P_x \times P_x$.

* the functor $At(P) \to Codisc(X)$ is the unique one that is the identity on objects.

+-- {: .query}
What is all of this $diag$ stuff?  I don\'t understand either $(P \times P)/_{diag} G$ or $(P_x \times P_x)_{diag} G$.  ---Toby

[[David Roberts]]: It's to do with the diagonal action of $G$ on $P\times P$ as opposed to the antidiagonal (if $G$ is abelian) or the action on only one factor. I agree that it's a bad notation.

_Toby_:  How well do you think it works now, with the notation suppressed and a note added in words?  (For what it\'s worth, the diagonal action seems to me the only obvious thing to do here, although admittedly the others that you mention do exist.)

_Todd_: I personally believe it works well. A small note is that this construction can also be regarded as a tensor product, regarding the first factor $P$ as a right $G$-module and the second a left module, where the actions are related by $g p = p g^{-1}$. 

_Toby_:  H\'m, maybe we should write [[diagonal action]] if there\'s something interesting to say about it.
=--

Notice that a splitting (a [[section]])

$$
  Codisc(X) \to At(P)
$$

of the Atiyah groupoid is a trivialization of $P$. On the other hand, locally on [[contractible space|contractible]] $U \subset X$ we have $Codisc(U) \simeq \Pi_1(U)$ with $U$ the [[fundamental groupoid]] of $U$, and a splitting $Codisc(U) \simeq \Pi_1(U) \to At(P)|_U$ is still a trivialization over $U$ but indicates now that one may want to interpret it as giving rise to a flat [[connection]].

Indeed, we have the sequence of 
of surjective and [[full functor]]s of
[[path category|path categories]]  

$$
  P_1(X) \to \Pi_1(X) \to Codisc(X)
$$

with $\Pi_1(X)$ the [[fundamental groupoid]] and $P_1(X)$ the smooth [[path groupoid]] and may refine the Atiyah groupoid by pulling back along these.

Write therefore $At'(P) := At(P) \times_{Codisc(X)} \Pi_1(X)$ for the [[pullback]]

$$
  \array{
     At'(P) &\to& \Pi_1(X)
     \\
     \downarrow && \downarrow
     \\
     At(P) &\to& Codisc(X)
  }
  \,.
$$ 

A splitting $\Pi_1(X) \to At'(P)$ of the top row is now precisely a flat [[connection]] on $P$.

If we pull back further to $A''$ 

$$
  \array{
     At''(P) &\to& P_1(X)
     \\
     \downarrow && \downarrow
     \\
     At'(P) &\to& \Pi_1(X)
     \\
     \downarrow && \downarrow
     \\
     At(P) &\to& Codisc(X)
  }
  \,.
$$ 

then splittings of $P_1(X) \to At''(X)$ are precisely (not necessarily flat) connections on $P$.

All this is more well known in terms of the [[Lie algebroid]] underlying the Atiyah Lie groupoid, i.e. the **Atiyah Lie algebroid** sequence

$$
  ad(P) \to at(P) \to T X
  \,,
$$

where 

* $ad(P) = P \times_g Lie(G)$ is the adjoint bundle of Lie algebras, associated via the adjoint action of $G$ on its Lie algebra;

* $at(P) = (T P)/G$ is the **Atiyah Lie algebroid**

* $T X$ is the [[Lie algebroid|tangent Lie algebroid]].

Indeed, a splitting $\nabla_{flat} : T X \to at(P)$ of this sequence in the category of [[Lie algebroid]]s is precisely again a flat connection on $P$ and integrates under [[Lie integration]] to the splitting of $At'(P)$ discussed above.

To get non-flat connections in the literature one often sees discussed splittings of the Atiyah Lie algebroid sequence in the category just of vector bundles. In that case one finds the curvature of the connection precisely as the obstruction to having a splitting even in Lie algebroids.

One can describe non-flat connections without leaving the context of Lie algebroids by passing to higher Lie algebroids, namely $L_\infty$-[[L-infinity-algebroid|algebroids]].

### Over the path $\infty$-groupoid

...

## Relation to differential nonabelian cohomology {#RelationToDiffNonabCohomology}

+-- {: .standout}

The following is not in the literature. -- [[Urs Schreiber|Urs]]

=--

We discuss the Atiyah Lie groupoid along the lines of [[nonabelian groupoid cohomology]] of the [[path n-groupoid]] of the base [[manifold]] $X$.


Write $\mathbf{B}G$ for the [[delooping]] of $G$.
Write $\Pi(X)$ for the [[path ∞-groupoid]] of $X$. For the present purpose of Atiyah 1-groupoids this may be taken to be simply the [[path n-groupoid|path 2-groupoid]].

+-- {: .un_remark}
###### Remark

Much of what makes the following discussion somewhat less than straightforward is the fact already manifest in and discussed at [[nonabelian group cohomology]]: nonabelian degree 2-cocycles with coefficients in the ([[delooping]] of the) [[automorphism 2-group]] $AUT(G)$ classify really [[action groupoid]]s of actions on bundles with typical fiber $F = Aut(G)$, while the object that one wants to see classified (there: a group extension; here: the Atiyah Lie groupoid) is obtained from this only after forgetting the elements in these fibers, and just remembering the action.

=--


+-- {: .un_prop}
###### Claim

A $G$-[[principal bundle]] $P \to X$ is classified by a morphism $g : X \to \mathbf{B}G$.

Putting a [[connection on a bundle|connection]] on $P$ give a parallel transport morphism $\Pi(X)  \to \mathbf{B}INN(G)$
into the [[inner automorphism 2-group]] of $G$, which fits into a diagram

$$
  \array{
    X &\stackrel{g}{\to}& \mathbf{B}G &&& {underlying\;cocycle}
    \\
    \downarrow && \downarrow
    \\
    \Pi(X) &\stackrel{(A,F)}{\to}& \mathbf{B} INN(G) &&& 
      {connection}
    \\
    \downarrow^{\mathrlap{Id}} && \downarrow
    \\
    \Pi(X) &\stackrel{F}{\to}& \mathbf{B} AUT(G)
    &&& {nonabelian\; curvature}
  }
  \,,
$$

where we have added the morphism $INN(G) \to AUT(G)$ into the [[automorphism 2-group]].

The [[action groupoid]] $(P \times_{G} Aut(G))//At(P)$ of the  Atiyah Lie groupoid acting on the [[associated bundle]] $(P \times_G Aut(G))$, regarded as a groupoid over $\Pi(X)$, is classified by $F$: it is the [[homotopy fiber]] of $F$, in that there is a [[homotopy pullback]] diagram

$$
  \array{
    \array{
       (P \times_{G} Aut(G) )//At(P) &\to& {*}
       \\
       \downarrow && \downarrow
       \\
       \Pi(X) &\stackrel{F}{\to}& \mathbf{B} AUT(G)
    }
  }
  \,.
$$

The Atiyah Lie groupoid itself is the corresponding quotient

$$
  (P \times_G Aut(G)) \to (P \times_{G} Aut(G))//At(P)
  \to At(P)
  \,.
$$

=--

+-- {: .proof}
###### Proof

**Setup**

Choose to model all [[∞-Lie groupoid]]s in terms of the local projective [[model structure on simplicial presheaves]] on the [[site]] [[CartSp]] of cartesian spaces. 

All the Lie $2$-groupoids appearing here are represented by [[Kan complex]] valued sheaves. They satisfy [[descent]] on contractible domains, hence on all representables, hence are fibrant in the local projective model structure.

As discussed in the subsection on [cofibrant objects](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects), a cofibrant replacement for the [[manifold]] $X$ is given by the [[Cech nerve]] $Y := C(\coprod U_i)$ of any good cover $\{U_i \to X\}$. So fix any such good cover of $X$.

Accordingly, a cofibrant version of the [[path ∞-groupoid]] is given by the [[coend]] $\Pi(Y) = \int^{U \in C} \Pi(U) \cdot Y(U)$. This is the $n$-groupoid generated in degree $k$ from 

* points in $(k+1)$-fold intersections;

* paths in $k$-fold intersections

* surfaces in $(k-1)$-fold intersections,

etc.

**The bundle $P \times_G Aut(G)$**

The bundle $P \times_G Aut(G)$ is, by definition, 
the one classified by the morphism

$$
  Ad(g) : X \stackrel{g}{\to} \mathbf{B}G \stackrel{Ad}{\to} 
  \mathbf{B}Aut(G)
$$

represented by a morphism

$$  
  X \stackrel{\simeq}{\leftarrow}Y \to \mathbf{B}Aut(G)
$$

in $SPSh(CartSp)_{proj}^{loc}$.

We compute the [[homotopy pullback]]

$$
  \array{
    P \times_G Aut(G) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{Ad(g)}{\to}& \mathbf{B}Aut(G)
  }
$$

as usual in terms of an ordinary [[pullback]] 

$$
  \array{
    P \times_G Aut(G) &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{Ad(g)}{\to}& \mathbf{B}Aut(G)
  }
$$


along the representing cocycle 
of the [[generalized universal bundle|universal bundle]] $\mathbf{E}Aut(G) \to \mathbf{B} Aut(G)$, which is the [[groupoid]]

$$
  \mathbf{E}Aut(G) = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{\alpha}}\swarrow && \searrow^{\mathrlap{\beta}}
       \\
       \bullet &&\stackrel{\gamma}{\to}&& \bullet
    }
  \right\}
$$

whose morphisms are commuting trianfles in $\mathbf{B}Aut(G)$, with the projection to $\mathb{B}Aut(G)$ being the projection onto the horizontal 
component.

So the objects of $P \times_G Aut(G)$ are pairs $((x,i), \alpha)$ consisting of a point $x \in X$ in a patch $U_i$, together with an element $\alpha \in Aut(G)$, and a morphism $((x,i), \alpha) \to ((y,j)\beta)$ exists iff $x = y$ and is then given by

$$
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{\alpha}}\swarrow && \searrow^{\mathrlap{\beta}}
       \\
       \bullet &&\stackrel{Ad(g_{i j}(x))}{\to}&& \bullet 
       \\
       \\
       (x,i) &&\to&& (x,j)
    }
  \right\}
  \,.
$$



**The homotopy fiber of $\Pi(X) \to \mathbf{B}AUT(G)$**

We compute now the [[homotopy pullback]]

$$
  \array{
    Q &\to& &\to& {*}
    \\
    \downarrow &&&& \downarrow
    \\
    \Pi(X) &\to& \mathbf{B}INN(G) &\to& \mathbf{B}AUT(G) 
  }
$$

for $\Pi(X) \to \mathbf{B} INN(G)$ coming from the choice of any [[connection on a bundle|connection]] on $P$, in terms of the ordinary  [[pullback]] 

$$
  \array{
    Q &\to& \mathbf{E}AUT(G)
    \\
    \downarrow && \downarrow
    \\
    \Pi(Y) &\to& \mathbf{B}AUT(G) 
  }
$$

along the representing cocycle $\Pi(Y) \to \mathbf{B}AUT(G)$ of the [[generalized universal bundle]] $\mathbf{E}AUT(G)$ of the [[automorphism 2-group]] $AUT(G)$.

The computation is (apart from the fact that it takes place in a smooth context which is taken care of by the abstract nonsense) entirely analogous as that of the 2-cocycles discussed at [[nonabelian group cohomology]], the only difference being that the domain is here not a one-object groupoid that is the [[delooping]] of a group, but the genuine many-object groupoid $\Pi(Y)$.

As there, we ventually make use of the translation between [[strict 2-group]]s and [[crossed module]]s - as described at [strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules) -- in order to translate some of the diagrams to follow into formulas.
We follow the **convention LB**, as described there, in order to do so.

In $\mathbf{E}AUT(G)$ 

* an object is an automorphism $\alpha \in Aut(G)$

* a morphism $(\gamma, b) :  \alpha \to \beta$ is a triangle

  $$
    \array{
      && \bullet
      \\
      & {}^{\mathllap{\alpha}}\swarrow 
      & {}^{\mathllap{b}}\swArrow& 
     \searrow^{\mathrlap{\beta}}
     \\
     \bullet &&\stackrel{\gamma}{\to}&& \bullet
    }
  $$

* a 2-cell $k : (\gamma_1, b_1) \cdots (\gamma_2, b_2) \Rightarrow (\gamma_3, b_3)$ 
  
  is a 2-cell

  $$
    \array{
       && \bullet
       \\
       & {}^{\mathllap{\gamma_1}}\swarrow 
       & {}^{\mathllap{k}}\swArrow& 
       \searrow^{\mathrlap{\gamma_2}}
       \\
       \bullet &&\stackrel{\gamma_3}{\to}&& \bullet
    }
  $$
  
  in $\mathbf{B}AUT(G)$ such that

  $$
    \array{
      && \bullet
      \\
      &\swarrow &{}^{\mathllap{b_3}}\swArrow& \searrow
      \\
      \bullet &&\to&& \bullet
    }
    \;\;\;
    =
    \;\;\;
    \array{
      && \bullet
      \\
      &\swarrow& \downarrow & \searrow
      \\
      \downarrow 
      &
        {}^{\mathllap{b_1}}\swArrow
      & 
        \bullet 
       &
      {}^{\mathllap{b_2}}\swArrow& \downarrow
      \\
      \downarrow 
      & \nearrow &\Downarrow^{\mathrlap{k}}
      & \searrow & \downarrow
      \\
      \bullet && \stackrel{}{\to}
      &&
      \bullet
    }
    \,.
  $$


Using this, we find the [[pullback]] 2-groupoid $\Pi(Y) \times_{\mathbf{B}AUT(K)} \mathbf{E}G$ to be given as follows:

* an object is pair $((x,i), \alpha)$ consisting of a point $x \in X$ and a patch $U_i$ containing it, and an automorphism $\alpha \in Aut(G)$

* a morphism is, over a path $(p,i) : (x,i) \to (y,i)$ in $U_i$ a diagram

  $$
    \array{
      && \bullet
      \\
      & {}^{\mathllap{\alpha}}\swarrow 
      & {}^{\mathllap{b}}\swArrow& 
     \searrow^{\mathrlap{\beta}}
     \\
     \bullet &&\stackrel{Ad(tra_{\nabla}(p))}{\to}&& \bullet
     \\
     \\
     (x,i) &&\stackrel{(p,i)}{\to}&& (y,i)
    }
    \,,
  $$

  where $tra_\nabla(p)$ is the [[parallel transport]] of the chosen connection on $P$ along the path $p$;

  and over a Cech morphism $(x,i) \to (x,j)$ a diagram

  $$
    \array{
      && \bullet
      \\
      & {}^{\mathllap{\alpha}}\swarrow 
      & {}^{\mathllap{b}}\swArrow& 
     \searrow^{\mathrlap{\beta}}
     \\
     \bullet &&\stackrel{Ad(g_{i j}(x))}{\to}&& \bullet
     \\
     \\
     (x,i) &&\stackrel{}{\to}&& (x,j)
    }
    \,,
  $$


* a 2-cell over a surface $\Sigma : p_1 \cdot p_2 \Rightarrow p_3$ is 

  $$
    \array{
      && \bullet
      \\
      &\swarrow &{}^{\mathllap{b_3}}\swArrow& \searrow
      \\
      \bullet &&\stackrel{Ad(tra_\nabla(p_3))}{\to}&& \bullet
    }
    \;\;\;
    =
    \;\;\;
    \array{
      && \bullet
      \\
      &\swarrow& \downarrow & \searrow
      \\
      \downarrow 
      &
        {}^{\mathllap{b_1}}\swArrow
      & 
        \bullet 
       &
      {}^{\mathllap{b_2}}\swArrow& \downarrow
      \\
      \downarrow 
      & {}^{\mathllap{Ad(tra_{\nabla}(p_1))}}
       \nearrow &\Downarrow^{\mathrlap{tra_\nabla(\Sigma)}}
      & \searrow^{\mathrlap{Ad(tra_\nabla(p_2))}}
      & \downarrow
      \\
      \bullet && \stackrel{}{\to}
      &&
      \bullet
    }
  $$

  and over a Cech 2-cell is

  $$
    \array{
      && \bullet
      \\
      &\swarrow &{}^{\mathllap{b_3}}\swArrow& \searrow
      \\
      \bullet &&\stackrel{Ad(g_{i k}(x))}{\to}&& \bullet
    }
    \;\;\;
    =
    \;\;\;
    \array{
      && \bullet
      \\
      &\swarrow& \downarrow & \searrow
      \\
      \downarrow 
      &
        {}^{\mathclap{b_1}}\swArrow
      & 
        \bullet 
       &
      {}^{\mathclap{b_2}}\swArrow& \downarrow
      \\
      \downarrow 
      & {}^{\mathclap{Ad(g_{i j}(x))}}
       \nearrow &\Downarrow^{\mathrlap{Id}}
      & \searrow^{\mathclap{Ad(g_{j k}(x))}}
      & \downarrow
      \\
      \bullet && \stackrel{}{\to}
      &&
      \bullet
    }
    \,.
  $$

**The identification with the groupoid $(P \times_G Aut(G)) // At(P)$**

We now show that the homotopy fiber computed above is indeed the groupoid $(P \times_G Aut(G)) // At(P)$.

The main point is the realizaiton of the Atiyah Lie groupoid $At(P)$ as a groupoid over $\Pi(Y)$.

A morphism in $At(P)$ over a path $p : x \to y$ is a fiber homomorphism $f : P_x \to P_y$. Since we have chose a [[connection on a bundle|connection]] $\nabla$ on $P$, we may always express this relative to the [[parallel transport]] of the connection along $p$, which provides a reference frame in which to measure morpisms between fibers, and defines for given $f$ a group element $b$ defined by

$$
  \array{
    && P_y
    \\
    & {}^{\mathllap{tra_\nabla(p)}}\nearrow & \downarrow^{b}
    \\
    P_x
    &\stackrel{f}{\to}&
    P_y
  }
  \,.
$$

When we express composition of fiber morphisms in terms of the compositiion of the group elements associated to them this way, we find an adjoint action of the parallel transport on the group elements:

$$
  \array{
    &&&& P_z
    \\
    && & {}^{\mathllap{tra_\nabla(p_2)}}\nearrow & \downarrow^{\mathrlap{Ad(tra_\nabla)(p_2)(b_1)}}
    \\
    && P_y && P_z
    \\
    & {}^{\mathclap{tra_\nabla(p_1)}}\nearrow & \downarrow^{b_1}
    & {}^{\mathclap{tra_\nabla(p_2)}}\nearrow & \downarrow^{b_2}
    \\
    P_x
    &\stackrel{f_1}{\to}&
    P_y
    &\stackrel{f_2}{\to}&
    P_z
  }
  \,.
$$

We see that this is precisely the composition rule satisfied by the group elements labeled $b_i$ in the above description of the homotopy pullback:


$$
  \array{
    &&& \bullet
    \\
    & \swarrow &\swArrow_{b_1}& \downarrow &\swArrow_{b_2}
    & & \searrow
    \\
    \bullet 
     &&\stackrel{Ad(tra(p_1))}{\to}&
    \bullet
     &\stackrel{Ad(tra(p_2))}{\to}&&
  }
  \;\;\;
  =
  \;\;\;
  \array{
    && \bullet
    \\
    & \swarrow &\swArrow_{b_2 Ad(tra_\nabla(p_2)(b_1))}& \searrow
    \\
    \bullet &&\stackrel{Ad(tra_\nabla(p_2 \cdot p_1 ))}{\to}&&
  }
$$

(with labels in terms of the [L B-convention]([strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules))).

If $p_1 \cdot p_2 $ and $p_3$ are two homotopica but different paths from $x$ to $y$, then the parallel transport between them differs by the integrated curvature 

$$
  \array{
    && y
    \\
    & {}^{\mathllap{p_1}}\nearrow &\Downarrow^{\Sigma}
    & \searrow^{\mathrlap{p_2}}
    \\
    x &&\stackrel{p_3}{\to}&& z
  }
  \;\;\;
  \mapsto
  \;\;\;
  \array{
    && \bullet
    \\
    & {}^{\mathllap{Ad(tra(p_1))}}\nearrow 
    &\Downarrow^{tra(\partial \Sigma)}
    & \searrow^{\mathrlap{Ad(tra(p_2))}}
    \\
    \bullet &&\stackrel{Ad(tra(p_3))}{\to}&& \bullet
  }
  \,.
$$

The same morphism $f : P_x \to P_z$ corresponds to two different group elements $b_{1 2}$ and $b_3$ depending on whether it is expressed with respect to the path $p_1 \cdot p_2$ or $p_3$. The difference is precisely the integrated curvature $tra(\partial\Sigma)$

$$
  \array{
    && \bullet
    \\
    & {}^{\mathllap{tra(p_1 \cdot p_2)}}
    \nearrow & \downarrow^{\mathrlap{b_{1 2}}}
    \\
    \bullet &\stackrel{f}{\to}& \bullet
    \\
    & {}_{\mathllap{tra(p_3)}}\searrow 
    & \uparrow^{\mathrlap{b_3}}
    \\
    && \bullet
  }
$$

i.e. 

$$
  b_3 = tra(\partial \Sigma) b_{1 2}
  \,.
$$

This is precisely the relation imposed by the 2-cells in the homotopy pullback, as read off from the above diagrams.

In summary, this shows that in the homotopy pullback 

* if we forget the labels $\alpha, \beta, \cdots \in Aut(K)$ on the diagonal morphism, the resulting groupoid is the Atiyah groupoid over $\Pi(X)$;

* the action of this on the labels, taken into account, is the action of the Atiyah Lie groupoid on $P \times_g Aut(G)$.

=--







[[!redirects Atiyah Lie-groupoid]]
