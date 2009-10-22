<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* tic
{:toc}


#Idea#

[[model category|Model structures]] on [[simplicial presheaf|simplicial presheaves]] [[models for ∞-stack (∞,1)-toposes]] (precisely for the [[hypercompletion|hypercomplete]] [[∞-stack]] [[(∞,1)-topos]]es).

Recall that

* a [[model category]] is a way to [[presentable (infinity,1)-category|present]] an [[(∞,1)-category]];

* in the context of [[(∞,1)-categories]] [[presheaf|presheaves]] on an $(\infty,1)$-category $C$ are given by [[(∞,1)-functors]] $C^{op} \to$ [[SSet]].

This suggests that the [[(∞,1)-category of (∞,1)-sheaves]] on some [[site]] $C$ can be 
[[presentable (infinity,1)-category|presented]]
by a [[model category]] structure on the ordinary
[[functor category]] 

$$
  [C^{op},SSet] \simeq [\Delta^{op}, PSh(C)]
$$ 

-- the category of [[simplicial presheaf|simplicial presheaves]] .

Various interrelated flavors of model structures on the category of simplicial presheaves on $C$ have been introduced and studied since the 1970s, originally by K. Brown and A. Jocal and then developed in detail by Jardine.

Notice that when regarded as a presentation of an [[(∞,1)-sheaf]], i.e. of an [[∞-stack]], a simplicial presheaf -- being an ordinary functor instead of a [[pseudofunctor]] -- corresponds to a [[rectified ∞-stack]]. It might therefore seem that a model given by simplicial presheaves is too restrictive to capture the full expected flexibility of a notion of [[∞-stack]].
But this is not so. 

In 

* [[Jacob Lurie]], [[Higher Topos Theory]]

a fully general definition of a [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-category of ∞-stacks]] is given it is shown -- proposition 6.5.2.1 --
that, indeed, the Brown--Joyal--Jardine model is a [[presentable (infinity,1)-category|presentation]] of that.

More precisely

* the [[global model structure on simplicial presheaves]] on a category is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-presheaves]];

* the [[Cech model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]];

