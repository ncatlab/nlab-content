[[!redirects Gysin sequence]]

#Contents#
* table of contents
{:toc}

## Idea

A [[long exact sequence in cohomology]] induced by a [[spherical fibration]]. A corollary of the [[Serre spectral sequence]]:

Let $R$ be a [[commutative ring]] and let

$$
  \array{
    S^n &\longrightarrow& E
    \\
    && \downarrow^{\mathrlap{\pi}}
    \\
    && B
  }
$$

be a [[fiber bundle]] of [[n-spheres]] over a [[simply connected topological space|simply connected]] [[simplicial complex]]. 

Then there exists a [[Thom class]]  $c \in H^{n+1}(B; R)$ such that the [[cup product]] operation $(-) \cup c$ sits in a [[long exact sequence]] of [[cohomology groups]] of the form

$$
  \cdots \to H^k(B; R) \stackrel{\pi^\ast}{\longrightarrow}
  \stackrel{}{\longrightarrow}
   H^{k-n}(B;R)
   \stackrel{(-)\cup c}{\longrightarrow}
   H^{k+1}(B; R)
   \to
   \cdots
  \,.
$$

(e.g. [Kochmann 96, corollary 2.2.6](#Kochmann96))


## Related concepts

* [[Gysin map]]

* [[Serre spectral sequence]]

## Reference

* {#Kochmann96} [[Stanley Kochmann]], section 2.2. of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


* Wikipedia, _[Gysin sequence](http://en.wikipedia.org/wiki/Gysin_sequence)_

* [[James Milne]], section 16 of _[[Lectures on Étale Cohomology]]_

[[!redirects Gysin sequences]]

