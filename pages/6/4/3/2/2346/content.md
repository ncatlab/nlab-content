+-- {: .standout}

[[Eric]]: This page could use some work. The **Definition** was appended as a result of the **Discussion** below and disturbed the flow of ideas a little bit. 

=--

#Idea#

The __graph__ of a [[function]] $f: X \to Y$ is a [[subset]] of the [[cartesian product]] $X \times Y$; $(a,b)$ belongs to the graph of $f$ if and only if $f(a) = b$.

It\'s easy to identify the properties of those subsets of $X \times Y$ that are the graphs of functions, and $f = g$ if they have the same graph (given $X$ and $Y$).  Consequently, it is common, especially (but not only) in material [[set theory]], to *define* a function from $X$ to $Y$ as such a subset, that is to identify a function with its graph.  On the other hand, from a more categorial foundation, it\'s common to define a [[subset]] to be a certain kind of function!

More generally, we can say that the __graph__ of a [[binary relation]] from $X$ to $Y$ is a subset of $X \times Y$; $(a,b)$ belongs to the graph if and only if $a$ is related to $b$.  The __graph__ of a [[relation]] of arbitrary arity is similarly a subset of an arbitrary [[cartesian product]]; see [[relation theory]] for more on this.  Note that *every* subset of $X \times Y$ defines a unique relation; this is the graph of a function if and only if the relation is both [[functional relation|functional]] and [[entire relation|entire]].


The graph of a binary relation from $X$ to $X$ is related to the notion of [[graph]] from [[graph theory]]; more precisely, such relations correspond to directed loop graphs (in the sense defined at [[graph]]) with vertex set $X$, and either can be defined as a subset of $X^2$.  In a similar way, [[spans]] from $X$ to $X$ correspond to [[digraph|directed pseudographs]] with vertex set $X$.

[[Bill Lawvere]] has also considered the __cograph__ of a function, which is dually a [[quotient set]] of the [[disjoint union]] $X \uplus Y$; $a$ is identified with $b$ if $f(a) = b$ (and additional identifications may follow).  This may be even more related to the sense of [[graph]] in graph theory; although the identifications are not done there, the cograph draws a picture in wich any relation (or [[multispan]]) of any arity becomes a directed loop graph (or directed pseudograph) whose vertex set is the disjoint union of the relation\'s domains.

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

+-- {: .query}
I really don\'t like this.  Discussion below.  ---Toby
=--

_Toby_:  What do you mean, 'the one'? the one definition? or the one concept?  What you wrote above is *not* a definition of what most people call the 'graph' of a function, which is a subset of the cartesian product $X \times Y$.  It\'s an interesting concept, but I don\'t see why it\'s more suitable for the nLab than the subset of $X \times Y$, or the other ideas (the quotient set of $X + Y$ and the simple directed graph on $X + Y$, which your definition at least mentions).

[[Eric]]: Moved the definition back down here. Sorry. I thought I was just transcribing what you had written.

***

#Definition#

Consider a function $f:X\to Y$ to be the image of the [[interval category]] $\mathbf{2}$ of a functor $F:\mathbf{2}\to Set$ with 

$$\begin{aligned}
&f = F(\to),\\
&X = F(0),\\
&Y = F(1).
\end{aligned}$$

The **graph** of $f$ is the [[category of elements]] $El_F(\mathbf{2})$.

The graph of $f$ has the [[disjoint union]] $X + Y$ as its set of objects, with the only nonidentity morphisms being arrows $a \to b$ such that $f(a) = b$.  This is a (simple) directed [[graph]] on the vertex set $X + Y$.

If we mod $X + Y$ out by the [[equivalence relation]] generated by the adjacency relation of this graph, then we get the **cograph** in the sense of Lawvere as a [[quotient set]].

***

I'm probably making a combination of mistakes. I _thought_ you were suggesting this category of elements was the same thing as the graph of a function. My time allotted to thinking about this is 15 second spurts every 3-4 hours, so I'm bound to get confused.

Maybe what I'm after is a nice arrow theoretic definition of **graph of a morphism** and then a **graph of a function** becomes a special case. It's obviously not a requirement, but I tend to try to rethink standard definitions here on the nLab arrow theoretically.

What I saw in the original version of this page is something that would be at home in a standard text and was hoping to nLab-ify it. Probably misguided.

[[!redirects graph of a relation]]
[[!redirects cograph]]