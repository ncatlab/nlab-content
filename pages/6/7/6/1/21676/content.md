
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _PL de Rham theorem_ is the variant of the [[de Rham theorem]] with the smooth [[de Rham complex]] replaced by the [[PL de Rham complex]].

## Statement

+-- {: .num_prop #PLdeRhamTheorem} 
###### Proposition
**([[PL de Rham theorem]])**

Let $k$ be a [[field]] of [[characteristic zero]] (such as the [[rational numbers]], [[real numbers]] or [[complex numbers]]). 

Then the evident operation of [[integration of differential forms]] over [[simplices]] induces a [[quasi-isomorphism]] between the [[PL de Rham complex]] with coefficients in $k$  and [[cochain complex]] for [[singular cohomology]] with [[coefficients]] in $k$

$$
  \Omega^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  C^\bullet(X; k)
$$

and hence an [[isomorphism]] from [[PL de Rham cohomology]] to [[ordinary cohomology]] with [[coefficients]] in $k$ (such as [[rational cohomology]], [[real cohomology]], [[complex cohomology]]):

$$
  H^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  H^\bullet(X; k)
$$

(for $X$ any [[topological space]]).

=--

([Bousfield-Gugenheim 76, Theorem 2.2](#BousfieldGugenheim76))


## Lemmas

Besides the [[Poincaré lemma]] for piecewise polynomial forms, the proof uses:

\begin{lemma}\label{ExtensionLemma}
**(extension lemma)**
Given a PL form on the [[boundary of a simplex]], it extends to (hence is the [[pullback of differential forms|restriction of]]) a PL form on the full [[n-simplex]].
\end{lemma}

(e.g. [Griffiths & Morgan 2013, Lemma 9.6](#GriffithsMorgan13))

\begin{proof}  Consider [barycentric coordinates](simplex#BarycentricCoordinates) for the given [[n-simplex]]

$$
  \Delta^n 
  \,\equiv\,
  \left\{
    \,
    (x^0, \cdots, x^n)
    \,\in\,
    \mathbb{R}^{n+1}
    \;\Big\vert\;
    \textstyle{\sum}_k x^k = 1 
    \,,
    \forall_i \, x^i \geq 0
    \,
  \right\}
$$

such that the $i$th vertex is the point $v_i \in \Delta^n$ with coordinates

$$
  x^n(v_i)
  \;=\;
  \delta^n_i
$$

and the $i$th-face is the subset

$$
  \sigma_i\big(\Delta^n\big)
  \;=\;
  \big\{
    \,
    (x^0, \cdots, x^n)
    \,\in\,
    \Delta^n
    \;\big\vert\;
    x^i = 0
    \,
  \big\}
  \,.
$$

With these coordinate expressions consider the functions
 
\[
  \label{ProjectionFunctions}
  \begin{array}{rcl}
    \mathllap{
      p_i
      \;\colon\;
    }
    \Delta^n
    \setminus
    \{v_i\}
    &\longrightarrow&
    \sigma_i(\Delta^{n})
    \\
    (x^k)_{k}
    &\mapsto&
    \left(
      \frac{x^k}{1-x^i}
    \right)_{k \neq i}
    \,.
  \end{array}
\]

Observe that given a polynomial form $\alpha$ on $\sigma_i(\Delta^n)$, its [[pullback of differential forms|pullback]] along $p_i$ is a form on $\Delta^n \setminus \{v_i\}$ which is polynomial in the variables $\{x^k\}_{k \neq i}$ and in the variable $1/(1-x^i)$. Therefore there is a power $N_i \in \mathbb{N}$ such that

\[
  \label{PartialExtension}
  \widehat \alpha
  \;\coloneqq\;
  (1 - x^i)^{N_i}
  \cdot 
  p_i^\ast(\alpha)
\]

is a differential form on $\Delta^n \setminus \{v_i\}$ such that

1. $\widehat \alpha$ extends to $v_i$ (by zero) to give a polynomial differential form on all of $\Delta^n$;

1. pulled back to the $i$th face, $\widehat \alpha$ coincides with $\alpha$ (there being the pullback of an identity map);

1. if $\alpha$ vanishes on the $j$-face in $\sigma(\Delta^n)$ then $\widehat{\alpha}$ vanishes on the $j$-face of $\Delta^n$ (there being a pullback of the former).

Now to complete the proof, consider a polynomial differential form $\omega$ on the [[boundary of a simplex|boundary]] $\partial \Delta^n$. We need to find an extension $\widehat \omega$ to all of $\Delta_n$.

First consider the above construction (eq:PartialExtension)
$$
  \widehat \omega_0
    \;\coloneqq\;
  \widehat {\omega \vert_{\sigma_0} }
$$ 
on the restriction of $\omega$ to $\sigma_0(\Delta^n)$ and notice that the difference

$$
  \omega_1
  \;\coloneqq\;
  \omega
    - 
  \widehat{\omega}_0 \vert_{\partial \Delta^n}
$$

vanishes on $\sigma_0$ and coincides with $\omega$ on all other faces. Therefore consider next the above construction (eq:PartialExtension)

$$
  \widehat \omega_2
  \;\coloneqq\;
  \widehat{ \omega_1 \vert_{\sigma_1} }
$$

on this difference restricted to $\sigma_1$ and notice that the difference

$$
  \omega_2
  \;\coloneqq\;
  \omega_1
    - 
  \widehat{\omega}_1 \vert_{\partial \Delta^n}
$$

vanishes on the union of faces $\sigma_0 \cup \sigma_1$ and coincides with $\omega$ on all remaining faces. Proceeding in this fashion one arrives at

$$
  \omega
  \;=\;
  \underset{
    \widehat{\omega}
  }{
    \underbrace{
      \textstyle{\sum}_k 
      \widehat{\omega}_k 
    }
  }
  \,
  \Big\vert_{\partial \Delta^n}
$$

and hence the term over the brace is an extension as required.
\end{proof}

\begin{remark}\label{ExtensionLemmaForPiecewiseSmoothForms}
**(extension lemma for piecewise smooth differential forms)**
  The Extension Lemma \ref{ExtensionLemma} holds also for other flavors of differential forms over simplices:

In (the proof of) [Griffiths & Morgan 2013, Cor. 9.9](#GriffithsMorgan13) this is observed for the case of smooth differential forms: Here the proof of Lemma \ref{ExtensionLemma} applies verbatim, except that the multiplication by $(1-x^i)^{N_i}$ in (eq:PartialExtension) needs to be replaced by multiplication with any [[bump function]] which vanishes in a neighbourhood of $x^i = 1$ and is unity for $x^i = 0$.

Moreover, we may observe that this same argument then also applies to differential forms on "extended simplices" (see [this Def.](shape+via+cohesive+path+∞-groupoid#SmoothExtendedSimplices))

$$
  \Delta^n_{ext} 
  \,\equiv\,
  \left\{
    \,
    (x^0, \cdots, x^n)
    \,\in\,
    \mathbb{R}^{n+1}
    \;\Big\vert\;
    \textstyle{\sum}_k x^k = 1 
    \,
  \right\}
  \,,
$$

where the condition $\forall_i \, x^i \geq 0$ is dropped (which plays no role in the above proof). 

This is noteworthy, because it implies, with the discussion at *[[shape via cohesive path ∞-groupoid]]* and using the [[fundamental theorem of dg-algebraic rational homotopy theory]], that that rational space encoded in a [[Sullivan model]]/[[Whitehead L-infinity algebra|Whitehead $L_\infty$-algebra]] $\mathfrak{a}$ is equivalently the [[shape modality|shape]] 

$$
  \esh 
  \,
  \Omega^1_{dR}(-;\mathfrak{a})_{flat}
$$

of the [[smooth set]] of [[flat L-infinity algebra valued differential forms|flat $\mathfrak{a}$-valued differential forms]].
\end{remark}

## Related statements

* [[PL de Rham complex of smooth manifold is equivalent to de Rham complex]]

* [[equivariant PL de Rham theorem]]

* [[de Rham theorem]]

## References

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

Including the variant of piecewise smooth forms:

* {#GriffithsMorgan13} [[Phillip Griffiths]], [[John Morgan]], Chapter 9 of: *Rational Homotopy Theory and Differential Forms*,  Progress in Mathematics **16**, Birkhauser (2013) &lbrack;[doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4)&rbrack;


