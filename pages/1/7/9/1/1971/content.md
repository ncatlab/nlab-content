##Idea##

A symmetric function is more-or-less a [[polynomial]] that is invariant under permutation of the variables.  This is only strictly correct if the number of variables is finite; the only symmetric *polynomials* in infinitely many variables are the constants.  To fix this, we allow infinitely many terms, as long as the *degree* is finite.  By default, the number of variables is countably infinite, indexed by [[natural numbers]].

For example, there is a $1$-dimensional space of homogeneous symmetric functions of degree $1$, with basis

$$ x_1 + x_2 + \cdots = \sum_i x_i .$$

There is a $2$-dimensional space of homogeneous symmetric functions of degree $2$, with basis

$$ x_1^2 + x_2^2 + \cdots = \sum_i x_i^2 $$

and 

$$ \sum_{i \lt j} x_i x_j .$$

(The homogeneous symmetric functions of degree $0$ are just the constants, as usual.)


##Definition##

Let $\Lambda_n$ be the [[ring]] consisting of polynomials in $n$ variables $x_1, \dots, x_n$ that are invariant under all permutations of the variables; these are the **symmetric functions in $n$ variables** or **symmetric polynomials** in $n$ variables.   There is an inclusion of rings

$$ \Lambda_n \hookrightarrow \Lambda_{n+1} ,$$

given by adding in new terms with the new variable to make the result symmetric.

Taking a suitable limit (or really [[colimit]]) of the rings $\Lambda_n$ as $n \to \infty$, we get $\Lambda_\infty$ or $\Lambda$, the ring of **symmetric functions in countably many variables**, or simply **symmetric functions** (sometimes also called **symmetric polynomials**, even though very few of them are really polynomials).

+-- {: .query}
[[David Corfield]]: Why does Hazewinkel in his description of the construction of $\Lambda$ on p. 129 of [this](http://arxiv.org/abs/0804.3888) use a graded projective limit construction in terms of projections of polynomial rings?

[[John Baez]]: Hmm, it sounds like you're telling me that there are 'projections' 

$$ \Lambda_{n+1} \to \Lambda_n $$

given by setting the $(n+1)$st variable to zero, and that Hazewinkel defines $\Lambda$ to be the limit (= projective limit) 

$$ \cdots \to \Lambda_2 \to \Lambda_1 \to \Lambda_0 $$

rather than the colimit

$$ \Lambda_0 \to \Lambda_1 \to \Lambda_2 \to \cdots $$

Right now I don't understand the difference between these two constructions well enough to tell which one is 'right'.
Can someone explain the difference?  Presumably there's more stuff in the limit than the colimit.

[[Mike Shulman]]: I think the difference is that the limit contains "polynomials" with infinitely many terms, and the colimit doesn't.  That's often the way of these things.

Actually, on second glance, I don't understand the description of the maps in the colimit system; are you sure they actually exist?  What exactly does it mean to "add in new terms with the new variable to make the result symmetric"?

[[David Corfield]]: The two constructions are explained very well in section 2.1 of the [Wikipedia article](http://en.wikipedia.org/wiki/Ring_of_symmetric_functions).

[[Mike Shulman]]: Thanks!  Here's what I get from the Wikipedia article: the projections are easy to define.  They are surjective and turn out to have sections (as ring homomorphisms).  The ring of symmetric functions can be defined either as the colimit of the sections, or as the the limit of the projections _in the category of graded rings_.  The limit in the category of all rings would contain too much stuff.
=--

The definition depends on the [[ground field|ground]] [[field]] (or [[commutative ring]] or [[rig]]) $k$, so we may write $\Lambda(k)$ to be precise.


##Properties##

Symmetric functions play a fundamental role throughout [[representation theory]], [[combinatorics]] and [[algebraic topology]].  $\Lambda$ is the free $\lambda$-[[lambda-ring|ring]] on one generator (a coincidence of notation that has not been ignored). It is also the [[Grothendieck ring]] of the [[free object|free]] [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] on one generator.  There are various bases of $\Lambda$ whose elements are in natural one-to-one correspondence with [[Young diagram|Young diagrams]].  

We may also obtain $\Lambda(\mathbb{C})$ by taking the [[Grothendieck group]] of the symmetric monoidal abelian category of $\mathbb{C}$-linear [[species]].  This category is defined to be the functor category

$$ [\mathbb{P}, Fin Vect_{\mathbb{C}}] $$

where $\mathbb{P}$ is the groupoid of [[finite sets]] and bijections, and $\FinVect_{\mathbb{C}}$ is the category of finite-dimensional complex vector spaces and linear maps.  This becomes a symmetric monoidal category thanks to [[Day convolution]].  For more on this, see [[Schur functor]].

+-- {: .query}
[[John Baez]]: Do we need the complex numbers in the previous paragraph, or will any field do equally well?  Maybe just any field of characteristic zero?  I really want to know!  Another way to put my question: take the category of representations of the permutation group $S_n$ in finite-dimensional vector spaces over the field $k$.  Take the Grothendieck group of this.  Does this depend on $k$?  Does something weird happen when $n$ is divisible by $char k$? 

_Toby_:  Since this is all algebra, any algebraically complete field of characteristic zero must work.  Do you know a reference for the proof?; can we see what it depends on?

_[[John Baez]]_: What I really care about is non-algebraically closed fields of characteristic nonzero.  The proof is lurking in any book on representations of the symmetric group.   It consists of two steps.  First, the $n$-box Young diagrams in turn correspond to the degree-$n$ symmetric polynomials in an obvious way.  Second, every rep of $S_n$ is completely reducible, and the irreducible ones are described by $n$-box Young diagrams.  The second part is still true over $\mathbb{Q}$, but I don't know if it's true over fields of nonzero characteristic, like finite fields.  I think it's _not_, since Brauer is famous for studying 'modular representations of symmetric groups', meaning reps over finite fields.  But I'd like to know how the story changes, if it does.  

_Toby_:  H\'m, I actually used to know something about this.  I have a vague idea that everything should work the same as in characteristic zero as long as the characteristic does not divide the order of the group.  So in particular, representations of $S_n$ over $\mathbb{F}_p$ should act just like representations over $\mathbb{C}$ whenever $p \gt n$.  Serre\'s 1971 book _Repr&#233;sentations lin&#233;aires des groupes finis_ spells this out; I forget how much it covers of the case when $p \leq n$, but it should clarify whether what I\'ve just said is correct.

_John_: Right, Maschke's theorem says that all reps of a group of order $k$ are completely reducible if we're working over $\mathbb{F}_p$ and $p$ does not divide $k$. The point is that we do a lot of stuff by 'averaging with respect to the group action', and to normalize Haar measure on a group of order $k$ we need to divide by $k$.  But presumably we'll get in trouble with the group $S_n$ whenever $p$ divides $n!$.  And I want to know precisely what happens then.

_Toby_:  I\'m at the UCR library right now, and Serre\'s book is checked out, so I can\'t tell you whether it\'s in there or not.  But it might be.


_Gon&#231;alo Marques_: There\'s an exercise at the end of section 6.1 of Serre\'s book (page 64 of the french edition) that says that if $k$ is a field of characteristic $p \gt 0$ then the group algebra of the group $G$ is semisimple iff $p$ doesn\'t divide the order of $G$

=--

[[!redirects symmetric functions]]
[[!redirects symmetric polynomial]]
[[!redirects symmetric polynomials]]