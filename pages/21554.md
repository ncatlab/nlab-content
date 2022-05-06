
### Colimits of equifibered transformations
  {#ColimitsOfEquifiberedTransformations}

+-- {: .num_prop #CartesianTransformationsOfColimitsInAnInfinityTopos} 
###### Proposition
**([[equifibered natural transformations]] of [[(∞,1)-colimits]] in an [[(∞,1)-topos]])**

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. For $\mathcal{I}$ a [[small (∞,1)-category]], write $\mathcal{I}^\rhd$ for the result of adjoining a [[terminal object]] (the shape of [[cocones]] under $\mathcal{I}$-shaped diagrams), and let 

$$
  X^\rhd \overset{f^\rhd}{\Rightarrow} Y^\rhd \;\colon\; \mathcal{I}^\rhd  \longrightarrow \mathbf{H}
$$

be a [[natural transformation]] between two $\mathcal{I}^\rhd$-shaped [[diagrams]] ([[(∞,1)-functors|∞-functors]]), with
$$
  X \overset{f}{\Rightarrow} Y \;\colon\; \mathcal{I}  \longrightarrow \mathbf{H}
$$

denoting its restriction away from the cocone tip.

If 

* $Y^\rhd$ is an [[(∞,1)-colimit]] diagram, 

and

* $f$ is a [[cartesian natural transformation]],

then the following are equivalent:

1. $X^\rhd$ is an [[(∞,1)-colimit]] diagram,

1. $f^\rhd$ is a [[cartesian natural transformation]].

=--

([Rezk 10, 6.5](infinity,1-topos#Rezk10), [[Higher Topos Theory|Lurie, Theorem 6.1.3.9 (4)]])

+-- {: .num_example } 
###### Example

Let $\mathcal{I} = \Delta^{op}$ be the [[opposite (∞,1)-category|opposite]] of the [[simplex category]], so that $\mathcal{I}^{\rhd} = \Delta_+^{op}$ is the opposite of the [[augmented simplex category]].

Let 

$$
  X_\bullet, Y_\bullet \colon \Delta^{op} \longrightarrow \mathbf{H}
$$ 

be [[groupoid objects in an (∞,1)-category|groupoid objects]] and write

$$
  \array{
     X_0
     \\
     \big\downarrow
     \\
     \mathcal{X}
  }
  \phantom{AAAAA}
  ,
  \phantom{AAAAA}
  \array{
     Y_0
     \\
     \big\downarrow
     \\
     \mathcal{Y}
  }
$$

for the corresponding [[effective epimorphisms]] into their [[(∞,1)-colimits]].

Then Prop. \ref{CartesianTransformationsOfColimitsInAnInfinityTopos} implies that the following are equivalent:

1. a morphism of [[groupoid objects in an (∞,1)-category|groupoid objects]] $X_\bullet \overset{f_\bullet}{\Rightarrow} Y_\bullet$ is a [[cartesian natural transformation]];

1. the corresponding transformation of [[effective epimorphisms]] 

   $$
     \array{
        X_0 &\overset{f_0}{\longrightarrow}& Y_0
        \\
        \big\downarrow &\swArrow& \big\downarrow
        \\
        \mathcal{X}
        &\underset{
          \underset{\longrightarrow}{\lim}f
        }{\longrightarrow}&
        \mathcal{Y}
     }
   $$

   is an [[(∞,1)-pullback]] square.

=--
