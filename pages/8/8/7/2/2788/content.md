>This page is an informal/speculative discussion of an alternative (yet hopefully equivalent) definition of [[functor]]. It first appeared as a discussion at [[functor]] itself, but was subsequently moved here.

##Definition##
Given categories $A$, $B$ and inclusion maps $i_A:A\to A\sqcup B$, $i_B:B\to A\sqcup B$, a **functor** is a map $F:A\to B$ that assigns morphisms $\alpha_x:i_A(x)\to i_B\circ F(x)$ and $\alpha_y:i_A(y)\to i_B\circ F(y)$ for any morphism $f:x\to y$ in $A$ such that the following diagram commutes:
$$ 
  \array{ 
    i_A(x)
    & 
    \stackrel{i_A(f)}{\to} 
    & 
    i_A(y) 
    \\ 
    \mathllap{\scriptsize{\alpha_x}}\downarrow 
    && 
    \downarrow\mathrlap{\scriptsize{\alpha_y}} 
    \\ i_B\circ F(x)
    & 
    \stackrel{i_B\circ F(f)}{\to} & i_B\circ F(y) 
  }
$$

<img src="http://ncatlab.org/nlab/files/alt_functor.jpg" width = "250"/>

***

[[nlab:Todd Trimble|Todd]]: If $A \sqcup B$ means the disjoint union of $A$ and $B$, then there are no morphisms of the form $i_A(x) \to i_B(F(x))$. 

[[Eric]]: Hi Todd. I saw your comment after I added the figure above. I am probably not expressing myself clearly. I want to get $Obj(A)$ and $Obj(B)$ into the same category while preserving all morphisms and then ADD components $\alpha_x$ and $\alpha_y$. Is that kind of thing allowed?

I think the picture expresses what I'm trying to do, but maybe I'm converting that into the wrong formulas.

[[Eric]]: The idea is that by requiring every such square to commute, you automatically get $F(g\circ f) = F(g)\circ F(f)$ and $F(Id_x) = Id_{F(x)}$. Or so I think...

[[Eric]]: Not to mention, this _looks_ more like a natural transformation, so a pattern is more apparent. 

[[Todd Trimble|Todd]]: What I was saying is that wherever these $\alpha_x$ are supposed to live, it's can't be in $A \sqcup B$, because in $A \sqcup B$, there simply are no morphisms of that form. 

Your picture suggests that you have in mind some category $C$ into which $A$ and $B$ embed; it can't be $A \sqcup B$ since your $\alpha_x$ simply don't exist there. But it's some $C$ in which such morphisms $\alpha_x$ exist, let's say. Then it looks like your notion of functor involves the following things: 

* Embeddings (full embeddings?) $i_A: A \to C$, $i_B: B \to C$ into some category $C$. 

* A rule which assigns to each object $x$ of $A$ an object $F(x)$ of $B$, and to each morphism $f: x \to y$ of $A$ a morphism $F(f): F(x) \to F(y)$ of $B$. In other words, a map $F: A \to B$ between the underlying directed graphs of $A$ and $B$. 

