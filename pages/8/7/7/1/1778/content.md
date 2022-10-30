
&#268;ech cohomology is less a special kind of [[cohomology]] than a special algorithm (see [[Čech methods]]) for _computing_ cohomology classes.


On the other hand, while the algorithm always produces results that look like cohomology classes, these actually are the abstractly defined cohomology classes only under certain assumptions. Historically &#268;ech cohomology has often been understood as being defined as whatever that algorithm computes, and theorems would be proven that determine under which conditions such "&#268;ech cohomology" coincides with cohomology defined by other means, where "by other means" traditionally is: "in terms of right derived functor definition of [[abelian sheaf cohomology]]".

From the discussion at [[abelian sheaf cohomology]] we know that the right derived functor definition computes the hom-set in the [[homotopy category of an (infinity,1)-category|homotopy category]] of an [[(infinity,1)-topos]] $\mathbf{H}$ that may alternatively be computed as a colimit over resolutions of the domain object

$$
  H(X,A)
  := 
  \pi_0 \mathbf{H}(X,A)
  = colim_{Y \stackrel{\in W \cap F}{\to} X} 
  C_H(Y,A)/_{homotopy}
$$

where the colimit is over all acyclic fibrations $Y \stackrel{\in W \cap }{\to} X$ in an appropriate [[model category]] $C_H$ that [[presentable (infinity,1)-category|presents]] $\mathbf{H}$. For $\mathbf{H}$ an [[infinity-stack]] [[(infinity,1)-topos]] this $C_H$ is a [[model structure on simplicial presheaves]] and the acyclic fibrations $Y \stackrel{\in W \cap F}{\to} X$ for $X$ an ordinary space are the [[hypercover]]s.

Now, for some coefficient objects $A$ it is sufficient to take the colimit here not over all [[hypercover]]s, but just over [[Cech cover|Čech cover]]s. The resulting formula

$$
  H(X,A)
  = colim_{Y \stackrel{Cech cover}{\to} X} 
  C_H(Y,A)/_{homotopy}
$$

is then called the formula for **&#268;ech cohomology** on $X$ with values in $A$.

Here a [[Cech cover|Čech cover]] is a simplicial presheaf that arises from an ordinary covering map $U \to X$ of $X$ by another space $U$ as the corresponding [[Čech nerve]] simplicial presheaf

$$
 \begin{aligned}
  Y := \left( 
    \cdots
    U \times_X U \times_X U
    \stackrel{\to}{\stackrel{\to}{\to}}
    U \times_X U \stackrel{\to}{\to} U 
  \right)
  \simeq
  hocolim_{[k] \in \Delta} U^{\times_X k}
 \end{aligned}
  \,.
$$

See [[descent for simplicial presheaves]] for more on the manipulations involved here.

To amplify, a general [[hypercover]] would start in degree 0 with a $U$ as above, but then in the next degree would have a cover $V \to U \times_X U$ of the fiber product, and so on, each fiber product in turn being covered by another space.

If $Y$ is not simply a [[Cech cover|Čech cover]] but also not the most general [[hypercover]] in that this iterative choice of further covering stops in degree $n$, then one also speaks of **&#268;ech cover of level $n$** and of the corresponding cohomology formula as **higher &#268;ech cohomology**. See for instance the reference by Tibor Beke below.



# Nonabelian Cech cohomology #

We start with describing the general " _nonabelian_ " &#268;ech cohomology (compare the terminology and remarks at [[nonabelian cohomology]]), i.e. the plain unwrapping of the above definition, before assuming that our coefficient object is [[abelian sheaf cohomology|abelian]] and before applying the [[Moore complex]] functor that sends the following simplicial computation to the maybe more familiar one in [[chain complex]]es.

The reasoning parallels that described at [[descent]] to some extent, but is maybe still worthwhile repeating here.

So let $C$ be some [[site]] and let $SSh(C)$ the category of [[simplicial presheaf|simplicial (pre)sheaves]] on $C$. Let $C(U)$ be the &#268;ech nerve for a cover $\pi : U \to X$ of some simplicial presheaf $X$ and let $A$ be any other simplicial presheaf that serves as the coefficient object.

Using [[end]] and [[coend]] notation we compute the required hom

