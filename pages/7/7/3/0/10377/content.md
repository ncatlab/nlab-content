
## Definition 

Given a [[poset]] (or [[proset]]) $P$, its __opposite__ (or __dual__, __inverse__, __converse__, __reverse__, etc), denoted $P^{op}$ (among other ways), is the poset (or proset) with the same [[underlying set]], with $x \leq y$ in $P^op$ iff $y \leq x$ (equivalently, $x \geq y$) in the original $P$.  We say that $\geq$ (the order relation in $P^op$ is the __opposite order__.  This is a special case of both an [[opposite relation]] ($\geq$ compared to $\leq$) and an [[opposite category]] ($P^op$ compared to $P$).

### In homotopy type theory

Given a [[preorder]] or (0,1)-category $P \coloneqq (F(P), \leq)$, an __opposite preorder__ or __opposite (0,1)-category__ is a preorder $P^\op \coloneqq (F(P), \geq)$ with $\geq$ defined as 

$$a:F(P), b:F(P) \vdash a \geq b \coloneqq b \leq a $$

where $F$ is the forgetful functor that gets the underlying type for a preorder. 

## See also

* [[poset]]

* [[opposite relation]]

* [[opposite magma]]

* [[opposite category]]

* [[antitone]]

[[!redirects opposite poset]]
[[!redirects opposite posets]]
[[!redirects opposite proset]]
[[!redirects opposite prosets]]
[[!redirects opposite order]]
[[!redirects opposite orders]]
[[!redirects opposite preorder]]
[[!redirects opposite preorders]]

[[!redirects dual poset]]
[[!redirects dual posets]]
[[!redirects dual proset]]
[[!redirects dual prosets]]
[[!redirects dual order]]
[[!redirects dual orders]]
[[!redirects dual preorder]]
[[!redirects dual preorders]]

[[!redirects inverse poset]]
[[!redirects inverse posets]]
[[!redirects inverse proset]]
[[!redirects inverse posets]]
[[!redirects inverse order]]
[[!redirects inverse orders]]
[[!redirects inverse preorder]]
[[!redirects inverse preorders]]

[[!redirects converse poset]]
[[!redirects converse posets]]
[[!redirects converse proset]]
[[!redirects converse posets]]
[[!redirects converse order]]
[[!redirects converse orders]]
[[!redirects converse preorder]]
[[!redirects converse preorders]]

[[!redirects reverse poset]]
[[!redirects reverse posets]]
[[!redirects reverse proset]]
[[!redirects reverse prosets]]
[[!redirects reverse order]]
[[!redirects reverse orders]]
[[!redirects reverse preorder]]
[[!redirects reverse preorders]]

[[!redirects opposite (0,1)-category]]
[[!redirects opposite (0,1)-categories]]