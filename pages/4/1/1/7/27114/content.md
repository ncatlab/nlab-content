
### Super-Minkowski Lie group
  {#ExampleSuperMinkowskiLieGroup}

We spell out the [[super-translation group|super-translation]] [[super Lie group]]-[[structure]] on the [[supermanifold]] $\mathbb{R}^{1,d\vert\mathbf{N}}$ [[underlying]] [[super Minkowski spacetime]], hence equivalently of the [[quotient group|quotient]] [[super Lie group]] of the [[super Poincaré group]] (the "[[supersymmetry]]" group) by its [[Lorentz group|Lorentzian]] [[spin group|spin]]-[[subgroup]]:

\[
  \label{SpinorToVectorPairingForSuperMinkowski}
  \mathbb{R}^{1,d\vert\mathbf{N}}
  \;\simeq\;
  Iso\big(
    \mathbb{R}^{1,d\vert\mathbf{N}}
  \big)
  \big/ Spin(1,d)
  \,.
\]

Here 

* $d \in \mathbb{N}$ is the spatial dimension (a [[natural number]]), 

* $\mathbf{N} \in Rep_{\mathbb{R}}\big(Spin(1,d)\big)$ is a  [[real numbers|real]] [[spin representation]] equipped with a  [[linear map]]
  
\begin{tikzcd}
  \mathbf{N}
  \otimes
  \mathbf{N}
  \ar[
    rr,
    "{
      \big(
        \overline{(-)}
        \Gamma
        (-)
      \big)
    }"
  ]
  &&
  \mathbb{R}^{1,d}
\end{tikzcd}

which is [[symmetric power|symmetric]] and [[spin group|$Spin(1,d)$]]-[[equivariant map|equivariant]]. 

First, the super-Minkowski [[super Lie algebra]] [[structure]] on the [[super vector space]]
$$
  \mathbb{R}^{1,d\vert\mathbf{N}}
  \;\coloneqq\;
  \mathbb{R}^{1+d} \times \mathbb{R}^N_{odd}
$$
is defined, [[formal duality|dually]], by the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] [[dgc-superalgebra]] with generators of $\mathbb{Z} \times \mathbb{Z}/2$ bidegree

| generator      | bidegree   |
|----------------|------------|
|  $e^a$         |  $(1,evn)$ |
|  $\psi^\alpha$ |  $(1,odd)$ |

for $a \in \{0,1, \cdots, d\}$ indexing a [[linear basis]] of $\mathbb{R}^D$ and $\alpha \in \{1,\cdots, N\}$ indexing a [[linear basis]] of $\mathbf{N}$ by the differential equations

\[
  \label{CEAlgebraOfSuperMinkowski}
  \begin{array}{ccl}
    \mathrm{d}\, e^a
    &\coloneqq&
    \big( \overline{\psi} \,\Gamma^a\, \psi \big) 
    \\
    \mathrm{d}\, \psi
    &=&
    0
  \end{array}
\]

The first differential is the [[linear dual]] of the archetypical [[super Lie bracket]] in the [[supersymmetry]] [[super Lie algebra]] which takes two odd elements to a spatial translation. The second differential is the [[linear dual]] of the fact that in the absence of rotational generators, no Lie bracket in the supersymmetry alegbra results in a non-vanishing odd element.

Next we regard $\mathbb{R}^{1,10\vert\mathbf{N}}$ not just as a [[super vector space]] but as a [[Cartesian superspace|Cartesian]] [[supermanifold]]. As such it has canonical [[coordinate functions]]

| generator        | bidegree   |
|------------------|------------|
|  $x^a$           |  $(0,evn)$ |
|  $\theta^\alpha$ |  $(0,odd)$ |

On this supermanifold, consider the [[super coframe field]] 

$$
  (e,\psi)
  \;\colon\;
  T\mathbb{R}^{1,d\vert\mathbf{N}}
  \xrightarrow{\;}
  \mathbb{R}^{1,10\vert\mathbf{N}}
$$

(where on the left we have the [[tangent bundle]] and on the right its [[typical fiber]] [[super vector space]]) given by

