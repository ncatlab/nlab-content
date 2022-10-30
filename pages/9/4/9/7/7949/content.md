[[!redirects ∞-image]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of _[[image]]_ from [[category theory]] to [[(∞,1)-category theory]].

## Defintion

### By epi/mono factorization in an $(\infty,1)$-topos

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Then by the discussion at _[[(n-connected, n-truncated) factorization system]]_ there is a [[orthogonal factorization system in an (∞,1)-category|orthogonal factorization system]] 

$$
  (Epi(\mathbf{H}), Mono(\mathbf{H})) \subset Mor(\mathbf{H}) \times Mor(\mathbf{H})
$$

whose left cl&#246;ass consists of the [[n-connected object in an (∞,1)-topos|(-1)-connected]] morphisms , the [[effective epimorphism in an (∞,1)-category|(∞,1)-effective epimorphisms]], while the right class consists of the [[n-truncated object in an (∞,1)-category|(-1)-truncated morphisms]] morphisms, hence the [[monomorphism in an (∞,1)-category|(∞,1)-monomorphisms]].

So given a morphism $f : X \to Y$ in $\mathbf{H}$ with epi-mono factorization

$$
  f : X \to im(f) \hookrightarrow Y
  \,,
$$

we may call $im(f) \hookrightarrow Y$ the **$\infty$-image** of $f$.

## Properties

### Syntax in homotopy type theory
 {#SyntaxInHomotopyTypeTheory}

Let the ambient [[(∞,1)-category]] be an [[(∞,1)-topos]] $\mathbf{H}$. Then its [[internal language]] is [[homotopy type theory]].
We discuss the [[syntax]] of $\infty$-images in this theory.

+-- {: .num_prop #SyntaxOfInfinityImage}
###### Proposition

If 

$$
  a\colon A \;\vdash \; b(a) \colon B(a)
$$

is a [[dependent type]] whose [[categorical semantics]] is given by a [[morphism]] $A \stackrel{b}{\to} B$ in $\mathbf{H}$, then the $\infty$-image of that morphism is the categorical semantics of the type

$$
  \vdash \; 
  \left(
    \sum_{a \colon A} \sum_{b' \colon B} \left[b' = b\left(a\right)\right]
  \right)
  \colon Type
$$

given by the [[dependent sum]] over a [[substitution]] into the [[bracket type]] of an [[identity type]].

=--

+-- {: .proof}
###### Proof

First observe that by the rules for [[categorical semantics]] of [[identity types]] and [[substitution]] the interpretation of $(b' = b(a))$ in a suitable [[model category]] [[presentable (∞,1)-category|presenting]] $\mathbf{H}$ is as the [[pullback]] $\tilde A$ (see at _[[homotopy pullback]]_ for more details on this) in

$$
  \array{
    \tilde A &\to& B^{I}
    \\
    \downarrow && \downarrow
    \\
    A \times B &\stackrel{(b,id_B)}{\to}& B \times B
  }
  \,,
$$

where all objects now denote [[fibrant object]] representatives of the given objects in the model category, and where the right morphism is the [[fibration]] out of a [[path space object]] for $B$. By the [[factorization lemma]] the composite $\tilde A \to A \times B \to B$ here is a [[fibration]] [[resolution]] of the original $A \stackrel{b}{\to} B$ and $\tilde A \to A \times B$ is a fibration resolution of $A \stackrel{(id_A,b)}{\to} A \times B$. Regarded in the [[slice category]] of the model category over $A \times B$ this now interprets the syntax $(b' = b(a))$ as an $A \times B$-[[dependent type]]. The interpretation of forming the [[bracket type]] of that is now precisely the [[n-truncated object in an (infinity,1)-category|(-1)-truncation]] of this morphism, which by the discussion there is the $\infty$-image $im_\infty(\tilde Q \to A \times B)$ regarded as an $A \times B$-dependent type. Finally the inerpretation of the two [[dependent sums]] is simply to regard $im_\infty(\tilde Q \to A)$ as an object in iteself (over the [[terminal object]]). And hence that is indeed the $\infty$-image of $im_\infty(A \stackrel{b}{\to} B) \simeq im_\infty(\tilde A \to B)$.

=--

+-- {: .num_remark }
###### Remark

If we allow ourselves to write the [[dependent sum]] in prop. \ref{SyntaxOfInfinityImage} either as the [[existential quantifier]] $\exists$ or as the extension formula $\{b \in B | \phi(b)\}$ then this reads

$$
  \left\{
    b' \in B | \exists a \in A . b' = b(a)
  \right\}
$$

which is manifestly the naive definition of [[image]].

=--


## Examples

### Automorphisms

Let $V \in \mathbf{H}$ be a $\kappa$-[[compact object in an (∞,1)-category|small object]], and let

$$
  * \stackrel{\vdash V}{\to} Obj_\kappa
$$

the corresponding morphism to the [[object classifier]]. Then the $\infty$-image of this is $\mathbf{B}\mathbf{Aut}(V)$, the [[delooping]] of the internal [[automorphism ∞-group]] of $V$.

## Related concepts

* [[homotopy image]]

