#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

The _graph of a function_ $f : X \to Y$ is the subset that $f$ "carves out" of the [[cartesian product]] $X \times Y$.



# Definition #

## Graph of a function ##

The traditional standard definition of a graph of a function is this:

+-- {: .un_defn}
###### Definition

The __graph__ $graph(f)$ of a [[function]] $f: X \to Y$ is that [[subset]] $graph(f) \hookrightarrow X \times Y$ of the [[cartesian product]] $X \times Y$ defined by the property that $(a,b) \in X \times Y$ belongs to the graph of $f$ if and only if $f(a) = b$:

$$
  graph(f) = \{(a,b) \in X \times Y | f(a) = b\}
  \,.
$$

=--

This can be understood as a special case of a [[graph of a functor]] by the following observation

+-- {: .un_lemma }
###### Lemma

For $f : X \to Y$ a [[function]], define a function

$$
  \chi_f : X \times Y \to \{0,1\}
$$

by regarding a [[set]] as a [[0-category]] and a 0-category as a [[(-1)-category]]-[[enriched category]] and then setting

$$
  \chi_f : X \times Y \stackrel{=}{\to} X^{op} \times Y \stackrel{f^{op} \times Id}{\to} Y^{op} \times Y \stackrel{Hom}{\to} \{0,1\}
  \,.
$$

Then $\chi_f$ is the [[characteristic function]] of $graph(f)$ in that the diagram

$$
  \array{
     graph(f) &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     X \times Y &\stackrel{\chi_f}{\to}& \{0,1\}
  }
$$

is a [[pullback]] diagram.

=--
 
In other words this means that in the context of [[(-1)-category]]-[[enriched category theory]] the graph of a function $f$, regarded as an [[enriched functor]] is the [[category of elements]] of the corresponding [[profunctor]]. More on this at [[graph of a functor]].

+-- {: .un_remark}
###### Remark

It is  easy to identify the properties of those subsets of $X \times Y$ that are the graphs of functions, and $f = g$ if they have the same graph (given $X$ and $Y$).  Consequently, it is common, especially (but not only) in [[material set theory]], to *define* a function from $X$ to $Y$ as such a subset, that is to identify a function with its graph.  On the other hand, from a more categorial foundation, as discussed above, it\'s common to define a [[subset]] to be a [[characteristic function]]!

=--

## Graph of a binary relation ##

More generally, we can say that the __graph__ of a [[binary relation]] from $X$ to $Y$ is a subset of $X \times Y$; $(a,b)$ belongs to the graph if and only if $a$ is related to $b$.  (Note that *every* subset of $X \times Y$ defines a unique relation; such a subset is the graph of a function if and only if the relation is both [[functional relation|functional]] and [[entire relation|entire]].)

Notice that with a function $f : X \to Y$ regarded as a [[profunctor]] $X \times Y \to (-1)Cat$ as described above, a relation $R \subset X \times Y$ corresponds to a general such [[profunctor]]. More precisely we have a [[pullback]] square

$$
  \array{
    R &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X \times Y &\stackrel{\chi_R}{\to}& \{0,1\}
  }
$$

where 

* $R \subset X \times Y$ is the relation $R$ regarded as a subset of $X \times Y$ in the traditional sense;

* $\chi_R : X \times Y \to \{0,1\}$ is the [[characteristic function]] of this subset.

So in this sense the ordinary notion of relation as a subset does really define the _graph of the relation_, while the relation itself is more naturally understood as the corresponding 0-[[profunctor]]/[[characteristic function]] $\chi_f$.


### Relation to graph theory ###

The graph of a binary relation from $X$ to $X$ is related to the notion of [[graph]] from [[graph theory]]; more precisely, such relations correspond to directed loop graphs (in the sense defined at [[graph]]) with vertex set $X$, and either can be defined as a subset of $X^2$.  In a similar way, [[spans]] from $X$ to $X$ correspond to [[digraph|directed pseudographs]] with vertex set $X$.

For the case of a relation from $X$ to $Y$ without $X = Y$, see under the cograph below.


