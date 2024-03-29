
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Sweedler notation_ is a special notation for discussion of operations in [[coalgebra]]s

## Definition

If $C$ is a [[coassociative coalgebra|coassociative]] [[coalgebra]] and then for $c\in C$, the comultiplication $\Delta$ maps $c$ to an element in $C\otimes C$ which is therefore a sum of the form $\sum_{i=1}^n a_i\otimes b_i$. Sweedler suggests that we do not make up new symbols like $a$ and $b$ but rather use composed symbols $c_{(1)}$ and $c_{(2)}$. Therefore

$$\Delta(c) = \sum_{i=1}^n c_{(1)i}\otimes c_{(2)i}.$$

Sweedler notation means that for certain manipulations involving just generic **linear** operations we actually do not need to think of the summation symbol $i$, so we can just write

$$\Delta(c) = \sum c_{(1)}\otimes c_{(2)} $$

with or even without summation sign. Surely in either case we need to remember that we do not have a factorization but we do have a sum of possibly more than one entry. One can formalize in fact which manipulations are allowed with such a reduced notation. 

It becomes more useful when we take into account coassociativity to justify extending the notation to write

$$ \array{\sum c_{(1)}\otimes c_{(2)} \otimes c_{(3)} := \sum c_{(1)(1)}\otimes c_{(1)(2)}\otimes c_{(2)} \\
= \sum c_{(1)}\otimes c_{(2)(1)}\otimes c_{(2)(2)}.}$$

Furthermore, we can extend it to [[coactions]], e.g. $\rho:V\to V\otimes C$, by $\rho(v) = \sum v_{(0)}\otimes v_{(1)}$. Then we can use the coaction axiom $(id_V\otimes \Delta)\circ\rho = (\rho\otimes id_C)\circ \rho$ to write

$$ \array{v_{(0)}\otimes v_{(1)} \otimes v_{(2)} := v_{(0)(0)}\otimes v_{(0)(1)} \otimes v_{(1)}\\
= v_{(0)}\otimes v_{(1)(0)}\otimes v_{(1)(1)},}$$

where we used the *sumless* Sweedler notation.

One big use is that the scalars like $\epsilon(a_{(3)})$ can be moved freely along the expression, which is difficult to write without calculating with Sweedler components: one would need lots of brackets and flip operators, and this could be messy and abstract.

## References

The notation is named after [[Moss Sweedler]]. Sometimes (though rarely) it is also called Heyneman-Sweedler notation. 