* A rule which assigns to each object $x$ of $A$ a morphism $\alpha_x: i_A(x) \to i_B(F(x)$, making that square commute. 

Okay, so far these conditions don't ensure functoriality: that $F(g \circ f) = F(g) \circ F(f)$ and $F(1_x) = 1_{F(x)}$. You're going to have to add more conditions to make that inference. For example, suppose $C$ has just one morphism from each object $i_A(a)$ to each object of $i_B(b)$. Then commutativity of those squares is automatic, for any directed graph morphism $F: A \to B$. Insofar as not all graph morphisms are functorial, you can't infer functoriality. 

You could ask that all the $\alpha_x$ be isomorphisms. Then commutativity plus that condition would give functoriality, and your concept amounts to that of ordinary functor $F$ together with an ordinary natural isomorphism $i_A \overset{\sim}{\to} i_B \circ F$. 

But the trouble with all this is that I have no idea what $C$ is supposed to be! It can't be $A \sqcup B$. Would it be something constructed in terms of $A$ and $B$ (and if so, what)? If it's just _any_ old category into which $A$ and $B$ embed and for which such isos $\alpha_x$ exist (and compatible with the $F(f)$ via commutative diagrams), then I have problems with that too. 

[[Eric]]; Hi Todd. I think I'm confused because with the standard definition of functor $F:A\to B$ no one ever complains about writing $F(x)\in B$, so in a way, isn't $F$ an _arrow_ from $x\in A$ to $F(x)\in B$? We also write $F(f)\in B$, which makes me think $F$ is a bunch of 1-arrows and 2-arrows. I mean, doesn't the picture make sense? Why is it so hard to convert the picture to a mathematical statement?

[[Urs Schreiber]]: concerning the nature of $C$: as I suggested before, it does make sense to take this to be the [[cograph of a functor]]. And indeed, in some situations it is useful to _define_ the notion of functor in terms of the notion of cograph. In [[Higher Topos Theory]] the notion of [[adjoint (infinity,1)-functor]] is defined entirely in terms of cographs of functors.


##Discussion##

[[Eric]]: Motivated by some discussion over at [[natural transformation]], I was wondering if the following alternative definition of functor holds water:

>##Definition##
>Given categories $A$, $B$, a **functor** is a map $F:A\to B$ that assigns maps $\alpha_x:x\to F(x)$ and $\alpha_y:y\to F(y)$ for any morphism $f:x\to y$ in $A$ such that the following diagram commutes:
$$ 
  \array{ 
    x
    & 
    \stackrel{f}{\to} 
    & 
    y 
    \\ 
    \mathllap{\scriptsize{\alpha_x}}\downarrow 
    && 
    \downarrow\mathrlap{\scriptsize{\alpha_y}} 
    \\ F(x) 
    & 
    \stackrel{F(f)}{\to} & F(y) 
  }
$$

If so, it has a certain beauty that appeals to me. Thanks!

Urs: that diagram seems to be meaningful only if $A = B$, right? In that case, this is a functor $F : A \to A$ together with a natural transformation from the identity functor on $A$ into $F$.

[[Eric]]: Yeah. It needs some work. Of course I don't want $A=B$, but I would like to be able to introduce morphisms from $A$ to $B$. Could I form some kind of category union or something? The picture is kind of neat. Each diagram in $A$ "hovers" above a diagram in $B$. If it can be ironed out, it might be an efficient definition.

Urs: now you are looking for the notion [[cograph of a functor]] (you should make us write out more details at that entry!)

[[Eric]]: **Gulp!** Ok. But is there a term for the (small) category $C = A\cup B$ where $C_0 = A_0\cup B_0$ and $C_1 = A_1\cup B_1$?

_Toby_:  You could just call that the _union_ of the two categories.  But it\'s not really a meaningful concept unless you already have $A$ and $B$ as [[subcategory|subcategories]] of some ambient category $D$, or something like that.  To ask whether an element of $A_0$ matches an element an element of $B_0$ (and similarly for $A_1$ and $B_1$) is [[evil]].

Alternatively, you could take it as understood that the sets $A_0$ and $B_0$ are disjoint, (and similarly for $A_1$ and $B_1$).  Then you get the _disjiont union_ of the two categories, and that is an important concept; it is the [[coproduct]] in [[Cat]].  And that is one of the ingredients of the [[cograph of a functor]], so probably it\'s what you want.

[[Eric]]: It seems like maybe I am trying to work backwards, i.e. define a functor via a cograph.

[[Eric]]: Ok! I think I got it. Does this hold water?

***

##Definition##
Given categories $A$, $B$ and inclusion maps $i_A:A\to A\sqcup B$, $i_B:B\to A\sqcup B$, a **functor** is a map $F:A\to B$ that assigns morphisms $\alpha_x:i_A(x)\to i_B\circ F(x)$ and $\alpha_y:i_A(y)\to i_B\circ F(y)$ for any morphism $f:x\to y$ in $A$ such that the following diagram commutes:
$$ 
  \array{ 
    i_A(x)
    & 
    \stackrel{i_A(f)}{\to} 
    & 
    i_A(y) 
    \\ 
    \mathllap{\scriptsize{\alpha_x}}\downarrow 
    && 
    \downarrow\mathrlap{\scriptsize{\alpha_y}} 
    \\ i_B\circ F(x)
    & 
    \stackrel{i_B\circ F(f)}{\to} & i_B\circ F(y) 
  }
$$
It follows that $i_A$ and $i_B$ are functors.

Note that a map $F:A\to B$ is a functor if the map $\alpha:i_A\Rightarrow i_B\circ F$ is a natural transformation.

***

Urs: to be frank, I don't get it! Also: what is it you are really after? The concept of a functor is entirely non-mysterious, it seems. What are you dissatisfied with, with the standard definition?

[[Eric]]: I enjoyed fiddling with [[natural transformations]] recently. I hadn't thought about them much. The introduction of "components" was kind of interesting. I also liked that "sheet transformation", which I now think of as a some kind of 3-morphism. So I was wondering if we could introduce "components" to define functors (which I now think of as 2-morphisms). Then I wondered if we could continue a pattern downward all the way to (-2)-categories.

The _pattern_ natural transformation $\to$ functor $\to$ morphism is not 100% clear to me. Each individually "makes sense", but I'd like to see a clearer pattern how they're related.

Basically, I'm trying to understand

* (-2)-morphisms
* (-1)-morphisms
* 0-morphisms
* 1-morphisms (morphisms)
* 2-morphisms (functors?)
* 3-morphisms (natural transformations? sheet transformations?)
* Etc.

in some consistent way.

For example, with categories $A$ and $B$ we have a [[functor category]] $[A,B]$ which is related to (if not equal to) a 2-category. How about sets $A$ and $B$ thought of as 0-categories? We could form a "morphism category" $[A,B]$ that is related (if not equal to) a 1-category. Then I can imagine a "truth category" $[True,True]$ that is related (if not equal) to a 0-category. Etc etc. This is all pretty elementary stuff I'm sure.

In a nutshell, I'm not saying there is anything wrong the definitions there, but I'm trying to understand them in a different way if possible.

[[!redirects functor (discussion)]]