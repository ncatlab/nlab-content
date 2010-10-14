+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contens
{:toc}


## Definition

A [[geometric morphism]] $f : \mathcal{E} \to \mathcal{S}$ between [[topos]]es is called **bounded** if there exists an object  $B \in \mathcal{E}$ -- called a **bound** of $f$ -- such that for every $A \in \mathcal{E}$ the following equivalent conditions hold:

* $A$ is a [[subquotient]] of an object of the form $(f^* I) \times B$ for some $I  \in S$: this means that there exists a diagram

  $$
    \array{
      S &\stackrel{epi}{\to}& A
      \\
      {}^{\mathllap{mono}}\downarrow  
      \\
      (f^* I) \times B
    }
    \,.
  $$

* (one more)

* (yet one more)

If the bounded morphism $f := \Gamma$ is the [[global section]] geometricmorphism of an $\mathcal{S}$-topos $\mathcal{E}$, then $\mathcal{E}$ is called a **bounded topos**.


## References

definition 3.1.7 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


[[!redirects bounded geometric morphisms]]

[[!redirects bounded topos]]
[[!redirects bounded toposes]]
[[!redirects bounded topoi]]
