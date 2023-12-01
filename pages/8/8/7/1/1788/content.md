
[[linear basis]]

$$
  \mathfrak{g}
  \;\simeq_{{}_\mathbb{R}}\;
  \mathbb{R}
  \big\langle 
    t_1, \cdots, t_{{}_{dim(\mathfrak{g})}}
  \big\rangle
$$

structure constants (using [[Einstein summation convention]], throughout):

$$
  [t_j, t_k]
  \;=\;
  f^i{}_{j k} t_i
$$

[[Jacobi identity]]

$$
  \big[t_i, [t_j, t_k] \big]
  \;=\;
  \big[ [t_i, t_j], t_k] \big]
  \,+\,
  \big[ t_j, [t_i, t_k] \big]
  \;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;
  f^\bullet{}_{i l} f^{l}{}_{j k}
  \;=\;
  f^\bullet{}_{l k}  f^l{}_{i j}
  \,+\,
  f^\bullet{}_{ j l } f^l{}_{ i k }
$$

one consequence:

$$
  \begin{array}{l}
  \big[A, [A, X]\big]^i
  \\
  \;\equiv\;
  f^i{}_{l m} f^m{}_{j k} A^l A^j X^k
  \\
  \;=\;
  \big(
    f^i{}_{m k}
    f^m{}_{l j} 
    A^l A^j
    +
    f^i{}_{ j m }
    f^m{}_{l k}
    A^l A^j
  \big)
  X^k
  \\
  \;=\;
  \big(
    f^i{}_{m k}
    f^m{}_{l j} 
    A^l A^j
    -
    f^i{}_{ l m }
    f^m{}_{j k}
    A^l A^j
  \big)
  X^k
  \\
  \\
  \;=\;
  \big[ [A,A], X \big]^i
  -
  \big[A, [A, X]\big]^i
  \end{array}
  \;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;
  \big[A, [A, X]\big]
  \;=\;
  \tfrac{1}{2}
  \big[ [A,A], X \big]
$$

[[covariant derivative]]:

$$
  (\mathrm{d}_{A} X)^i
  \;\equiv\;
  \mathrm{d} X^i + [A, X]^i
  \;=\;
  \mathrm{d} X^i + f^i_{j k} A^j X^k
$$

[[curvature]]:

$$
  \begin{array}{l}
    \mathrm{d}_A \mathrm{d}_A X
    \\
     \;=\;
     \mathrm{d}_A \big(
       \mathrm{d}X + [A,X]
     \big)
     \\
     \;=\;
     [A, \mathrm{d}X]
     +
     \mathrm{d}[A,X] 
     +
     \big[ A, [A, X] \big]
     \\
     \;=\;
     [A, \mathrm{d}X]
     +
     [\mathrm{d} A,X] 
     -
     [A, \mathrm{d} X] 
     +
     \tfrac{1}{2}\big[ [A, A],  X \big]
     \\
     \;=\;
     \big[
       \underset{
         \equiv \, F_A
       }{
         \underbrace{
           \mathrm{d} A + \tfrac{1}{2}[A, A]
         }   
       }
       ,\,
       X
     \big]
  \end{array}
$$

[[Bianchi identity]]:

$$
  \begin{array}{l}
    \mathrm{d}_A \mathrm{d}_A \mathrm{d}_A X
    \\
    \;=\;
    \mathrm{d}_A \big[ F_A ,\, X \big]
    \\
    \;=\;
    \big[ \mathrm{d}_A F_A ,\, X \big]
    +
    \big[ F_A ,\, \mathrm{d}_A X \big]
    \\
    \;=\;
    \big[ \mathrm{d}_A F_A ,\, X \big]
    +
    \mathrm{d}_A \mathrm{d}_A \mathrm{d}_A X
   \end{array}
   \;\;\;\;\;\;\;
   \Rightarrow
   \;\;\;\;\;\;\;
   \mathrm{d}_A F_A \,=\, 0
$$

[[invariant polynomial]]:

