# Defunctionalization
* table of contents
{: toc}

## Idea

_Defunctionalization_ is a method of converting a [[functional programming|functional program]] into one that involves no higher order functions nor lambda expressions. It is a whole program transformation. 

## Program transformation

The idea is it to consider a type $Defun(A,B)$ for every pair of types $A,B$ as a proxy for the true [[function type]] $A\to B$. 
This type $Defun(A,B)$ is a [[coproduct]]
$$
 Defun(A,B)=\coprod_{x_1:C_1,\dots,x_n:C_n\, \vdash \,\lambda y.\,t\,  :\,  A\to B}C_1\times \dots \times C_n
$$ 
over all [[lambda abstractions]] $\lambda y.\,t$ that appear syntactically in the program. Notice that lambda abstractions may have free variables $x_1:C_1,\dots,x_n:C_n$, because they may appear deep inside the program. 
An inhabitant of the type $Defun(A,B)$ is sometimes called a _closure_, because it is a syntactic expression together with an environment: a valuation for its free variables.

The type $Defun(A,B)$ has a canonical evaluation function 
$eval:Defun(A,B)\times A\to B$
roughly given by
$$
 eval(((x_1:C_1\dots x_n:C_n\vdash \lambda y.\,t:A\to B),(x_1,\dots x_n)),y)=t
$$
and so it behaves like a function space.

Since $A$, $B$ and the $C_i$’s can also be defunctionalized, this is a method to transform a whole functional program into one with no lambda expressions nor any true function types. 

The coproduct type $Defun(A,B)$ is typically not a true function space in the sense of [[cartesian closed categories]] for two reasons. 

* it does not admit arbitrary lambda abstractions -- just the lambda abstractions that happen to be included in the coproduct. 

* it does not equate lambda abstractions that are semantically equal but syntactically different. 

(Thus it violates both existence and uniqueness in the universal property.)

## Connection to adjoint functor theorems

Recall that a cartesian [[internal hom]] $B^A$, if it exists, is a [[representable functor|representation]] of $Hom(-\times A,B)$. 
As such, in many concrete situations, we can deduce its existence from an [[adjoint functor theorem]]. 
Recall that the [[solution set condition]] in this instance requires a set $I$ and an $I$-indexed family of objects $C_i$ 
together with morphisms
$$
 f_i:C_i\times A\to B
$$
such that every morphism $f:C\times A\to B$ factors as 
$$
 C\times A \stackrel{g\times A}\to C_i\times A\stackrel{f_i}\to B
$$
for some $i\in I$ and $g\colon C\to C_i$. 
Then, as is usually observed, the coproduct 
$$
 \coprod_{i\in I}C_i
$$
is a weak internal hom, from which the internal hom is recovered by taking a [[coequalizer]]. This coproduct is strongly reminiscent of the coproduct type $Defun(A,B)$ used in defunctionalization. 

## Example
Consider the [[factorial]] function in [[continuation-passing style]], written in [[Haskell]]:

    factcps :: Integer -> (Integer -> Integer) -> Integer
    factcps x k = if x == 0 then k 1 else factcps (x-1) (\y -> k (x * y))

    fact :: int -> int
    fact x = factcps x (\x -> x)

The idea is that `factcps x k` calculates the factorial of `x` but does not return the result, instead, it calls the "continuation" `k` with the result. Since `fact 5` calls `factcps 5` with the identity function, it will eventually return `120`. 

If this is the whole program, then there are only two [[lambda abstractions]] we need to deal with, both of type `Integer -> Integer`. The first one `\y -> k (x * y)` has free variables `x` and `k`; we'll call it `Multiply`. The second `\x -> x` has no free variables; we'll call it `Identity`.

To defunctionalize this we define a type `DefunIntInt`, which is $Defun(Integer,Integer)$ above:

    data DefunIntInt = Multiply Integer DefunIntInt | Identity
    eval :: DefunIntInt -> Integer -> Integer 
    eval (Multiply x k) y = eval k (x * y)
    eval (Identity) x = x

And now we can write the program without [[lambda abstractions]]:

    factcps :: Integer -> DefunIntInt -> Integer
    factcps x k = if x == 0 then eval k 1 else factcps (x-1) (Multiply x k)

    fact :: Integer -> Integer
    fact x = factcps x Identity

In fact, in this example, the type `DefunIntInt` is isomorphic to the type of integer lists, and squinting slightly it can be seen as a call stack. 

## References

Defunctionalization was probably introduced by John Reynolds in 

* [[John C. Reynolds]], Definitional Interpreters for Higher-Order Programming Languages. In Proceedings of the Annual ACM Conference. 1972.  [pdf]( https://homepages.inf.ed.ac.uk/wadler/papers/papers-we-love/reynolds-definitional-interpreters-1998.pdf)

There and elsewhere a common theme is to first convert programs to [[continuation-passing style]], which makes the control stack explicit, and then to defunctionalize, which makes the control stack look like a stack; the net result is a kind-of abstract machine. 
