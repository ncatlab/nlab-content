\tableofcontents

## Idea

The *binomial types* or *binomial sets* are the [[categorification]] of the [[binomial coefficients]] and the extensions from [[finite types]]/[[finite sets]] to arbitrary types or sets. 

## Definition

In [[type theory]], given types $A$ and $B$, the **binomial type** of $A$ and $B$ is defined as

$$\left(\begin{array}{c}A \\ B\end{array}\right) \coloneqq \sum_{f:A \to \mathbb{2}} \left[B \simeq \sum_{a:A} f(a) =_\mathbb{2} 1\right]$$

The above definition could also be translated directly into [[set theory]] notation as follows: 

$$\left(\begin{array}{c}A \\ B\end{array}\right) \coloneqq \biguplus_{f \in \mathbb{2}^A} \left[B \cong \{a \in A \vert f(a) = 1\}\right]$$

where $\left[A\right]$ is the [[support of a set|support]] of set $A$ and $\mathbb{2}^A$ is the [[function set]] with domain $A$ and codomain $\mathbb{2}$. This results in **binomial sets**. 

### Locally small binomial types

There is an alternate way to express the second definition, by use of a [[univalent universe]] instead of deloopings and loop space types, but the resulting type is only locally small relative to the universe. 

We define the type of decidable embeddings as the type of functions whose fibers are decidable:
$$A \hookrightarrow_d B \coloneqq \sum_{f:A \to B} \prod_{b:B} \left(\sum_{a:A} f(a) =_B b\right) \vee \neg \left(\sum_{a:A} f(a) =_B b\right)$$ 

Let $(U, \mathrm{El})$ be a [[univalent Tarski universe]], and given type $A$, let us define $U_A$ to be the type of all types in $U$ which are merely equivalent to $A$:
$$U_A \coloneqq \sum_{X:U} \left[A \simeq \mathrm{El}(X)\right]$$
Then given [[essentially small type|essentially $U$-small types]] $A$ and $B$, the locally $U$-small binomial type is defined as 
$$\left(\begin{array}{c}A \\ B\end{array}\right)_U \coloneqq \sum_{X:U_B} \left[\mathrm{El}(X) \hookrightarrow_d A\right]$$

## See also

* [[binomial theorem]]
* [[categorification]]

## References

The above definitions of binomial types could be found respectively in remark 17.6.7 and definition 17.6.7 of:

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects binomial type]]
[[!redirects binomial types]]

[[!redirects binomial set]]
[[!redirects binomial sets]]