$$
 \begin{aligned}
    SSh(C(U), A)
    &
    \simeq
    SSh( \int^{[k] \in Delta} \Delta^k \cdot C(U)_k, A )
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSh(\Delta^k \cdot C(U)_k, A )   
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSet(\Delta^k , SSh(C(U)_k,A) )   
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSet(\Delta^k , A(U \times_X \cdots \times_X U) )   
 \end{aligned}
  \,.
$$

An object in this last expression -- an $A$-valued cocycle on $X$ relative to $U$ -- is a diagram in [[SSet]] of the form

$$
  \array{
    \vdots && \vdots
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^2
    &\stackrel{f}{\to}&
    A(U \times_X U \times_X U)
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^1
    &\stackrel{g}{\to}&
    A(U \times_X U)
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^0
    &\stackrel{a}{\to}&
    A(U)
  }
  \,.
$$

This picks

* an object $a \in A(U)$

* a morphism $g : \pi_1 ^* a \to \pi_2^* a in A(U \times_X U)$

* a 2-morphism 
  $$ 
    \array{
      && \pi_{2}^* a
      \\
      & {}^{\pi_{12}^* g}\nearrow &\Downarrow^{f}& \searrow^{\pi_{23}^* g}
      \\
      \pi_{1}^* a
      &&\stackrel{\pi_{13}^* g}{\to}&&
      \pi_3^* a
    }
  $$
  in $A(U \times_X U \times_X U)$

* etc.

If we follow tradition and write 

* $U = \sqcup_i U_i$;

* and $U \times_X U = \sqcup_{i j} U_{i j} := \sqcup_{i j} U_i \cap U_j$

* etc

this is

* an collection of objects $(a_i \in A(U_i))$

* a collection of morphisms 
  $(g_{i j} : a_i|_{U_{ij}} \to a_{j}|_{U_{i j}} 
  in A(U_{i j}))$

* a collection of 2-morphisms 
  $$ 
   \left(
    \array{
      && a_{j}|_{U_{i j k}}
      \\
      & {}^{g_{ij}|_{U_{i j k}}}\nearrow 
      &\Downarrow^{f_{i j k}}& 
       \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}}      
       &&\stackrel{g_{i k}|_{U_{i j k}}}{\to}&&
      a_k|_{U_{i j k}}
    }
   \right)
  $$
  in $A(U_{i j k})$

* etc.

This is a **&#268;ech-cocycle** on $X$ with values in $A$ relative to $U$.

A **transformation/homotopy/coboundary** between two such cocycles is a cylinder over these diagrams, i.e. 

* a collection of morphism
  $ h_i : a_i  \to a'_i  in A(U_i)$;

* a collection of 2-morphism
  $$
    \array{
      a_i|_{U_{i j}} 
       &\stackrel{g_{i j}}{\to}&
      a_j|_{U_{i j}}
      \\
      \;\;\;\downarrow^{h_i|_{U_{i j}}} 
      &\Downarrow^{a_{i j}}& 
      \;\;\;\downarrow^{h_j|_{U_{i j}}}
      \\
      a'_i|_{U_{i j}} 
       &\stackrel{g_{i j}}{\to}&
      a'_j|_{U_{i j}}      
    }
  $$
  on $U_{i j}$

