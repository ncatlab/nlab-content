
# Concurrency theory
* table of contents
{: toc}

## Idea

*Concurrency* (or maybe rather _parallelism_ ([Harper](#Harper))) is a joint property of several (maybe interacting) [[event structure|processes]] proceeding simultaneously. Here the word "simultaneously" indicates that the evolution of the participating processes is indexed along an irreversible [[directed object]].

## Calculi

### [[π-calculus]]

The processes can either be the nil process $0$, parallel execution $P \mid Q$, sending on channel $c$ and then continuing $\overline{c}\langle x \rangle.P$, receiving on channel $c$ and then continuing $c(x).P$, replicating a process $!P$ or introduction of a new name $(\nu x)P$.

### Rho Calculus

## Related entries

* [[parallel computing]]

* [[models for concurrency]]

* [[Directed Algebraic Topology and Concurrency]]

* [[Some geometric perspectives in concurrency theory]]

* in a wider sense also articles related to [[directed homotopy theory]], cf.

  * [[Directed Algebraic Topology]]

  * [[directed homotopy type theory]]



## References

* wikipedia [process calculus](https://en.wikipedia.org/wiki/Process_calculus)
* [[Bob Harper]], _[Parallelism is not concurrency](http://existentialtype.wordpress.com/2011/03/17/parallelism-is-not-concurrency/)_
 {#Harper}

* [[Lisbeth Fajstrup]], [[Eric Goubault]], [[Emmanuel Haucourt]], [[Samuel Mimram]], [[Martin Raussen]], [[Directed Algebraic Topology and Concurrency]]

* _The Pi calculus: toward global computing_ Rchain [blog](https://blog.rchain.coop/blog/2019/04/03/the-pi-calculus-toward-global-computing)
* zoranskoda:[[zoranskoda:distributed consensus]]

category:computer science

[[!redirects concurrency]]
[[!redirects concurrency theory]]
[[!redirects copncurrency theory]]
