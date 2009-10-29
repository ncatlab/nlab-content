#Idea#

The _delooping_ of an object $A$ is, if it exists, a uniquely [[pointed object]] $\mathbf{B} A$ such that $A$ is the [[loop space object]] of $\mathbf{B} A$:

$$
  A \simeq \Omega(\mathbf{B} A)
$$

In particular, if $A = G$ is a [[group]] then its delooping 

* in the context [[Top]] is the [[classifying space]] $\mathcal{B}G$

* in the context $\infty$ [[Infinity-Grpd]] is the one-object groupoid $\mathbf{B}G$.

Under the [[homotopy hypothesis]] these two objects are identified: the [[geometric realization]] of the groupoid $\mathbf{B}G$ is the classifying space $\mathcal{B}G$:

$$
  |\mathbf{B}G| \simeq \mathcal{B}G
  \,.
$$


#Definition#

Loop space objects are defined in any [[(∞,1)-category]] $\mathbf{C}$ with [[homotopy pullback]]s: for $X$ any [[pointed object]] of $\mathbf{C}$ with point ${*} \to X$, its [[loop space object]] is [[generalized the|the]] [[homotopy pullback]] $\Omega X$ of this point along itself:

$$
  \array{
    \Omega X &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& X
  }
  \,.
$$

Conversely, if $A$ is given and a [[homotopy pullback]] diagram 

$$
  \array{
    A &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& \mathbf{B}A
  }
$$

exists, with the point ${*} \to \mathbf{B} A$ being essentially unique, by the above $A$ has been realized as the [[loop space object]] of $\mathbf{B} A$

$$
  A = \Omega \mathbf{B} A
$$

and we say that $\mathbf{B} A$ is the **delooping** of $A$.

#Remarks#

If $\mathbf{B}$ is even a [[stable (∞,1)-category]] then all deloopings exist and are then also denoted $\Sigma A$ and called the **[[suspension]]** of $A$.


#Characterization of deloopable objects#

In section 6.1.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

a definition of 
[[groupoid object in an (infinity,1)-category]] $\mathbf{C}$ is given
as a homotopy simplicial objects, i.e. a [[(infinity,1)-functor]]

$$
  C  : \Delta^{op} \to \mathbf{C}
$$
$$
  \cdots
  C_2 \stackrel{\to}\rightrightarrows
  C_1 
  \rightrightarrows 
 C_0
$$

satisfying certain conditions (prop. 6.1.2.6) which are such that if $C_0 = {*}$ is the [[point]] we have an internal _group_ in a homtopical sense, given by an object $C_1$ equipped with a coherently associative multiplication operation  $C_1 \times C_1 \to C_1$ generalizing that of [[Jim Stasheff|Stasheff]] [[H-space]] from the $(\infty,1)$-catgeory [[Top]] to arbitrary $(\infty,1)$-categories.

Lurie calls the groupoid object $C$ an 
_effective_ [[groupoid object in an (infinity,1)-category]] precisely if it arises as the delooping, in the above sense, of some object $\mathbf{B}C$.

One of the characterizing properties of an [[(infinity,1)-topos]] is that _every_ groupoid object in it is effective.

This is the analog of [[Jim Stasheff|Stasheff]]'s classical result about [[H-space]]s.

See the remark at the very end of section 6.1.2 in [[Higher Topos Theory|HTT]].




#Examples#


## topological loop spaces ##

For $C = $ [[Top]] the [[(infinity,1)-category]]
of [[topological space]]s, a space is deloopable if it is an [[H-space]] and hence homotopy equivalent to a [[loop space]].


## delooping of a group to a groupoid ##

Let $G$ be a [[group]] regarded as a [[discrete category|discrete groupoid]] in the [[(∞,1)-topos]] [[∞Grpd]] of [[∞-groupoids]].

Then $\mathbf{B} G$ exists and is, up to equivalence, the [[groupoid]]

* with a single object $\bullet$,

