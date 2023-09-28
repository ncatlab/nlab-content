
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[quantum channel]]

$$
  chan \,\colon\,
  \mathscr{H}_1 \otimes \mathscr{H}^\ast_1
  \longrightarrow
  \mathscr{H}_1 \otimes \mathscr{H}^\ast_1  
$$

is called *unital* if it preserves the [[maximally mixed quantum state]].

In any [operator-sum decomposition](quantum+channel#QuantumChannelsAndDecoherence) of the channel as

$$
  chan
  \;\colon\;
  \rho
  \;\mapsto\;
  \underset{s}{\sum}
  \,
  E_s \cdot \rho \cdot E_s^\dagger
$$

this means that not only 

$$
  \underset{s}{\sum} \, E_s^\dagger \cdot E_s
  \;=\;
  id_{\mathscr{H}_1}
$$

(reflecting the preservation of the [[trace]] of [[density matrices]]) but also

$$
  \underset{s}{\sum} \, E_s \cdot E_s^\dagger
  \;=\;
  id_{\mathscr{H}_2}
  \,.
$$


## Related concepts

* [[unistochastic quantum channel]]

## References

See most references on *[[quantum channels]]*.

* [[Christian Mendl]], *Unital Quantum Channels*, talk (2007) &lbrack;[pdf](http://christian.mendl.net/science/talks/ringberg%202007.pdf)&rbrack;



[[!redirects unital quantum channels]]


