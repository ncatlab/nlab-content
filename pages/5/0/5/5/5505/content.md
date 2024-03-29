
A **thread** is an element of a [[cofiltered limit]] of [[topological spaces]] (usually studied in the generality of [[projective spectrum|projective spectra]]) or (in a more rarely used terminology) of a cofiltered limit of sets.   

Thus let $F: D^{op}\to Set$ be a functor where $D$ is a [[small category|small]] [[filtered category]] (for example, a [[directed set]]). Then $lim F = lim_{d\in D} F(d)$ consists of families $(s_d)_{d\in D}$ where $s_d \in F(d)$ and for every morphism $\delta:d\to e$ in $D$, $F(\delta)(s_e) = s_d$. Such families are called _threads_. 

If $F: D^{op}\to Top$ is a functor where $D$ is a small filtered category then $lim F$ has the same underlying set (of threads) as the composition $U\circ F$ where $U:Top\to Set$ is the forgetful functor; the topology of $lim F$ is the subspace topology on $lim (U\circ F)$ understood as a subset of the Cartesian product $\prod_d F(d)$ equipped with the (product)[[Tihonov's topology]].


[[!redirects thread]]
[[!redirects threads]]
