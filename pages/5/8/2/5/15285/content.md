**[[function field analogy]]**

|   | [[number fields]] ("[[function fields]] of [[curves]] over [[F1]]")  |  [[function fields]] of [[curves]] over [[finite fields]] $\mathbb{F}_q$ ([[arithmetic curves]])  | [[Riemann surfaces]]/[[complex curves]] |  
|----|-------------------|----------------------|----|
| **[[affine line|affine]] and [[projective line]]**  |  |  |  |
|   | $\mathbb{Z}$ ([[integers]]) | $\mathbb{F}_q[z]$ ([[polynomials]], [[polynomial algebra]] on [[affine line]] $\mathbb{A}^1_{\mathbb{F}_q}$) |  $\mathcal{O}_{\mathbb{C}}$ ([[holomorphic functions]] on [[complex plane]]) |
|   | $\mathbb{Q}$ ([[rational numbers]]) | $\mathbb{F}_q(z)$ ([[rational fractions]]/[[rational function on an affine variety|rational function on affine line]] $\mathbb{A}^1_{\mathbb{F}_q}$)  | [[meromorphic functions]] on [[complex plane]] |
|   | $p$ ([[prime number]]/non-archimedean [[place]])  |  $x \in \mathbb{F}_p$, where $z - x \in \mathbb{F}_q[z]$ is the [[irreducible element|irreducible]] [[monic polynomial]] of [[degree of a polynomial|degree]] one | $x \in \mathbb{C}$, where $z - x \in \mathcal{O}_{\mathbb{C}}$ is the [[function]] which [[subtracts]] the [[complex number]] $x$ from the [[variable]] $z$ |
|   | $\infty$ ([[place at infinity]])  |   |  $\infty$  |
|   | $Spec(\mathbb{Z})$ ([[Spec(Z)]])  |  $\mathbb{A}^1_{\mathbb{F}_q}$ ([[affine line]]) |  [[complex plane]]  |
|   | $Spec(\mathbb{Z}) \cup place_{\infty}$   | $\mathbb{P}_{\mathbb{F}_q}$ ([[projective line]])  |  [[Riemann sphere]]  |
|  | $\partial_p \coloneqq \frac{(-)^p - (-)}{p}$ ([[Fermat quotient]]) | $\frac{\partial}{\partial z}$ ([[coordinate]] [[derivation]])  |  " |
|   | [[genus of a number field|genus of the rational numbers]] = 0 |  |  [[genus of a surface|genus of the Riemann sphere]] = 0 |
| **[[formal neighbourhoods]]**  |   |   |   |
|   | $\mathbb{Z}/(p^n \mathbb{Z})$ ([[prime power local ring]]) |  $\mathbb{F}_q [z]/((z-x)^n \mathbb{F}_q [z])$ ($n$-th order univariate [[local Artinian ring|local Artinian $\mathbb{F}_q$-algebra]])  |  $\mathbb{C}[z]/((z-x)^n \mathbb{C}[z])$ ($n$-th order univariate [[Weil algebra|Weil $\mathbb{C}$-algebra]])  |
|   | $\mathbb{Z}_p$ ([[p-adic integers]]) |  $\mathbb{F}_q[ [ z -x ] ]$ ([[power series]] around $x$)  |  $\mathbb{C}[ [z-x] ]$ ([[holomorphic functions]] on [[formal disk]] around $x$)  |
|   |  $Spf(\mathbb{Z}_p)\underset{Spec(\mathbb{Z})}{\times} X$ ("$p$-[[arithmetic jet space]]" of $X$ at $p$) |  |  [[formal disks]] in $X$  |
|   | $\mathbb{Q}_p$ ([[p-adic numbers]]) | $\mathbb{F}_q((z-x))$ ([[Laurent series]] around $x$) |  $\mathbb{C}((z-x))$ ([[holomorphic functions]] on punctured [[formal disk]] around $x$) |
|   | $\mathbb{A}_{\mathbb{Q}} = \underset{p\; place}{\prod^\prime}\mathbb{Q}_p$ ([[ring of adeles]])  | $\mathbb{A}_{\mathbb{F}_q((t))}$  ( [adeles of function field](ring%20of%20adeles#ForAGlobalField) ) |  $\underset{x \in \mathbb{C}}{\prod^\prime} \mathbb{C}((z-x))$ ([[restricted product]] of holomorphic functions on all punctured formal disks, finitely of which do not extend to the unpunctured disks) |
|   | $\mathbb{I}_{\mathbb{Q}} = GL_1(\mathbb{A}_{\mathbb{Q}})$ ([[group of ideles]])  | $\mathbb{I}_{\mathbb{F}_q((t))}$  ( [[group of ideles|ideles of function field]] ) |  $\underset{x \in \mathbb{C}}{\prod^\prime} GL_1(\mathbb{C}((z-x)))$   |
| **[[theta functions]]**  |  |  |  |
|   |  [[Jacobi theta function]] |  |  |  |
| **[[zeta functions]]**  |  |  |  |
|   |  [[Riemann zeta function]] | [[Goss zeta function]] | |
|    |  |  |  |
| **[[branched covering]] curves**  |  |  |  |
|   | $K$ a [[number field]] ($\mathbb{Q} \hookrightarrow K$ a possibly [[ramified]] [[finite set|finite]] [[dimension|dimensional]] [[field extension]]) |  $K$ a [[function field]] of an [[algebraic curve]] $\Sigma$ over $\mathbb{F}_p$ |  $K_\Sigma$  ([[sheaf of rational functions]] on [[complex curve]] $\Sigma$)  |
|   | $\mathcal{O}_K$ ([[ring of integers]]) |   | $\mathcal{O}_{\Sigma}$ ([[structure sheaf]])  |
|   | $Spec_{an}(\mathcal{O}_K) \to Spec(\mathbb{Z})$ ([[spectrum of a commutative ring|spectrum]] with archimedean [[places]])   | $\Sigma$ ([[arithmetic curve]]) |   $\Sigma \to \mathbb{C}P^1$ ([[complex curve]] being [[branched cover of Riemann sphere]])  |
|   | $\frac{(-)^p - \Phi(-)}{p}$ (lift of [[Frobenius morphism]]/[[Lambda-ring]] structure) | $\frac{\partial}{\partial z}$ | "  |
|   | [[genus of a number field]] |  [[genus of an algebraic curve]] | [[genus of a surface]] | 
| **[[formal neighbourhoods]]**  |   |    |    |
|   | $v$ prime ideal in [[ring of integers]] $\mathcal{O}_K$ | $x \in \Sigma$ | $x \in \Sigma$ |
|   | $K_v$ ([[formal completion]] at $v$)  |   | $\mathbb{C}((z_x))$ ([[function algebra]] on punctured [[formal disk]] around $x$) |
|   | $\mathcal{O}_{K_v}$ ([[ring of integers]] of [[formal completion]]) |    |  $\mathbb{C}[ [ z_x ] ]$ ([[function algebra]] on [[formal disk]] around $x$) |
|   | $\mathbb{A}_K$ ([[ring of adeles]]) |   |  $\prod^\prime_{x\in \Sigma} \mathbb{C}((z_x))$ ([[restricted product]] of [[function rings]] on all punctured [[formal disks]] around all points in $\Sigma$)  | 
|   | $\mathcal{O}$ |  | $\prod_{x\in \Sigma} \mathbb{C}[ [z_x] ] $ (function ring on all [[formal disks]] around all points in $\Sigma$) |
|   | $\mathbb{I}_K = GL_1(\mathbb{A}_K)$ ([[group of ideles]]) |  | $\prod^\prime_{x\in \Sigma} GL_1(\mathbb{C}((z_x)))$ |
| **[[Galois theory]]** |   |   |   |
|   |  [[Galois group]] |  " | $\pi_1(\Sigma)$ [[fundamental group]]  |
|   |  [[Galois representation]] |  " | [[flat connection]] ("[[local system]]") on $\Sigma$ |
| **[[class field theory]]** |   |   |   |
|  | [[class field theory]] | " | [[geometric class field theory]] |
|    | [[Hilbert reciprocity law]] | [[Artin reciprocity law]] | [[Weil reciprocity law]] |
|  | $GL_1(K)\backslash GL_1(\mathbb{A}_K)$ ([[idele class group]]) | " |   | 
|  | $GL_1(K)\backslash GL_1(\mathbb{A}_K)/GL_1(\mathcal{O})$  | " |  $Bun_{GL_1}(\Sigma)$ ([[moduli stack of bundles|moduli stack of line bundles]], by [[Weil uniformization theorem]])  | 
| **non-abelian class field theory and automorphy**  |   |  |  |  |
|   | number field [[Langlands correspondence]] |  function field [[Langlands correspondence]] | [[geometric Langlands correspondence]] |
|   | $GL_n(K) \backslash GL_n(\mathbb{A}_K)//GL_n(\mathcal{O})$ ([[constant sheaves]] on this [[stack]] form [[unramified]] [[automorphic representations]]) |  " | $Bun_{GL_n(\mathbb{C})}(\Sigma)$ ([moduli stack of bundles on the curve](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence) $\Sigma$, by [[Weil uniformization theorem]])   | 
|   | [Tamagawa-Weil for number fields](Weil+conjecture+on+Tamagawa+numbers#NumberFieldCase)  | [Tamagawa-Weil for function fields](Weil+conjecture+on+Tamagawa+numbers#FunctionFieldCase)  |   |
| **[[theta functions]]**  |  |  |  |
|  |  [[Hecke theta function]]  |  | [[functional determinant]] [[determinant line bundle|line bundle]] of [[Dirac operator]]/chiral [[Laplace operator]] on $\Sigma$ |    
| **[[zeta functions]]**  |  |  |  |
|   |  [[Dedekind zeta function]] | [[Weil zeta function]] | [[zeta function of a Riemann surface]]/[[zeta function of an elliptic differential operator|of the Laplace operator]] on $\Sigma$ |
|   |   |  |  |  |
| **[[higher dimensional arithmetic geometry|higher dimensional spaces]]**  |   |  |  |  |
| **[[zeta functions]]**  | [[Hasse-Weil zeta function]]  |  |  |  |

