
+-- {: .standout}

This entry contains research material.

=--

+-- {: .query}

[[Urs Schreiber|Urs]]: while thinking about twists in twisted K-theory by [[gerbes]], about [[orientifold]] gerbes, and then further about [[string structure|String]]-gerbes twisted by Chern-Simons 2-gerbes etc. in an attempt to understand what's going on in the examples that govern [[schreiber: Background fields in twisted differential nonabelian cohomology|twisted differential nonabelian cohomology]] it turned out after a while that the following rather simple (I'd say: elegant) definition, simple as it may be, efficiently captures quite a few examples of what are called a "twists" of one sort or another in cohomological situations.

I used to dislike the undescriptive term "twist" and the way it is being used often to say nothing but "oh, and by the way, it so happens that we can modify the previous cohomological definition slightly by fiddling here, ah, and it turns out that modification defines another cohomology class". But given the following transparennt and systematic definition and in view of the examples that it does capture, I am currently inclined to go as far as saying _this is the_ definition of "twisted cohomology".

Last not least, it turned out that with this definition one can solve some puzzles in the definition of higher non-flat connection to obtain a cute definition that says literally that: a non-flat [[principal ∞-bundle]] with conneciton is a twisted _flat_ differential cocycle, with the twist being the curvature class. This sounds almost too plausible to be true, but by just turning the crank on this using the following definition, out drops an entire Chern-Weil theory for $\infty$-bundles. 

This are the kind of reasons that make me be fond of the following definition. But be critical and try to poke holes into it to see if it is watertight.

=--

#Definition#

Let $\mathbf{H}$ be some [[(∞,1)-topos]] and write $H = Ho_{\mathbf{H}}$ for its [[homotopy category of an (∞,1)-category]]. 

Recall from the discussion at [[cohomology]] that for $X$ and $A$ objects in $\mathbf{H}$ we say

* objects of the [[∞-groupoid]] $\mathbf{H}(X,A)$ are $A$-valued **cocycles** on $X$:

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

Since the $\infty$-groupoid valued hom in an [[(∞,1)-category]] is [[exact functor|exact]] with respect ot [[homotopy limits]], it follows that for every object $X$, there is  fibration sequence of cocycle [[∞-groupoids]]

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

* $\mathbf{H}$ an [[(∞,1)-topos]];

* $A \to \hat G \to G$ a [[fibration sequence]] in $\mathbf{H}$;

* $X\in \mathbf{H}$ an object of $\mathbf{H}$;

* and $c \in \mathbf{H}(X,G)$ a $G$-cocycle on $X$

the **$c$-twisted $A$-cohomology of $X$** is the the set of equivalence classes

$$
  H^c(X,A) := \pi_0 \mathbf{H}^c(X,A)
$$

of the [[∞-groupoid]] $\mathbf{H}^c(X,A)$ that is defined as the [[homotopy pullback]]

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

# Relation to other definitions #

For the special case that $G$ in the above is the [[delooping]] $\mathbf{B} G$ of an ordinary  [[group]] $G$, $A$ is a [[spectrum]] (an arbitrarily [[delooping|deloopable]] object, for the present purpose) and given an [[action]] of $G$ on $A$, there is an established definition of [[generalized (Eilenberg-Steenrod) cohomology]] with coefficients $A$ twisted by a $G$-[[principal bundle]].

Namely given the $G$-[[principal bundle]] $P \to X$ form the associated $A$-bundle $P \times_G A$. Then define a twisted $A$-cocycle on $X$ to be a [[section]] $X \to P \times_G A$ of this associated bundle.

This is the definition of twisted cohomology as it appears for instance essentially as definition 22.1.1 of

* May, Sigurdsson, _Parametrized homotopy theory_

(When comparing with their definition take their $G$ to be the trivial group and identify their $\Gamma$ and $\Pi$ with our $G$).

We now discuss how this is a special case of the above definition of twisted cohomology.

A pair consisting of a space $A$ acted on by a  group  $G$ can be equivalently thought of in terms of one single space: the homotopy quotient of $A$ by $G$, a concrete realization of which is the Borel construction $\mathbf{E}G \times_G A$. This is not a spectrum anymore, but is a space.

