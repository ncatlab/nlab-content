Short exact sequences of Lie algebras are the diagrams of the form

$$ 0\to \mathfrak{k}
\overset{i}\to \mathfrak{g}\overset{p}\to\mathfrak{b}\to 0$$

where $\mathfrak{k},\mathfrak{g},\mathfrak{b}$ are Lie algebras, $i,p$ are homomorphisms of Lie algebras and the underlying diagram of vector spaces is exact, i.e. $Ker(p)=Im(i)$, $Ker(i)=0$ and $Im(p)=0$. 

We also say that this diagram (and sometimes loosely $\mathfrak{g}$ itself) is a **Lie algebra extension** of $\mathfrak{b}$ by the "kernel" $\mathfrak{k}$. Lie algebra extensions may be obtained from Lie [[group extension]]s via the tangent Lie algebra functor. 

Then each element $g \in \mathfrak{g}$ defines
a derivative $\phi(g)$ on $\mathfrak{k}$ by $\phi(g)(k) = [g,k]$.
The rule $g \mapsto \phi(g)$ defines a homomorphism of Lie algebras
$\phi : \mathfrak{g} \rightarrow Der(\mathfrak{k})$.
Indeed, 

$$\phi([g_1,g_2])(k) = [[g_1,g_2],k] =
[[g_1,k],g_2] + [g_1,[g_2,k]] = -\phi(g_2)([g_1,k]) + \phi(g_1)([g_2,k])
= [-\phi(g_2)\circ\phi(g_1) + \phi(g_1)\circ\phi(g_2)](k) = [\phi(g_1),\phi(g_2)](k),$$

for all $g_1,g_2 \in {\mathfrak g}$, for all $k \in \mathfrak{k}$.
The restriction $\phi|_{\mathfrak{k}}$ takes
(by definition) values in the Lie subalgebra $Int(\mathfrak{k})$ of inner derivatives of $\mathfrak{k}$.
If $g_1$ and $g_2$ are in the same coset, that is
$g_1 + \mathfrak{k} = g_2 + {\frak k}$,
then there is $k \in \mathfrak{k}$ with $g_1 + k = g_2$ and
such that for all $k' \in \mathfrak{k}$ we have
$\phi(g_1) + \phi(k) = \phi(g_1 + k') = \phi(g_2 + k + k') = \phi(g_2)+\phi(k + k')$ and therefore

$$\array{\phi(g_1) + Int(\mathfrak{k}) &=& \phi(g_1) + \phi(\mathfrak{k})\\ 
&=& \phi(g_1 + \mathfrak{k}) \\
&=& \phi(g_2 + \mathfrak{k}) \\
&=& \phi(g_2) + \phi(\mathfrak{k})\\
&=& \phi(g_2) + Int(\mathfrak{k}).}$$

Thus we obtain a well-defined map $\phi_* : \mathfrak{g}/\mathfrak{k} \to Der(\mathfrak{k})/Int(\mathfrak{k})$.

Choose a $k$-linear section of the projection
$\mathfrak{g} \rightarrow \mathfrak{g}/\mathfrak{k}\cong \mathfrak{b}$
and denote by $\psi$ the composition $\phi \circ \sigma$
where  $\sigma : \mathfrak{g}/\mathfrak{k} = \mathfrak{b} \rightarrow \mathfrak{g}$.
One considers the problem of reconstructing the group $\frak g$ from
the knowledge of $\psi : \mathfrak{g}/\mathfrak{k} \rightarrow Der(\mathfrak{k})$ and $\mathfrak{k}$.
In order to derive the necessary relations we
will identify $\mathfrak{g}$ with $\mathfrak{b} \times \mathfrak{k}$ (as a set).

Indeed, write each element $g \in G$ as
$\sigma(b) + k, b \in \mathfrak{g}/\mathfrak{k}$, $k \in \mathfrak{k}$ by setting $b := [g], k := -\sigma([g]) + g$. Elements $b \in \mathfrak{b}$ and
$k \in \mathfrak{k}$ in that decomposition are unique.
Thus we obtain a bijection $\mathfrak{g} \rightarrow \mathfrak{b} \times \mathfrak{k}$, $g \mapsto ([g], -\sigma([g]) + g )$.
The commutation rule has to be figured out.
If $(b_1,k_1) = g_1$, and $(b_2,k_2) = g_2$, then
\begin{equation}
[g_1,g_2] = [\sigma(b_1) + k_1,\sigma(b_2) + k_2] =
[\sigma(b_1),\sigma(b_2)] + [\sigma(b_1),k_2] - [\sigma(b_2),k_1] +[k_1,k_2].
\label{putkhilie}
\end{equation}

 Now $[\sigma(b_1),\sigma(b_2)] \in [b_1b_2]$ so it can be represented uniquely
in the form $\sigma([b_1,b_2]) + k$ where $k \in \mathfrak{k}$ can be obtained by evaluating the antisymmetric $k$-bilinear form
$\chi : \mathfrak{b} \wedge \mathfrak{b} \rightarrow \mathfrak{k}$ defined by
$\chi(b_1 \wedge b_2) = - \sigma([b_1,b_2]) + [\sigma(b_1),\sigma(b_2)]$
 on $(b_1,b_2)$.
Then formula \eqref{putkhilie} becomes
$$\array{
[g_1,g_2] & = & \sigma([b_1,b_2]) + \chi(b_1\wedge b_2)
+ \phi(\sigma(b_1))(k_2) + \phi(-\sigma(b_2))(k_1) + [k_1,k_2] \\
       & = & \sigma([b_1,b_2]) + \chi(b_1\wedge b_2) + \psi(b_1)(k_2)
        -\psi(b_2)(k_1) + [k_1,k_2].
}$$

so that

\begin{equation}
(b_1,k_1)(b_2,k_2) = ([b_1,b_2],\chi(b_1\wedge b_2) +
        \psi(b_1)(k_2) - \psi(b_2)(k_1) +  [k_1,k_2]).
\label{mrulelie}
\end{equation}

Thus all the information about the commutators is encoded
in functions $\chi : \mathfrak{n} \wedge \mathfrak{b} \rightarrow Der(\mathfrak{k})$
and $\psi : \mathfrak{b} \to Der(\mathfrak{k})$,
without knowledge of $\sigma$.

However, not every pair $(\chi,\psi)$ will
give some commutation rule on $\mathfrak{b} \times k$ satisfying Jacobi identity, and also some different pairs may lead to the isomorphic extensions. 

In order to satisfy the Jacobi identity, this pair needs to form a nonabelian 2-cocycle in the sense of [[nonabelian Lie algebra cohomology]].