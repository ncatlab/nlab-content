
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Mayer-Vietoris sequence_ is the term for the [[fiber sequence]] -- or often for the corresponding [[long exact sequence of homotopy groups]] -- induced from an [[(∞,1)-pullback]] (or for a [[homotopy pullback]] presenting it).

## Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-limits]] and let $X, Y, B$ be [[pointed objects]] and

$$
  f : X \to B
$$

and

$$
  g : Y \to B
$$

be any two [[morphisms]] with common [[codomain]] preserving the base points. Let $X \times_B Y$ be the [[(∞,1)-pullback]]

$$
  \array{
    X \times_B Y &\to& Y
    \\
    \downarrow &\swArrow_\simeq& \downarrow^{\mathrlap{g}}
    \\
    X &\stackrel{f}{\to}& B
  }
  \,.
$$

The corresponding **Mayer-Vietoris sequence** is the [[fiber sequence]] of the induced morphism $X \times_B Y \to X \times Y$. Often the term is used (only) for the corresponding [[long exact sequence of homotopy groups]].

## Properties

### General

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[presentable (∞,1)-category]]. 

Then the [[homotopy fiber]] of $X \times_B Y \to X \times Y$ is the [[loop space object]] $\Omega B$.

=--
 
+-- {: .proof}
###### Proof

One checks (for instance by choosing a presentation by a [[combinatorial model category]] and then proceeding as below in the discussion _[Presentation by fibrant objects](#PresentationByFibrantObjects)_) that the defining [[(∞,1)-pullback]] is equivalent to the $(\infty,1)$-pullback

$$
  \array{ 
    X \times_B Y &\to& B
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\Delta_B}}
    \\
    Y \times Y &\stackrel{(f,g)}{\to}& B
  }
  \,,
$$

where the right vertical morphism is the [[diagonal]] on $B$. Then by the [[pasting law]] for $(\infty,1)$-pullbacks it follows that with the left square in 

$$
  \array{
    \Omega B &\to& X \times_B Y &\to & B
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& X \times Y &\stackrel{(f,g)}{\to}& B \times B
  }
$$

an $(\infty,1)$-pullback, so is the total outer rectangle. But by the converse of the first claim, this is equivalent to the $(\infty,1)$-pullback

$$
  \array{
    \Omega B &\to& * 
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& B
  }
  \,,
$$

which is the defining pullback for the [[loop space object]].

=--

Therefore the Mayer-Vietoris [[fiber sequence]] is of the form

$$
  \Omega B \to X \times_B Y \to X \times Y
  \,.
$$

+-- {: .num_cor}
###### Corollary

The corresponding [[long exact sequence of homotopy groups]] starts out as

$$
  \cdots \to \pi_{n+1} B \to \pi_n X \times_B Y \stackrel{(f_*, g_*)}{\to} \pi_n X \oplus \pi_n Y \stackrel{f_* - g_*}{\to} \pi_n B \to \cdots 
$$

$$
  \cdots \to \pi_2 B \to \pi_1 X \times_B Y \stackrel{(f_+, g_*)}{\to}  \pi_1 X \times \pi_1 Y \stackrel{f_* \cdot g_*^{-1}}{\to} \pi_1 B \to \pi_0 X \times_B Y \to \pi_0 (X \times Y)
  \,.
$$

=--

This has historically been the definition of Mayer-Vietories sequences ([Eckmann-Hilton](#EckmannHilton)).

### Presentation by fibrant objects
 {#PresentationByFibrantObjects}

Suppose that the [[(∞,1)-category]] $\mathcal{C}$ is [[simplicial localization|presented]] by a [[category of fibrant objects]] $C$ (for instance the [[subcategory]] on the fibrant objects of a [[model category]]). 

Then the $(\infty,1)$-pullback $X \times_B Y$ is presented by a [[homotopy pullback]], and by the [[factorization lemma]], this is given by the ordinary [[limit]]

$$
  \array{
    X \times^h_B Y &\to& &\to& Y
    \\
    \downarrow && && \downarrow^{\mathrlap{g}}
    \\
    && B^I &\to& B 
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& B
  }
  \,,
$$

where $B \stackrel{\simeq}{\to} B^I \to B \times B$ is a [[path object]] for $B$. This limit coincides, up to [[isomorphism]], with the [[pullback]]

$$
  \array{
    X \times_B^h Y &\to& B^I
    \\
    \downarrow && \downarrow
    \\
    X \times Y &\stackrel{(f,g)}{\to}& B \times B
  }
  \,.
$$

This implies in particular that the [[homotopy fiber]] of $X \times_B^h Y \to X \times Y$ is the [[loop space object]] $\Omega B$, being the [[fiber]] of the [[path space object]] projection.


## References

An original reference is

* B. Eckmann and P. Hilton, _Unions and intersections in homotopy theory_, Comment. Math. Helv. 3 (1964),2 93-307.
 {#EckmannHilton}

A more modern review that emphasizes the role of [[fiber sequences]] is in

* Eldon Dyer, Joseph Roitberg, _Note on sequence of Mayer-Vietoris type_, Proceedings of the AMS, volume 80, number 4 (1980) ([pdf](http://www.ams.org/journals/proc/1980-080-04/S0002-9939-1980-0587950-8/S0002-9939-1980-0587950-8.pdf))

[[!redirects Mayer-Vietoris sequences]]