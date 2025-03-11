
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Concurrency theory
* table of contents
{: toc}

## Idea

In the theory of [[computation]], *concurrency* (or maybe rather _parallelism_, cf. [Harper 2011](#Harper11)) refers to the situation of several (maybe interacting) [[event structure|processes]] proceeding simultaneously. Here the word "simultaneously" indicates that the evolution of the participating processes is indexed along an irreversible [[directed object]].

## Calculi

### π-Calculus

With [[π-calculus]], the processes can either be the nil process $0$, parallel execution $P \mid Q$, sending on channel $c$ and then continuing $\overline{c}\langle x \rangle.P$, receiving on channel $c$ and then continuing $c(x).P$, replicating a process $!P$ or introduction of a new name $(\nu x)P$.


### $\rho$-Calculus

(...)

## Related entries

* [[parallel computing]]

* [[models for concurrency]]

* [[Directed Algebraic Topology and Concurrency]]

* [[Some geometric perspectives in concurrency theory]]

* in a wider sense also articles related to [[directed homotopy theory]], cf.

  * [[Directed Algebraic Topology]]

  * [[directed homotopy type theory]]



## References

* Wikipedia: *[Process calculus](https://en.wikipedia.org/wiki/Process_calculus)

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Concurrency_(computer_science)">Concurrency (computer science)</a>*

* {#Harper11} [[Bob Harper]]: _[Parallelism is not concurrency](http://existentialtype.wordpress.com/2011/03/17/parallelism-is-not-concurrency/)_ (2011)
 

* [[Lisbeth Fajstrup]], [[Eric Goubault]], [[Emmanuel Haucourt]], [[Samuel Mimram]], [[Martin Raussen]]: *[[Directed Algebraic Topology and Concurrency]]*

* _The Pi calculus: toward global computing_ Rchain (2019) &lbrack;[blog](https://blog.rchain.coop/blog/2019/04/03/the-pi-calculus-toward-global-computing)&rbrack;

* [[Zoran Skoda]]: *[[zoranskoda:distributed consensus]]*

category:computer science

[[!redirects concurrency]]
[[!redirects concurrency theory]]
[[!redirects copncurrency theory]]
