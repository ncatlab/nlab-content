
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _deformation retract_ is a [[retract]] which is also a [[section]] up to [[homotopy]]. Equivalently, it is a [[homotopy equivalence]] one of whose two homotopies is in fact an [[identity]].

## Definition

Let $\mathcal{C}$ be a [[category]] equipped with a notion of [[homotopy]] between its [[morphisms]]. Then a _deformation retraction_ of a morphism

$$
  i : A \to X
$$

(the _deformation retract_ itself) is another morphism

$$
  r : X \to A
$$

such that 

$$
  \array{
    && X
    \\
    & {}^{\mathllap{i}}\nearrow &\Downarrow^=& \searrow^{\mathrlap{r}}
    \\
    A &&\stackrel{=}{\to}&& A
  }
$$

and

$$
  \array{
    && A
    \\
    & {}^{\mathllap{r}}\nearrow &\Downarrow^{\simeq}& \searrow^{\mathrlap{i}}
    \\
    X &&\stackrel{=}{\to}&& X
  }
  \,.
$$

In particular, if "homotopy" in $\mathcal{C}$ means [[left homotopy]] with respect to an [[cylinder object]] $I \otimes X$

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{d_0}} & \searrow^{\mathrlap{Id_X}}
    \\
    I \otimes X &\stackrel{\sigma_X}{\to}& X
    \\
    \uparrow^{\mathrlap{d_1}} & \nearrow_{\mathrlap{Id_X}}
    \\
    X
  }
  \,,
$$

then a deformation retract of $i : A \to X$ is a morphism $r : X \to A$ such that $r \circ i = id_A$ and such that there exists a morphism $\eta : I \otimes X \to X$ fitting into a diagram

$$
  \array{
    X &\stackrel{r}{\to}& A
    \\
    \downarrow^{\mathrlap{d_0}} && \downarrow^{\mathrlap{i}}
    \\
    I \otimes X &\stackrel{\eta}{\to}& X
    \\
    \uparrow^{\mathrlap{d_1}} & \nearrow_{\mathrlap{Id_X}}
    \\
    X
  }
  \,.
$$

Hence a deformation retract is a (left) [[homotopy equivalence]] where one of the two homotopies occuring is in fact an [[identity]].

If the cylinder object assignment here is functorial, we say that $\eta$ is a **strong deformation retract** if moreover 

$$
  \eta \circ (I \otimes i) = \sigma_X \circ (I \otimes i)
$$

(hence if the homotopy restricted to the inclusion is "constant" as seen by the chosen cylinder object).


In parts of the literature, deformation retracts are required to be strong by default.

## Examples

### In topological spaces

In the category [[Top]] of [[topological spaces]] the standard [[cylinder object]] is given by [[cartesian product]] with the [[interval]] $I \coloneqq [0,1]$.

With respect to the corresponding notion of [[left homotopy]],  if $X$ is a topological space and $A\subset X$ a [[topological subspace|subspace]], then $A$ is a strong deformation retract of $X$ if there exists a [[continuous map]] $H \colon X\times I\to X$ such that $H(a,t) = a$ for all $a\in A$, $t\in I=[0,1]$, $H(x,0) = x$ for all $x\in X$ and $H(x,1)\in A$ for all $x\in X$. 

Equivalently, there are [[continuous maps]] $i \colon A\to X$ and $r \colon X\to A$ such that $r \circ i = id_A$ and $i\circ r\sim id_X (rel A)$, where $\sim (rel A)$ denotes [[homotopy]] with fixed $A$. More generally, for any continuous map $j \colon Z\to Y$ we say that it is __deformation retractable__ if there is $r \colon Y\to Z$ such that $j\circ r\sim id_Y$ and $r\circ j = id_Z$.

