If $K= \{K_n| n \geq 0\}$ is a [[cubical set]], then a [[connection]] structure on $K$ consists of functions $\Gamma^+_i, \Gamma^- _i: K_n \to K_{n+1}$, $i=1, \ldots \, , n; n \geq 1$, satisfying the relations for $\alpha, \beta=\pm$: 

1. $\Gamma^\alpha_i\Gamma^\beta_j= \Gamma^\beta_{j+1} \Gamma^\alpha _i$ if $i \lt j$; 

1.  $\Gamma^\alpha_i\Gamma^\alpha_i= \Gamma^\alpha_{i+1} \Gamma^\alpha _i$;

1. $\partial^\alpha_j \Gamma^\alpha_j= \partial ^\alpha_{j+1} \Gamma ^\alpha_j = id$;

1. $\partial^\alpha_j \Gamma^{-\alpha}_j= \partial ^\alpha_{j+1} \Gamma ^{-\alpha}_j = \varepsilon _j \partial^\alpha_j$;

1. $ \partial^\alpha_i \Gamma ^\beta_j = \begin{cases}\Gamma^\beta_{j-1} \partial ^\alpha _i & \text{if }\; i \lt j \\    \Gamma^\beta_j \partial ^\alpha _{i-1} & \text{if }\;  i \gt j+1; \end{cases} $

1. $ \Gamma^\alpha_j \varepsilon_j = \varepsilon^2_j = \varepsilon_{j+1}\varepsilon _j$;

1. $\Gamma^\alpha_i \varepsilon _j = \begin{cases}
\varepsilon_{j+1} \Gamma^\alpha _i & \text {if }\;  i \lt j \\
\varepsilon _j \Gamma^\alpha_{i-1} & \text{if }\;  i \gt j ;
\end{cases}$  

The connections are to be thought of as "extra degeneracies". A degenerate cube of type $\varepsilon_j x$ has opposite faces equal and all other faces degenerate.

 A cube of
type  $ \Gamma_i^\alpha  x$  has a pair  of adjacent faces equal and
all other faces of type $\Gamma_j^\alpha  y$  or $\varepsilon_j y$ .
Cubical complexes with this, and other, structures  have  also
been considered by Evrard.

The prime example of  a  cubical   set  with  connections  is the
singular cubical complex  $KX$  of a space   $X$.   Here for $n
\ge 0$ $K_n$ is  the  set  of singular $n$-cubes in $X$ (i.e.
continuous maps $I^n   \to   X$)  and the connection $
\Gamma_i^\alpha :K_{n } \to   K_{n+1}$  is induced by the map
$\gamma_i^\alpha   : I^{n+1} \to
 I^{n}$    defined by

   $$   \gamma _i^\alpha (t_1 ,t_2 ,\ldots \, ,t_{n+1} ) =
             (t_1 ,t_2 ,\ldots\, ,t_{i-1},A(t_i ,t_{i+1}),t_{i+2},\ldots \, ,t_{n+1} )
             $$

 where $A(s,t)=\max(s,t), \min(s,t)$ as $\alpha=-,+$ respectively.



##References## 

* Evrard, M., "Homotopie des complexes simpliciaux et cubiques", Preprint(1976).


*  Brown, R.  and  Higgins, P.J., "On the algebra of cubes",
_J. Pure Appl.  Algebra_ 21 (1981) 233-260.

* F. Al-Agl, R. Brown and R. Steiner, "Multiple categories: the
equivalence
  between a globular and cubical approach", _Advances in Mathematics_, 170,
  (2002), 71--118.

*  M. Grandis and L. Mauri, "Cubical sets and their
site",  _Theory Applic. Categories_, 11 (2003) 185-201.