* with $Hom_{\mathbf{B} G}(\bullet, \bullet) = G$, or equivalently $Aut_{\mathbf{B}G}(\bullet) = G$,

* and with composition of morphisms in $\mathbf{B} G$ being given by the product operation in the group.

More informally but more suggestively we may write

$$
  \mathbf{B} G = \{ \bullet \stackrel{g}{\to} \bullet | g \in G\}
$$

or

$$
  \mathbf{B}G = \{ 
     \bullet \righttoleftarrow g \;|\; g \in G 
  \}
$$

to emphasize that there is really only a single object.

Notice how the [[homotopy pullback]] works in this simple case:

the universal 2-cell $\eta$

$$
  \array{
    G &\to& {*}
    \\
    \downarrow &\Downarrow^{\eta}& \downarrow
    \\
    {*} &\to& \mathbf{B}G
  }
$$

filling this [[2-limit]] diagram is the [[natural transformation]] from the constant [[functor]]

$$
  G \to {*} \to \mathbf{B}G
$$

to itself, whose component map

$$
  \eta : Obj(G) \to Mor(\mathbf{B}G)
$$ 

is just the identity map, using that $Obj(G) = G$ and $Mor(\mathbf{B}G) = G$.

#Discussion#

_Eric_: When the two arguments coincide in $Hom_{\mathbf{B}G}(\bullet,\bullet)$, is there another notation, e.g. maybe $Aut_{\mathbf{B}G}(\bullet)$ or something? 

_[[Urs Schreiber|Urs]]_: yes. In general for $C$ a category and $c \in C$ an object one writes $End_C(c) := Hom_C(c,c)$ (for "endomorphisms"). One writes $Aut_C(c) \subset End_C(c)$ for the subset of all endomorphims that are invertible (are "automorphisms"). So for $C$ a groupoid, we have alsways $End_C(c) = Aut_C(c)$. 

_[[Eric]]_: Thanks. Maybe I read too much into choices of notation, but I can sort of see why you prefer $\bullet\to\bullet$ if you are accustomed to thinking in terms of $Hom(\bullet,\bullet)$. They look the same! My brain is wired to think of $Aut(\bullet)$, so I prefer $\bullet\righttoleftarrow$ (because they look the same). Maybe there is no connection. I know it is irrelevant, but just a random observation :)

Urs: Well, the main reason is that one doesn't get very far with any computation or any nontrivial statement when not allowing oneself to write several $\bullet$s, even though they all denote the same object. Try drawing the naturality squares of the natural transformations that appear in the above discussion without using several copies of the point!

And notice that in every other context, you wouldn't hesitate to use several copies of one symbol that denotes the same variable. Try writing an equation with many $x$s in it by writing all the $x$s on the same spot. All you'd get is an unreadable mess. Nobody would ever complain that in $x = ln(x)$ the two $x$s are really the same and should hence be drawn on the same spot.

Remarkably, I should add that I had this discussion before with professional pure mathematicians. Once they stopped a talk I gave when I wrote $\bullet \stackrel{g}{\to} \bullet$ to the board, complaining that Ii drew two copies of that bullet. If it's just about saying quickly what $\mathbf{B}G$ is like that's fine with me, but for doing anything nontrivial with it it becomes useless. Try drawing $\mathbf{B}G$ for $G$ a 2-group or a 3-group! Not to speak of drawing the transformations between functors between these.

_[[Eric]]_: Here is an attempt to convert one of your diagrams above to a single $\bullet$ version.

[[delooping1.jpg:pic]]

I'm not saying one way is better than the other. I'm just making a statement about my inability to process some of the diagrams. Some diagrams are not even amenable to these "3d projections", but for those that can be, it would help me to convert them.

_[[Eric]]_: Here is another attempt in case that one is not quite right...

[[delooping2.jpg:pic]]

_Toby_:  I think that perhaps part of the problem is that people see '$\bullet$' as a generic placeholder like '$-$'; notice that the two dashes in '$[-,-]$' below do *not* refer to the same thing!  (With '$x$', you know that the two copies refer to the same thing, else one of them would be '$y$' instead.)  So perhaps people need to be told that the bullet is like a letter and *not* like a dash.