## Graph of an $n$-ary relation ## 

The __graph__ of a [[relation]] of arbitrary arity is similarly a subset of an arbitrary [[cartesian product]]; see [[relation theory]] for more on this.



## Cograph of a function ##

[[Bill Lawvere]] has also considered the __cograph__ of a function, which is dually a [[quotient set]] of the [[disjoint union]] $X \uplus Y$; $a$ is identified with $b$ if $f(a) = b$ (and additional identifications may follow).  

By regarding again a set as a [[0-category]], this is a special case of the notion of [[cograph of a functor]]

A function $f : X \to Y$ determins a [[functor]] $\bar f : I \to Set$ from the [[interval category]] $I = \mathbf{2} = \{a \to b\}$ to [[Set]] by setting $\bar f(a) = X$, $\bar f(b) = Y$ and $\bar f(a \to b) = f$.

Then let $cograph(f)$ be the corresponding [[category of elements]], given by the [[2-pullback]]

$$
  \array{
     cograph(f) &\to& {*}
     \\
     \downarrow && \downarrow
     \\
     I &\stackrel{\bar f}{\to}& Set
  }
$$

wich is computed by the strict [[pullback]]

$$
  \array{
     cograph(f) &\to& Set_{*}
     \\
     \downarrow && \downarrow
     \\
     I &\stackrel{\bar f}{\to}& Set
  }
  \,.
$$

The cograph of $f$ in the sense of Lawvere is the set of connected components of this category, i.e. $\pi_0(cograph(f))$.

### Relation to graph theory ###

The notion of cograph of a function may be even more related to the sense of [[graph]] in graph theory; although the identifications are not done there, the cograph draws a picture in which any relation (or [[multispan]]) of any arity becomes a directed graph (or directed multigraph) whose vertex set is the disjoint union of the relation\'s domains.  When the vertex set is broken up into a disjoint union in this way, graph theorists study this as _multipartite graphs_; in particular, directed bipartite graphs with vertex set broken up as $X + Y$ correspond precisely to binary relations from $X$ to $Y$.

# Generalization #

The notion of _graph of a function_ is a special case of the notion [[graph of a functor]] obtained for functors between [[0-category|0-categories]].

Accordingly, the notion of _cograph of a function_ is a special case of the notion of [[cograph of a functor]].


#Discussion#

[[Eric]]: I think it might be neat to take the opportunity here to relate **graph of a function** more explicitly to other things here on the nLab. As I read this, I thought of a category with one object (monoid in Set?) and one morphism

$$\bullet\righttoleftarrow f.$$

Then a graph (or is it cograph?) is a [[category of elements]] of this category.

Then you could maybe talk more generally about **graph of a morhism**. Or something...

_Toby_:  The above graph of a function definitely generalises to the graph of a morphism; I didn\'t say anything about it, because I didn\'t want to have to think about what categories it\'s possible to do this in.  (Probably a [[regular category]] or something like that.)

I don\'t understand what you\'re saying above.  You seem to introduce the [[trivial category]] and then ask for its category of elements.  Categories don\'t have categories of elements, objects of categories do; but this category has just one object, so I\'ll use that.  But the category of elements of that one object is also trivial.  The real problem is that nothing in this category has to do with any function $f: X \to Y$; all you\'ve done is label an abstract morphism with the same name '$f$'.  Can you try to explain again what you mean?

[[Eric]]: What I had in mind was to think of that one object $\bullet$ as a set (but didn't want to pin it down too much so I didn't say "set"). The morphism $f$ is a nontrivial [[endomorphism]].

When we [[category of elements|explode]] that simple category, we get one object (which will be a node of the graph) for each element in $\bullet$. We also get one morphism for any two elements $a$ and $b$ for which $f:a\to b$.

As usual, it is just an idea and I was hoping that if it made any sense at all we could clean it up and include it in the main text.

For example, let $\bullet = \{x,y,z\}$ and $f:\bullet\to\bullet$ with

