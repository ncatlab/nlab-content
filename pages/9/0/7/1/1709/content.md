
+-- {: .standout}

This entry consists of research material.

=--

+-- {: .query}

[[Urs Schreiber|Urs]]: while thinking about twists in twisted K-theory by [[gerbe]]s, about [[orientifold]] gerbes, and then further about [[string structure|String]]-gerbes twisted by Chern-Simons 2-gerbes etc. in an attempt to understand what's going on in the examples that govern [[schreiber: Background fields in twisted differential nonabelian cohomology|twisted differential nonabelian cohomology]] it turned out after a while that the following rather simple (I'd say: elegant) definition, simple as it may be, efficiently captures quite a few examples of what are called a "twists" of one sort or another in cohomological situations.

I used to dislike the undescriptive term "twist" and the way it is being used often to say nothing but "oh, and by the way, it so happens that we can modify the previous cohomological definition slightly by fiddling here, ah, and it turns out that modification defines another cohomology class". But given the following transparennt and systematic definition and in view of the examples that it does capture, I am currently inclined to go as far as saying _this is the_ definition of "twisted cohomology".

Last not least, it turned out that with this definition one can solve some puzzles in the definition of higher non-flat connection to obtain a cute definition that says literally that: a non-flat [[principal infinity-bundle]] with conneciton is a twisted _flat_ differential cocycle, with the twist being the curvature class. This sounds almost too plausible to be true, but by just turning the crank on this using the following definition, out drops an entire Chern-Weil theory for $\infty$-bundles. 

This are the kind of reasons that make me be fond of the following definition. But be critical and try to poke holes into it to see if it is watertight.

=--

#Definition#

Let $\mathbf{H}$ be some [[(infinity,1)-topos]] and write $H = Ho_{\mathbf{H}}$ for its [[homotopy category of an (infinity,1)-category]]. 

Recall from the discussion at [[cohomology]] that for $X$ and $A$ objects in $\mathbf{H}$ we say

* objects of the [[infinity-groupoid]] $\mathbf{H}(X,A)$ are $A$-valued **cocycles** on $X$:

* morphisms in $\mathbf{H}(X,A)$ are **coboundaries** between these cocycles;

* equivalence classes in $\mathbf{H}(X,A)$ are [[cohomology]] classes,

* so that the [[homotopy category of an (infinity,1)-category|homotopy]] [[hom-set]]
  $$
    H(X,A) := \pi_0 \mathbf{H}(X,A)
  $$
  is the $A$-valued **cohomology** set of $X$. It is a group if $A$ is [[k-tuply groupal n-groupoid|groupal]].

Now consider the **obstruction problem** in cohomology:

let $A \to \hat G \to G$ be a [[fibration sequence]] in $\mathbf{H}$, i.e. a sequence such that the square

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \hat G &\to& G
  }
$$

is a [[homotopy pullback]] square, with ${*}$ denoting [[generalized the|the]] [[point]] ([[generalized the|the]] [[terminal object]]).

Since the $\infty$-groupoid valued hom in an [[(infinity,1)-category]] is [[exact functor|exact]] with respect ot [[homotopy limit]]s, it follows that for every object $X$, there is  fibration sequence of cocycle [[infinity-groupoid]]s

$$
  \array{
    \mathbf{H}(X,A) &\to& {*}
    \\
    \downarrow && \downarrow^{const_{*}}
    \\
    \mathbf{H}(X,\hat G) &\to& \mathbf{H}(X,G)
  }
  \,.
$$


This may be read as:

* the **obstruction** to lifting a $\hat G$-cocycle to an $A$-cocycle is its image in $G$-cohomology (all with respect to the given [[fibration sequence]])

But it also says:

* $A$-cocycles are, up to equivalence, precisely those $\hat G$-cocycles whose class in $G$-cohomology is the trivial class (given by the trivial cocycle $const_{*} : {*} \to G$).

This may motivate the following definition 

+-- {: .un_defn}
###### Definition (twisted cohomology)

For 

* $\mathbf{H}$ an [[(infinity,1)-topos]];

* $A \to \hat G \to G$ a [[fibration sequence]] in $\mathbf{H}$;

* $X\in \mathbf{H}$ an object of $\mathbf{H}$;

* and $c \in \mathbf{H}(X,G)$ a $G$-cocycle on $X$

the **$c$-twisted $A$-cohomology of $X$** is the the set of equivalence classes

$$
  H^c(X,A) := \pi_0 \mathbf{H}^c(X,A)
$$

