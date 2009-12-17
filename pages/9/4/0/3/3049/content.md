Given a [[comonad]] $\mathbf{G}=(G,\delta,\epsilon)$ in a category $A$, a [[natural transformation]]
$t : GG\rightarrow GG$ is **a symmetry** of $\mathbf{G}$
if it sastisfies the quantum Yang-Baxter equation (transposed braid relation)

$$
G(t) t_G G(t) = t_G G(t) t_G
$$

and also

\begin{equation}\label{symmG}
t^2 = 1_{GG},\,\,\,\,t\delta = \delta,\,\,
\,\,\,\epsilon_G t = G(\epsilon),\,\,\,
\delta_G t = G(t) t_G G(\delta)\end{equation}
In that case, the pair $(G,t)$ is called a **symmetric comonad.

The [[simplicial set]] obtained by the standard construction from a symmetric comonad has always a structure of a [[symmetric simplicial set]].

* M. Grandis, Finite sets and symmetric simplicial sets,
Theory of Applications of Categories,
Vol. 8, No. 8, pp. 244--253, [link]().

* Z. &#352;koda, Cyclic structures for simplicial objects from comonads, [math.CT/0412001](http://arxiv.org/abs/math.CT/0412001).
