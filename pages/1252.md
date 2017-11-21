
# (Reflexive)-transitive closures
* table of contents
{: toc}

## Of a relation

The __transitive closure__ of a binary [[relation]] $\sim$ on a [[set]] $S$ is the smallest [[transitive relation]] that contains $\sim$.

Often one wants the __reflexive-transitive closure__ of $\sim$, which is the smallest transitive relation that contains $\sim$ and is also [[reflexive relation|reflexive]].

These can be defined explicitly as follows: $ x \sim^* y$ if and only if, for some [[natural number]] $n$, there exists a sequence $(r_0, \ldots, r_n)$ such that
$$ x = r_0 \sim \cdots \sim r_n = y .$$
If you accept $0$ as a natural number, then this defines the reflexive-transitive closure; if not, then this defines the transitive closure.

For the transitive closure, it\'s also possible to rephrase the above slightly (using only $r_1$ through $r_{n-1}$) to avoid any reference to [[equality]].  Thus [[prerelations]] have transitive closures but not necessarily reflexive-transitive closures.


## Of a material set

In material [[set theory]], the __transitive closure__ of a [[pure set]] $X$ is the [[transitive set]] $X^*$ whose members are the elements of the [[downset]] of $X$ under the transitive closure (in the previous sense) of $\in$.  That is, it consists of the members of $X$, their members, their members, and so on.  The result is a [[transitive set]], the smallest transitive set that contains $X$ as a [[subset]].

Analogously, the __reflexive-transitive closure__ of $X$ may be defined as the transitive closure of the [[successor]] $X \cup \{X\}$ of $X$, or equivalently the transitive closure of $\{X\}$ itself.  Either way, this is the same as $X^* \cup \{X\}$.  This is the smallest transitive set that contains $X$ as a [[member]].  (It is not, however, normally a [[reflexive set]]; that is, it does not belong to itself.)


[[!redirects transitive closure]]
[[!redirects transitive closures]]

[[!redirects reflexive-transitive closure]]
[[!redirects reflexive-transitive closures]]
