
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
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

The Leray-Hirsch theorem states sufficient fiberwise condition for the [[ordinary cohomology]] of the total space of a [[fiber bundle]] with [[coefficients]] in a [[commutative ring]] to be [[free module]] over the [[cohomology ring]] of the base space.

An important consequence is the [[Thom isomorphism]].

## Statement

Let 

$$
  \array{
     F &\stackrel{\iota}{\hookrightarrow}& E
     \\
     && \downarrow^{\mathrlap{p}}
     \\
     && X
  }
$$

be an $F$-[[fiber bundle]] in [[Top]] and let $R$ be a [[commutative ring]]. 

If there exists a [[finite set]] of elements 

$$
  \alpha_i \in H^\bullet(E,R) \;\;\, i \in I
$$

in the [[ordinary cohomology]] of $E$ with [[coefficients]] in $R$, such that for each point $x \in X$ the restriction of the $\alpha_i$ to the [[fiber]] $F_x$ is $R$-[[linearly independent]] and their $R$-[[linear span]] is [[isomorphism|isomorphic]] to the cohomology $H^\bullet(F,R)$ of the fiber

$$
  H^\bullet(F, R)
  \simeq
  \langle \{\iota_x^\ast \alpha_i\}_{i \in I} \rangle_R
  \;\;\;\;
  \in R Mod
$$

then also the $\{\alpha_i\}$ are $H^\bullet(X,R)$-[[linearly independent]] and the cohomology of the total space is their $H^\bullet(X,R)$-[[linear span]]:

$$
  H^\bullet(E,R) \simeq \langle \{\alpha_i\}_{i \in I} \rangle_{H^\bullet(X,R)}
  \;\;\;\;\;
  \in H^\bullet(X,R) Mod
$$

in fact there is an isomorphism

$$
  H^\bullet(X,R) \otimes_R H^\bullet(F,R)
  \stackrel{\simeq}{\longrightarrow}
  H^\bullet(E,R)
$$

given by pulling back classes and forming their [[cup product]]:

$$
  \underset{i,j}{\sum} c_i \otimes \iota^\ast(\alpha_j)
    \mapsto 
  \underset{i,j}{\sum}
  p^\ast(c_i) \cup \alpha_j
  \,.
$$

## Related concepts

* [[Thom isomorphism]]

## References

### For ordinary cohomology

Review of the theorem for [[ordinary cohomology]]:


* [[Alan Hatcher]], _[Algebraic topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, 2002, theorem 4D.1 on p. 432 ([pdf](https://www.math.cornell.edu/~hatcher/AT/ATch4.4.pdf))

* {#Ebert12} [[Johannes Ebert]], section 2.3 of _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf)) 

### For generalized cohomology

Discussion for [[Whitehead-generalized cohomology|Whitehead-generalized]] [[multiplicative cohomology theories]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Theorem 7.4 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__, Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Section 3.1 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))