* the [[local model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the _hypercompletion_ of the [[(∞,1)-category of (∞,1)-sheaves]] (see the discussion at [[hypercover]]).

* the [[Bousfield localization]] of the global [[model category]] structure to the local one presents the corresponding [[localization of an (∞,1)-category]] from presheaves to sheaves, mimicking the corresponding statement for a [[category of sheaves]].

Originally K. Brown had considered in [[BrownAHT]] not a model structure on simplicial presheaves but

* a [[category of fibrant objects]] structure on locally Kan simplicial sheaves (see there for details)

and Joyal had originally considered a 

* [[local model structure on simplicial sheaves]].

Joyal's [[local model structure on simplicial sheaves]] is [[Quillen equivalence|Quillen equivalent]] to the injective [[local model structure on simplicial presheaves]]. 

By repackaging [[Kan complex]]es as [[simplicial groupoids]] one obtains a [[model structure on presheaves of simplicial groupoids]] which is also Quillen equivalent to the above.

If K. Brown's [[category of fibrant objects]] on locally Kan simplicial sheaves is restricted to globally Kan simplicial sheaves on a [[topos]] with [[point of a topos|enough point]] then it is the full subcategory on the fibrant objects in the projective [[local model structure on simplicial sheaves]].


But since in all cases the weak equivalences are the same (where they apply, for Brown's model if the topos has enough points), all these local [[homotopical category|homotopical categories]] define equivalent [[homotopy category|homotopy categories]].

By Lurie's result these are in each case in turn equivalent to the [[homotopy category of an (infinity,1)-category|homtopy category of]] the [[(∞,1)-topos]] of [[∞-stacks]]. So in particular they serve as a home for general [[cohomology]].


Various old results appear in a new light this way. For instance using the old result of [[BrownAHT]] on the way ordinary [[abelian sheaf cohomology]] is embedded in the [[homotopy theory]] of simplicial sheaves, one sees that the old right derived functor definition of [[abelian sheaf cohomology]] really computes the [[∞-stackification]] of a sheaf of [[chain complex]]es regarded under the [[Dold?Kan correspondence]] as a simplicial sheaf.


# the different model structures and their interrelation #

It is the very point of [[model category]] structures on a given [[homotopical category]] that there may be several of them: each [[presentable (infinity,1)-category|presenting]] the same [[(∞,1)-category]] but also each suited for different computational purposes.

So it is good that there are many model structures on simplicial (pre)sheaves, as there are. 

## injective/projective - local/global - presheaves/sheaves ##

The following diagram is a map for part of the territory:

$$
  \array{
     &&
       (\infty,1)Sh(C)
     &&&
       (\infty,1)PSh(C)
     &&&
       (\infty,1)Sh(C)
     \\
     && 
       \uparrow^{presentation}
     &&&
       \uparrow^{presentation}
     &&& 
       \uparrow^{presentation}
     \\
     SSh(C)^{l loc}_{inj} & 
     \stackrel{\stackrel{sheafification}{\leftarrow}}
       {\stackrel{embedding}{\to}}& 
     SPSh(C)^{l loc}_{inj} 
     &\stackrel{}{\leftarrow}|&
     SPSh(C)_{inj}
     &\stackrel{\stackrel{Id}{\leftarrow}}
       {\stackrel{Id}{\rightarrow}}&
     SPSh(C)_{proj}
     &\stackrel{}{\mapsto}&
     SPSh(C)_{proj}^{l loc}
     &
     \stackrel{\stackrel{sheafification}{\to}}
       {\stackrel{embedding}{\leftarrow}}& 
     SSh(C)_{proj}^{l loc}
     \\
     Joyal
     &\stackrel{Quillen equivalence}{\leftrightarrow}&
     Jardine
     &\stackrel{left Bousf. localization}{\leftarrow|}&
     Heller
     &\stackrel{Quillen equivalence}{\leftrightarrow}&
     Bousfield-Kan 
    &\stackrel{left Bousf. localization}{\mapsto}&
     Blander
     &\stackrel{Quillen equivalence}{\leftrightarrow}& 
     Brown-Gersten    
     \\
     \\
     &
     everything cofibrant;
     \\
     & fibrant = global injective fib...     
     \\
     \;\;\; 
     & ...satisfying descent
     &&&&&&&&
     cofibrant = global projective cofib;
     \\
     &&&&&&&&&
     fibrant = Kan valued and...    
     \\
     &&&&&&&&&
     \;\;\; 
     ...satisfying descent

  }
$$

Here 

* "inj" denotes the injective model structure: fibrations are objectwise fibrations

* "proj" denotes the projective model structure: fibrations are objectwise fibrations

* no "loc" subscript means global model structure: weak equivalences are the objectwise weak equivalences:

* "l loc" denotes **left** [[Bousfield localization]] at [[hypercovers]] (at [[stalk]]wise acyclic fibrations if the [[point of a topos|topos has enough points]])

The identity functor on the category $SPSh(C)$ of [[simplicial presheaves]] is a [[Quillen adjunction]] for the projective and injective [[global model structure on simplicial presheaves|global model structure]] and this is a [[Quillen equivalence]].

The [[local model structure on simplicial sheaves|local model structures on simplicial sheaves]] are just the restrictions of [[local model structure on simplicial presheaves|those on simplicial presheaves]]. 

These are related by a [[Quillen adjunction]] given by the usual [[geometric embedding]] of the [[category of sheaves]] as a full [[subcategory]] of that of presheaves -- with [[sheafification]] the [[left adjoint]] -- and this is also  [[Quillen equivalence]].

The characteristic of the _left_ Bousfield localizations is that for them the fibrant objects are those that satisfy
[[descent]]: see [[descent for simplicial presheaves]].

In either case 

* the global model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-presheaves]]

while

* the local model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-sheaves]] (i.e. [[∞-stacks]]).


The following diagram collection [[model category|model categories]] that are [[presentable (infinity,1)-category|presentations]] for the [[(∞,1)-category of (∞,1)-sheaves]]. All indicated morphism pairs are [[Quillen equivalences]].

$$
  \array{
     PSh(X, SGrpd)
     &\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&
     Sh(X,SGrpd)
     &\stackrel{}{\leftrightarrow}&
     Sh(X, SSet)^{l loc}_{inj}
     &\stackrel{\stackrel{sheafification}{\leftarrow}}
        {\stackrel{embedding}{\to}}&
     PSh(X, SSet)^{l loc}_{inj}
     &\stackrel{\stackrel{Id}{\leftarrow}}
        {\stackrel{Id}{\to}}&
     PSh(X, SSet)^{l loc}_{proj}
     &\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&
     Sh(X, SSet)^{l loc}_{proj}
     \\
     \\
     Luo-Bubenik-Tim
     &&
     Joyal-Tierney
     &&
     Joyal
     &&
     Jardine
     &&
     Blander
     &&
     Brown-Gersten     
  }
$$