\[
  \label{LIFormsOnSuperMinkowski}
  \begin{array}{ccl}
    e^a 
      &\coloneqq& 
    \mathrm{d}x^a 
      + \big(\overline{\theta} \,\Gamma^a \mathrm{d}\theta\big)
    \\
    \psi 
      &\coloneqq&
    \mathrm{d}\theta
  \end{array}
\]

It is clear that this is a [[coframe field]] in that for all $x \in \mathbb{R}^{1,d\vert\mathbf{N}}$ it restricts to an [[isomorphism]]
$$
  T_{x}\mathbb{R}^{1,d\vert\mathbf{N}}
  \xrightarrow{\;\sim\;}
  \mathbb{R}^{1,d\vert\mathbf{N}}
$$
and the peculiar second summand in the first line is chosen such that its [[de Rham differential]] has the same form as the differential in the [[Chevalley-Eilenberg algebra]] (eq:CEAlgebraOfSuperMinkowski).

(Incidentally, a [[frame field]] [[linear dual]] to the [[coframe field]] (eq:LIFormsOnSuperMinkowski) is 

$$
  \begin{array}{ccl}
    D_a 
    &\coloneqq&
    \partial_{x^a}
    \\
    D_\alpha &\coloneqq&
    \partial_{\theta^\alpha}
    +
    \overline{\theta}\Gamma^a \partial_{v^a}
  \end{array}
  \;\;\;\;\;\;\;
  \text{such that}
  \;\;\;\;
  \begin{array}{ll} 
    e^a(D_b) \,=\, \delta^a_b \,,
      & 
    e^a(D_\alpha) \,=\, 0
    \\
    \psi^\alpha(D_a) \,=\, 0 \,,
    &
    \psi^\alpha(D_\beta) \,=\, \delta^\alpha_\beta
  \end{array}
$$

which are the operators often stated right away in introductory texts on [[supersymmetry]].)

This fact, that the [[Maurer-Cartan equations]] of a [[coframe field]] (eq:LIFormsOnSuperMinkowski) coincide with the defining equations (eq:CEAlgebraOfSuperMinkowski) of the [[Chevalley-Eilenberg algebra]] of a [[Lie algebra]] of course characterizes the [[left invariant 1-forms]] on a [[Lie group]], and hence what remains to be done now is to construct a [[super Lie group]]-[[structure]] on the [[supermanifold]] $\mathbb{R}^{1,d\vert\mathbf{N}}$ with respect to which the coframe (eq:LIFormsOnSuperMinkowski) is [[left invariant 1-form]].

Recalling (from [[embedding of smooth manifolds into formal duals of R-algebras|here]]) that a [[morphism]] of [[supermanifolds]] is dually given by a reverse [[algebra homomorphism]] between their [[function algebras]], which in the present case are freely generated by the above [[coordinate functions]], we denote the canonical coordinates on the [[Cartesian product]] $\mathbb{R}^{1,d\vert\mathbf{N}} \times \mathbb{R}^{1,d\vert\mathbf{N}}$ by $(x^a_{'}, \theta^\alpha_{'})$ for the first factor and $(x^a, \theta^\alpha)$ for the second, and declare a group [[binary operation|product operation]] as follows:

