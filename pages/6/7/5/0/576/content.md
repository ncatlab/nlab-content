
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _$\dagger$-compact category_ is a category which is a 

* [[compact closed category]] 

and a

* [[symmetric monoidal †-category]] 

in a compatible way.  So, notably, it is a [[monoidal category]] in which

* every object has a dual;

* every morphism has an $\dagger$-adjoint.



## Definition

A category $C$ that is equipped with the structure of a [[symmetric monoidal †-category]] and is [[compact closed category|compact closed]] is **$\dagger$-compact** if the dagger-operation takes [[units]] of [[dual objects]] to [[counits]] in that for every object $A$ of $C$ we have

$$
  \array{
    && A \otimes A^*
    \\
    & {}^{\epsilon_A^\dagger}\nearrow
    \\
    I && \downarrow^{\mathrlap{\sigma_{A \times A^*}}}
    \\
    & {}_{\eta_A}\searrow
    \\
    && A^* \otimes A
  }
  \,.
$$


## Examples
 {#Examples}

\begin{example}
**(finite-dimensional Hilbert spaces)**
\linebreak
The category of [[Hilbert spaces]] (over the [[complex numbers]]) with [[finite number|finite]] [[dimension]] is a standard example of a $\dagger$-compact category. This example is [[completeness theorem|complete]] for [[equation]]s in the language of $\dagger$-compact categories; see [Selinger 2012](#Selinger2012).

The finite parts of [[quantum mechanics]] ([[quantum information theory]] and [[quantum computation]]) are naturally formulated as the theory of $\dagger$-compact categories. For more on this see at _[[finite quantum mechanics in terms of †-compact categories]]_.
\end{example}

\begin{example}
**(spans)**
\linebreak
For $C$ a category with [[finite limits]]  the category $Span_1(C)$ whose morphisms are [[span|spans]] in $C$ is $\dagger$-compact.  The $\dagger$ operation is that of relabeling the legs of a span as source and target.  The tensor product is defined using the cartesian product in $C$.   Every object $X$ is dual to itself with the unit and counit given by the span
$ I \stackrel{!}{\leftarrow} X \stackrel{Id \times Id}{\to} X \times X$.
See [Baez 2007](#Baez07).
\end{example}


## Properties

### Relation to self-duality

If each [[object]] $X$ of a [[compact closed category]] is equipped with a [[self-duality]] structure $X \simeq X^\ast$, then sending morphisms to their [[dual morphisms]] but with these identifications pre- and postcomposed

$$
  (-)^\dagger \;\colon\; 
  (X \stackrel{f}{\longrightarrow} Y)
  \mapsto
  (Y \stackrel{\simeq}{\to} Y^\ast \stackrel{f^\ast}{\longrightarrow} X^\ast \stackrel{\simeq}{\to} X)
$$

constitutes a dagger-compact category structure.

See for instance ([Selinger, remark 4.5](#Selinger)).

Applied for instance to the category of (complex) finite-dimensional [[inner product spaces]] this dagger-operation sends [[matrices]] to their [[conjugate transpose matrix |(conjugate) transpose]]. 

A good example of a $\dagger$-compact category where most objects are *not* isomorphic to their duals is the category of continuous unitary representations of [[U(n)]] on finite-dimensional complex Hilbert spaces. 

## Related concepts

* [[bra-ket notation]]

* [[quantum information theory via dagger-compact categories]]

## References

The concept was introduced in 

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], _A categorical semantics of quantum protocols_, in _Proceedings of the 19th IEEE conference on Logic in Computer Science_ (LiCS'04), IEEE Computer Science Press, 2004. ([arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130))
 
with an expanded version in 

* {#AbramskyCoecke08} [[Samson Abramsky]], [[Bob Coecke]], *Categorical quantum mechanics*, in *[[Handbook of Quantum Logic and Quantum Structures]]*, Elsevier (2008) &lbrack;[arXiv:0808.1023](http://arxiv.org/abs/0808.1023), [ISBN:9780080931661](https://www.sciencedirect.com/book/9780444528698/)&rbrack; 

under the name "strongly compact" and used for [[finite quantum mechanics in terms of dagger-compact categories]].
The topic was taken up

* [[Peter Selinger]], _Dagger compact closed categories and completely positive maps_, in _Proceedings of the 3rd International Workshop on Quantum Programming Languages_ (QPL 2005), ENTCS 170 (2007), 139--163. 
([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))

where the alternative terminology "dagger-compact" was proposed, and used for the abstract characterization of [[quantum operations]] ([[completely positive maps]] on [[Bloch regions]] of [[density matrices]]).

The examples induced from [[self-duality]]-structure are discussed abstractly in 

* {#Selinger} [[Peter Selinger]], _Autonomous categories in which $A \cong A^\ast$_, talk at QPL 2010 ([[SelingerSelfDual.pdf:file]])

That finite-dimensional Hilbert spaces are "complete for dagger-compactness" is shown in

* {#Selinger2012} [[Peter Selinger]] (2012), _Finite dimensional Hilbert spaces are complete for dagger compact closed categories_, ([arXiv:1207.6972](http://arxiv.org/abs/1207.6972)).
   

The example of [[spans]]:

* {#Baez07} [[John Baez]], _Spans in quantum theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))


[[!redirects dagger compact category]]
[[!redirects dagger compact categories]]
[[!redirects dagger-compact category]]
[[!redirects dagger-compact categories]]
[[!redirects † compact category]]
[[!redirects † compact categories]]
[[!redirects †-compact category]]
[[!redirects †-compact categories]]

[[!redirects dagger compact closed category]]
[[!redirects dagger compact closed categories]]
[[!redirects dagger-compact closed category]]
[[!redirects dagger-compact closed categories]]
[[!redirects † compact closed category]]
[[!redirects † compact closed categories]]
[[!redirects †-compact closed category]]
[[!redirects †-compact closed categories]]