On the right this lists the model structures on simplicial (pre)sheaves, here displayed as (pre)sheaves with values in [[simplicial sets]], using $SPSh(C) \simeq PSh(C,SSet)$.

On the left we have the Joyal--Tierney and Luo--Bubenik--Tim [[model structures on presheaves of simplicial groupoids]].

(...have to check here the relation $Sh(X,SGrpd)\leftrightarrow PSh(X, SGrpd)$)

## dependence on the underlying site ##


+-- {: .un_prop }
###### Proposition

Let $C,D$ be [[site]]s and let $f : C \to D$ be a [[functor]] that induces a 
morphism of [[site]]s in that $f_* : PSh(D) \to PSh(C)$ preserves [[sheaf|sheaves]]
and its [[left adjoint]] $f^* : PSh(C) \to PSh(D)$ (given by left [[Kan extension]])
is left [[exact functor]] in that it preserves finite [[limit]]s.

Then the induced [[adjunction]]
$$
  f_* : SPSh(D)_{inj}^{loc} \stackrel{\leftarrow}{\to} SPSh(C)_{inj}^{loc} : f^*
$$
is a [[Quillen adjunction]] for the local injective model structure on presheaves
on both sides.

=--

+-- {: .proof}
###### Proof

This is "little fact 5)" on page 10, 11 of

* Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

=--


### examples ###


+-- {: .un_prop }
###### Proposition


Let $C = $ [[CartSp]], $D = $ [[Diff]] and let $f : CartSp \hookrightarrow Diff$ be
the canonical inclusion of a [[subcategory]]. 

Then there is a [[Quillen equivalence]]

$$
  f_* : SPSh(Diff)_{inj}^{loc} \stackrel{\leftarrow}{\to}
      SPSh(CartSp)_{inj}^{loc} : f^*
  \,.
$$

=--

+-- {: .query}

[[Urs Schreiber]]: check this proof

=--

+-- {: .proof}
###### Proof


The functor

$$
  f_* : PSh(Diff) \to PSh(CartSp)
$$

that simply restricts a sheaf on the category of all [[manifold]]s to those on just cartesian spaces clearly respects the [[sheaf]] condition.

Its [[left adjoint]] is given by the left [[Kan extension]] formula

$$
  f^* A : (X \in Diff) \mapsto \lim_{\to}_{(X \to \mathbb{R}^n)} A(\mathbb{R}^n)
  \,.
$$

Since [[CartSp]] has [[terminal object]] also the [[comma category]] $(X/f)$ has a [[terminal object]] and is hence a [[filtered category]]. Therefore this is a [[filtered category|filtered colimit]] and therefore commutes with finite [[limit]]s. Since [[limit]]s of [[sheaf|sheaves]] are computed objectwise (see [[limits and colimits by example]]) it follows that $f^*$ preserves finite [[limit]]s.

So $f$ does induce a morphism of [[site]]s and thus satisfies the assumptions of the above theorem, which tells us that

$$
  f_* : SPSh(Diff)_{inj}^{loc} \stackrel{\leftarrow}{\to} SPSh(CartSp)_{inj}^{loc} : f^*
$$

is a [[Quillen adjunction]]. 

But we know more: as discussed in 

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

the [[Grothendieck topos]] $Sh(Diff)$ has [[point of a topos|enough topos points]], 

$$
  (p_n)_* : Set \stackrel{\leftarrow}{\to} Sh(Diff) : (p_n)^*
$$

one for each $n \in \mathbb{N}$, which are given by taking [[colimit]]s over the evaluation of simplicial presheaves on the [[poset]] of open $n$-disks $D(r) = \{x \in \mathbb{R}^n | |x| \lt r\}$ centered at the origin of $\mathbb{R}^n$

$$
  (p_n)^* A  = \lim_\to_{r \in \mathbb{R}} A(D(r))
  \,.
$$

Since the open $n$-disk is [[diffeomorphism|diffomorphic]] to $\mathbb{R}^n$, we may think of these [[stalk]]s actually as colimits over diagrams in [[CartSp]]. It follows that the functor $f_* : SPSh(Diff)_{inj}^{loc} \to SPSh(CartSp)_{inj}^{loc}$ preserves all weak equivalences.

By the same logic, for $A \in SPSh(Diff)$ and $B \in SPSh(CartSp)$ we find that if a morphism

$$
  f^* A \to B
$$

is a weak equivalence precisely if it is one on all the above disk-[[stalk]]s, which is the same condition that its [[adjunct]]

$$
  A \to f_* B
$$

is a weak equivalence, simply because testing on the [[point of a topos|topos points]] $p_n$ takes place entirly in [[CartSp]].

