for related entries see

* [[gerbe (as a stack)]]

* [[bundle gerbe]]

***

#Idea#

The concept _gerbe_ is a [[vertical categorification|categorification]]
of the concept of [[principal bundle]], together with a generalisation analogous to that from bundles to [[sheaf|sheave]]s.

Recall that a $G$-[[principal bundle]] (for $G$ a [[group]]) is a space $P$
equipped with a map $P \to X$ to a base space $X$,
such that each [[fiber]] of $P$ looks like $G$
in a nice way.

A _$G$-gerbe_ is similarly a space $P \to X$ such that
each fiber looks like $\mathbf{B}G$ in a nice way.
We can also replace $G$ with a sheaf of groups,
or even with a $2$-[[2-group|group]].

Here "space" may mean ordinary [[topological space]]. In that case
$\mathbf{B} G$ is the [[classifying space]] of the group $G$
and the above describes the construction by Stasheff and Wirth 
of fibrations with fiber $B G$.

+--{: .query}
[[David Roberts]]: The list of axioms in Wirth-Stasheff about [[fibration theory|fibration theories]] is somewhat incomplete in my opinion (sorry Jim) - but only in a minor way. When it talks about the assignment of a category to each space, then goes on to talk about homotopies in that category, it seems to me we should be talking about $(infty,1)$-categories. Even without such an extension, one needs to make sense of homotopies, and so should have the minimal structure required to talk about that - perhaps a category of fibrant objects?
=--

More generally, "space" may refer to 
[[space and quantity|generalized spaces]], called 
[[infinity-stack]]s: objects
in any [[(infinity,1)-topos]].

Recall from [[motivation for sheaves, cohomology and higher stacks]]
that this is just heavy terminology for a very simple idea. 
The notion that a generalized space, also called an [[infinity-stack]], is an object in an $(\infty,1)$-topos
simplifies the situation conceptually by
separating 

* conceptual structures (certain spaces with certain fibers) 

from their 

* implementation (details of what is regarded as a generalized space and how). 

In particular, while 
gerbes are traditionally, originally by Giraud, 
introduced as 1-[[stack]]s with extra
[[stuff, structure, property|properties]], one need not mention
any details of stacks for describing the concept and behaviour
of gerbes, all one needs is to remember that $\infty$-stacks are general notions of spaces, for which there is the familiar toolbox from [[homotopy theory]] of spaces, notably notions of [[homotopy limit|homotopy pullback]] and [[fibration sequence]]. This makes transparent the relation between

* gerbes
* Stasheff--Wirth fibrations  
* nonabelian group extensions.

All of these are the same structure implemented in different contexts of generalized spaces.

For instance the last item here interprets extensions $G \to H \to K$ of a [[group]] $K$ by a group $G$ as a $G$-gerbe over $\mathbf{B}K$, namely as a fibration  $\mathbf{B}H \to \mathbf{B}K$ with fiber $\mathbf{B}G$.



When the group $G$
in question is [[abelian group|abelian]], the theory of gerbes is
very straightforwardly the generalization of that of [[principal bundle]]s,
because in this case the one-object [[groupoid]] $\mathbf{B}G$ 
obtained by shifting $G$ in categorical degree (see the discussion at [[group]]) 
still has itself a 
group-structure: it is a [[2-group]]. Much of what makes 
the discussion of nonabelian gerbes less than obvious is due to the
fact that when $G$ is not abelian then the way in which $\mathbf{B}G$
still relates to a group-like structure is slightly more involved and proceeds via the [[automorphism 2-group]] $AUT(G)$ of $G$.

Recall that an ordinary $G$-[[principal bundle]] $P \to X$
is a fibration of (generalized) spaces for which there is a 
morphism $g : X \to \mathbf{B} G$ such that $P$ is the 
[[homotopy pullback]] of the [[point]] along $g$:

$$
  \array{
    P &\to & {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}G
  }
  \,.
$$
So $P \to X \to \mathbf{B}G$ is a [[fibration sequence]] that extends for each
choice of point ${*} \to X$ of $X$ to the left to a fibration sequence
$G \to P \to X \to \mathbf{B}G$. This says that the fiber of $P \to X$ over each
point looks like the group $G$. General nonsense implies then
that the action of $G$ on itself induces an action of $G$ on all of $P$
and that this action is indeed [[principal bundle|principal]].

When $G$ is an abelian group, so that $\mathbf{B}G$ itself has a group
structure, the object $\mathbf{B}\mathbf{B}G$ exists and the above
statement has an immediate [[vertical categorification|categorification]]:

A $G$-gerbe for $G$ an abelian group is a fibration 
$P \to X$ such that there is a morphism $g : X \to \mathbf{B}\mathbf{B}G$
such that $P$ is the [[homotopy pullback]] of the point along
this fibration.

$$
  \array{
    P &\to & {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}\mathbf{B}G
  }
  \,.
$$

In this case for each point ${*} \to X$ of $X$  this yields
a [[fibration sequence]]
$$
  \cdots \to \mathbf{B}G \to P \to X \to \mathbf{B}\mathbf{B} G
$$
which says that the fiber of $P \to X$ over each point of $X$ looks like
$\mathbf{B}G$.

As in the previous case of ordinary bundles, general nonsense implies that 
$P \to X$ comes with a principal $\mathbf{B}G$-action. $P$ is therefore also
called a $\mathbf{B}G$-[[principal 2-bundle]] or a $\mathbf{B}G$-[[torsor]].
In its concrete incarnation as a [[stack]], $P$ is called a $G$-gerbe.

Moreover, since [[cohomology]] on $X$ with values in $\mathbf{B}\mathbf{B}G$ is nothing but the [[hom-set]] 

