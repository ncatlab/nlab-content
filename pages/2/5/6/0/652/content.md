_Sharing graphs_ are another kind of [[string diagram]] which focuses on the syntax of a language.  Given a [BNF](http://en.wikipedia.org/wiki/Backus-Naur_form) description of a context-free grammar, we get a category whose objects are (roughly) lists of subterms and whose morphisms are rules for composing the subterms into terms.  

##Example: Untyped lambda calculus
Lambda calculus terms are recursively defined as follows:

:$t$ ::= $v$ | $t(t)$ | $\lambda v.t$

where $x$ is a countably infinite set of variables.  There are three equivalences on terms, $\alpha$ (for handling dummy variables), $\beta$ (substitution of terms), and $\eta$ (extensionality).  The corresponding category has 

* two generating types, V and T
* six function symbols

  * $\lambda:V^* \times T \to T.$  Lambda takes an antivariable and a term that may use the corresponding variable.
  * $\cap:1 \to V^* \times T.$  This turns an antivariable "x" introduced by lambda into the term "x".
  * $A:T \times T \to T.$ (Application) This takes $f$ and $x$ and produces $f(x)$.
  * $swap:T \times T \to T \times T$
  * $!:T \to 1$
  * $\Delta:T \to T \times T.$

* relations

  * The last three function symbols come with relations that make the category cartesian (and justify the use of $\times$ above).  Leaving off the last two would give linear lambda calculus.

  * $\beta-\eta: A \circ (\lambda \times 1_T) \circ (1_{V^*} \times P \times 1_T) \circ (\cap \times 1_{T^n} \times 1_T) \Leftrightarrow P \circ swap_{1_{T^n}, 1_T}$

    This is the categorical encoding of

    $(\lambda x.P)(y) \Leftrightarrow P[y/x]$

    where the free variables of the term P are $\{x, x_1, \ldots, x_n\}$.

The string diagrams corresponding to this category are called sharing graphs.

Peter Selinger said of this example:

"Sharing graphs" are extremely well-studied. See e.g.

$[1]$ [Stefano Guerrini, A general theory of sharing graphs (1997)](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.530)

There is a reduction strategy on sharing graphs that is provably the most efficient possible reduction strategy for lambda calculus; this goes back to the work of Levy and Lamping (both cited in the above paper).

Guerrini also gives an algebraic semantics of these sharing graphs, see section 7. I don't know whether it is related to your categorical view.

I also like the book by Peyton-Jones:

$[2]$ [Simon Peyton Jones, The Implementation of Functional Programming Languages (1987)](http://research.microsoft.com/en-us/um/people/simonpj/papers/slpj-book-1987/)

It shows how to use sharing graphs as the basis for a practical implementation of lazy programming languages. As far as I know, this is still state-of-the-art and is used in the implementation of Haskell. In keeping with the practical nature of the book, the sharing graphs
are represented in slightly different form (with syntactic variables rather than backpointers), but this is of course equivalent.

As for the categorical semantics, what you have in mind is a kind of abstract syntax with variable binding. To put this into perspective, the semantics of ordinary abstract syntax (i.e., without variable binding), is given by an object $A$ in a cartesian category, together with interpretations for each $n$-ary function symbol $f : A^n \to A.$ One can then inductively define the interpretation of terms, speak of the free such object, etc.

Things get slightly more complicated if one adds variable binding to this picture. This has also been studied, though perhaps not in the same form as you are proposing.  Perhaps the closest to your approach is

$[3]$ [Martin Hofmann, Semantical analysis of higher-order abstract syntax (1999)](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.46.4082)

Here one has $var : V \to T,$ $app : T \times T \to T,$ and $lam : (V \Rightarrow T) \to T$ (see top of p.9, with the obvious changes in notation). You will note the use of a function space $(V \Rightarrow T)$ in place of your cartesian product $V^* \times T.$

Another very similar paper is

$[4]$ [M.P.Fiore, G.D.Plotkin and D.Turi. Abstract syntax and variable binding (1999)](http://citeseerx.ist.psu.edu/showciting?cid=198434) (Also available [here](http://www.cl.cam.ac.uk/~mpf23/papers/Types/Types.html).)

Here, one has $var : V \to T,$ $app : T \times T \to T,$ and $lam : \delta T \to T$ (as contained e.g. in the commutative diagram on p.6). Again, $\delta T$ is something akin to the function space $(V \Rightarrow T),$ but is also isomorphic, in a suitable sense, to $(T \Rightarrow T),$ as far as I remember (this is important for substitution, see below).

A third, technically slightly different (but conceptually similar) approach to abstract syntax with variable binders is:

$[5]$ [Murdoch J. Gabbay, Andrew M. Pitts: A new approach to abstract syntax with variable binding (1999)](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.38.9383)

$[6]$ [Murdoch J. Gabbay, Andrew M. Pitts: A new approach to abstract syntax with variable binding (2002)](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.62.9845)

See especially the second-to-last line of $[6, p.356]$, and you immediately see the similarity. Their [A]T operation is akin to $(V \Rightarrow T)$ in $[3]$ and $\delta T$ in $[4]$.

It is fun to note that $[3-5]$ all appeared (independently) in the same conference in 1999. Semantics of variable binders was clearly a pressing problem that year.

I can comment briefly on the main difference between these works and what you are proposing. One thing that is important in syntax is substitution (of a term for a variable). In fact, in the usual abstract syntax (without binders), a term with n variables is represented as a morphism $A^n \to A.$ This is useful for substitution:
namely, if $f : A \times A^n \to A$ represents the term $t(x,y_1,...,y_n)$ and $g : A^n \to A$ represents $s(y_1,...,y_n),$ then $f \circ \langle g, id \rangle$ represents $t[s/x].$

In the presence of variables, a term with $n$ variables is represented as $1 \to V^{*n} \times T$ (in your notation). However, for reasons of substitution, one would still like this hom-set to be in 1-1 correspondence with $T^n \to T.$  Somehow this is what the papers $[3-6]$ manage to do, each in their own way.

I hope these references will be useful. It would be great if you had a more abstract monoidal framework of which the particular constructions in $[3-6]$ are concrete examples. I have always wondered about the precise connection between $[3-6],$ and whether there is a bigger picture.