of the [[infinity-groupoid]] $\mathbf{H}^c(X,A)$ that is defined as the [[homotopy pullback]]

$$
  \array{
    \mathbf{H}(X,A) &\to& {*}
    \\
    \downarrow && \downarrow^{c}
    \\
    \mathbf{H}(X,\hat G) &\to& \mathbf{H}(X,G)
  }
  \,.
$$

=--

**Remarks**

* Notice that compared to the previous [[fibration sequence]] arising in the obstruction problem, the [[homotopy limit]] in the above definition replaces the trivial cocycle $const_{*}$ by the prescribed $G$-cocycle $c$.

# Examples #

Some somewhat trivial examples of this appear in various context. For instance [[group cohomology]] on a group with coefficients in a nontrivial module can be regarded as an example of twisted cohomology. See there for more details.


To get a feeling for how the definition does, it is instructive to see how for the fibration sequence being simply a central extension of ordinary groups, $\mathbf{B}\hat G \to \mathbf{B}G \stackrel{\omega}{\to} \mathbf{B}^2A$ a central extension of groups, classified by a [[group cohomology|group 2-cocycle]] $\omega$, $c$-twisted $\hat G$-cohomology produces precisely the familiar notion of [[twisted bundle]]s, with the twist being the lifting [[gerbe]] that obstructs the lift of a $G$-bundle to a $\hat $G$-bundle$.

This is also the first example in the following list
which is taken from the last section of

* [[schreiber: Background fields in twisted differential nonabelian cohomology]]

and contains examples that are of interest in the wider context of [[string theory]].



* fibration sequence: $\mathbf{B}U(n) \to \mathbf{B} PU(n) \to \mathbf{B}^2 U(1)$

  * twisting cocycle: lifting gerbe;

  * twisted cocycle: twisted bundles / gerbe modules

  * twisted Bianchi identity: $d F_\nabla = H_3$

  * occurence: Freed-Witten anomaly cancellation on [[nLab:brane|D-brane]]

* fibration sequence: $\mathbf{B}String(n) \to \mathbf{B} Spin(n) \stackrel{\frac{1}{2}p_1}{\to} \mathbf{B}^3 U(1)$

  * twisting cocycle: Chern-Simons 2-gerbe;

  * twisted cocycle: twisted nonabelian String-gerbe with conection

  * twisted Bianchi identity: 
    $d H_3 \propto \langle F_\nabla \wedge F_\nabla \rangle$

  * occurence: [[nLab:Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]]

  * Proof. 
  
    * (with Danny Stevenson and Christoph Wockel: ([SSSS](http://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf))) use BCSS model ([BCSS](http://arxiv.org/abs/math/0504123)) of $String(n)$ with [Brylinski-McLaughlin construction](http://golem.ph.utexas.edu/category/2008/02/construction_of_cocycles_for_c.html) of $\frac{1}{2}p_1$ 

    * (using ([SaScSt I](http://arxiv.org/abs/0801.3480), [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf)):) compute local differential form data after differentiating smooth $\infty$-groupoids to  [[nLab:Lie infinity-algebroid|L-infinity algebroids]] using the formalism of ([SaScSt I](http://arxiv.org/abs/0801.3480))

  * for aspects of the twisetd case see also

    * [AsJu](http://arxiv.org/abs/hep-th/0409200)

    * for aspects of the untwisted case see also ([Wa](http://arxiv.org/abs/0906.0117))

* fibration sequence: $\mathbf{B}Fivebrane(n) \to \mathbf{B} String(n) \stackrel{\frac{1}{6}p_2}{\to} \mathbf{B}^7 U(1)$

  * twisting cocycle: Chern-Simons 6-gerbe;

  * twisted cocycle: twisted nonabelian Fivebrane-gerbe with connection

  * occurence: dual [[nLab:Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]] for NS 5-brane magnetic dual to string

  * ([SaScSt II](http://arxiv.org/abs/0805.0564) [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf))
  

* fibration sequence: $\mathbf{B}^2 U(1) \to \mathbf{B} (U(1) \to \mathbb{Z}_2) \stackrel{}{\to} \mathbf{B} \mathbb{Z}_2$

  * twisting cocycle: $\mathbb{Z}_2$-orbifold;

  * twisted cocycle: [[nLab:orientifold|orientifold gerbe]] / Jandl gerbe with connection

  * occurence: unoriented string

  * unwrap the above abstract nonsense and use the above results to find [SchrSchwWal](http://arxiv.org/abs/hep-th/0512283) and the bosonic part of [DiFrMo](http://arxiv.org/abs/0906.0795)




