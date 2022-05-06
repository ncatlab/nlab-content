
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Generally, a _connecting homomorphism_ is a [[morphism]] of the kind produced by the [[snake lemma]]. 

Specifically, when the [[double complex]] that goes into the snake lemma is regarded as part of a [[short exact sequence]] $A_\bullet \to B_\bullet \to C_\bullet$ of [[chain complexes]], then the connecting homomorphisms induce morphisms $\delta_n : H_n(C) \to H_{n-1}(A)$ on the [[homology groups]] of these chain complexes which exhibit the corresponding [[long exact sequence in homology]] of the form

$$
  \cdots
   \to
  H_n(A) \to H_n(B) \to H_n(C) 
   \stackrel{\delta_n}{\to}
  H_{n-1}(A) \to H_{n-1}(B) \to H_{n-1}(C)   
   \to
  \cdots
  \,.
$$

This long exact sequence is the image under [[chain homology]]

$$
  H_0(-) : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
$$

of the long [[homotopy fiber sequence]] of chain complexes induced by the short exact sequence. Hence the connecting homomorphism is the image under $H_\bullet(-)$ of a [[mapping cone]] inclusion on chain complexes.


## For long (co)homology exact sequences 

In the case that $\mathcal{A} \simeq R$[[Mod]] for some [[ring]] $R$,
the construction of the connecting homomorphism for [[homology long exact sequences]] is easily described in terms of elements and checking its properties is elementary, see _[In terms of elements](#OnHomologyInTermsOfElements)_ below. By the [embedding theorems](abelian%20category#EmbeddingTheorems) the general case can be reduced to this case. But there is also a general abstract description without recourse to elements, which we discuss further below in _[General abstract construction](#OnHomologyGeneralAbstract)_ .

### In terms of elements
 {#OnHomologyInTermsOfElements}

Let $R$ be a [[commutative ring]] and let $\mathcal{A} = R$[[Mod]]. Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] in $\mathcal{A}$.

Let

$$
  0 \to A_\bullet \stackrel{i}{\to} B_\bullet \stackrel{p}{\to}  C_\bullet \to 0
$$

be a [[short exact sequence]] in $Ch_\bullet(\mathcal{A})$.

+-- {: .num_defn #ConnectingForHomologyInComponents}
###### Definition

For $n \in \mathbb{Z}$, define a [[group homomorphism]]

$$
  \delta_n : H_n(C) \to H_{n-1}(A)
  \,,
$$

called the **$n$th connecting homomorphism** of the short exact sequence,
by sending

$$
  \delta_n : [c] \mapsto [\partial^B \hat c]_A
  \,,
$$

where 

1. $c \in Z_n(C)$ is a [[cycle]] representing a given [[homology group]]; 

1. $\hat c \in C_n(B)$ is any lift of that cycle to an element in $B_n$, which exists because $p$ is a [[surjection]] (but which no longer needs to be a cycle itself);

1. $[\partial^B \hat c]_A$ is the $A$-homology class of $\partial^B \hat c$  which is indeed in $A_{n-1} \hookrightarrow B_{n-1}$ by exactness (since $p(\partial^B \hat c) = \partial^C p(\hat c) = \partial^C c = 0$) and indeed in $Z_{n-1}(A) \hookrightarrow A_{n-1}$ since $\partial^A \partial^B \hat c = \partial^B \partial^B \hat c = 0$.


=--

+-- {: .num_prop}
###### Proposition

Def. \ref{ConnectingForHomologyInComponents} is indeed well defined in that 
the given map is independent of the choice of lift $\hat c$ involved and in that the group structure is respected.

=--

+-- {: .proof}
###### Proof

To see that the constructon is well-defined, let $\tilde c \in B_{n}$ be another lift. Then $p(\hat c - \tilde c) = 0$ and hence 
$\hat c - \tilde c \in A_n \hookrightarrow B_n$.
This exhibits a homology-equivalence $[\partial^B\hat c]_A \simeq [\partial^B \tilde c]_A$ since
$
  \partial^A(\hat c - \tilde c) 
  = 
  \partial^B \hat c - \partial^B \tilde c$.


To see that $\delta_n$ is a group homomorphism, let $[c] = [c_1] + [c_2]$ be a sum. Then $\hat c \coloneqq \hat c_1 + \hat c_2$ is a lift and by linearity of $\partial$ we have $[\partial^B \hat c]_A = [\partial^B \hat c_1] + [\partial^B \hat c_2]$.

=--

+-- {: .num_prop}
###### Proposition

Under [[chain homology]] $H_\bullet(-)$ the morphisms in the short exact sequence together with the connecting homomorphisms yield the [[homology long exact sequence]]

$$
  \cdots
   \to
  H_n(A) \to H_n(B) \to H_n(C) 
   \stackrel{\delta_n}{\to}
  H_{n-1}(A) \to H_{n-1}(B) \to H_{n-1}(C)   
   \to
  \cdots
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider first the exactness of $H_n(A) \stackrel{H_n(i)}{\to} H_n(B) 
\stackrel{H_n(p)}{\to} H_n(C)$.

It is clear that if $a \in Z_n(A) \hookrightarrow Z_n(B)$ then the image of $[a] \in H_n(B)$ is $[p(a)] = 0 \in H_n(C)$.
Conversely, an element $[b] \in H_n(B)$ is in the kernel of $H_n(p)$ if there is $c \in C_{n+1}$ with $\partial^C c = p(b)$. Since $p$ is surjective let $\hat c \in B_{n+1}$ be any lift, then $[b] =  [b - \partial^B \hat c]$ but $p(b - \partial^B c) = 0$ hence by exactness $b - \partial^B \hat c \in Z_n(A) \hookrightarrow Z_n(B)$ and so $[b]$ is in the image of $H_n(A) \to H_n(B)$. 


It remains to see that

1. the [[image]] of $H_n(B) \to H_n(C)$ is the [[kernel]] of $\delta_n$;

1. the [[kernel]] of $H_{n-1}(A) \to H_{n-1}(B)$ is the [[image]] of $\delta_n$.

This follows by inspection of the formula in def. \ref{ConnectingForHomologyInComponents}. We spell out the first one:

If $[c]$ is in the image of $H_n(B) \to H_n(C)$ we have a lift $\hat c$ with $\partial^B \hat c = 0$ and so $\delta_n[c] = [\partial^B \hat c]_A  = 0$. Conversely, if for a given lift $\hat c$ we have that $[\partial^B \hat c]_A = 0$ this means there is $a \in A_n$ such that $\partial^A a \coloneqq \partial^B a = \partial^B \hat c$. But then $\tilde c \coloneqq \hat c - a$ is another possible lift of $c$ for which $\partial^B \tilde c = 0$ and so $[c]$ is in the image of $H_n(B) \to H_n(C)$.
 

=--



+-- {: .num_remark}
###### Remark

Of course the situation for [[cochain cohomology]] is formally dual to this situation. For convenience we repeat the statement for dual chains:

Let $A^\bullet \to B^\bullet \to C^\bullet$ be a short exact sequence of cochain complexes.

For $[c]_C \in H^n(C)$ the class of a closed element $c$, by surjectivity of $B \to C$ there is an element $\hat c \in B$ mapping to it. This need not be closed anymore, but of course $d_B \hat c$ is. By the fact that $B \to C$ is a chain map we have that the image of $d_B \hat c$ in $C$ vanishes. Therefore by the exactness of the sequence the element $d_B \hat c$ may be regarded as a closed element of $A$. The cohomology class $[d_B \hat c]_A$ of this is what the connecting homomorphism 

$$
  \delta^n : H^n(C) \to H^{n+1}(A)
$$

assigns to $[c]_C$:

$$
  \delta : [c]_C \mapsto [d_B\hat c]_A
  \,.
$$

This is indeed well defined, in that it is independent of the choice of $\hat c$: for $\hat c'$ another choice, we have that the difference $\hat c - \hat c'$ is in the kernel of $B \to C$ hence is in $A$. Then $d_B \hat c' = d_B \hat c + d_A(\hat c - \hat c')$. Hence $[d_B \hat c]_A = [d_B \hat c']_A$.

=--

### General abstract
 {#OnHomologyGeneralAbstract}

+-- {: .num_theorem}
###### Theorem

Let $0 \to A_\bullet \stackrel{f}{\to} B_\bullet \stackrel{g}{\to} C_\bullet \to 0$
be a [[short exact sequence]] of [[chain complexes]] in some [[abelian category]] $\mathcal{A}$. Then for all $n \in \mathbb{Z}$ there are natural _connecting homomorphisms_ $\partial : H_n(C) \to H_{n-1}(A)$ such that we have a [[long exact sequence]] of the form

$$
  \cdots \stackrel{g}{\to}
  H_{n+1}(C)
  \stackrel{\partial}{\to}
  H_n(A)
  \stackrel{f}{\to}
  H_n(B)
  \stackrel{g}{\to}
  H_n(C)
  \stackrel{\partial}{\to}
  H_{n-1}(A)
  \stackrel{f}{\to}
  \cdots
$$

in [[chain homology]].

=--

+-- {: .proof}
###### Proof

Applying the [[snake lemma]] to the [[commuting diagram]]

$$
  \array{
     && 0 && 0 && 0   
     \\
     && \downarrow && \downarrow && \downarrow 
     \\
     0 &\to& Z_n A &\to& Z_n B &\to & Z_n C
     \\
     && \downarrow && \downarrow && \downarrow 
     \\
     0 &\to& A_n &\to& B_n &\to & C_n &\to & 0 
     \\
     && \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{d}}     
     \\
     0 &\to& A_{n-1} &\to& B_{n-1} &\to & C_{n-1} &\to& 0
     \\
     && \downarrow && \downarrow && \downarrow 
     \\
     && \frac{A_{n-1}}{im(d)(A_n)} &\to& \frac{B_{n-1}}{im(d)(B_n)} &\to & \frac{C_{n-1}}{im(d)(C_n)} &\to & 0 
     \\
     && \downarrow && \downarrow && \downarrow 
     \\
     && 0 && 0 && 0     
  }
$$

shows that the rows in the commuting diagram


$$
  \array{
      && \frac{A_{n}}{im(d)(A_{n+1})} &\to& \frac{B_{n}}{im(d)(B_{n+1})} &\to & \frac{C_{n}}{im(d)(C_{n+1})} &\to & 0 
      \\
     && \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{d}}     
     \\
     0 &\to& Z_{n-1} A &\stackrel{f}{\to}& Z_{n-1} B &\stackrel{g}{\to}& Z_{n-1} C
  }
$$

are [[exact sequences]]. Therefore applying the [[snake lemma]] to this, once more, yields the desired long exact sequence.

=--

## Examples

+-- {: .num_example}
###### Example

The [[nLab:connecting homomorphism]] of the [[nLab:long exact sequence in homology]] induced from short exact sequences of the form 

$$
  A/A_{n tor} \stackrel{(-)\cdot n}{\to} A \to A/(n A)
$$

is called a _[[nLab:Bockstein homomorphism]]_.

=--

## Properties

### Relation to homotopy fiber sequences

The connecting homomorphism in a [[long exact sequence in homology]] induced from a short exact sequence $A_\bullet \stackrel{f}{\to} B_\bullet \to C_\bullet$ is equivalently the image under the [[homology group]] functor of the [[homotopy cofiber sequence]] induced by $f$. This is discussed in detail at _[[mapping cone]]_ in the section _[homology exact sequences](mapping+cone#HomologyExactSequencesAndFiberSequences)_.

## Related concepts

* [[long exact sequence in homology]]

  * [[long exact sequence in chain homology]]

  * [[long exact sequence in generalized homology]]

## References

For instance section 1.3 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_


[[!redirects connecting homomorphisms]]
