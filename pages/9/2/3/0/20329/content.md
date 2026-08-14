

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--




\tableofcontents

## Definition

+-- {: .num_defn #CentralProduct}
###### Definition


Given a [[pair]] of [[groups]], $G_1$ and $G_2$, and a joint [[subgroup]] 

\[
  \label{SubgroupInclusion}
  C \xhookrightarrow{\iota_i} Z(G_i)
  \,,\;\;
  i \in \{ 1,2 \}
\]

in each of their [[centers]], then the corresponding ("external") _central product_ is the [[quotient group]]

$$
  G_1 \circ G_2
  \;\coloneqq\;
  \big( 
    G_1 \times G_2
  \big)/_{diag} C
$$

of the [[direct product group]] $G_1 \times G_2$ by the [[diagonal]] subgroup $C \xhookrightarrow{(\iota_1, \iota_2)} G_1 \times G_2$.

=--

([Dummit & Foote 2003 p. 157](#DummitFoote2003))


+-- {: .num_remark #MaterialDefinition}
###### Remark
**([[structural set theory|structural]] over [[material set theory|material]] definition)**

Beware that texts such as [Gorenstein 1980 p. 29](#Gorenstein80) insists on stating the choices in Def. \ref{CentralProduct} as that of 

1. two separate subgroups $C_i \xhookrightarrow{\iota_i} Z(G_i)$ 

1. an [[isomorphism]] $C_1 \xrightarrow[\simeq]{\phi} C_2$ between them

and insists that the second groups as via $(-)^{-1}\circ \phi$

These clauses matter if one thinks of the subgroup inclusions as in [[material set theory]]. But we speak [[structural set theory]], which means that a [[subgroup]] inclusion as in (eq:SubgroupInclusion) is really a choice of _[[monomorphism|monic]] [[homomorphism]]_, and this choice already absorbs the choice of $\phi$ and or of $(-)^{-1}\circ \phi$.


=--

+-- {: .num_remark}
###### Remark
**(notation)**

Beware that there is no widely accepted convention for the notation of central products, and that most notational conventions suppress the choices of central subgroups involved.  The "$\circ$"-notation is popular in [[finite group]]-theory, while in [[Riemannian geometry]] people tend to use "$\cdot$" (see [[Sp(n).Sp(1)]]) or just plain juxtaposition, with no symbol for the central product at all.

=--


## Examples

### In Riemannian geometry and spin geometry

In [[Riemannian geometry]] and [[spin geometry]]:

\begin{example}
A [[Spin^c-group]] is a central product of a [[spin group]] with the [[circle group]].
\end{example}

\begin{example}
The groups [[Sp(n).Sp(1)]] and [[Spin(n).Spin(m)]] are central products of [[quaternionic unitary groups]] and of [[spin groups]], respectively.
\end{example}


## Related concepts

* [[direct product of groups]]

* [[semidirect product group]]

* [[free product of groups]]

* [[central extension of groups]]


## References

* {#Gorenstein80} Daniel Gorenstein; p. 29, Thm. 5.3 of: _Finite Groups_, New York (1980)

\begin{imagefromfile}
    "file_name": "Gorenstein-CentralProduct.png",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


* M. Aschbacher; (11.1) in: *Finite Group Theory*, Cambridge University Press (2012) &lbrack;[ISBN:9781139175319](https://www.cambridge.org/core/books/finite-group-theory/EB5CE66C17982A6B48855F2EDC2DA6F9), [doi:10.1017/CBO9781139175319](https://doi.org/10.1017/CBO9781139175319)&rbrack;

\begin{imagefromfile}
    "file_name": "Aschbacher-CentralProduct.png",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


* {#DummitFoote2003} David S. Dummit, Richard M. Foote; Ex. 12 on p. 157 of: *Abstract Algebra*, Wiley (2003) &lbrack;[ISBN:978-0-471-43334-7](https://www.wiley.com/en-us/Abstract+Algebra%2C+3rd+Edition-p-9780471433347), [pdf](https://rksmvv.ac.in/wp-content/uploads/2021/04/David_S_Dummit_Richard_M_Foote_Abstract_Algeb_230928_225848.pdf)&rbrack;

\begin{imagefromfile}
    "file_name": "DummitFoote-CentralProduct.png",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


See also:

* Wikipedia, _[Central product](https://en.wikipedia.org/wiki/Central_product)_

* GroupProps, _[External central product](https://groupprops.subwiki.org/wiki/External_central_product)_

For more references see at *[[Sp(n).Sp(1)]]*.

[[!redirects central products of groups]]

[[!redirects external central product of groups]]
[[!redirects external central products of groups]]

[[!redirects internal central product of groups]]
[[!redirects internal central products of groups]]

[[!redirects central product group]]
[[!redirects central product groups]]

[[!redirects external central product group]]
[[!redirects external central product groups]]

[[!redirects internal central product group]]
[[!redirects internal central product groups]]

[[!redirects central product]]
[[!redirects central products]]

[[!redirects external central product]]
[[!redirects external central products]]

[[!redirects internal central product]]
[[!redirects internal central products]]