Once we place ourselves in a context where both $G$ and $A$ live, this is best thought of in terms of [[fibration sequences]]

So for instance the fact that some $G$ acts on some $A$ is witnessed by the existence of a left-long fibration sequence

$$
  \cdots \to A \to A//G \to \mathbf{B}G.
$$

If it should happen that the fibration sequence extends one step to the right,

$$
  \cdots \to A \to A//G \to \mathbf{B}G \to S,
$$

we can assume, from properties of fibration sequences that $S = \mathcal{B}A.$ 

In language used among nonabelian cohomologists, ss it said that we have

$\mathbf{B}G \to S$ is the [[action]]

in contrast to the classical

$G \times A \to A$ is the action.
 
Then $A//G =G \times A$ with this map and the projection to $A$  is the [[action groupoid]] .



So we look at the remaining fibration sequence, which sits by definition in a homotopy pullback square

$$
  \array{
     A &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     A//G &\to& \mathbf{B}G
  }
$$

The universal property of this homotopy pullback says precisely that:

- the obstruction to lifting a ("nonabelian" or "twisted") $A//G$-cocycle
  $X \to A//G$ to an $A$-cocycle $X \to A$ is its image in first $G$-cohomology under the above horizontal map. That's the twist.

Read the other way round it says:

$A$-cocycles are precisely those $G$-twisted $A$-cocycles whose twist vanishes.

More formally, but without adding any genuine new information, since cohomology is just connected components of the Hom in our context, we know that for any $X$ we have a fibration sequence

