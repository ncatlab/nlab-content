
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[Goodwillie calculus]], an [[(∞,1)-category]] is called _differentiable_ if [[(∞,1)-functors]] to it admit "derivatives" in the form of [[n-excisive approximations]].

## Definition

+-- {: .num_defn }
###### Definition

An [[(∞,1)-category]] $\mathcal{C}$ is **differentiable** if

1. it has [[finite (∞,1)-limits]];

1. it has [[sequential limit|sequential]] [[(∞,1)-colimits]];

1. the [[(∞,1)-colimit]] [[(∞,1)-functor]] $\underset{\longrightarrow}{\lim} Func(\mathbb{N}, \mathcal{C}) \longrightarrow \mathcal{C}$ is a [[left exact (∞,1)-functor]], hence commutes with [[finite (∞,1)-limits]].

=--

## Examples

+-- {: .num_example }
###### Example

Every [[(∞,1)-topos]] is a differentiable $(\infty,1)$-category.

=--

([Lurie, example 7.1.1.8](#Lurie))

## Properties

### $n$-Excisive reflection / Taylor tower

By [[Goodwillie calculus]], [[(∞,1)-functors]] to differentiable $(\infty,1)$-categories have [[n-excisive approximations]]/[[Taylor towers]].

## References

* [[Jacob Lurie]], _[[Higher Algebra]]_
  {#Lurie}

[[!redirects differentiable (infinity,1)-categories]]

[[!redirects differentiable (∞,1)-category]]
[[!redirects differentiable (∞,1)-categories]]