

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Fivebrane structure_ is the next higher analog of that of [[spin structure]] and [[string structure]].

Recall from the discussion there that a [[string structure]] on [[manifold]] $X$ with [[spin structure]] is a lift $\hat g$ of the classifying map $g : X \to \mathcal{B}Spin(n)$ of the [[tangent bundle]] associated to a [[Spin group]]-[[principal bundle]] through the next step in the [[Whitehead tower]] of $O(n)$, called $\mathcal{B}String(n)$ -- the [[delooping]] of the [[String group]]:

$$
  \array{
    && \mathcal{B} String(n)
    \\
    & {\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathcal{B}Spin(n)
  }
  \,.
$$

The names "Spin" and "String" both derive from the role these structures play in [[quantum field theory]]: a [[spin structure]] is required on $X$ for it to serve as a target space for spinning particles (superparticles), while a [[string structure]] is required for it to serves as a target for "spinning strings" -- superstrings -- (see [[heterotic string theory]] for more).
Topologists just say (said) $O(n)\langle 2\rangle$ for $Spin(n)$ and $O(n)\langle 6\rangle$ for $String(n)$, respectively. 

They wrote $O(n)\langle 8\rangle$ for the next step in the [[Whitehead tower]] of $O(n)$.

It was [[Hisham Sati]] who first realized that a lift of the [[tangent bundle]] $T X$ to this highly connected structure group is related to $X$ serving as a target for "spinning 5-branes" -- super-5-branes -- in what is called [[dual heterotic string theory]]. Following the history of the term [[String group]] he gave the topological group $O(n)\langle 8\rangle$ the name [[Fivebrane group]]:  $Fivebrane(n)$.

Accordingly, a **Fivebrane structure(n)** on a manifold $X$ with [[string structure]] is a lift of $\hat g : X \to \mathcal{B}String(n)$ to $\hat \hat g$

$$
  \array{
    && \mathcal{B} Fivebrane(n)
    \\
    & {\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathcal{B}String(n)
  }
  \,.
$$

In the article

* H. Sati, U. Schreiber, J. Stasheff, _Fivebrane structures_ , Reviews in Math. Phys. (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSII">web</a>)

the physical interpretation of this topological lift was established by comparison with known [[quantum anomaly]] cancellaton conditions in [[dual heterotic string theory]].

Thee term "Fivebrane" apparently quickly caught on in the mathematical community, for instance in 

* Christopher L. Douglas, Andr&#233; G. Henriques, Michael A. Hill, _Homological obstructions to string orientations_ ([arXiv](http://arxiv.org/abs/0810.2131))

Since [[gauge theory]] is not just about [[principal bundle]]s, but about principal [[connection on a bundle|bundles with connection]], what matters in physics is not just the topological Spin-, String- and Fivebrane Structures, but their refinement to [[schreiber:differential nonabelian cohomology]]. The full picture of such differential Fivebrane structures in heterotic String theory is described at [[schreiber:twisted differential String- and Fivebrane structures|twisted differential String- and Fivebrane structures]].

## Further references

* blog entry: [Dual formulation of String theory and Fivebrane structures](http://golem.ph.utexas.edu/category/2008/04/dual_formulation_of_string_the.html)

[[!redirects fivebrane structure]]