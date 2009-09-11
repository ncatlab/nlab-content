Given a morphism of [[commutative unital rings]] $f:R\to S$, the __module of K&#228;hler differentials__ is the $S$-module $\Omega^1_{S/R}$ corepresenting the functor

$$Der_R(S,f_*(-)) : S-Mod\to Set : M\mapsto Der_R(S,f_* M)$$

where $f_*:S-Mod\to R-Mod$ is the restriction of scalars. In other words,  $Der_R(S,f_*M)\cong Hom_S(\Omega^1_{S/R},M)$. Let $I$ be the augmentation ideal, i.e. the kernel of the multiplication map

$$ I := Ker(m:S\otimes_R S\to S)$$

Then $\Omega^1_{S/R}= I/I^2$ and there is a canonical induced map $d: S\to \Omega^1_{S/R}$
given by $d s = [1\otimes s - s\otimes 1]$. 

If $R$ is in charecteristic zero, one introduces K&#228;hler $p$-forms, which are elements of the $p$-th [[exterior power]] $\Omega^p_{S/R}:=\Lambda_R^p \Omega^1_{S/R}$. The module of K&#228;hler differentials readily generalizes as a sheaf of K&#228;hler differentials for a separated morphism $f:X\to Y$ of (commutative) [[schemes]], namely it is the pullback along the embedding of the ideal sheaf of the [[diagonal subobject|diagonal subscheme]] $X\hookrightarrow X\times_Y X$.

Compare the role of [[universal differential envelope]] and [[Amitsur complex]] for  analogous constructions in the noncommutative case. The appropriate extension of the module of relative K&#228;hler differentials to the derived setting is the [[cotangent complex]] of Grothendieck-Illusie. 

[[!redirects Kahler differential]]
[[!redirects Kahler differentials]]
[[!redirects Kähler differentials]]