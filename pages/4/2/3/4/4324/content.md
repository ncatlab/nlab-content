
<div class="rightHandSide toc">
[[!include stable homotopy theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **connective spectrum** is a [[spectrum]] whose [[homotopy group]]s in negative degree vanish. These are equivalently

* **[[infinite loop space]]s** 

* or [[group object in an (infinity,1)-category|grouplike]] [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[∞-groupoid]]s.

Connective spectra form a [[sub-(∞,1)-category]] of [[spectra]]

$$
  Top \stackrel{\supset}{\leftarrow} ConnectSp(Top) \hookrightarrow Sp(Top)
  \,.
$$

There are objects in $Sp(Top)$, though, that do not come from "naively" [[delooping]] a [[topological space]] infinitely many times.  These are the **non-connective spectra**.  For general spectra there is a notion of [[homotopy groups]] of negative degree. The connective ones are precisely those for which all negative degree [[homotopy groups]] vanish.

### Strict 

Non-connective spectra are well familiar in as far as they are in the image of the [[nerve]] operation of the [[Dold-Kan correspondence]]: this identifies [[∞-groupoids]] that are not only connective spectra but even have a _strict_ symmetric monoidal [[group]] structure with non-negatively graded [[chain complex]]es of abelian groups. 

$$
 \array{
  Ch_+ &\stackrel{Dold-Kan \; nerve}{\to}&
  ConnectSp(\infty Grp) \subset \infty Grpd
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \to 0 \to 0 \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

The [[homology]] groups of the chain complex correspond precisely to the [[homotopy groups]] of the corresponding [[topological space]] or [[∞-groupoid]].

The free stabilization of the [[(∞,1)-category]] of non-negatively graded chain complexes is simpy the [[stable (∞,1)-category]] of arbitrary chain complexes. There is a stabilized Dold-Kan correspondence that identifies these with special objects in $Sp(Top)$. 

$$
 \array{
  Ch &\stackrel{Dold-Kan \; nerve}{\to}&
   Sp(\infty Grp) 
  \\
  (\cdots A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0 \stackrel{\partial}{\to} A_{-1} 
  \stackrel{\partial}{\to} A_{-2} \to \cdots)
  &\stackrel{}{\mapsto}&
  N(A_\bullet)
 }
$$

So it is the homologically nontrivial parts of the chain complexes in negative degree that corresponds to the non-connectiveness of a spectrum.

[[!redirects connective spectra]]