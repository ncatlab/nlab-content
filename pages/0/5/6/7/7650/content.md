
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a ([[Hausdorff topological space|Hausdorff]]) [[compact topological group]] $G$, the _Milnor construction_ of the [[universal principal bundle]] for $G$ (also known as _Milnor's join construction_) constructs the [[join of topological spaces|join]] of infinitely many copies of $ G $, i.e., the colimit of [[join of topological spaces|joins]]

$$
  (E G)_{Milnor} 
  \;\coloneqq\; 
  \underset
    {\underset{n \in \mathbb{N}}{\longrightarrow}}
    {\lim} 
  \;
  \big( 
   \underset
     {n \; factors}
     {\underbrace{G \ast G \ast \ldots \ast G}}
  \big)
$$

and canonically equips it with a continuous and [[free action|free]] right [[group action]] of $ G $ that yields the structure of a [[G-CW-complex]]. Consequently, the natural [[quotient space]] projection $(E G)_{Milnor} \to (E G)_{Milnor}/G $ is a model for the [[universal principal bundle]] $ E G \to B G $ of locally trivial principal $ G $-bundles over [[paracompact Hausdorff spaces]], or equivalently, of [[numerable bundle]] $G$-[[principal bundles]] over all [[Hausdorff topological spaces]].

There is a generalisation of Milnor's construction that works for [[topological groupoids]], and reduces to the above case when the groupoid is $\mathbf{B}G$, the delooping of the group $G$.


## Related entries

* [[classifying space]]

* [[universal principal bundle]]

* [[bar construction]]

## References

* [[John Milnor]], *Construction of Universal Bundles I*, Ann. of Math. __63__ 2 (1956) 272-284 &lbrack;[jstor:1969609](http://www.jstor.org/stable/1969609)&rbrack;

* [[John Milnor]], _Construction of Universal Bundles II_, Ann. of Math. __63__ 3 (1956) 430-436 &lbrack;[jstor:1970012](http://www.jstor.org/stable/1970012)&rbrack;

  reprinted in: *Collected Works of John Milnor* &lbrack;[gBooks](http://books.google.com/books?id=WyZeeEn8VFwC)&rbrack;

* [[John Milnor]], [[James Stasheff]], _Characteristic Classes_, Princeton University Press.

* [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin Schottenloher]], _The Milnor Construction: Homotopy Classification of Principal Bundles_, [doi](http://dx.doi.org/10.1007/978-3-540-74956-1_8), in:
Basic Bundle Theory and K-Cohomology Invariants, Lecture Notes in Physics, Vol. 726 (2008) 75-81.

[[!redirects Milnor's construction]]

[[!redirects Milnor's classifying space]]

[[!redirects Milnor classifying space]]
[[!redirects Milnor classifying spaces]]
