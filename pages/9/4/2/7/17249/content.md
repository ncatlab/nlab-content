
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[categories]] like [[sSet]], the [[internal hom]] $[X,Y]$ between two [[objects]] is often called the _function complex_ ("[[simplicial complex]] of [[functions]] from $X$ to $Y$).

## Definition

### General
 {#GeneralDefinition}

Suppose $\mathcal{C}$ is a [[category]] that admits small [[coproducts]].

Given [[simplicial objects]] $X,A\in \mathcal{C}^{\Delta^{op}}$,
their __function complex__ is the [[simplicial set]]

$$
  Hom_{\Delta}(X,A)
  \;\;
  \in
  \;\;
  sSet
$$

whose set of $n$-simplices is the set of maps
$\Delta^n\otimes A\to B$

$$
  \big(
    Hom_{\Delta}(X,A)  
  \big)_n
  \;\;
  =
  \;\;
  Hom_{\mathcal{C}}
  \big(
    \Delta^n \otimes X 
    ,\,
    A
  \big)
  \,,
$$

where $\otimes$ denotes the [[copowering]] of [[simplicial objects]] over [[simplicial sets]] given by

$$
  (S \otimes X)_n 
  \,=\,
  \coprod_{i \in S_n}
  X_n
  \,.
$$

### In simplicial sets

Specializing the general definition above to $\mathcal{C} = $ [[sSet]] itself, the required tensoring is just the [[product of simplicial sets]] and the function complex is the [[cartesian closed category|cartesian]] [[internal hom]] given by

$$
  X, A \,\in\, sSet
  \;\;\;\;
  \vdash
  \;\;\;\;
  \left\{
  \,
  \begin{array}{l}
    Maps(X,A)
    \;\; \in \;\; 
    sSet
    \\
    Maps(X,A)_\bullet
    \;\; = \;\; 
    Hom_{sSet}\big(
      \Delta[\bullet] \times X 
      ,\,
      A
    \big)
  \end{array}
  \right.
$$

(e.g. [Goerss & Jardine (2009), I.5](#GoerssJardine09))


## Properties
 {#Properties}

In [[SimplicialSets]], the [[evaluation map]] --- defined as the [[counit of an adjunction|counit]] of the $\big(X \times (-)\big)\dashv Maps(X,-)$-[[adjoint functor|adjunction]] ---  is given by

$$
  \begin{array}{cc}
    X \times Maps(X,A) 
    &\xrightarrow{\;\; ev^X_A  \;\;}&
    A
    \\
    \phantom{A}
    \\
    X_n 
      \times 
    \overset{
      \mathclap{
        Hom(X \times \Delta[n], A)
      }
    }{
      \overbrace{
        Maps(X,A)_n
      }
    }
    &\xrightarrow{\; \big(ev^X_A\big)_n  \;}&
    A_n
    \\
    \big(
      x 
      ,\, 
      f 
    \big)    
    &\mapsto&
    f(x, \iota_n)
    \,,
  \end{array}
$$

where 

$$
  \iota_n 
     \;\coloneqq\; 
  id_{\Delta[n]}
  \;\in\;
  Hom_{sSet}\big( \Delta[n],\, \Delta[n] \big)
  \;\simeq\;
  (\Delta[n])_n
$$

denotes the unique non-degenerate $n$-cell inside $\Delta[n]$.

(e.g. [Goerss & Jardine (2009), p. 20](#GoerssJardine09))



## Related concepts

* [[internal hom]]

* [[simplicial object]]

* [[simplicial set]]

## References

The original definition of a function complex in the generality stated above:

* [[Daniel M. Kan]], _On c.s.s. categories_, Boletín de la Sociedad Matemática Mexicana 2 (1957), 82–94.  [PDF](https://dmitripavlov.org/scans/kan-on-css-categories.pdf).

Textbook accounts:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section I.5 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack;


[[!redirects function complexes]]