$$
  H^2(X,G) = Ho(X, \mathbf{B}\mathbf{B} G)
$$

in the [[homotopy category of an (infinity,1)-category|homotopy category]] of our generalized spaces, it is a tautology that these $G$-gerbes are classified by $H^2(X,G)$. 

Notice in particular that for $G = U(1)$ we have $H^2(X, U(1)) \simeq H^3(X, \mathbb{Z})$, so that $U(1)$-gerbes in the above sense are classified by third integral cohomology.
This classification statement was the main motivatoin for the study of the realization of the notion of gerbe that goes by the name [[bundle gerbe]].


In this fashion, for $G$ abelian, the entire concept of 
$G$-$(n-1)$-gerbe is straightforward: it is the
$(n-1)$-[[infinity-stack|stack]] incarnation of $\mathbf{B}^n G$-[[principal infinity-bundle]]s, i.e. of fibrations $P \to X$ of (generalized) spaces
that arise as homotopy pullbacks of the form
$$
  \array{
    P &\to & {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{B}\mathbf{B}^n G
  }
  \,.
$$

Accordingly, such $(n-1)$-gerbes for $G$ abelian are classified in [[cohomology]] by $H^{n+2}(X,G)$.
(Another way to see why this is possible for $G$ an abelian group is that not only is $\mathbf{B}G$ a $2$-group, but $\mathbf{B}^n G$ is an $(n-1)$-[[n-group|group]], which is what we need in general for an $n$-gerbe.)

Moreover, for $A$ any pointed connected generalized space (any parameterized $\infty$-groupoid
with a single object),
we may say that $A$-principal $\infty$-bundles are fibrations $P \to X$
classified in this way by classifying morphisms $X \to A$
$$
  \array{
    P &\to & {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& A
  }
  \,.
$$
The fiber of such an $\infty$-bundle is the [[loop space object]] $\Omega A$.
The classifying morphism $X \to A$ is then called a cocycle in
[[nonabelian cohomology]].

In particular, for $H$ any [[2-group]] (not necessarily of the
form $H = \mathbf{B}G$ for $G$ an abelian group as above) an $H$-[[principal 2-bundle]] is a fibration in this sense classified
by a morphism $X \to \mathbf{B} H$. The typical fiber of
such a $2$-bundle looks like $H$.

Now, a $G$-gerbe for $G$ nonabelian is supposed to be a fibration
whose typical fiber is $\mathbf{B}G$. Since this is not a [[2-group]],
one has to say what one wants to mean by this.

This now is the crucial fact that translates between the
straightfoirward definition of $H$-[[principal 2-bundle]]s
as above and the notion of $G$-gerbe:

For every group $G$, there is the [[2-group]] $AUT(G)$, defined equivalently
as follows:

* $AUT(G)$ is the automorphism $2$-group of the [[groupoid]] $\mathbf{B}G$, i.e. 
  $$
    AUT(G) = Aut_{Grpd}(\mathbf{B}G)
    \,;
  $$  

* $AUT(G)$ is the [[2-group]] corresponding to the [[crossed module]] 
  given by the sequence
  $(G \stackrel{Ad}{\to} Aut(G))$ of groups, with the canonical action
  of $Aut(G)$ on $G$.

From the second description it is manifest that one can 
project out a copy of $\mathbf{B}G$ out of $AUT(G)$ (the shifted copy): there is a morphism $AUT(G) \to \mathbf{B}G$ 
obtained simply by identifying all objects of $AUT(G)$.
Indeed, $AUT(G)$ is a groupoid extension of $\mathbf{B}G$ by 
the [[discrete category|discrete groupoid]] on $Aut(G)$ in that
$$
  Aut(G) \to AUT(G) \to \mathbf{B}G
$$
is a fibration sequence.

This means that any $AUT(G)$-[[principal 2-bundle]] with typical fiber
the groupoid $AUT(G)$ has underlying it a fibration with
typical fiber the one-object groupoid $\mathbf{B}G$. This
underlying object is the $G$-gerbe.

Notice in particular that when $G$ is abelian there is a canonical morphism

$$
  \mathbf{B}\mathbf{B} G \to  \mathbf{B} AUT(G)
$$

which however is not an equivalence when $G$ has nontrivial automorphisms. Therefore $G$-gerbes in the sense of nonabelian $G$-gerbes classified by $H(X,\mathbf{B}AUT(G))$ are even for $G$ abelian a bit more general than the things classified by just $H(X, \mathbf{B}^2 G)$, which are however also often called $G$-gerbes (in particular "[[bundle gerbe]]s").


This is the general nonsense underlying the concept of gerbe. 

See also

* [[gerbe (as a stack)]]
* [[bundle gerbe]].


#References#

There is a lengthier description of gerbes (at this level of generality) in the Menagerie notes that are available from [[Tim Porter|Tim Porter's]] home page.

Other material available online includes the following:

* I. Moerdijk, _Introduction to the language of stacks and gerbes_ ([arXiv](http://arxiv.org/abs/math/0212266))

* Larry Breen, _Notes on 1- and 2-gerbes_ ([arXiv](http://arxiv.org/abs/math/0611317))

See the references given there for more, in particular also the reference to the work by Jardine which relates to the discussion of gerbes in the context of [[infinity-stack]]s using the [[model structure on simplicial presheaves]].


The work by Stasheff and Wirth mentioned at the beginning is

* James Wirth & Jim Stashef, _Homotopy Transition Cocycles_ ([arXiv](http://arxiv.org/abs/math.AT/0609220) [blog](http://golem.ph.utexas.edu/category/2006/09/wirth_and_stasheff_on_homotopy.html))