$$
  \array{
     \mathbf{H}(X,A) &\to& {*}
     \\
     \downarrow && \downarrow^{{*} \mapsto {*}}
     \\
     \mathbf{H}(X,A//G) &\to& \mathbf{H}(X,\mathbf{B}G)
  }
  \,.
$$

So if we fix the twist in $\mathbf{H}(X, \mathbf{B}G)$ (which you'd want to write as $H^1(X,G)$) to some $c \in \mathbf{H}(X, \mathbf{B}G)$ then the $c$-twisted $A$-cohomology is precisely that bit of $\mathbf{H}(X,A//G)$ that sits in the homotopy fiber over $c$.

Therefore we may say that the $c$-[[twisted cohomology]] is the homotopy pullback
$\mathbf{H}^c(X,A)$ in 

$$
  \array{
     \mathbf{H}^c(X,A) &\to& {*}
     \\
     \downarrow && \downarrow^{{*} \mapsto c}
     \\
     \mathbf{H}(X,A//G) &\to& \mathbf{H}(X,\mathbf{B}G)
  }
  \,.
$$

To see that this does indeed reproduce the description in terms of sections of associated bundles, 

look at the long fibration sequence one step down the row, where it reads

$$
  \array{
    A//G \simeq \mathbf{E}G\times_G A &\to& {*}
     \\
     \downarrow && \downarrow
     \\ 
     \mathbf{B}G  &\stackrel{\rho}{\to}& \mathbf{B}A
  }
$$

and exhibts $A//G$ as the bundle with fiber $A$ $\rho$-associated to the universal $G$-bundle.

For the given $G$-cocycle $X \to \mathbf{B}G$ the corresponding associated bundle with fiber $A$ over $X$ is the further homotopy pullback $P$ in

$$
  \array{
    P &\to&
    A//G \simeq \mathbf{E}G\times_G A &\to& {*}
     \\
     \downarrow &&
     \downarrow && \downarrow
     \\ 
     X &\to&
     \mathbf{B}G  &\stackrel{\rho}{\to}& \mathbf{B}A
  }
$$



And again it is precisely the universal property of the homotopy pullback that asserts that sections $X \to P$ of this bundle are in bijection, up to homotopy, with those maps $X \to A//G$ whose projection to $X \to \mathbf{B}G$ reproduces the prescribed twist.



We may summarize this by a 

**Principle**

* Higher [[nonabelian cohomology]] disguises as twisted higher abelian cohomology;

* conversely: twisted higher abelian cohomology is really nonabelian cohomology





# Examples #

Some somewhat trivial examples of this appear in various context. For instance [[group cohomology]] on a group with coefficients in a nontrivial module can be regarded as an example of twisted cohomology. See there for more details.


To get a feeling for how the definition does, it is instructive to see how for the fibration sequence being simply a central extension of ordinary groups, $\mathbf{B}\hat G \to \mathbf{B}G \stackrel{\omega}{\to} \mathbf{B}^2A$ a central extension of groups, classified by a [[group cohomology|group 2-cocycle]] $\omega$, $c$-twisted $\hat G$-cohomology produces precisely the familiar notion of [[twisted bundles]], with the twist being the lifting [[gerbe]] that obstructs the lift of a $G$-bundle to a $\hat $G$-bundle$.

This is also the first example in the following list
which is taken from the last section of

* [[schreiber: Background fields in twisted differential nonabelian cohomology]]

and contains examples that are of interest in the wider context of [[string theory]].



* fibration sequence: $\mathbf{B}U(n) \to \mathbf{B} PU(n) \to \mathbf{B}^2 U(1)$

  * twisting cocycle: lifting [[gerbe]] / [[magnetic charge]] / [[Kalb-Ramond field]];

  * twisted cocycle: [[twisted bundles]] / [[bundle gerbe modules]]

  * twisted Bianchi identity: $d F_\nabla = H_3$

  * occurence: Freed-Witten [[quantum anomaly|anomaly]] cancellation on [[brane|D-brane]]

  * with slight variation: [[twisted K-theory]]

* fibration sequence: $\mathbf{B}String(n) \to \mathbf{B} Spin(n) \stackrel{\frac{1}{2}p_1}{\to} \mathbf{B}^3 U(1)$

  * twisting cocycle: Chern-Simons 2-gerbe / [[supergravity C-field]];

  * twisted cocycle: twisted nonabelian [[string structure|String]]-gerbe with conection

  * twisted Bianchi identity: 
    $d H_3 \propto \langle F_\nabla \wedge F_\nabla \rangle$

  * occurence: [[Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]]

  * Proof. 
  
    * (with Danny Stevenson and Christoph Wockel: ([SSSS](http://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf))) use BCSS model ([BCSS](http://arxiv.org/abs/math/0504123)) of $String(n)$ with [Brylinski-McLaughlin construction](http://golem.ph.utexas.edu/category/2008/02/construction_of_cocycles_for_c.html) of $\frac{1}{2}p_1$ 

    * (using ([SaScSt I](http://arxiv.org/abs/0801.3480), [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf)):) compute local differential form data after differentiating smooth $\infty$-groupoids to  $L_\infty$-[[Lie infinity-algebroid|algebroids]] using the formalism of ([SaScSt I](http://arxiv.org/abs/0801.3480))

  * for aspects of the twisetd case see also

    * [AsJu](http://arxiv.org/abs/hep-th/0409200)

    * for aspects of the untwisted case see also ([Wa](http://arxiv.org/abs/0906.0117))

* fibration sequence: $\mathbf{B}Fivebrane(n) \to \mathbf{B} String(n) \stackrel{\frac{1}{6}p_2}{\to} \mathbf{B}^7 U(1)$

  * twisting cocycle: Chern-Simons 6-gerbe;

  * twisted cocycle: twisted nonabelian Fivebrane-gerbe with connection

  * occurence: dual [[Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]] for NS 5-brane magnetic dual to string

  * ([SaScSt II](http://arxiv.org/abs/0805.0564) [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf))
  

* fibration sequence: $\mathbf{B}^2 U(1) \to \mathbf{B} (U(1) \to \mathbb{Z}_2) \stackrel{}{\to} \mathbf{B} \mathbb{Z}_2$

  * twisting cocycle: $\mathbb{Z}_2$-orbifold;

  * twisted cocycle: [[orientifold|orientifold gerbe]] / Jandl gerbe with connection

  * occurence: unoriented string

  * unwrap the above abstract nonsense and use the above results to find [SchrSchwWal](http://arxiv.org/abs/hep-th/0512283) and the bosonic part of [DiFrMo](http://arxiv.org/abs/0906.0795)


# References #

For the special case of [[generalized (Eilenberg-Steenrod) cohomology]] twisted by a $G$-[[principal bundle]] see [section 22.1](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf#page=381) of

* May, Sigurdsson, _Parametrized homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

