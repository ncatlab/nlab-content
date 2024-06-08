+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea 

The notion of a *cocartesian coclosed category* is [[abstract duality|dual]] to that of a *[[cartesian closed category]]*. 

## Definition 

A **cocartesian coclosed category** is a category $C$ with [[finite coproducts]] and [[coexponential objects]]. 

## Properties

Any category which is both cartesian closed and cocartesian coclosed is a [[thin category]], though it may not be the terminal category (e.g., any [[Boolean algebra]] is such a category).

+--{: .proof}
###### Proof
Let a category be given which is both cartesian closed and cocartesian coclosed. Cartesian closure tells us that the [[product]] of any object with the initial object $0$ will be itself initial (as [[left adjoints]] preserve [[colimits]]). Furthermore, given any [[morphism]] from an object $A$ to $0$, we can pair this with the [[identity morphism]] on $A$ to obtain a morphism from $A$ into $A \times 0$ with a [[left inverse]] given by projection, thus identifying $A$ as a [[retract]] of an initial object, and therefore as an initial object itself. It follows immediately that any two [[parallel morphisms]] to $0$ are equal; equivalently, by the dual reasoning, any two parallel morphisms out of $1$ are equal. But this means any two parallel morphisms in general are equal, as maps from $X$ to $Y$ can be identified with maps from $1$ to $Y^X$; accordingly, the category must be a thin category.
=--

## Examples

The [[Kleisli category]] of a [[continuation monad]] $K_R = R^{R^{(-)}}$ on a cartesian closed category with coproduct $\mathbf{C}$ is cocartesian coclosed.
In fact $(-) \times R^A \dashv A + (-)$, which we can prove using the cartesian closure of $\mathbf{C}$:
$$
\mathbf{Kl}(K_R)(B \times R^A, C)\cong
\mathbf{C}(B \times R^A, R^{R^C}) \cong
\mathbf{C}(B \times R^A \times R^C, R) \cong
$$
$$
\mathbf{C}(B \times R^{A + C}, R)\cong
\mathbf{C}(B, R^{R^{A+C}}) \cong
\mathbf{Kl}(K_R)(B, A+C)
$$

## See also

* [[coclosed category]]

* [[coclosed monoidal category]]

* [[cocartesian monoidal category]]

* [[locally cocartesian coclosed category]]

* [[cartesian closed category]]

* [[cocartesian closed category]]

[[!redirects cocartesian coclosed categories]]