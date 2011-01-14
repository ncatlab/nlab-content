The spectral sequence $E_{(n)}^{p,q}$ of a $\mathbb{Z}$-filtered graded cohomology complex $d:F_i{C_j} \to F_i C_{j+1}$ is a tool for organizing data derivable from the families of long exact cohomology sequences
$$ \cdots\to H^j (F_i) \to H^j (F_{i+1}) \to H^j(F_{i+1}/F_i) \to H^{j+1}(F_i)\to\cdots $$

#### Definition
The whole of the spectral sequence can be defined as the spectral sequence of the [exact couple](spectral+sequence#exact_couples)

$$ D\overset{\varphi}{\to} D \to E \to D $$

where $D = \bigoplus_i H^{\bullet}(F_i)$, where $\varphi$ is the cohomology morphism induced by the inclusion of chain complexes $F_i\to F_{i+1}$ and $E = \bigoplus_i H^\bullet(F_i/F_{i-1})$, the total cohomology of the associated bigraded complex.  (The usual bigrading of the initial term is a bit weird maybe, but we'll get used to that.)

At every stage we have a new family of long exact sequences

#### Convergence, ideally

It is instructive to note that in the $n$th derived exact couple $\varphi^n D\to E_{(n)} \to \varphi^n D\to{}$, the hidden part $\varphi^n D$ is the submodule $D_{(n)}$ of $\bigoplus_{i} H(F_{i+n})$ representable by elements of $F_i$; that is, we may sensibly call it
$$F_{i} D_{(n)} = \frac{\ker(d)\cap F_i}{F_i\cap dF_{i+n}}.$$
Separating the grades, the exactness of the couple at $E_{(n)}$ then says 
$$ F_{i} H^j(F_{i+n})\to F_{i+1}H^j(F_{i+n+1}) \to E_{(n)}^{i\dots} \to F_i H^{j+1}(F_{i+n}) \to F_{i+1}H^{j+1}(F_{i+n+1}) $$

One can see this as converging (if it sensibly converges) to either a subquotient of $F_i$ _or_ to a submodule $F_i H^\bullet(C) \lt H^\bullet(C)$.  Taking the latter interpretation, we hope to find in the limiting case exact sequences
$$ F_i H^j(C)\to F_{i+1} H^j(C) \to E_{(\infty)}^{i\dots} \to F_i H^{j+1}(C) \to F_{i+1} H^{j+1}(C).$$
At this stage one can check that the morphisms $F_i H^j(C)\to F_{i+1} H^j(C)$ are indeed definable, and in fact injective, so that whatever $E_{(\infty)}$ should be, the morphism $E_{(\infty)}^{i\dots}\to F_i H^{j+1}$ is null; that is, our long-exact sequence breaks up into the short exact sequences
$$ 0\to F_i H^j(C) \to F_{i+1} H^j(C)\to E_{(\infty)}^{i\dots} \to 0 .$$

In summary, if the spectral sequence $E_{(n)}$ converges in a sensible way to the correct thing $E_{(\infty)}$, then that correct thing is also the associated graded module of the filtration of $H^\bullet(C)$ induced by the filtration of $C$.