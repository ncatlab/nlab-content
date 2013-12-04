
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Grothendieck context_ is a pair of two [[symmetric monoidal categories]] $(\mathcal{X}, \otimes_X, 1_{X})$, $(\mathcal{Y}, \otimes_Y, 1_Y)$ which are connected by an [[adjoint triple]] of [[functors]] such that the leftmost one is a [[closed monoidal functor]].

This is the variant/special case of the [[yoga of six operations]] with two [[adjoint pairs]] $(f_! \dashv f^!)$ and $(f^\ast \dashv f_\ast)$ for $f_! \simeq f_\ast$. 

$$
  f^\ast \dashv (f_\ast = f_!) \dashv f^!
  \;\colon\;
  \mathcal{X}
    \stackrel{\overset{f^\ast}{\leftarrow}}{\stackrel{\overset{f_\ast = f_! }{\longrightarrow}}{\underset{f^!}{\leftarrow}}}
  \mathcal{Y}
  \,.
$$

(The other specialization of the [[six operations]] where $f^\ast \simeq f^!$ is called the _[[Wirthmüller context]]_).


## References

A clear discussion of axioms of [[six operations]] and their consequences, with emphasis on the Wirthm&#252;ller isomorphisms, is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_ ([pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

[[!redirects Grothendieck contexts]]