Along those lines, sometimes it\'s nice to use '$G$' itself in place of the bullet.  Ultimately, you can think of this as Cayley\'s Theorem: every group acts on itself (somewhat ambiguously on the left or on the right).  Then with $\{ G \righttoleftarrow g \;|\; g \in G \}$, you have a picture of $\mathbf{B}G$ as a [[subcategory]] of [[Set]], consisting of the underlying set of $G$ as the only object and the functions given by the action of the elements of $G$ on that set as the morphisms.

_Urs_: I have to admit that I don't quite understand Eric's  pictures. Here is what I meant concerning the transformation:

let $f_1, f_2 : G \to H$ be two group homomorphisms and $\eta : \mathbf{B}f_1 \Rightarrow \mathbf{B} f_2 $ be a [[natural transformation]] between the corresponding functors $\mathbf{B} f_1, \mathbf{B}f_2 : \mathbf{B}G \to \mathbf{B}H$. Then $\eta$ has a single component $\eta : {*} \to H$ to be denoted $\eta_* \in H$, which is required to make the naturality square 

$$
  \array{
     {*} &\stackrel{\eta_*}{\to}& {*}
     \\
     \downarrow^{f_1(g)} && \downarrow^{f_2(g)}
     \\
     {*} &\stackrel{\eta_*}{\to}& {*}
  }
$$

commute, for all $g \in G$. You can't draw such diagrams when insisting that all the points ${*}$ appearing here are to be drawn on the same spot.

And, yes, as Toby indicates, we could give that point any other name, which maybe makes that more manifest. Let's call it $x$, then we have

$$
  \array{
     x &\stackrel{\eta_*}{\to}& x
     \\
     \downarrow^{f_1(g)} && \downarrow^{f_2(g)}
     \\
     x &\stackrel{\eta_*}{\to}& x
  }
$$

and the desire to draw all $x$s on the same spot should diminish yet a bit more.


***

_Eric_: Is there a difference between $Hom$ and $hom$? For example, [[hom-set]] says $hom$, but [[internal hom]] has $Hom$, $hom$, and $HOM$.

_[[Urs Schreiber|Urs]]_: I have added some links regarding this point at [[Notation]]. There is no really universally adopted convention here, but people do use the different capitalizations to indicate different things.

Usually "Hom" is the ordinary [[hom-set]], while some variant of this is usually chosen for the [[internal hom]]. Sometimes "HOM", yes. Many people like an underlined "Hom" for the internal Hom. But also $hom$ and $[-,-]$ may denote internal homs. The last one is the standard choice in Kelly's standard book on [[enriched category theory]] (though concerning just [[monoidal category]] here), so I like that one.

_[[Eric]]_: Is $[-,-]$ also [[functor category]]? I see you answered this at [[Notation]]. Handy :)

_Urs_: yes, you see by itself one often write $Func(-,-)$ for the functor category. But the category [[Cat]] is an [[enriched category]] over itself, with the [[internal hom]] being $[-,-] := Func(-,-)$. So I like writing $[-,-]$ for the functor category. But in many other places you'll find $Func(-,-)$ or other things.

***

>The following discussion originally took place at [[Dijkgraaf-Witten theory]].

_Eric_: This notation seems to cause some initial confusion. At least until you realize both $\bullet$'s are the same, so the morphism is really a loop. Why not just represent it as a loop? I like this notation:

  $$\mathbf{B}G = \{\bullet\righttoleftarrow g | g\in G\}$$

  What do you think?

  Or better yet

  $$\mathbf{B}G = \bullet\righttoleftarrow G.$$

_Toby_:  I like your first suggestion, so I implemented it; but I think that I only understand the second suggestion since I already know what it means.

  [[Urs Schreiber|Urs]]: added link to [[delooping]] above so that we have one page where this is treated discussed, since it appears in lots of other entries, too.

[[!redirects deloopings]]