A pair $(X,A)$ is an __[[NDR-pair]]__ if there is a [[pair]] of continuous maps, $u \colon X\to I,\; H \colon X\times I\to X$ such that $H(a,t)=a$ for all $a\in A$ and all $t$, $H(x,0)=x$ for all $x\in X$, $u^{-1}(0)=A$ and $H(x,1)\in A$ for all $x$ such that $u(x)\lt 1$. 
If $(X,A)$ is an NDR-pair, then the inclusion has a left [[homotopy inverse]] iff $A$ is also a [[retract]] of $X$ (in [[Top]], in the standard [[category theory|category-theoretic]] sense).

The pair $(X,A)$ is a __DR-pair__ if it is a deformation retract and there is a function $u \colon X\to I$ such that $A=u^{-1}(0)$ (i.e. it gives simultaneously a deformation retract and a NDR-pair). If $(X,A)$ is an NDR-pair then the inclusion $A\hookrightarrow X$ is a homotopy equivalence iff $A$ is a deformation retract of $X$. Any map $f:X\to Y$ is a [[homotopy equivalence]] iff $X$ is the deformation retract of the mapping cylinder of $f$. If $(X,A)$ is an NDR-pair and $A$ is [[contractible space|contractible]], then the quotient map $X\to X/A$ is a homotopy equivalence. 


### In chain complexes
 {#ExamplesInChainComplexes}

\begin{proposition}\label{EZAWDeformationRetract}
**([[Eilenberg-Zilber/Alexander-Whitney deformation retraction]])** \linebreak

Let 

* $A, B \,\in\, sAb = $ [[SimplicialAbelianGroups]]

and denote 

* by $N(A), N(B) \,\in\, Ch^+_\bullet = $ [[ConnectiveChainComplexes]] their [[normalized chain complexes]], 

* by $A \otimes B \,\in\, sAb$ the degreewise [[tensor product of abelian groups]],

* by $N(A) \otimes N(B)$ the [[tensor product of chain complexes]].

Then there is a [[deformation retraction]]

\begin{tikzcd}
  N(A) \otimes N(B)
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    from=s,
    to=t,
    -,
   shift left=1pt
  ]
  \ar[
    from=s,
    to=t,
    -,
   shift right=1pt
  ]
\end{tikzcd}

\begin{tikzcd}
  N( A \otimes B )
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    from=s,
    to=t,
    Rightarrow
  ]
\end{tikzcd}

where 

* $\nabla_{A,B}$ is the [[Eilenberg-Zilber map]];

* $\Delta_{A,B}$ is the [[Alexander-Whitney map]].

\end{proposition}

For unnormalized chain complexes, where we have a [[homotopy equivalence]], this is the original [[Eilenberg-Zilber theorem]] ([Eilenberg & Zilber 1953](EZAW+deformation+retraction#EilenbergZilber53), [Eilenberg & MacLane 1954, Thm. 2.1](EZAW+deformation+retraction#EilenbergMacLane54)). The above [[deformation retraction]] for normalized chain complexes is [Eilenberg & MacLane 1954, Thm. 2.1a](EZAW+deformation+retraction#EilenbergMacLane54). Both are reviewed in [May 1967, Cor. 29.10](EZAW+deformation+retraction#May67). Explicit description of the [[homotopy operator]] is given in [Gonzalez-Diaz & Real 1999](EZAW+deformation+retraction#GonzalezDiazReal99).



## Related concepts

* [[retract]], [[neighbourhood retract]]

* [[section]]

* There is also the notion of a [[deformation retract of a homotopical category]], which has a similar feel in some ways but is not closely related.  (It should not be confused with the idea of a deformation retract *in* a [[model category]], which is a direct generalization of the notion described above for [[Top]].)


## References ##

Textbook accounts

* [[George Whitehead]], chapter 1 of: *Elements of Homotopy Theory*, Springer 1978 ([doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0))

* [[Peter May]], Section 6.4 of: _[[A concise course in algebraic topology]]_, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

[[!redirects deformation retracts]]

[[!redirects deformation retraction]]
[[!redirects deformation retractions]]

[[!redirects strong deformation retract]]
[[!redirects strong deformation retracts]]