* a collection of 3-morphisms
  $$
    \array{
      && a_j|_{U_{i j k}}
      \\
      & {}^{g_{ij}|_{U_{i j k}}}\nearrow
      &\Downarrow^{f_{i j k}}& 
      \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}} 
       &&\stackrel{g_{i k}}{\to}&&
      a_k|_{U_{i j k}}
      \\
      \;\;\;\downarrow^{h_i|_{U_{i j}}} 
      &&\Downarrow^{a_{i k}}&& 
      \;\;\;\downarrow^{h_j|_{U_{i j}}}
      \\
      a'_i|_{U_{i j k}} 
       &&\stackrel{g_{i k}}{\to}&&
      a'_k|_{U_{i j k}}      
    }
    \;\;
    \;\;
    \;\;
    \;\;
    \;\;
    \stackrel{\rho_{i j k}}{\Rightarrow}
    \;\;
    \;\;
    \;\;
    \;\;
    \;\;
    \array{
      && a_j|_{U_{i j k}}
      \\
      & 
      {}^{g_{ij}|_{U_{i j k}}}\nearrow
      &\Downarrow^{a_{i j}\cdot a_{j k}|_{U_{i j k}}}& 
      \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}} 
       && a'_j|_{U_{i j k}} &&
      a_k|_{U_{i j k}}    
      \\
      \downarrow^{h_{i}|_{U_{i j k}}}
      &
        {}^{g'_{i j}|_{U_{i j k}}}\nearrow 
      &
       \Downarrow^{f'_{ijk}}
      &
        \searrow^{g'_{j k}|_{U_{i j k}}} 
      &
      \downarrow^{h_{k}|_{U_{i j k}}} 
      \\
      a'_i|_{U_{i j k}}
      &&\stackrel{g'_{i k}|_{U_{i j k}}}{\to}&&
      a'_k|_{U_{i j k}}
    }
  $$

We now plug in some concrete coefficient object 
$n$-types for low $n$ and reproduce some concrete formulas
from this.

## Nonabelian 1-cocycles: principal bundles ##

For $G$ a [[group]] let 
$\mathbf{B} G$ by abuse of notation denote 

* first of all the corresponding
[[delooping|delooped]] [[groupoid]], 

* then the corresponding [[nerve]] 

* then finally the corresponding simplicial sheaf that for each object $U$ assigns the [[nerve]] for the group $Hom(U,G)$:

  $$
    \mathbf{B}G : U \mapsto
    \left\{
      \array{
        \mathbf{B}G(U)_0 = Hom(U,{*}) = {*}
        \\
        \mathbf{B}G(U)_1 = Hom(U,G)
        \\
        \mathbf{B}G(U)_2 = Hom(U,G)\times Hom(U,G)
        \\
        \vdots
      }     
    \right.
  $$

The above then says that 

* a $\mathbf{B}G$-&#268;ech cocycle is

  * a collection of $G$-valued functions 

     $$
       (g_{ij} \in Hom(U_{i j}, G))
     $$
  
  * a collection of identities between $G$-valued functions

    $$
      g_{ij}|_{U_{i j k }} 
       \cdot
      g_{j k}|_{U_{i j k }}
      =
      g_{i k}|_{U_{i j k }}
    $$

* a $\mathbf{B}G$-&#268;ech coboundary is
  
  * a collection of $G$-valued functions

    $$
      (h_i \in Hom(U_i , G))
    $$

  * a collection of identites between $G$-valued functions

    $$
      g_{ij} \cdot h_j|_{U_{i j}}
      = 
      h_i|_{U_{i j}} \cdot g'_{j k}
      \,.
    $$

Remembering that the &#268;ech cohomology is the colimit over refinement of covers over cohomology classes defined this way, one sees the standard

+-- {: .un_theorem }
###### Theorem

&#268;ech cohomology with coefficients in $\mathbf{B}G$
(as above) classies $G$-[[principal bundle]]s

$$
  colim_{U \stackrel{Cech cover}{\to} X}
  SSh(C(U), \mathbf{B}G)/_{homtopy}
  \simeq
  G Bund(X)/_\sim
$$

=--


## Nonabelian 2-cocycles: gerbes and principal 2-bundles ##


In one degree higher the general [[homotopy n-type|homotopy 2-type]] coefficient object is modeled using a strict [[2-group]] $H$ coming from a [[crossed module]]
$G_2 \stackrel{\delta}{\to} G_1$.

The [[nerve]] of the corresponding [[delooping|delooped]]
[[2-groupoid]], regarded immediately as a simplicial sheaf starts out like

$$
  \mathbf{B}(G_2 \to G_1)
  :
  U 
  \mapsto
  \left\{
    \array{
       \mathbf{B}(G_2 \to G_1)(U)_{0}
       = 
       Hom(U, G_1)
       \\
       \mathbf{B}(G_2 \to G_1)(U)_{1}
       = 
       Hom(U, G_1) \times Hom(U, G_1)
       \times Hom(U, G_2)
       \\
       \vdots
    }
  \right.
  \,.
$$

One finds that a &#268;ech-cocycle now is
(see also the diagrams at [[group cohomology]] for this)

* a collection of functions 

  $$
    (g_{i j} \in Hom(U_{i j}, G_1))
  $$

* a collection of functions
  
  $$
    (f_{i j k }\in Hom(U_{i j k}, G_2) )
  $$

* a collection of identities  

  $$
    \delta(f_{i j k}|_{U_{i j k}})
    g_{i j}|_{U_{i j k}}
    g_{j k}|_{U_{i j k}}
    =
    g_{i k}|_{U_{i j k}}  
  $$

* and a collection of identities

  $$
    f_{i k l}|_{U_{i j k l}}
    \cdot
    f_{i j k}|_{U_{i j k l}}
    =
    \alpha(g_{i j}|_{U_{i j k l}})(f_{j k l})
    \cdot
    f_{i j k}|_{U_{i j k l}}
  $$

This is a **nonabelian &#268;ech 2-cocycle**.

Reading off the formulas for the coboundaries is
left as an excercise for the reader.

For the specical case the 

$$
  (G_2 \to G_1) = (G \to Aut(G))
$$

this is the nonabelian cohomology classifying
[[gerbe]]s.


# Abelian Cech cohomology #

In much of the literature _Cech cohomology_ denotes exclusively the abelian case, which we now describe.

In the special case that the coefficient [[simplicial presheaf]] $A$ is in the image of the [[nerve]] operation 

$$
  N : Ch_+ \to sAb \to SSet
$$

on [[chain complex]]es with values in [[simplicial set]]s that happen to be abelian [[simplicial group]]s, the computation of Cech cocycles may be entirely pulled back to the world of [[homological algebra]] by making use of the [[Dold-Kan correspondence]] that provides an [[adjoint equivalence]] between simplicial sets with values in abelian groups and non-negatively graded chain complexes.

**Remark** The following derivation of abelian Cech cohomology from nonabelian Cech cohomology restricted to nerves of chain complexes needs of the [[Dold-Kan correspondence]] only that it is an [[adjunction]], not that it is an [[adjoint equivalence]]. 

The following structure arises, 
when one computes Cech cohomology in this context,
as shown below.

+-- {: .un_defn}
###### Cech complex

Let $\{U_i \to X\}$ be a collection of open subsets
of $X$
and let $A_\bullet$ be a sheaf with coefficients
in non-negatively graded chain complexes $Ch_+$.

Then define the **Cech chain complex** $C(U,A_\bullet)$ 
of $A_\bullet$ relative to $U$ by

$$
  C(U,A_\bullet)_k :=
  \oplus_{k = l-n}
  \prod_{i_0, i_1, \cdots, i_n}
  A_l(U_{i_1, \cdots, i_n})
$$

where $U_{i_1, \cdots, i_n} = U_{i_0} \cap \cdots \cap U_{i_n}$ if all indices are pairwise different, and empty otherwise, and
with differential given by

$$
  (d a)_{i_0, \cdots, i_n} = 
  d_A a_{i_0, \cdots, i_n}
  \pm 
  \sum_{0 \leq j \leq n} (-1)^{j}
  a_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_n} 
  |_{U_{i_0, \cdots, i_n}}
$$

where on the right we sum over all components of $a$ obtained by discarding one of the original $(n+1)$ subscripts.

=--

+-- {: .un_prop }
###### Proposition (abelian Cech cohomology)

Let $A_\bullet$ be a sheaf with values in $Ch_+$
and write $N(A_\bullet)$ for the corresponding
simplicial sheaf under the [[nerve]] operation
of the [[Dold-Kan correspondence]].

Then the general (nonabelian) Cech cohomology
of $N(A_\bullet)$ as defined above coincides
with the cohomology of the Cech complex of
$A_\bullet$:

$$
  H(X, N(A_\bullet))
  \simeq
  colim_U H_0(C(U,A_\bullet))
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying idea is to use the 
adjunction of the [[Dold-Kan correspondence]]
to move the nerve operation $N(A_\bullet)$ 
on the right to the
free abelian chain complex operation 
$C_bullet(F(C(U)))$
on the 
[[Cech cover]] simplicial sheaf $C(U)$ and then 
use the [[Yoneda lemma]] to evaluate $A_\bullet$
on $N_\bullet(F(C(U)))$. The result is the 
Cech complex of $A_\bullet$. 
Cocycles and homotopies/coboundaries
are in bijection on both sides.

Spelled out in full detail this looks a bit more lengthy,
but is nothing but this simple idea.

Before starting the computation notice the following
observation on the image of the [[Cech cover]]
$C(U)$ under the [[Dold-Kan correspondence]]:

For $Y = C(U)$ a [[Cech cover]] on a sieve 
$\{U_i \to X\}_{i \in I}$, and for $W$ any test object,
the non-degenerate $n$-simplices in $C(U)(W)$ are the

$$
  U_{i_0, i_1, \cdots, i_n}(W)
$$ 

with all indices pairwise different, $i_k \neq i_l$. 

Accordingly the free abelian simplicial group-valued
sheaf $F(C(U))$ is for each $W$ and $n$ the 
free abelian group generated from these 
$U_{i_0, i_1, \cdots, i_n}(W)$ with pairwise distinct elements, i.e. that given by
formal interger combinations of these element.

In turn, the normalized [[Moore complex]] sheaf

$$
  N_\bullet(F(C(U))) 
$$

assigns to a test domain $W$ the complex that in
each degree is the free abelian group on these 
elements.



With this in hand,
we compute the set of $N(A_\bullet)$-valued cocycles on $U$ as follows:

$$
  \begin{aligned}
    Hom_{SPSh}(C(U), N(A_\bullet))
    &\simeq
    \int_W Hom_{SSet}( C(U)(W) , N(A_\bullet)(W) )
    \\
    & \simeq
    \int_W Hom_{SSet}( C(U)(W) , N(A(W)_\bullet) )    
    \\
    & \simeq
    \int_W Hom_{SAb}( F(C(U)(W)) , N(A(W)_\bullet) )    
    \\
    & \simeq
    \int_W Hom_{Ch_+}( N_\bullet(F(C(U)(W))) ,
         A(W)_\bullet )    
    \\
    & \simeq
    \int_W \int_{n}  
       Hom_{Ab}( N_n(F(C(U)(W)), A(W)_n ) 
    \\
    & \simeq
       \int_{n}
       \int_W   
       Hom_{Ab}( N_n(F(C(U)(W)), A(W)_n )  
    \\
    & \simeq
       \int_{n}
       \int_W  
       Hom_{Set}( \coprod_{i_0, i_1, \cdots, i_k} 
       U_{i_0,i_1, \dots, i_n}(W) , A(W)_n )  )
    \\
    & \simeq
    \int_{n}
       \prod_{i_0, i_1, \cdots, i_n} 
       A(U_{i_0,i_1, \dots, i_n})_l  
     )
    & =
    ker d_{C(U, A_\bullet)} \subset C(U,A_\bullet)_0
  \end{aligned}
  \,.
$$

Here

* The first step is the definition of morphism of [[presheaf|presheaves]] using the [[end]] notation;

* the second step is the definition of the [[nerve]] of of [[chain complex]]es applied to chain complex valued sheaves;

* the third step uses that the free simplicial abelian group functor is [[left adjoint]] to the forgetful one that remembers the underlying simplicial set;

* the fourth step then uses the [[Dold-Kan correspondence]], or actually just that the normalized [[Moore complex]] functor is [[left adjoint]] to the [[nerve]] of [[chain complex]]es;

* the fifth step expresses the set of morphisms of [[chain complex]]es as an [[end]] (being itself a [[natural transformation]]);

* the sixth step uses the [[Fubini theorem]] of [[enriched category theory]] to commute the two [[end]]s

* the seventh step uses that the chain complex in the left argument is generated freely on elements of a set to rewrite the hom of abelian groups into one of sets;

* this finally allows to apply the [[Yoneda lemma]] in step eight

* and in step nine one notices that the result thus obtained is the set of 0-cycles in the Cech complex $C(U,A_\bullet)$.

An entirely analogous argument shows that dividing out homotopies is respected. To see that one just needs to observe that the normalized [[Moore complex]] of the 1-[[simplex]] serves as an [[interval object]] in chain complexes.

...

=--


#References#

* Tibor Beke, _Higher &#268;ech theory_ ([journal](http://www.math.uiuc.edu/K-theory/0646/), [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))


[[!redirects Čech cohomology]]