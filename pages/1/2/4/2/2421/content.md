
<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>


#Contents#

* automatic toc goes here
{:toc}


#Super Lie groups#

##Definition##


A _super Lie group_ is a [[group object]] in the [[category]] [[SDiff]] of [[supermanifold]]s, that is a super [[Lie group]].

### in terms of generalized group elements ###

One useful way to characterize [[group object]]s $G$ in the
[[category]] $SDiff$ of [[supermanifold]] is by first sending 
$G$ with the [[Yoneda embedding]] to a [[presheaf]] on $SDiff$
and then imposing a lift of $Y(G) : SDiff^{op} \to Set$
through the [[forgetful functor]] [[Grp]] $\to$ [[Set]]
that sends a (ordinary) [[group]] to its underlying [[set]].

So a group object structure on $G$ is a diagram

$$
  \array{
    && Grp
    \\
    & {}^{(G,\cdot)}\nearrow & \downarrow
    \\
    SDiff^{op} &\stackrel{Y(G)}{\to}& Set
  }
  \,.
$$

This gives for each [[supermanifold]] $S$ an ordinary group 
$(G(S), \cdot)$, so in particular a product operation

$$
  \cdot_S : G(S) \times G(S) \to G(S)
  \,.
$$

Moreover, since morphisms in $Grp$ are group homomorphisms, it follows
that for every morphism $f : S \to T$ of [[supermanifold]]s we get a 
commuting diagram

$$
  \array{
    G(S) \times G(S) &\stackrel{\cdot_S}{\to}& G(S)
    \\
    \uparrow^{G(f)\times G(f)}  && \uparrow^{G(f)}
    \\
    G(T) \times G(T) &\stackrel{\cdot_T}{\to}& G(T)     
  } 
$$

Taken together this means that there is a morphism

$$
  Y(G \times G)  \to Y(G)
$$

of representable presheaves. By the [[Yoneda lemma]], this uniquely
comes from a morphism $\cdot : G \times G \to G$, which is the 
product of the group structure on the object $G$ that we are after.

etc.  


This way of thinking about supergroups is often explicit in 
some parts of the literature on supergeometry: some authors
define a supergroup or [[super Lie algebra]] as a
rule that assigns to every [[Grassmann algebra]] $A$ 
over an ordinmary [[vector space]] an ordinary [[group]]
$G(A)$
or [[Lie algebra]] and to a morphism of [[Grassmann algebra]]s
$A \to B$
_covariantly_ a morphism of groups $G(A) \to G(B)$. 
But the [[Grassmann algebra]] on an $n$-dimensional [[vector space]]
is naturally isomorphic to the function ring on the [[supermanifold]]
$\mathbb{R}^{0|n }$. So the definition of supergroups in terms of 
Grassmann algebras is secretly the same as the above definition
in terms of the [[Yoneda embedding]].




##Examples##


### the super-translation group ###

also called the **super-Heisenberg group**

The additive group structure on $\mathbb{R}^{1|1}$ is given on [[generalized element]]s in (i.e. in the logic internal to) the [[topos]] of [[sheaf|sheaves]] on the category [[SCartSp]] of [[cartesian space|cartesian]] superspaces by

$$
  \mathbb{R}^{1|1} \times \mathbb{R}^{1|1} \to 
  \mathbb{R}^{1|1}
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

Recall how the notation works here: by the [[Yoneda embedding]] we have a [[full and faithful functor]]

> [[SDiff]] $\hookrightarrow$ $Fun(SDiff^{op}, Set)$

and we also have the theorem, discussed at [[supermanifold]]s, that maps from some $S \in SDiff$ into $\mathbb{R}^{p|q}$ is given by a tuple of $p$ even section $t_i$ and $q$ odd sections $\theta_j$. The above notation specifies the map of supermanifolds by displaying what map of sets of maps from some test object $S$ it corresponds to under the [[Yoneda embedding]].

Now,  or each $S \in $ [[SDiff]] there is a [[group]] structure on the [[hom-set]] $SDiff(S, \mathbb{R}^{1|1}) \simeq C^\infty(S)^{ev} \times C^\infty(X)^{odd}$ given by precisely the above formula for this given $S$

$$
  \mathbb{R}^{1|1}(S) \times \mathbb{R}^{1|1}(S) \to 
  \mathbb{R}^{1|1}(S)
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

where $(t_i, \theta_i) \in C^\infty(S)^{ev} \times C^\infty(S)^{odd}$ etc and where the addition and product on the right takes place in the function [[super algebra]] $C^\infty(S)$.

Since the formula looks the same for all $S$, one often just writes it without mentioning $S$ as above.


### the super Euclidean group ###

The super-translaton group is the $(1|1)$-dimensional case of the [[super Euclidean group]].


### $GL(n|N)$ ###

...

### $OSp(2p|N)$ ###

...


[[!redirects super Lie group]]