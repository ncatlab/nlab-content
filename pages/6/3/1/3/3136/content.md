
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A lifting gerbe is a [[cohomology|cocycle]]/[[gerbe]] -- or equivalently the [[principal infinity-bundle]] that it classifies -- arising as the obstruction to the lift of a $G$-[[principal bundle]] or more generally of any $G$-[[principal infinity-bundle]], through a [[group extension|shifted central extension]]


$$
  \mathbf{B}^{n-1} A \to \hat G \to G
$$

of $G$, for some abelian group $A$.

## Definition

Such an extension is classified (or rather its [[delooping]] is) by a cocycle

$$
  \mathbf{B}G \to \mathbf{B}^{n+1} A
$$

in [[group cohomology]].

For $X \to \mathbf{B}G$ the cocycle in [[nonabelian cohomology]] classifying a $G$-[[principal bundle]] or [[principal infinity-bundle]], the corresponding lifting $A$-gerbe is the thing classified by the composite cocycle

$$
  X \to \mathbf{B}G \to \mathbf{B}^n A
  \,.
$$

## Examples

In the literature the following simplest case of the general situation is usually considered exclusively:

for $G$ an ordinary [[group]] and 

$$
  U(1) \to \hat G \to G
$$

a $U(1)$-central [[group extension]], classified by a 2-cocycle 
$\mathbf{B}G \to \mathbf{B}^2 U(1)$ in ordinary [[group cohomology]], and for $X \to \mathbf{B}G$ the cocycle of a $G$-[[principal bundle]], the corresponding lifting gerbe is given by the cocycle

$$
  X \to \mathbf{B}G \to \mathbf{B}^2 U(1)
  \,.
$$

In the literature this is often discussed in terms of the model for gerbes given by $U(1)$-principal [[bundle gerbe]]s: let $P \to X$ be the total space of the [[bundle]] classified by $X \to \mathbf{B}G$. Regard this as the [[surjective submersion]] that is part of the data of the [[bundle gerbe]] to be constructed. By principality of $P$, there is a canonical morphism

$$
  P \times_X P \to G
$$

that sends two elements in the fiber of the bundle to the unique group element that takes the first to the second. Along this morphism, form the [[pullback]] of the extension $\hat G \to G$ to get $L$ in

$$
  \array{
    L &\to& \hat G
    \\
    \downarrow && \downarrow
    \\
    P \times_X P &\to& G
  }
  \,.
$$

This $L$ is the line bundle ingredient in the lifting bundle gerbe. There is canocically a multiplication map that completes the definition.