$$
  \langle -,-\rangle
  \;\colon\;
  \mathfrak{g} \otimes \mathfrak{g}
  \to
  \mathbb{R}
$$

$$
  k_{i j}
  \;\equiv\;
  \langle t_i, t_j\rangle
$$

invariance

$$
  \big\langle
    [t, -]
    ,\,
    -
  \big\rangle
  +
  \big\langle
    -
    ,\,
    [t,-]
  \big\rangle
  \;=\;
  0
$$

The induced trilinear pairing

$$
  \langle -,-,- \rangle
  \;\coloneqq\;
  \big\langle -,[-,-] \big\rangle
$$

is also $\mathfrak{g}$-invariant, in that

$$
  \begin{array}{l}
    \big\langle
      [t,-], -,-
    \big\rangle
    +
    \big\langle
      -, [t,-], -
    \big\rangle
    +
    \big\langle
      -, -, [t,-]
    \big\rangle
    \\
    \;\equiv\;
    \big\langle
      [t,-], [-,-]
    \big\rangle
    +
    \Big\langle
      -, \big[[t,-], -\big]
    \Big\rangle
    +
    \Big\langle
      -, \big[-, [t,-]\big]
    \Big\rangle
    \\
    \;=\;
    \big\langle
      [t,-], [-,-]
    \big\rangle
    +
    \Big\langle
      -, \big[ t, [-, -] \big]
    \Big\rangle
    \\
    \;=\;
    0
    \,,
  \end{array}
$$

where we used first the Jacobi identity and then the invariant of the bilinear pairing.

Moreover, for a [[semisimple Lie algebra]]
the trilinear pairing is also skew-symmetric and hence in particular invariant under cyclic permutation of its arguments.

$$
  \big\langle
    t_i, t_j k
  \big\rangle
  \;=\;
  \big\langle
    t_k, t_i j
  \big\rangle
$$

\linebreak

[[Poisson bracket]]:

$$
  \big\{ E^i, A^j \big\}
  \;\equiv\;
  k^{ i j }
$$


$$
  \begin{array}{l}
    \Big\{
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \big(
        \mathrm{d}_A \beta
      \big)
    \Big\}
    \\
    \;\equiv\;
    \Big\{
      \big(\mathrm{d}_A \alpha_i\big)
      E^i
      ,\,
      \big(
        \mathrm{d}\beta
        + [A, \beta]
      \big)
    \Big\}
    \\
    \;=\;
    \big(\mathrm{d}_A \alpha_i\big)
    \Big[
      \big\{
        E^i
        ,\,
        A
      \big\}
      ,\,
      \beta
    \Big]
    \\
    \;=\;
    \big(\mathrm{d}_A \alpha_i\big)
    \big[
      t^i
      ,\,
      \beta
    \big]
    \\
    \;=\;
    \Big[
      \big(\mathrm{d}_A \alpha\big)
      ,\,
      \beta
    \Big]
  \end{array}
$$

notably:

$$
  \begin{array}{l}
    \Big\{
      \underset{x}{\textstyle{\int}}
      \big(\mathrm{d}_A \alpha_i(x)\big) \wedge E^i(x)
      ,\,
      \mathrm{d} A(x')
    \Big\}
    \\
    \;=\;
    \underset{x}{\textstyle{\int}}
    \big( \mathrm{d}_A \alpha(x) \big)
    \wedge
    \mathrm{d}_{x'} \delta(x,x')
    \\
    \;=\;
    -
    \underset{x}{\textstyle{\int}}
    \big( \mathrm{d}_A \alpha(x) \big)
    \wedge
    \mathrm{d}_{x} \delta(x,x')
    \\
    \;=\;
    -
    \underset{x}{\textstyle{\int}}
    \Big(
      \mathrm{d}
      \big( \mathrm{d}_A \alpha(x) \big)
    \Big)
    \delta(x,x')
    \\
    \;=\;
    -
    \mathrm{d} \big( \mathrm{d}_A \alpha(x') \big)
  \end{array}
$$

and hence

$$
  \begin{array}{l}
    \Big\{
      \underset{x}{\textstyle{\int}}
      \big(\mathrm{d}_A \alpha_i(x)\big) \wedge E^i(x)
      ,\,
      F_A(x')
    \Big\}
    \\
    \;=\;
    -
    d_A \big(\mathrm{d}_A \alpha\big)(x')
  \end{array}
$$

Poisson bracket of electric with electric fluxes

$$
  \begin{array}{l}
  \Big\{
    \big( \mathrm{d}_A \alpha_i \big) E^i
    ,\,
    \big( \mathrm{d}_A \beta_j \big) E^j
  \Big\}
  \\
  \;=\;
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  -
  \Big[
    \big(\mathrm{d}_A \beta\big)
    ,\,
    \alpha
  \Big]_i
  E^i
  \\
  \;=\;
  \Big[
    \big(\mathrm{d}_A \alpha\big)
    ,\,
    \beta
  \Big]_i
  E^i
  +
  \Big[
    \alpha
    ,\,
    \big(\mathrm{d}_A \beta\big)
  \Big]_i
  E^i
  \\
  \;=\;
  \big(
    \mathrm{d}_A
    [\alpha,\beta]_i
  \big)
  E^i
  \end{array}
$$

Poisson bracket of electric with magnetic flux:

$$
  \begin{array}{l}
  \Big\{
    \textstyle{\int}
    \big( \mathrm{d}_A \alpha_i \big) 
    \wedge 
    E^i
    ,\,
    \textstyle{\int}
    \big( \mathrm{d}_A \beta_j \big) 
    \wedge
    F_A^j    
  \Big\}
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle
    \big[
      \mathrm{d}_A \alpha
      ,\,
      \beta_j
    \big]
    ,\,
    F_A^j
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle
    \big(
      \mathrm{d}_A \beta
    \big)
    ,\,
    \mathrm{d}_A
    \big(
      \mathrm{d}_A \alpha
    \big)
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \big\langle
    \mathrm{d}_A \alpha
    ,\,
    \beta
    ,\,
    F_A
  \big\rangle
  +
  \textstyle{\int}
  \big\langle
    \mathrm{d}_A \beta
    ,\,
    F_A
    ,\,
    \alpha
  \big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle  
    \mathrm{d}_A \alpha
    ,\,
    \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \mathrm{d}_A  \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \beta
    ,\,
    \underset{= 0}{
      \underbrace{
        \mathrm{d}_A F_A
      }
    }
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \Big\langle  
    \mathrm{d} \alpha
    ,\,
    \beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \mathrm{d}\beta
    ,\,
    F_A
  \Big\rangle
  +
  \textstyle{\int}
  \Big\langle  
    \alpha
    ,\,
    \beta
    ,\,
    \mathrm{d} F_A
  \Big\rangle
  \\
  \;=\;
  \textstyle{\int}
  \mathrm{d}
  \big\langle
    \alpha
    ,\,
    \beta
    ,\,
    F_A
  \big\rangle
  \\
  \;=\;
  0
  \end{array}
$$

\linebreak

$$
  \begin{array}{l}
    \big\{
      \Phi_E^\alpha
      ,\,
      \Phi_B^{\beta}
    \big\}
    \\
    \;\equiv\;
    \Big\{
      \underset{x \in Int(S)}{\textstyle{\int}}
      \big(
        \mathrm{d} \alpha_i(x)
        +
          \epsilon_{i j k} 
          A^j(x) \wedge \alpha^k(x) 
      \big)
      \wedge E^i(x)
      ,\;
      \underset{x' \in Int(S)}{\textstyle{\int}}
      \big(
        \mathrm{d} \beta_l(x)
        +
          \epsilon_{l m n} 
          A^m(x') \wedge \beta^n(x') 
      \big)
      \wedge
      \big(
        \mathrm{d} A^l(x')
        +
          \epsilon^l{}_{r s} 
          A^r(x') \wedge A^s(x') 
      \big)      
    \Big\}
    \\
    \;=\;
    \epsilon_{i j k}
    (d_A \alpha)^i \beta^j (F_A)^k
    -
    \epsilon_{i j k}
    (F_A)^k \alpha^i (d_A \beta)^j
  \end{array}
$$

$$
  \begin{array}{l}
    \big\{
      \Phi_E^\alpha
      ,\,
      \Phi_E^{\beta}
    \big\}
    \\
    \;\equiv\;
    \Big\{
      \underset{x \in Int(S)}{\textstyle{\int}}
      \mathrm{d} \alpha_i(x) \wedge E^i(x)
      +
      \epsilon_{i j k} 
        A^j(x) \wedge \alpha^k(x) \wedge E^i(x)
      ,\;
      \underset{x' \in Int(S)}{\textstyle{\int}}
      \mathrm{d} \beta_l(x') \wedge E^l(x')
      +
      \epsilon_{l m n} 
        A^m(x') \wedge \beta^n(x') \wedge E^l(x')
    \Big\}
    \\
    \;=\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \underset{x' \in Int(S)}{\textstyle{\int}}
    \big\{
       E^i(x)
       ,\,
       A^m(x')
    \big\}
    \epsilon_{l m n}
    \mathrm{d} \alpha_i(x) 
    \wedge
    \beta^n(x') \wedge E^l(x')
    \\
    \phantom{\;=\;}
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \underset{x' \in Int(S')}{\textstyle{\int}}
    \epsilon_{i j k }
    \big\{
      A^j(x) 
      ,\,
      E^l(x')
    \big\}
    \alpha^k(x) \wedge E^i(x) \wedge \mathrm{d}\beta_l(x')
    \\
    \phantom{\;=\;}
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \underset{x' \in Int(S')}{\textstyle{\int}}
    \epsilon_{i j k}
      A^j(x) \wedge \alpha^k(x)
      \big\{
        E^i(x)
        ,\,
        A^m(x')
      \big\}
      \epsilon_{l m n}
      \beta^n(x')
      \wedge E^l(x')
    \\
    \phantom{\;=\;}
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \underset{x' \in Int(S')}{\textstyle{\int}}
      \epsilon_{l m n}
      A^m(x')
      \wedge
      \beta^n(x')
      \big\{
        E^l(x')
        ,\,
        A^j(x)
      \big\}
      \epsilon_{i j k}
      \alpha^k(x) \wedge E^i(x)
    \\
    \;=\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \epsilon_{l m n}
    \big(\mathrm{d} \alpha^m(x)\big) 
    \wedge
    \beta^n(x) \wedge E^l(x)
    \;-\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \epsilon_{i j k}
    \alpha^k(x) \wedge  
    E^i(x)     
    \wedge \big(\mathrm{d}\beta^j(x)\big)
    \\
    \phantom{\;=\;}
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \epsilon^m{}_{j k}
    \epsilon_{l m n}
      A^j(x) 
      \wedge 
      \alpha^k(x)
      \wedge
      \beta^n(x)
      \wedge E^l(x)
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
      \epsilon^j{}_{m n}
      \epsilon_{i j k}
      A^m(x')
      \wedge
      \beta^n(x')
      \wedge \alpha^k(x) \wedge E^i(x)
    \\
    \;=\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \epsilon_{l m n}
    \big(\mathrm{d}_A \alpha^m(x)\big) 
    \wedge
    \beta^n(x) \wedge E^l(x)
    \;+\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \epsilon_{i j k}
    \alpha^k(x) 
    \wedge  
    \big(\mathrm{d}_A \beta^j(x)\big)
    \wedge
    E^i(x)     
    \\
    \;=\;
    \underset{x \in Int(S)}{\textstyle{\int}}
    \mathrm{d}_A
     \Big(
      \big[
        \alpha(x) 
        ,\,
        \beta(x) 
       \big]
    \big)_l
    E^l(x)
  \end{array}
$$




