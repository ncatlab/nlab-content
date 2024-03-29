
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[noncommutative topology]] the standard notion of [[homomorphism]] of [[C*-algebras]] is too restrictive for some applications, related to the fact that some noncommutative $C^\ast$-algebras correspond to "locally badly behaved" noncommutative topological spaces. The notion of _asymptotic $C^\ast$-homomorphism_ is more flexible than that of plain $C^\ast$-homomorphisms and designed to correct this problem. Homotopy classes of asymptotic $C^\ast$-homomorphisms are the [[hom-sets]] in a [[category]] called _[[E-theory]]_. See there for more details.

## Definition

+-- {: .num_defn #AsymptoticHomomorphism}
###### Definition

For $A,B$ two [[C*-algebras]], an **asymptotic** homomorphism between them is a $[0,\infty)$-parameterized collection of [[continuous functions]] $\{\phi_t \colon A \to B\}_{t \in [0, \infty)}$, such that

* for each $a \in A$, the [[function]] $t \mapsto \phi_t(a)$ is a [[continuous function]];

* in the [[limit of a sequence|limit]] $t \to \infty$, $\phi_t$ becomes a [[star-algebra]] [[homomorphism]].

=--

As for ordinary $C^\ast$-algebra homomorphisms one puts:

+-- {: .num_defn #AsymptoticHomotopy}
###### Definition

For $f_t, g_t \colon A \to B $ to asymptotic $C^\ast$-homomorphisms, def. \ref{AsymptoticHomomorphism}, a (right) [[homotopy]] between them is an asyptotic homomorphism $\eta_t \colon A \to C([0,1],B)$ which restricts to $f$ at 0 and to $g$ at $1$, hence such that it fits into a [[commuting diagram]] of the form

$$
  \array{
     && B
     \\
     & {}^{\mathllap{f_t}}\nearrow & \uparrow^{\mathrlap{ev_0}}
     \\
    A &\stackrel{\eta_t}{\to}& C([0,1], B)
    \\
    & {}_{\mathllap{g_t}}\searrow & \downarrow^{\mathrlap{ev_1}}
    \\
    && B
  }
  \,.
$$

Homotopy of asymptotic $C^\ast$-homomorphisms is clearly an [[equivalence relation]]. Write $[A,B]$ for the [[set]] of homotopy-[[equivalence classes]] of asymptotic homomorphisms $A \to B$.

=--

+-- {: .num_prop}
###### Proposition

For $A,B \in $ [[C*Alg]], the set $[A, C_0((0,1), B)]$ is naturally an [[abelian group]] under the composition operation which sends the homotopy classes presented by $f,g \colon A \times (0,1) \to B$ to the homotopy class of

$$
  f + g \;\colon\; A \times (0,1) \stackrel{\cdot 2}{\to} A \times (0,2) \stackrel{x \mapsto \left\{  \array{f(x) & x \lt 1 \\ g(x-1) & x \gt 1 } \right.  }{\to} B
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The $t$-wise composition of two asymptotic $C^\ast$-homomorphisms is not in general itself an asymptotic $C^\ast$-homomorphims. However, every asympotic homomorphism is homotopic to one which is an [[equicontinuous function]], and $t$-wise composition of equicontinuous asymptotic $C^\ast$-homomorphisms is again an asymptotic homomorphism.

=--



## Examples

+-- {: .num_example }
###### Example

Two asymptotic $C^\ast$-homomorphisms which differe just by a reparameterization of $[0,\infty)$ while having the same [[limit of a sequence|limit]] can be related by a homotopy, def. \ref{AsymptoticHomotopy}.

=--

+-- {: .num_example }
###### Example
**(self-adjointification homotopy)**

For $f_t \colon A \to B $ an asymptotic $C^\ast$-homomorphism, there is a homotopy to the asymptotic morphism 

$$
  \tilde f_t(a) \coloneqq \tfrac{1}{2}\left(f(a) + f(a^\ast)^\ast\right)
  \,.
$$


=--


## References

The notion was introduced in 

* [[Alain Connes]], [[Nigel Higson]], _D&#233;formations, morphismes asymptotiques et $K$-th&#233;orie bivariante_, C. R. Acad. Sci. Paris S&#233;r. I Math. __311__ (1990), no. 2, 101&#8211;106, [MR91m:46114](http://www.ams.org/mathscinet-getitem?mr=1065438), [pdf](ftp://ftp.bnf.fr/578/N5781521_PDF_107_112DM.pdf)
 {#ConnesHigson90}

A review is for instance around p. 23 of 

* _Introduction to KK-theory and E-theory_, Lecture  notes (Lisbon 2009) ([pdf slides](http://oaa.ist.utl.pt/files/cursos/courseD_Lecture4_KK_and_E1.pdf))
 {#Introduction}


[[!redirects asymptotic C-star-homomorphisms]]

[[!redirects asymptotic C*-homomorphism]]
[[!redirects asymptotic C*-homomorphisms]]