\[\label{GroupOperationOnSuperMinkowski}\]
\begin{tikzcd}
    \mathbb{R}
      ^{1,d\,\vert\,\mathbf{N}}
    \times
    \mathbb{R}
      ^{1,d\,\vert\,\mathbf{N}}
    \ar[
      rr,
      "{ \mathrm{prd} }"
    ]
    &&
    \mathbb{R}
      ^{1,d\,\vert\,\mathbf{N}}
    \\[-45pt]
    x_{'}^a + x^a
    -
    \big(
      \hspace{1pt}
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \theta
    \big)
    \ar[rr, <-|, "{ \mathrm{prd}^\ast }"]
    &\phantom{--}&
    x^a
    \\[-45pt]
    \theta_{'}
    +
    \theta
    \ar[rr, <-|]
    &\phantom{--}&
    \theta
    \,.
\end{tikzcd}

(cf. [CAIP99, (2.1) & (2.6)](super-translation+group#CAIP99))

Here the choice of notation for the coordinates on the left is adapted to thinking of this group operation equivalently as the left multiplication action of the group on itself, which makes the following computation nicely transparent. 

{#LeftActionOfSuperMinkowskiOnItsTangentBundle} Indeed, the induced left action of the super-group on its [[odd tangent bundle]]

\begin{tikzcd}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \times
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \ar[
      r,
      hook
    ]
    \ar[
      rr,
      rounded corners,
      to path={
           ([yshift=+00pt]\tikztostart.north)  
        -- ([yshift=+10pt]\tikztostart.north)  
        -- node[yshift=5pt] {
           \scalebox{.7}{$
             \mathrm{act}
           $}
        }
           ([yshift=+10pt]\tikztotarget.north)  
        -- ([yshift=+00pt]\tikztotarget.north)  
      }
    ]
    &
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \times
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \ar[
      r,
      "{ \mathrm{prd}_\ast }"
    ]
    &    
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
\end{tikzcd}

is dually given by

\begin{tikzcd}
    C^\infty
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \,\widehat{\otimes}\,
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \ar[
      r,
      <<-
    ]
    \ar[
      rr,
      <-,
      rounded corners,
      to path={
           ([yshift=+00pt]\tikztostart.north)  
        -- ([yshift=+08pt]\tikztostart.north)  
        -- node[yshift=5pt]
           {
             \scalebox{.7}{$
               \mathrm{act}^\ast
             $}
           }
           ([yshift=+08pt]\tikztotarget.north)  
        -- ([yshift=+00pt]\tikztotarget.north)  
      }
    ]
    &
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \,\widehat{\otimes}\,
    \Omega^\bullet_{\mathrm{dR}}
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \ar[
      r,
      <-,
      "{ \mathrm{prd}^{\mathrlap{\ast}} }"
    ]
    &
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
\end{tikzcd}

and [[left invariant 1-form|left-invariance]] of the coframe (eq:CEAlgebraOfSuperMinkowski) means that it is fixed by this operation (so the [[differential]] $\mathrm{d}$ in the following computation is just that of the second factor, hence acting on unprimed coordinates only):

$$
  \begin{array}{ccl}
    \mathrm{act}^\ast e^a
    &=&
    \mathrm{act}^\ast 
    \Big(
      \mathrm{d}x^a
      +
      \big(\overline{\theta}
      \,\Gamma^a\,
      \mathrm{d}\theta\big)
    \Big)
    \\
    &=&
    \mathrm{d}\,\mathrm{act}^\ast x^a
    +
    \big(\overline{\mathrm{act}^\ast\theta}
    \,\Gamma^a\,
    \mathrm{d}\,\mathrm{act}^\ast\theta\big)
    \\
    &=&
    \mathrm{d}
    \Big(
      x^a_{'} + x^a
      -
      \big(
        \overline{\theta}_{'}
        \,\Gamma^a\,
        \theta
      \big)
    \Big)
      +
      \big(
        (\overline{\theta}_{'} + 
        \overline{\theta})
        \,\Gamma^a\,
        \mathrm{d}(
          \theta_{'} + \theta
        )
      \big)
    \\
    &=&
    \mathrm{d}x^a 
    -
    \big(
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \mathrm{d}\theta
    \big)
    \,+\,
    \big(
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \mathrm{d}\theta
    \big)
    \,+\,
    \big(
      \overline{\theta}
      \,\Gamma^a\,
      \mathrm{d}\theta
    \big)
    \\
    &=&
    \mathrm{d}x^a 
    \,+\,
    \big(
      \overline{\theta}
      \,\Gamma^a\,
      \mathrm{d}\theta
    \big)
    \\
    &=&
    e^a
    \mathrlap{\,,}
  \end{array}
  \;\;\;\;\;
  \begin{array}{ccl}
    \mathrm{prd}^\ast
    \psi
    &=&
    \mathrm{prd}^\ast
    \mathrm{d}\theta
    \\
    &=&
    \mathrm{d}
    \,
    \mathrm{prd}^\ast \theta
    \\
    &=&
    \mathrm{d}\big(
      \theta_{'}
      +
      \theta
    \big)
    \\
    &=&
    \mathrm{d}\theta
    \\
    &=&
    \psi
    \mathrlap{\,.}
    \\
    {}
  \end{array}
$$

This shows that if (eq:GroupOperationOnSuperMinkowski) is the [[binary operation|group product]] of a [[group object]] [[internalization|in]] [[SuperManifolds]] then the corresponding [[super Lie algebra]] is the super-Minkowski [[super translation Lie algebra]] and hence that this group object is the desired super-Minkowski super Lie group.

So, defining the remaining [[group object]]-operations as follows:

**[[neutral element]]:**

\begin{tikzcd}
    \ast
    \ar[
      rr,
      "{ \mathrm{e} }"
    ]
    &&
    \mathbb{R}^{1,10\,\vert\,\mathbf{32}}
    \\[-40pt]
    0
    \ar[rr, <-|, "{\mathrm{e}^\ast}"]
    &&
    x^a
    \\[-40pt]
    0 
    \ar[rr, <-|, "{\mathrm{e}^\ast}"]
    &&
    \theta
\end{tikzcd}

**[[inverse elements]]:**

\begin{tikzcd}
    \mathbb{R}^{1,10\,\vert\,\mathbf{32}}
    \ar[
      rr,
      "{ \mathrm{inv} }"
    ]
    &&
    \mathbb{R}^{1,10\,\vert\,\mathbf{32}}
    \\[-40pt]
    -x^a 
    \ar[rr, <-|, "{ \mathrm{inv}^\ast }"]
    &&
    x^a
    \\[-40pt]
    -\theta^\alpha
    \ar[rr, <-|, "{ \mathrm{inv}^\ast }"]
    &&
    \theta^\alpha
\end{tikzcd}


we conclude by checking the [[group object]]-[[axioms]]:

For **[[associativity]]** we need to check that the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
      G \times G \times G
      \ar[
        rr,
        "{ 
          \mathrm{prd}
          \,\times\, 
          \mathrm{id}
        }"
      ]
      \ar[
        dd,
        "{
          \mathrm{id}
          \,\times\,
          \mathrm{prd}
        }"{description, pos=.45}
      ]
      &&
      G \times G
      \ar[
        dd,
        "{ \mathrm{prd} }"{description, pos=.45}
      ]
      \\
      \\
      G \times G
      \ar[
        rr,
        "{
          \mathrm{prd}
        }"
      ]
      && 
      G
\end{tikzcd}

and indeed it does --- the term $\big(\overline{\theta} \Gamma^a \theta\big)$ vanishes because the $\theta^\alpha$ anti-commute among themselves, while the pairing (eq:SpinorToVectorPairingForSuperMinkowski) is symmetric:

\begin{tikzcd}
    &[-210pt]
    x^a_{''}
    +
    x^a_{'} 
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{''}
      \,\Gamma^a\,
      \theta_{'}
    \big)
    + 
    x^a
    +
    \big(
      \hspace{1pt}
      \overline{(\theta_{''} + \theta_{'})}
      \,\Gamma^a\,
      \theta
    \big)    
    \ar[
      rr,
      <-|
    ]
    \ar[dl, equals]
    &&
    x^a_{'} + x^a
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \theta
    \big)    
    \ar[
      ddd,
      <-|
    ]
    \\[-10pt]
    x^a_{''} + 
    x^a_{'} + x_a
    +\big(
      \hspace{1pt}
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \theta
    \big)
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{''}
      \,\Gamma^a\,
      (\theta_{'} + \theta)
    \big)
    \ar[
      dd,
      <-|
    ]
    \\
    \\
    x^a_{''} + x^a
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{''}
      \,\Gamma^a\,
      \theta
    \big)
    \ar[rrr, <-|]
    &&& x^a
\end{tikzcd}

\begin{tikzcd}
    \theta_{''}
    +
    \theta_{'}
    +
    \theta
    \ar[
      ddd, <-|
    ]
    \ar[rrr, <-|]
    &&&
    \theta_{'} + \theta
    \ar[ddd, <-|]
    \\
    \\
    \\
    \theta_{''}
    +
    \theta
    \ar[rrr, <-|]
    &&&
    \theta
\end{tikzcd}


For **[[unitality]]** we need to check that the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
      G
      \ar[
        r, 
        shorten=-2pt,
        "{ \sim}"{pos=.4}
      ]
      \ar[
        d, 
        shorten >=-2pt,
        "{ \sim }"{sloped, swap, pos=.4}
      ]
      \ar[
       ddrr,
       equals
      ]
      &[-24pt]
      G \times \ast
      \ar[
        r,
        "{
          \mathrm{id}
          \,\times\, 
          \mathrm{e}        
        }"{pos=.4}
      ]
      &
      G \times G
      \ar[
        dd,
        "{
          \mathrm{prd}
        }"{description}
      ]
      \\[-10pt]
      \ast \times G
      \ar[
        d,
        "{
          \mathrm{e}
          \,\times\,
          \mathrm{id}
        }"{description, pos=.43}
      ]
      \\
      G \times G
      \ar[
        rr,
        "{ \mathrm{prd} }"
      ]
      &&
      G
\end{tikzcd}

and indeed it does:

\begin{tikzcd}
    x^a
    \ar[
      r, <-|
    ]
    \ar[
      d,
      <-|
    ]
    \ar[
      dddrrr,
      equals
    ]
    &[-15pt]
    x_{'}^a 
    \ar[
      rr, <-|
    ]
    &&
    x_{'}^a + x^a 
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{
}
      \,\Gamma^a\,
      \theta
    \big)    
    \ar[
      ddd,
      <-|
    ]
    \\
    x^a_{'}
    \ar[dd, <-|]
    \\
    \\
    x_{'}^a + x^a 
    +
    \big(
      \hspace{1pt}
      \overline{\theta}_{'}
      \,\Gamma^a\,
      \theta
    \big)
    \ar[
      rrr,
      <-|
    ]
    &&&
    x^a
\end{tikzcd}

\begin{tikzcd}
    \theta
    \ar[
      r, <-|
    ]
    \ar[
      d, <-|
    ]
    \ar[
      dddrrr,
      equals
    ]
    &
    \theta_{'}
    \ar[
      rr, <-|
    ]
    &&
    \theta_{'} + \theta
    \ar[
      ddd,
      <-|
    ]
    \\
    \theta
    \ar[
      dd, <-|
    ]
    \\
    \\
    \theta_{'} + \theta
    \ar[
      rrr,
      <-|
    ]
    &&&
    \theta
\end{tikzcd}

And finally, for **[[inverse element|invertibility]]** we need to check that the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
      G 
      \ar[
        rr,
        shift left=5pt,
        "{
          (\mathrm{id} ,\, \mathrm{inv})
        }"
      ]
      \ar[
        rr,
        shift right=5pt,
        "{
          (\mathrm{inv} ,\, \mathrm{id})
        }"{swap}
      ]
      \ar[
        dd,
        "{ \exists! }"{description}
      ]
      &&
      G \times G
      \ar[
        dd,
        "{ 
          \mathrm{prd} 
        }"{description}
      ]
      \\
      \\
      \ast
      \ar[
        rr,
        "{ \mathrm{e} }"
      ]
      &&
      G
\end{tikzcd}

and indeed it does:

\begin{tikzcd}
    &[-20pt]
    x^a
    - x^a 
    - 
    \big(
      \hspace{1pt}
      \overline{\theta}
      \,\Gamma^a\,
      \theta
    \big)
    \ar[
      rr,
      <-|
    ]
    &&
    x_{'}^a
    + x^a + 
    \big(
      \hspace{1pt}
      \overline{\theta}
      \,\Gamma^a\,
      \theta
    \big)
    \ar[
      ddd,
      <-|
    ]
    \\[-15pt]
    0
    \ar[
      ur,
      equals
    ]
    \ar[
      dd,
      <-|
    ]
    \\
    \\
    0
    \ar[
      rrr,
      <-|
    ]
    &&&
    x^a
\end{tikzcd}

\begin{tikzcd}
    &
    \theta - \theta
    \ar[
      rr,
      <-|
    ]
    &&
    \theta_{'}
    +
    \theta
    \ar[
      ddd,
      <-|
    ]
    \\
    0
    \ar[
      dd,
      <-|
    ]
    \ar[
      ur,
      equals
    ]
    \\
    \\
    0
    \ar[
      rrr, <-|
    ]
    &&&
    \theta
\end{tikzcd}

$\Box$

\linebreak