$$\begin{aligned}
f(x) &= y \\
f(y) &= z \\
f(z) &= x.
\end{aligned}$$

When we "explode" this simple category 

$$Explode\left(\bullet\righttoleftarrow f\right)$$

we get a graph with three nodes and three directed edges forming a ring.

I guess, to be a little more explicit, I can call that [[concrete category]] $C$, i.e.

$$C = \bullet\righttoleftarrow f$$

_and_ we have a functor $F:C\to Set$. Then $F(\bullet)$ is really a set and $F(f)$ is really a function.

Then 

$$Explode(C) = Elem(F,C).$$

This [[category of elements]] seems to warrant being associated with the **graph of a function** $f$. Furthermore, this allows us to consider the **graph of an endomorphism**. But then, I could be confused.

_Toby_:  Ah, I understand now!  $C$ is equipped with a functor to $Set$ (or potentially to something else); I should have guessed this, since you\'d linked to [[category of elements]], and I interpreted the phrase [[generalised element|differently]].  Also, $f$ is not an identity morphism of $C$; instead, $C$ is freely generated by an endomorphism $f$, so its morphisms are in fact $f^n$ for $n = 0, 1, 2, \ldots$.  The a functor from $C$ to $Set$ is a set equipped with an endofunction, and a functor from $C$ to $D$ is an object of $D$ equipped with an endomorphism.

OK, so if we explode this functor, then an object of the explosion is an element $x$ of $F(\bullet)$, and a morphism $x \to x'$ is a natural number $n$ such that $F(f)^n(x) = x'$.  You seem to have wanted a morphism $x \to x'$ to exist only if $F(f)(x) = x'$, but this won\'t work, since then you won\'t be able to compose morphisms $x \to x' \to x''$.  My way, you can compose them, by adding the $n$s.

Then I get this result:  If we take this function $F(f): F(\bullet) \to F(\bullet)$, treat a function as a special kind of relation, convert between relations and directed loop graphs (see today\'s [[graph]] for the definition), treat a directed loop graph as a special directed pseudograph aka [[digraph]], and form the [[quiver]] of that digraph, then the result is the same as the above category of elements!

[[Eric]]: Neat! :) You are right. My category $\bullet\righttoleftarrow f$ wasn't even a category. Oops! But it generates a category the way you outlined. However, an endofunction $f:X\to X$ does generate a [[digraph]] in the obvious way, i.e. each element of $X$ is a node and we have a directed edge $x\to x'$ if $f(x) = x'$. This digraph generates a [[quiver]] and this quiver corresponds to the [[category of elements]] obtained from the category generated by the endofunction. Phew! :)

Let me recap to make sure I got it...

Given an endofunction $f:X\to X$, we can do two things with it:

1. Construct a digraph $G_f$
1. Construct a category $C_f$ with one object $X$ and morphisms being powers of $f$.

The quiver $Q(G_f)$ and the category of elements $Explode(C_f)$ coincide. That is cool, unfortunately, I don't know if it is relevant to **graph of a function**.

Doh! Now, I think I know what I did wrong. In trying to make things simpler by considering just one object, I made them more complicated.

What we really want is a concrete category $X\stackrel{f}{\to} Y$ with TWO objects $X$ and $Y$ and one morphism $f:X\to Y$. Now, composition does not come into the picture.

Now, _I think_, 

$$Explode(X\stackrel{f}{\to} Y)$$

is the **graph of a morphism** $f$. 

If there is any truth to that, then this can be applied to any morphism of any concrete (or regular?) category.

PS: By the way, I think I'm confused and should probably remove this discussion unless you think there is anything worth extracting from it.