=--

+-- {: .un_remark}
###### Remark

This fact is noteworthy for the following reason: 

By the result of

* Daniel Dugger, Sharon Hollander, Daniel C. Isaksen, _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/)) 

which is described at [[descent for simplicial presheaves]],
the fibrant objects in $SPSh(C)^{loc}$ are those that satisfy [[descent]] along all [[hypercover]]s of [[representable functor|representables]]. But [[descent]] on the contractible $\mathbb{R}^n$s is a drastically simpler condition than on an arbitrary [[manifold]] $X$.

For instance, let $G$ be a [[Lie group]] and write $\mathbf{B}G$  for its corresponding degreewise representable simplicial presheaf $(\mathbf{B}G)_n = G^{\times n}$. 

Then regarded as an object of $SPSh(Diff)^{loc}$ the object $\mathbf{B}G$ of course does not satisfy descent. Instead, its fibrant replacement is (the recified version of) $G Bund$, the [[stack]] of $G$-[[principal bundle]]s.

But regarded as an object in $SPSh(CartSp)$ the object $\mathbf{B}G$ does satisfy descent, because every $G$-[[principal bundle]] on $\mathbb{R}^n$ is [[isomorphism|isomorphic]] to the trivial one, and the [[automorphism group]] of the trivial $G$-bundle is just $C(\mathbb{R}^n,G)$.

So there are considerably more fibrant objects in $SPSh(CartSp)^{loc}$ than there are in $SPSh(Diff)^{loc}$. Accordingly, there must be less cofibrant objects in $SPSh(CartSp)^{loc}$ to compensate this.

Indeed, notice that every [[representable functor|representable]] in any of the model structures on $SPSh(C)$ is cofibrant. So an arbitrary [[manifold]] $X$ is cofibrant in $SPSh(Diff)^{loc}$ and therefore there we have

$$
  Ho_{SPSh(Diff)^{loc}}(X, \mathbf{B}G )
  \simeq
  \pi_0 SPSh(X, G Bund)
  \simeq
  G Bund(X)_\sim
$$ 

as expected. In $SPSh(CartSp)$, however, $X$ is in general not representable, hence in general not cofibrant. But by the proposition below we have that the [[Cech nerve]] $C(U)$ of any good cover $U = \coprod_i U_i$ of $X$ is cofibrant. Hence here we find the above result by a different intermediate step

$$
  Ho_{SPSh(Cart)^{loc}}(X, \mathbf{B}G )
  \simeq
  \pi_0 SPSh(C(U), \mathbf{B}G)
  \simeq
  G Bund(X)_\sim
  \,.
$$

=--



# some properties and constructions #


## fibrant objects ##

The fibrant objects in the [[local model structure on simplicial presheaves]] are those that satisfy [[descent for simplicial presheaves]]. See there for more details.

## cofibrant objects ##

In the injective [[local model structure on simplicial presheaves]] all objects are cofibrant. For the projective local structure we can make at least the following statement


+-- {: .un_prop }
###### Proposition

In the _projective_ [[local model structure on simplicial presheaves|local model structure]] all objects that are degreewise [[coproduct]]s of [[representable functor|representable]]s are cofibrant.

=--

+-- {: .query}

[[Urs Schreiber]]: check this statement and proof
=--

+-- {: .proof}
###### Proof

Notice that cofibrant objects in $SPSh(C)_{proj}^{loc}$ are those objects such that maps out of them lift through all objectwise acyclic Kan fibrations.
In particular all [[representable functor|representable]]s are cofibrant in $SPSh(C)^{loc}_{proj}$.

Assume that $U$ is degreewise a coproduct of representables. Write $U_k = \coprod U_{i_0, \cdots, i_k}$. 

>(Notation is motivated from covers for the moment. )

We have

$$
  U \simeq \int^{[k] \in \Delta} \Delta^k \cdot U_k
$$

and this expression remains valid when we perform the coend only over injective maps in $\Delta$ and reading $U_k$ as the non-degenerate $k$-cells in $U$. This is what we shall mean by this notation in the following.


Then we have

