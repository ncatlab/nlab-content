
# Specker sequences
* table of contents
{: toc}

## Definition

A __Specker sequence__ is a [[bounded function|bounded]] [[computable function|computable]] [[increasing function|increasing]] [[infinite sequence]] of [[rational numbers]] with no [[computable number|computable]] [[supremum]].


## Examples

Since there is a sequence of all [[Turing machine|Turing machines]], define a sequence $(S_n)_n$ as
$$ S_n = \sum_{i + j = n} 2^{-i} \{i\}_j ,$$
where $\{i\}_j$ is the [[bit]] ($0$ or $1$) giving whether the $i$th Turing machine halts before $j$ steps.  The theoretical limit of this sequence is
$$ \sum_i 2^{-i} \{i\} ,$$
where $\{i\}$ is the bit giving whether the $i$th Turing machine halts at all, but this is uncomputable (on pain of solving the [[halting problem]]).

Many famous non-computable numbers may be expressed as limits of Specker sequences.  For example, a [[Chaitin constant]] is defined as the sum of an [[infinite series]] with non-negative computable terms (each of which is a [[dyadic rational]]), and so is the limit of a Specker sequence.


## In constructive mathematics

In [[Russian constructivism]], all [[real numbers]] are computable, so a Specker sequence has no (located) supremum, giving a counterexample to the [[classical mathematics|classical]] [[least upper bound principle]] ($LUP$).

In many other varieties of [[constructive mathematics]], the computability of all real numbers can be neither proved nor refuted, but Specker sequences still provide [[weak counterexample|weak counterexamples]].

For a non-computable number that can be expressed as the limit of a Specker sequence, the sequence itself is a way to work with the number in constructive mathematics without assuming that it exists as a real number.  (This amounts to treating it as a computable [[lower real number]].)


[[!redirects Specker sequence]]
[[!redirects Specker sequences]]
