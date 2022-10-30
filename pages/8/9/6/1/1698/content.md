
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

A _homotopy fiber sequence_ is a "long left-[[exact sequence]]" in an [[(∞,1)-category]]. (The dual concept is that of _[[cofiber sequence]]_.)

Traditionally fiber sequences have been considered in the context of [[homotopical category|homotopical categories]] such as [[model category|model categories]] and [[category of fibrant objects|Brown category of fibrant objects]] which [[presentable (infinity,1)-category|present]] the [[(∞,1)-category]] in question. In particular, classically this was considered for [[Top]] itself. In these cases they are obtained in terms of [[homotopy pullbacks]]. Since, as discussed there, the homotopy fiber of a morphism may be computed as the ordinary 1-categorical [[fiber]] of any [[fibration]] [[resolution]] of this morphism, one often also speaks of _fibration sequences_.



## Definition
 {#Definition}

### In $(\infty,1)$-category theory

Let $C$ be an [[(∞,1)-category]] with small [[limits]] and consider [[pointed objects]] of $C$, i.e. morphisms ${*} \to A$ from the [[terminal object]] ${*}$ ([[generalized the|the]] [[point]]) to some object $A$. All unlabeled morphisms from the point in the following are these chosen ones and all other morphisms are taken with respect to these points.

Notice that in the case that $C$ happens to be a [[stable (∞,1)-category]] for which ${*} = 0$ all objects are canonically pointed and the notions of left- and right-exact fibration sequences coincide.

But for the notion of fibration sequence to make sense, we do not need to assume that $C$ is a stable $(\infty,1)$-category. In particular, in the context of [[nonabelian cohomology]] (see [[gerbe]] and [[principal 2-bundle]]) one considers fibration sequences in non-stable $(\infty,1)$-categories.


Now let $f : A \to B$ be a morphism in $C$.

The **homotopy fiber** or **homotopy kernel** or **[[mapping cocone]]** of $f$ is [[generalized the|the]] [[pullback]] (which in our $(\infty,1)$-categorical context means [[homotopy limit|homotopy pullback]]) of the point along $f$:

$$
  \array{
     ker(f) &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     A &\stackrel{f}{\to}& B
  }
  \,.
$$

### In categories of fibrant objects

> under construction

In ([Quillen 67, section I.3](#Quillen67)) it was shown how the theory of fiber sequences and [[cofiber sequences]] arises in the abstract homotopy theory of [[model categories]]. Focusing on the fiber sequences, this perspective depends only on the [[category of fibrant objects]] inside the model category, and in fact makes sense generally in this context. This was spelled out in ([Brown 73, section 4](#Brown73)), which we review here. 


+-- {: .num_lemma #FiberOfFibrationIsCompatibleWithWeakEquivalences}
###### Lemma

In [[pointed objects]] $\mathcal{C}_f^{\ast/}$ of a [[category of fibrant objects]] $\mathcal{C}_f$, def. \ref{FullSubcategoriesOfFibrantCofibrantObjects}, consider a morphism of [[fiber]]-diagrams, hence a [[commuting diagram]] of the form

$$
  \array{
    fib(f_1) &\longrightarrow& X_1 &\underoverset{\in Fib}{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{}} && \downarrow && \downarrow
    \\
    fib(f_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{f_2}{\longrightarrow}& Y_2
  }
  \,.
$$

If the two vertical morphisms on the right are weak equivalences, then so is the vertical morphism in the left

=--

([[BrownAHT|Brown 73, section 4, lemma 3]])


+-- {: .proof}
###### Proof

Factor the diagram in question

$$
  \array{
    fib(f_1) &\longrightarrow& X_1 &\underoverset{\in Fib}{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{}} && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    fib(f_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{f_2}{\longrightarrow}& Y_2
  }
$$

through the pullback of the bottom horizontal line:

$$
  \array{
    fib(f_1) &\longrightarrow& X_1 &\underoverset{\in Fib}{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{id}}
    \\
    fib(\phi) &\longrightarrow& f^\ast X_2 &\underoverset{\in Fib}{\phi}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{\in W}} && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W}}    
    \\
    fib(f_2) &\longrightarrow& X_2 &\underoverset{\in Fib}{f_2}{\longrightarrow}& Y_2
  }
$$

Here $f^\ast X_2 \to X_2$ is a weak equivalence by lemma \ref{InCfPullbackAlongFibrationPreservesWeakEquivalences} and with this $X_1 \to f^\ast X_2$ is a weak equivalence by assumption and [[two-out-of-three]].

Moreover, this diagram exhibits $fib(f_1)\to fib(\phi)$ as the base change (along $\ast \to Y_2$) of $X_1 \to f^\ast X_2$. 

Hence it is now sufficient to observe that in category of fibrant objects, base change preserves weak equivalences (...).

=--

Hence we say:

+-- {: .num_defn #HomotopyFiber}
###### Definition

Let $\mathcal{C}$ be a [[model category]]. For $f \colon X \longrightarrow Y$ any morphism, then its **[[homotopy fiber]]**

$$
  hofib(f)\longrightarrow X
$$

is the morphism in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$, def. \ref{HomotopyCategoryOfAModelCategory}, which is represented by the [[fiber]], def. \ref{FiberAndCofiberInPointedObjects}, of any fibration resolution of $f$.

=--

We may now state the abstract version of the statement of prop. \ref{SerreFibrationGivesExactSequenceOfHomotopyGroups}:

+-- {: .num_prop #ExactSequenceOfHomotopyFiberAtOneStage}
###### Proposition

Let $\mathcal{C}$ be a [[model category]]. For $f \colon X \to Y$ any morphism of [[pointed objects]], and for $A$ a [[pointed object]], def. \ref{CategoryOfPointedObjects}, then the sequence

$$
  [A,hofib(f)]_\ast \overset{i_\ast}{\longrightarrow} [A,X]_\ast \overset{f_\ast}{\longrightarrow} [A,Y]_{\ast}
$$

is [[exact sequence|exact]] (the sequence being the image of the [[homotopy fiber]] sequence of def. \ref{HomotopyFiber} under the hom-functor of the pointed [[homotopy category of a model category]]

$$
  [A,-]_\ast \;\colon\; Ho(\mathcal{C}^{/\ast}) \longrightarrow Set^{\ast/}
  \,.
$$


=--

+-- {: .proof}
###### Proof

We may choose representatives such that $A$ is cofibrant, and $f$ is a fibration. Then we are faced with an ordinary pullback diagram

$$
  \array{
    hofib(f) &\overset{i}{\longrightarrow}& X
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    \ast &\longrightarrow& Y
  }
$$ 

and the hom-classes are represented by genuine morphisms in $\mathcal{C}$. From this it follows immediately that $ker(p_\ast)$ includes $im(i_\ast)$. Hence it remains to show that every element in $ker(p_\ast)$ indeed comes from $im(i_\ast)$.

But an element in $ker(p_\ast)$ is represented by a morphism $\alpha \colon A \to X$ such that there is a left homotopy as in the following diagram

$$
  \array{
     && A &\overset{\alpha}{\longrightarrow}& X
     \\
     && {}^{\mathllap{i_0}}\downarrow &{}^{\tilde \eta}\nearrow& \downarrow^{\mathrlap{p}}
     \\
     A &\overset{i_1}{\longrightarrow} & Cyl(A) &\overset{\eta}{\longrightarrow}& Y
     \\
     \downarrow && && \downarrow^{\mathrlap{=}}
     \\
     \ast && \longrightarrow && Y
  }
  \,.
$$

Now by lemma \ref{ComponentMapsOfCylinderAndPathSpaceInGoodSituation} the square here has a lift $\tilde \eta$, as shown. This means that $i_1 \circ\tilde \eta$ is left homotopic to $\alpha$. But by the universal property of the fiber, $i_1 \circ \tilde \eta$ factors through $i \colon hofib(f) \to X$.

=--



### In homotopy type theory

In [[homotopy type theory]] the homotopy fiber of a function term $f : A \to B$ over a function term $pt_B : * \to B$ is the type

$$
  \sum_{a : A} (f(a) = pt_B)
  \,,
$$

hence the [[dependent sum]] over $A$ of the [[identity type]] on $B$ with $f(a)$ and $pt_B$ [[substitution|substituted]]. (A special case of the discussion at [[homotopy pullback]])

For the corresponding [[Coq]] code  see

* [[Vladimir Voevodsky]], _[Foundations/Generalities/uuo.v](https://github.com/vladimirias/Foundations/blob/master/Generalities/uu0.v)_

See also at [[fiber type]]. 

## Long fibration sequences

A crucial difference between $\infty$-categorical fibration sequences
and ordinary 1-categorical sequences is that the former are always _long_ : in contrast to the ordinary kernel of a kernel, which is necessarily trivial, the homotopy kernel of a homotopy kernel is typically far from trivial, but is a [[loop space object]]. Due to that, each fibration sequence extend to the left by as many steps (times 3) as the objects involved have nontrivial [[homotopy group]]s.


### Kernel of a kernel: loop objects

In particular the homotopy fiber of the point ${*} \to B$ is the [[loop space object]] $\Omega B$ of $B$ (by definition):

$$
  \array{
     \Omega B &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     {*} &\stackrel{}{\to}& B
  }
  \,.
$$

Notice that the ordinary 1-categorical [[pullback]] of a point to itself is necessarily just the point again. Much of what makes [[(∞,1)-category]]-theory richer than ordinary category theory is this fact that the kernel of the point is not trivial, but loops. This implies in particular that **the kernel of the kernel is in general nontrivial**.

Namely the homotopy kernel of the morphism $ker(f) \to A$ constructed above is by definition the homotopy limit in the diagram

$$
  \array{
    ker(ker(f)) &\to& ker(f)
    \\
    \downarrow && \downarrow
    \\
    {*} &\to & A
  }
$$

This is the same kind of diagram as before, just depicted after taking its mirror image along a diagonal. The point of drawing it this way is that this suggests to form the pasting diagram with the one that defines $ker(f)$

$$
  \array{
    ker(ker(f)) &\to& ker(f) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& A &\stackrel{f}{\to}& B
  }
  \,.
$$


Since the $(\infty,1)$-categorical pullback [satisfies the pasting law](http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting) just as ordinary [[pullback]] diagrams do, it follows that the total outer square obtained this way is itself a [[homotopy pullback]]. But by definition of the [[loop space object]] $\Omega B$ this means that the kernel of the kernel is loops:

$$
  ker(ker(f)) \simeq \Omega B
  \,.
$$

I.e. all three squares in 

$$
  \array{
    \Omega B &\to& ker(f) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& A &\stackrel{f}{\to}& B
  }
$$

are (homotopy) pullback squares.

### Long fibration sequences
 {#ContinuingToLongFiberSequences}

Continuing this way to the left with the [[pasting law]], we obtain a long fiber sequence of morphisms to the left of the form

$$
  \cdots
    \to
  \Omega ker(f)
    \longrightarrow
  \Omega A 
    \stackrel{\Omega f}{\longrightarrow}
  \Omega B 
    \longrightarrow 
  ker(f) 
    \stackrel{g}{\longrightarrow}
  A 
    \stackrel{f}{\longrightarrow} B
  \,.
$$

A subtlety to be aware of here is that $\Omega B$ is not quite $ker(ker(f))$, but the latter instead is $\bar \Omega f$, where $\bar \Omega$ denotes loops with reversed orientation.

A classical discussion of this in terms of computing homotopy fibers via [[path object]] fibrant replacements is e.g. in
([Switzer 75, around 2.57](#Switzer75)). But let's see it just diagrammatically:

First observe that it is indeed $\Omega f$ and not $\bar \Omega f$ that appears in the above: by "bending around" the bottom left "$\ast \to $" we get

$$
  \array{
    \Omega A &\longrightarrow& \ast
    \\
    \downarrow^{\mathrlap{\Omega f}} && \downarrow
    \\
    \Omega B & \longrightarrow & ker(f) &\longrightarrow& \ast
    \\
    \downarrow && \downarrow^{\mathrlap{g}} && \downarrow
    \\
    \ast &\longrightarrow & A &\stackrel{f}{\longrightarrow}& B
  }
  \;\;\;\;\;
  \simeq  
  \;\;\;\;\;
  \left(
  \array{
    \ast &\longrightarrow& \ast
    \\
    \downarrow && \downarrow
    \\
    ker(f) &\longrightarrow& \ast
    \\
    \downarrow^{\mathrlap{g}} && \downarrow
    \\
    A &\stackrel{f}{\longrightarrow}& B
    \\
    \uparrow && \uparrow
    \\
    \ast &\longrightarrow& \ast
  }
  \right)
  \stackrel{\underset{\longleftarrow}{\lim}}{\mapsto}
  \left(
    \Omega A \stackrel{\Omega f}{\longrightarrow} \Omega B
  \right)
  \,.
$$

On the other hand, if we define the homotopy fiber of any morphism $\phi$ by the diagram

$$
  \array{
    ker(\phi) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    & \stackrel{\phi}{\longrightarrow} & 
  }
$$

then $ker(g)$ is given by the diagram

$$
  \array{
    ker(g) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    ker(f) &\stackrel{g}{\longrightarrow}& A
  }
$$

but what appears in the above pasting diagram is instead this diagram "reflected at the diagonal axis"

$$
  \array{
    ker(g) &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    ker(f) &\stackrel{g}{\longrightarrow}& A
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{
    \Omega B &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    ker(f) &\stackrel{g}{\longrightarrow}& A
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \left(
  \array{
    \Omega B &\longrightarrow& ker(f)
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& A
  }
  \right)^{-1}
$$

Here "$(-)^{-1}$" denotes the inverse of the [[2-morphism]] ([[homotopies]]). Since it is these 2-morphisms/homotopies that become the loops in the loop space, it is here that loop reversal appears in translating between the naive iterated homotopy fiber to the construction that actually appears in the above pasting composite.



 


### Long exact sequences in cohomology {#LongSequCoh}


Usually, when looking at fibration sequences in 1-categorical contexts of the [[homotopy category of an (∞,1)-category]], one doesn't see these long fibration squences directly, but only "in cohomology".

This can be usefully understood as follows:

recall from [[cohomology]] that for $X$ and $A$ objects in an [[(∞,1)-category]] $C$ that is an [[(∞,1)-topos]], the $\infty$-groupoid of $A$-valued cocycle on $X$ is just $Hom_C(X,A)$, so that the corresponding cohomology classes are

$$
  H(X,A) = \Pi_0 Hom_C(X,A) = Ho_C(X,A)
  \,,
$$

where $Ho_C$ is the corresponding [[homotopy category of an (∞,1)-category]].

The upshot being that in the right $(\infty,1)$-context cohomology is just the [[hom-object]].

But the [[hom-functor]] has the crucial property that it is an [[exact functor]] in both arguments. This holds for $(\infty,1)$-categories just as well as for ordinary categories. For our context this means in particular that for 

$$
  \array{
    A \times_K B &\to& B
    \\
    \downarrow && \downarrow
    \\
    A &\to& K
  }
$$

a homotopy pullback in $C$, for every $X \in K$ the induced diagram

$$
  \array{
     Hom_C(X,A \times_K B) &\to& Hom_C(X,B)
    \\
    \downarrow && \downarrow
    \\
    Hom_C(X,A) &\to& Hom_C(X,K)
  }
$$

is again homotopy pullback diagram (of [[∞-groupoids]]); in particular the morphism $Hom_C(X,A \times_K B)\to Hom_C(X,A) \times_{Hom_{C}(X,K)} Hom_C(X,B)$ induced by the universal property of homotopy pullback is an equivalence. 

So in particular for

$$
  \cdots
  \to
  \Omega \Omega B
  \to
  \Omega ker(f)
  \to
  \Omega A \stackrel{\bar \Omega f}{\to}
  \Omega B \to ker(f) \to A \stackrel{f}{\to} B
$$

a fibration sequence and for $X$ any object, there is a fibration sequence

$$
  \cdots
  \to
  Hom_C(X,\Omega \Omega B)
  \to
  Hom_C(X,\Omega ker(f))
  \to
  Hom_C(X,\Omega A) \stackrel{Hom_C(X,\bar \Omega f)}{\to}
  Hom_C(X,\Omega B) \to Hom_C(X,ker(f)) \to Hom_C(X,A) \stackrel{Hom_C(X,f)}{\to} Hom_C(X,B)
$$

is again a fibration sequence, now of $\infty$-groupoids. By projecting everything to connected components with $\Pi_0$ this then yields an ordinary long exact sequence of pointed sets


$$
  \cdots
  \to
  Ho_C(X,\Omega \Omega B)
  \to
  Ho_C(X,\Omega ker(f))
  \to
  Ho_C(X,\Omega A) \stackrel{Ho_C(X,\bar \Omega f)}{\to}
  Ho_C(X,\Omega B) \to Ho_C(X,ker(f)) \to Ho_C(X,A) \stackrel{Ho_C(X,f)}{\to} Ho_C(X,B)
  \,.
$$

Due to the identitfication of [[cohomology]] with these homotopy hom-sets via $Ho_C(X,A) =: H(X,A)$, this is a "long exact sequence in cohomology"


$$
  \cdots
  \to
  H(X,\Omega \Omega B)
  \to
  H(X,\Omega ker(f))
  \to
  H(X,\Omega A) \stackrel{H(X,\bar \Omega f)}{\to}
  H(X,\Omega B) \to H(X,ker(f)) \to H(X,A) \stackrel{H(X,f)}{\to} H(X,B)
  \,.
$$

### Long exact sequences of homotopy groups

See [[long exact sequence of homotopy groups]].

## Examples

### Characterization of equivalences {#CharOfEquivalences}

We may read off from the non-triviality of the homotopy fiber $A$ of a morphism $f : B \to C$ to which extent $f$ fails to be an [[equivalence in a quasi-category|equivalence]].

+-- {: .un_prop}
###### Proposition

A morphism $f : B \to C$ in [[∞Grpd]] is an equivalence precisely if all its homotopy fibers over every point of $C$ are [[contractible]], i.e. are equivalent to $*$.

More generally, a morphism $f : B \to C$ in any [[(∞,1)-category]] $\mathcal{C}$ is an equivalence if for all objects $X \in \mathcal{C}$ all homotopy fibers of the morphism $\mathcal{C}(X,f) : \mathcal{C}(X,B) \to \mathcal{C}(X,C)$ are contractible.

=--

For more on this see [[n-truncated object of an (∞,1)-category]]. Also [[Higher Topos Theory|HTT, around example 5.5.6.13]]. For more on homotopy fibers of hom-spaces see [the section below](#OfFuncCats).


### Fiber sequences of $(\infty,1)$-functor categories {#OfFuncCats}

We have seen that for $A \to B \stackrel{f}{\to} C$ a fiber sequence in 
an $(\infty,1)$-category $\mathcal{C}$,
then for any other object $X$ we obtain
a fiber sequence

$$
  Hom_{\mathcal{C}}(X,A)
  \to 
  Hom_{\mathcal{C}}(X,B)
  \stackrel{f_*}{\to}
  Hom_{\mathcal{C}}(X,C)
$$

in [[∞Grpd]], where the point of $Hom_{\mathcal{C}}(X,C)$ is $X \to * \to C$ with $* \to C$ the point of $C$, so that $Hom_{\mathcal{C}}(X,A)$ is the homotopy fiber over this point of the morphism given by postcomposition with $B \to C$.

Often it is important to know the homotopy fibers of $f_*$ also over other objects in $Hom_{\mathcal{C}}(X,C)$. This is notably the case when considering [[twisted cohomology]] with coefficients in $A$.


+-- {: .un_prop}
###### Proposition

The homotopy fiber of  $Hom_{\mathcal{C}}(X,B) \stackrel{f_*}{\to} Hom_{\mathcal{C}}(X,C)$ over a morphism $c : X \to C$ may be identified with the [[hom-object in a quasi-category|hom-object]] 

$$
  Hom_{\mathcal{C}_{/C}}(c,f)
$$

in the [[over quasi-category|over (∞,1)-category]] $\mathcal{C}_{/C}$.



=--

This is [[Higher Topos Theory|HTT, prop. 5.5.5.12]].

+-- {: .proof}
###### Proof

Model all [[(∞,1)-categories]] as [[quasi-categories]]. 

Using the discussion at [[hom-object in a quasi-category]], we observe that 

$$
  Hom_{\mathcal{C}}(X,C) \simeq \mathcal{C}_{/C} \times_{\mathcal{C}} \{X\}
$$


and

$$
  Hom_{\mathcal{C}}(X,B) \simeq \mathcal{C}_{/B} \times_{\mathcal{C}} \{X\}
  \simeq \mathcal{C}_{/f} \times_{\mathcal{C}} \{X\}
$$

under which identification the map $f_*$ is induced by the canonical

$$
  \phi''  : \mathcal{C}_{/f} \to \mathcal{C}_{/C}
  \,.
$$

So we are done if we can show that the ordinary [[pullback]] [[diagram]]

$$
  \array{  
     \mathcal{C}_{/f} \times_{\mathcal{C}_{/C}} \{c\}
     &\to& \mathcal{C}_{/f} \times_{\mathcal{C}} \{X\}
     \\
     \downarrow^{\mathrlap{\phi}} && \downarrow^{\mathrlap{\phi'}}
     \\
     \{c\} &\to& \mathcal{C}_{/C} \times_{\mathcal{C}} \{X\}
  }
$$

is a [[homotopy pullback]] square, because we have an isomorphism of simplicial sets

$$
  \mathcal{C}_{/f} \times_{\mathcal{C}_{/C}} \{c\}
  \simeq
  Hom^R_{\mathcal{C}_{/X}}(c,f)
  \,,
$$

as one checks.

Since in the above diagram all objects are [[Kan complex]]es, for the diagram to be a homotopy pullback it is sufficient that $\phi'$ is a [[Kan fibration]] for which in turn it is sufficient that it is a [[left fibration]]. 

That follows by noticing that the right vertical morphism fits into the pullback diagram

$$
  \array{
     \mathcal{C}_{/f} \times_{\mathcal{C}} \{X\} &\to& \mathcal{C}_{/f}
     \\
     \downarrow^{\mathrlap{\phi'}} && \downarrow^{\mathrlap{\phi''}}
     \\
     \mathcal{C}_{/C} \times_{\mathcal{C}} \{X\}
     &\to&
     \mathcal{C}_{/C}
  }
  \,.
$$

But by general properties of [[left fibration]]s, the right vertical map is a left fibration. And since these are stable under pullbacks, so is $\phi'$.


=--



### Principal $\infty$-bundles

Fibration sequences are familiar from the context of [[principal bundles]].

Let $G$ be a [[group]] and let $\mathbf{B}G$ denote the corresponding one-object [[groupoid]] (in the world of [[∞-groupoids]]) or else the [[classifying space]] $\mathcal{B}G$.

Notice that 

$$
  G \simeq \Omega \mathbf{B} G
  \,.
$$

Then that a $G$-[[principal bundle]] $P \to X$ is classified by morphism $X \to \mathbf{B}G$ means that it is the homotopy fiber of this morphism.

Indeed, as indicated at [[generalized universal bundle]] and at [[homotopy limit]], we may compute the homotopy pullback

$$
  \array{
  P &\to& {*}
  \\
  \downarrow && \downarrow
  \\
  X &\to& \mathbf{B}G
 }
$$

by first forming the standard _fibrant replacement_ of the diagram $X \to \mathbf{B}G \leftarrow {*}$. That is given by
the diagram

$$
  X \to \mathbf{B}G \leftarrow \mathbf{E}G  
  \,,
$$

where $\mathbf{E}G \simeq {*}$ is the total "space" (or 2-groupoid) of the universal $G$-bundle. Once we have done this weakly equivalent replacement, the [[homotopy pullback]] may be computed as the _ordinary_ pullback

$$
  \array{
   P &\to & \mathbf{E}G
   \\
   \downarrow && \downarrow
   \\
   \hat X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,, 
$$

in the ordinary 1-category of $n$-groupoids or spaces, using a replacement $\hat X \stackrel{\simeq}{\twoheadrightarrow} X$ of $X$ by an acyclic fibration (called "[[hypercover]]" in this context) (for instance the &#268;ech groupoid associated with an open cover of $X$). 

One recognizes the usual statement that principal $G$-bundles all arise as pullbacks of the universal $G$-principal bundle. 

The fact that such pullbacks really are bundles whose fiber is $G$ is the statement of the long fibration sequence induced by $g$ which says that picking any point ${*} \to X$ of $X$ and then pulling back $P$ to that point (i.e. restricting it to that point) yields $\Omega \mathbf{B}G = G$:

$$
  \array{
   G \simeq
   \Omega \mathbf{B}G
   &\to&
   P &\to & \mathbf{E}G
   \\
   \downarrow && \downarrow && \downarrow
   \\
   {*}&\stackrel{x}{\to}& \hat X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,, 
$$

The same logic -- even the same diagrams -- work for [[principal 2-bundles]] and generally for [[principal ∞-bundles]].

### Action groupoids {#ActionGroupoid}

Let $G$ be an [[∞-group]] in that $\mathbf{B}G$ is an [[∞-groupoid]] with a single object. An action of $G$ on an [[(∞,1)-category]] is an [[(∞,1)-functor]]

$$
  \rho : \mathbf{B}G \to (\infty,1)Cat
$$

to [[(∞,1)Cat]]. This takes the single object of $\mathbf{B}G$ to some $(\infty,1)$-category  $V$.

The _[[action groupoid]]_ $V//G$ is the [[limit in a quasi-category|(∞,1)-categorical colimit]] over the action:

$$
  C//G := \lim_\to \rho
  \,.
$$

By the result [described here](http://ncatlab.org/nlab/show/limit+in+a+quasi-category#WithValInooGrpd) this is, equivalent to the pullback of the "universal $(\infty,1)Cat$-bundle" $Z \to (\infty,1)Cat$, namely to the [[coCartesian fibration]]

$$
  \array{
    V//G &\to& Z
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\rho}{\to}& (\infty,1)Grpd
  }
$$

classified by $\rho$ under the [[(∞,1)-Grothendieck construction]]. We obtain a [[fiber sequence]] to the left by adjoining the $(\infty,1)$-categorical pullback along the point inclusion $* \to \mathbf{B}G$

$$
  \array{
    V&\to& V//G &\to& Z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& \mathbf{B}G &\stackrel{\rho}{\to}& (\infty,1)Grpd
  }
  \,.
$$

The resulting total $(\infty,1)$-pullback rectangle is the fiber of $Z \to (\infty,1)Cat$ over the $(\infty,1)$-category $C$, which is $V$ itself, as indicated.

Notice that every fibration sequence $V \to V//G \to \mathbf{B}G$ with $V//G \to \mathbf{B}G$ a [[coCartesian fibration]] arises this way, up to equivalence.


### Integral versus real cohomology {#Integralreal}

One of the most basic fibration sequences that appears all over the place in practice is the sequence of [[Eilenberg-MacLane object]]s

$$
  \cdots
  \to
  \mathbf{B}^{n-1} \mathbb{R}/\mathbb{Z}
  \to 
  \mathbf{B}^n \mathbb{Z}
  \to 
  \mathbf{B}^n \mathbb{R}
  \to  
  \mathbf{B}^n \mathbb{R}/\mathbb{Z}
  \to 
  \mathbf{B}^{n+1} \mathbb{Z}
  \to 
  \cdots
$$

in $\mathbf{H} = $ [[∞Grpd]]/[[Top]], where $\mathbb{R}$ is the abelian group (under addition) of [[real number]], $\mathbb{Z}$ the abelian group of [[integer]]s, and where $\mathbb{R}/\mathbb{Z} = S^1 = U(1)$ is their [[quotient]] group, the circle group or [[unitary group]] $U(n)$ for $n=1$.

A quick way to see that this is indeed a fibration sequence is to realize that $\mathbb{R}/\mathbb{Z}$ is equivalent to the weak quotient [[action groupoid]] $\mathbb{R}//\mathbb{Z}$. Since everything here is in the image of the [[Dold-Kan correspondence]]

$$
  \infty Grpd \simeq
  KanCplx
  \hookrightarrow
  sSet 
   \stackrel{\overset{U}{\leftarrow}}{\underset{F}{\to}}
  sAb
  \stackrel{\overset{\Xi}{\leftarrow}}{\underset{N^\bullet}{\to}}
  Ch^+
$$

it is useful to model this fiber sequence as a sequence of [[chain complex]]es

$$
  (
  \mathbf{B}^n\mathbb{R}
  \to 
  \mathbf{B}^n \mathbb{R}//\mathbb{Z}
  \to 
  \mathbf{B}^{n+1} \mathbb{Z}
  )
  \;\;\;
  =
  \;\;\;
  U \Xi
  \left(
     \left[
     \array{
       \vdots
       \\
       \downarrow
       \\
       0
       \\
       \downarrow
       \\
       \mathbb{R}
       \\
       \downarrow
       \\
       \vdots
     }
     \right]
     \;\;\;
     \to
     \;\;\;
     \left[
     \array{
       \vdots
       \\
       \downarrow
       \\
       \mathbb{Z}
       \\
       \downarrow
       \\
       \mathbb{R}
       \\
       \downarrow
       \\
       \vdots
     }
     \right]
     \;\;\;
     \to
     \;\;\;
     \left[
     \array{
       \vdots
       \\
       \downarrow
       \\
       \mathbb{Z}
       \\
       \downarrow
       \\
       0
       \\
       \downarrow
       \\
       \vdots
     }
     \right]
  \right)
  \,.
$$

Written this way the second morphism is evidently a degreewise surjection, hence is a fibration in the [[model structure on chain complexes]]. Therefore this being a fibration sequence is equivalent (as described at [[homotopy pullback]]) to the first morphism being equivalent to the ordinary [[kernel]] of the second, which clearly it is.

From this fiber sequence we obtain long exact sequences in cohomology, for instance in [[singular cohomology]]: let $X$ be a [[topological space]] and for $A$ an abelian group let

$$
  H^n(X,A) := \pi_0 \infty Grpd( \Pi(X), \mathbf{B}^n A)
$$

be its cohomology with coefficients in $A$, computed in [[∞Grpd]] which we may [[presentable (∞,1)-category|present]] by [[sSet]], where the [[fundamental ∞-groupoid]] $\Pi(X)$ is the singular simplicial complex $Sing X$ and we have

$$
  H^n(X,A) = \pi_0 sSet(Sing X, U \Xi A[n])
  \,.
$$

Then, as discussed [above](LongSequCoh), the fiber sequence of coefficients  $
  \cdots
  \to
  \mathbf{B}^{n-1} \mathbb{R}/\mathbb{Z}
  \to 
  \mathbf{B}^n \mathbb{Z}
  \to 
  \mathbf{B}^n \mathbb{R}
  \to  
  \mathbf{B}^n \mathbb{R}/\mathbb{Z}
  \to 
  \mathbf{B}^{n+1} \mathbb{Z}
  \to 
  \cdots
$ yields the long exact sequence in cohomology

$$
  \cdots 
  H^{n-1}(X,\mathbb{R}/\mathbb{Z})
  \to H^n(X,\mathbb{Z}) \to H^n(X,\mathbb{R}) \to 
  H^n(X,\mathbb{R}/\mathbb{Z})
  \to
  H^{n+1}(X,\mathbb{Z})
  \to
  \cdots
  \,.
$$

In applications it often happens that one has a situation where the _real_ cohomology is trivial, i.e $H^n(X,\mathbb{R}) = 0$ in some degree $n$. In that case the exactness of the sequence

$$
  \cdots 
  \to H^n(X,\mathbb{Z}) 
  \to 0 \to 
  H^n(X,\mathbb{R}/\mathbb{Z})
  \to
  H^{n+1}(\mathbb{Z})
  \to
  0
  \to
  \cdots
$$

implies that in this case we have an [[isomorphism]]

$$
  H^n(X,\mathbb{R}/\mathbb{Z})
  \stackrel{\simeq}{\to}
  H^{n+1}(\mathbb{Z})
  \,.
$$



### Mayer-Vietoris sequences 
 {#MayerVietoris}


A **[[Mayer-Vietoris sequence]]**  is a fiber sequence obtained from an $(\infty,1)$-pullback diagram of [[pointed objects]]:

if 

$$
  \array{
    A \times_C B &\to& B
    \\
    \downarrow && \downarrow^{\mathrlap{g}}
    \\
    A &\stackrel{f}{\to}& C
  }
$$

is an [[limit in a quasi-category|infinity-pullback]] diagram in $\mathbf{H}$, then it naturally induces a fiber sequence that starts out as

$$
  \Omega C \to A \times_C B \to A \times B
  \,.
$$

This -- or its associated [[long exact sequence of homotopy groups]] -- is called the _[[Mayer-Vietoris sequence]]_ of the pullback. See there for details.

#### Of a cover

The original example of Mayer-Vietoris sequences is obtained from the situtation where a [[homotopy pushout]] diagram

$$
  \array{
    U \cap V &\hookrightarrow& U
    \\
    \downarrow && \downarrow
    \\
    V &\to& X
  }
$$

in $\mathbf{H} = $ [[∞Grpd]]/[[Top]] is given (which modeled in [[sSet]] or in terms of [[CW-complex]]es in [[Top]] may be modeled by an ordinary pushout), and where $A \in \infty Grpd$ is some coefficient group object. Then applying the $(\infty,1)$-categorical hom $\mathbf{H}(-, A) : \mathbf{H}^{op} \to \infty Grpd$ yields the $\infty$-pullback diagram

$$
  \array{
    \mathbf{H}(X, A) &\to& \mathbf{H}(U,A)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(V,A) &\to& \mathbf{H}(U \cap V, A)
  }
  \,.
$$

By the above this is equivalent to 

$$
  \mathbf{H}(X,A) \to \mathbf{H}(U,A) \times \mathbf{H}(V,A)
  \to \mathbf{H}(U \cap V, A) 
$$

being a fibration sequence. The corresponding long exact sequence in cohomology (as discussed above) is what is traditionally called the Mayer-Vietoris sequence of the cover of $X$ by $U$ and $V$ in $A$-cohomology.

## Related concepts

* [[tower of homotopy fibers]]

* [triangulated category -- long fiber-cofiber sequences](triangulated+category#LongExactSequences)

## References

The observation of [[long exact sequences of homotopy groups]] for homotopy fiber sequences originates (according to [Switzer 75, p. 35](#Switzer75)) in 

* M. G. Barratt, _Track groups I, II_. Proc. London Math. Soc. 5, 71-106, 285-329 (1955). 

The first exhaustive study of these is due to 

* {#Puppe58} [[Dieter Puppe]], _Homotopiemengen und ihre induzierten Abbildungen I_, Math. Z. 69,  299-344 (1958). 

whence the terminology _Puppe sequences_.


Classical textbook accounts include

* {#Switzer75} [[Robert Switzer]], around 2.57 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#Kochmann96} [[Stanley Kochmann]], prop. 3.2.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Lecture notes:

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 1 of: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])


The construction in the axiomatic homotopy theory of [[model categories]] is due to 

* {#Quillen67} [[Daniel Quillen]], chapter I.3 of  _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43 43, Berlin (1967)

and in the context of [[categories of fibrant objects]] due to 

* {#Brown73} [[Kenneth Brown]], section 4 of _[[BrownAHT|Abstract Homotopy Theory and Generalized sheaf Cohomology]]_, 1973 .


A discussion of fiber sequences in terms of [[associated ∞-bundles]] is in

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ ([arXiv](http://arxiv.org/abs/1009.2930))

Related discussion on the behaviour of [[fiber sequence]]s under left [[Bousfield localization of model categories]] is in

* [[Matthias Wendt]], _Fibre sequences and localization of simplicial sheaves_,
Alg. Geom. Topol. 13(3), 2013, pp. 1779--1813. ([preprint pdf](http://home.mathematik.uni-freiburg.de/arithmetische-geometrie/preprints/wendt-flocal.pdf) and [ArXiv](http://arxiv.org/abs/1011.4784).)


[[!redirects fiber sequences]]

[[!redirects fibration sequence]]
[[!redirects fibration sequences]]

[[!redirects Puppe sequence]]
[[!redirects Puppe sequences]]

[[!redirects homotopy fiber]]
[[!redirects homotopy fibers]]
[[!redirects homotopy fibre]]
[[!redirects homotopy fibres]]
[[!redirects homotopy kernel]]
[[!redirects homotopy kernels]]

[[!redirects homotopy exact sequence]]
[[!redirects homotopy exact sequences]]

[[!redirects homotopy fiber sequence]]
[[!redirects homotopy fiber sequences]]
[[!redirects homotopy fibre sequence]]
[[!redirects homotopy fibre sequences]]

[[!redirects (∞,1)-fiber]]
[[!redirects (∞,1)-fibers]]
[[!redirects (∞,1)-fibre]]
[[!redirects (∞,1)-fibres]]

[[!redirects long homotopy fiber sequence]]
[[!redirects long homotopy fiber sequences]]