_Toby_:  I was going to say something about what if $f: X \to Y$ without $X = Y$, but I also fell into the trap of trying the simpler one first.  Yes, let\'s take the abstract general category $\mathbf{2}$ (the [[interval category]]) and make it a concrete category with $F: \mathbf{2} \to Set$ representing an arbitrary arrow in $Set$.  Then the category of elements $El_F(\mathbf{2})$ has the disjoint union $X + Y$ as its set of objects, with the only nonidentity morphisms being arrows $a \to b$ such that $f(a) = b$.  Then this looks like a (simple) directed graph on the vertex set $X + Y$; if we mod $X + Y$ out by the equivalence relation generated by the adjacency relation of this graph, then we get the cograph in the sense of Lawvere.  To get the graph as a subset of $X \times Y$, we can think of $X \times Y$ as a subset of $(X + Y)^2 = X^2 + 2 X \times Y + Y^2$, note that every (non-loop) edge of the directed graph above (which can be thought of as a subset of $(X + Y)^2$) belongs to the first $X \times Y$ summand, and restrict the target to get a subset of $X \times Y$, which is the graph of $f$.

[[Eric]]: I was thinking about adding the category theoretic version in your last comment as the main definition above. It is the one most suitable to the nLab I think.

_Toby_:  What do you mean, 'the one'? the one definition? or the one concept?  What you wrote above is *not* a definition of what most people call the 'graph' of a function, which is a subset of the cartesian product $X \times Y$.  It\'s an interesting concept, but I don\'t see why it\'s more suitable for the nLab than the subset of $X \times Y$, or the other ideas (the quotient set of $X + Y$ and the simple directed graph on $X + Y$, which your definition at least mentions).

[[Eric]]: Moved the definition back down here. Sorry. I thought I was just transcribing what you had written.

+-- {: .un_defn}
###### Definition

Consider a function $f:X\to Y$ to be the image of the [[interval category]] $\mathbf{2}$ of a functor $F:\mathbf{2}\to Set$ with 

$$\begin{aligned}
&f = F(\to),\\
&X = F(0),\\
&Y = F(1).
\end{aligned}$$

The **graph** of $f$ is the [[category of elements]] $El_F(\mathbf{2})$.

The graph of $f$ has the [[disjoint union]] $X + Y$ as its set of objects, with the only nonidentity morphisms being arrows $a \to b$ such that $f(a) = b$.  This is a (simple) directed [[graph]] on the vertex set $X + Y$.

If we mod $X + Y$ out by the [[equivalence relation]] generated by the adjacency relation of this graph, then we get the **cograph** in the sense of Lawvere as a [[quotient set]].
=--

I'm probably making a combination of mistakes. I _thought_ you were suggesting this category of elements was the same thing as the graph of a function. My time allotted to thinking about this is 15 second spurts every 3-4 hours, so I'm bound to get confused.

Maybe what I'm after is a nice arrow theoretic definition of **graph of a morphism** and then a **graph of a function** becomes a special case. It's obviously not a requirement, but I tend to try to rethink standard definitions here on the nLab arrow theoretically.

What I saw in the original version of this page is something that would be at home in a standard text and was hoping to nLab-ify it. Probably misguided.

_Toby_:  It was all correct except for the claim that what it defines is the graph of the function!

Part of the problem is that the graph of a function isn\'t really a concept that we can try to turn around and see from another, more categorial, point of view.  That\'s because it is itself just a way of looking at the function itself!  Compare how they do it in material set theory: the function *is* its graph, literally.  When I started this page, I didn\'t think that there was anything very $n$-categorial to do in it; it was just something obvious to write in contrast to [[graph]].

But now that you\'ve brought up this bit with the category of elements, I do think that there is a place for it.  I\'ll try to rewrite the page to make things clearer: that a function (or even relation) might be viewed as being given by a 'graph' in various senses, which we are describing here.  Then we can mention all of them.

[[Urs Schreiber]]: have only had a chance to look at your conversation here now. I think that the notion of both graph as well as cograph of a function are usefully regarded as special cases of [[graph of a functor]] and [[cograph of a functor]]. I have created these entries and added more details there, and I have now also expanded the discussion above, incorporating your discussion here as well as indicating the way this fits into the more general picture.

_Toby_:  Thanks, Urs, that\'s great!


[[!redirects graph of a relation]]
[[!redirects cograph]]
[[!redirects cograph of a function]]