$$
  \begin{aligned}
    SPSh(U,B)
    &=
    SPSh(\int^k \Delta^k \cdot U_k, B)
    \\
    &\simeq \int_k SPSh(\Delta^k\cdot U_k, B)
    \\
    &\simeq \int_k SSet(\Delta^k, SPSh(U_k, B))
    \\
    &\simeq \int_k SSet(\Delta^k, 
     SPSh(\coprod U_{i_0, \cdots U_{i_k}},
    B))
    \\
    &\simeq \int_k SSet(\Delta^k, 
    \prod SPSh(U_{i_0, \cdots U_{i_k}},
    B))
    \\
    &\simeq \int_k \prod_r SSet(\Delta^k, 
    SPSh(U_{i_0, \cdots U_{i_k}},
    B))
    \\
    &\simeq \int_k  \prod  SSet(\Delta^k, B(U_{i_0, \cdots U_{i_k}})
  \end{aligned}
  \,.
$$

We need to show that for any morphism $A \to B$ that is objectwise an acylic [[Kan fibration]] and for every morphism $U \to B$ there is a lift

$$
  \array{
    && A
    \\
    & \nearrow & \downarrow
    \\
    U &\to& B
  }
  \,.
$$

By the above this is the same as producing a section of the induced morphism

$$
  \int_k \prod  SSet(\Delta^k, A(U_{i_0, \cdots U_{i_k}})
  \to
  \int_k \prod  SSet(\Delta^k, B(U_{i_0, \cdots U_{i_k}})
$$

of simplicial sets, and this is componentwise an acyclic fibration.

Now construct a lift by induction over $k$. First for the 0-cells, we do have a lift

$$
  \array{
    && \prod A(U_i)
    \\
    & {}^{L_0}\nearrow & \downarrow
    \\
    \Delta^0 &\to & \prod B(U_i)
  }
$$

because $A \to B$ is objectwise an acyclic fibration. Accordingly, there is then a lift

$$
  \array{
    \Delta^0 \coprod \Delta^0
    &\stackrel{}{\to}& \prod A(U_{i j})
    \\
    \downarrow & \nearrow & \downarrow
    \\
    \Delta^1 &\to & \prod B(U_{i j})
  }
$$

and so on. At the $k$th induction step we produce a lift 

$$
  \array{
    \partial \Delta^k
    &\stackrel{}{\to}& \prod A(U_{i_0, \cdots, i_k})
    \\
    \downarrow & \nearrow & \downarrow
    \\
    \Delta^k &\to & \prod B(U_{i_0, \cdots, i_k})
  }
  \,,
$$

where the top horizontal morphism is just built from the restrictions of the previously obtained lifts to further intersections of the  $U_i$. 

The way these lifts are constructed they do satisfy the naturality condition that makes them objects of the required [[end]], so they do give the desired lift.

=--









#References#

A nicely helpful introduction and survey is provided in the notes

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://math.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

This in particular gives a detailed account on the relation and difference between the "Cech model structure" (section 3) which localizes (only) at Cech [[covers]], and the Jardine model structure (section 4), which localizes at all [[stalk]]wise weak equivalences ([[hypercovers]]). The latter is what in [[Higher Topos Theory|HTT]] is called the _hypercompletion_ .

The standard lecture notes are

* **Jardine07** J. Jardine, _Field Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

based on

* **Jardine01** J. Jardine, _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3 (2), 2001, pp.361--384

and ...

See also

* Benjamin Blander, _Local projective model structures on simplicial presheaves_,  K-Theory, Volume 24, Number 3, November 2001 , pp. 283--301(19) ([journal](http://www.ingentaconnect.com/content/klu/kthe/2001/00000024/00000003/00384649?crawler=true))

A detailed study of [[descent]] for simplicial presheaves is given in

* **DHI04** Daniel Dugger, Sharon Hollander, Daniel C. Isaksen, _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/)) 

* **DI02** D. Dugger, D. Isaksen, _Weak equivalences of simplicial presheaves_ ([arXiv](http://arxiv.org/abs/math/0205025))

A survey of many of the model structures together with a treatment of the left local projective one is in

* Benjamin Blander, _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

See also

* Daniel Isaksen, _Flasque model structure for simplicial presheaves_  ([web](http://www.math.uiuc.edu/K-theory/0679/), [pdf](http://www.math.uiuc.edu/K-theory/0679/flasque.pdf))

The characterization of the model category of simplicial presheaves as the canonical [[presentable (infinity,1)-category|presentation]] of the (hypercompletion of) the [[(∞,1)-category of (∞,1)-sheaves]] on a site is in

* [proposition 6.5.2.1](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=528) of 

  * [[Jacob Lurie]], [[Higher Topos Theory]]

Last not least, it is noteworthy that the idea of localizing simplicial sheaves at stalkwise weak equivalences is already described and applied in 

* Kenneth Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaff cohomology]],

using instead of a full [[model category]] structure the more lightweight one of a Brown [[category of fibrant objects]].

[[Note on Formatting|?]]