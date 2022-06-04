
#Contents#
* table of contents
{:toc}

## Idea

The _graph of a function_ $f : X \to Y$ is the subset that $f$ "carves out" of the [[cartesian product]] $X \times Y$.



## Definition 

### Graph of a function 

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

### Graph of a binary relation 

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


#### Relation to graph theory 

The graph of a binary relation from $X$ to $X$ is related to the notion of [[graph]] from [[graph theory]]; more precisely, such relations correspond to directed loop graphs (in the sense defined at [[graph]]) with vertex set $X$, and either can be defined as a subset of $X^2$.  In a similar way, [[spans]] from $X$ to $X$ correspond to [[digraph|directed pseudographs]] with vertex set $X$.

For the case of a relation from $X$ to $Y$ without $X = Y$, see under the cograph below.


### Graph of an $n$-ary relation 

The __graph__ of a [[relation]] of arbitrary arity is similarly a subset of an arbitrary [[cartesian product]]; see [[relation theory]] for more on this.


### Cograph of a function 
  {#cograph}

[[Bill Lawvere]] has also considered the __cograph__ of a function, which is dually a [[quotient set]] of the [[disjoint union]] $X \uplus Y$; $a$ is identified with $b$ if $f(a) = b$ (and additional identifications may follow).  However it may make more sense to define the cograph to be a quotient [[poset]] of (the discrete poset) $X \uplus Y$; we declare $a \lt b$ if $f(a) = b$ (and *no* additional relationships follow).  By regarding again a set as a [[0-category]], the latter notion of cograph is a special case of the notion of [[cograph of a functor]], as follows:

A function $f : X \to Y$ determines a [[functor]] $\bar f : I \to Set$ from the [[interval category]] $I = \mathbf{2} = \{a \to b\}$ to [[Set]] by setting $\bar f(a) = X$, $\bar f(b) = Y$ and $\bar f(a \to b) = f$.

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

which is computed by the strict [[pullback]]

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

The cograph of $f$ in the sense of Lawvere is the set of [[connected component]]s of this category, i.e. $\pi_0(cograph(f))$.


#### Relation to graph theory 

The notion of cograph of a function may be even more related to the sense of [[graph]] in graph theory; although the identifications are not done there, the cograph draws a picture in which any relation (or [[multispan]]) of any arity becomes a directed graph (or directed multigraph) whose vertex set is the disjoint union of the relation\'s domains.  When the vertex set is broken up into a disjoint union in this way, graph theorists study this as _multipartite graphs_; in particular, directed bipartite graphs with vertex set broken up as $X + Y$ correspond precisely to binary relations from $X$ to $Y$.


## Generalization 

The notion of _graph of a function_ is a special case of the notion [[graph of a functor]] obtained for functors between [[0-category|0-categories]].

Accordingly, the notion of _cograph of a function_ is a special case of the notion of [[cograph of a functor]].

## Related concepts

* [[graph morphism]]





[[!redirects graph of a relation]]
[[!redirects cograph of a function]]
[[!redirects cograph]]
[[!redirects Cograph]]