
The possibly most evident definition of equivalences as [[quasi-inverse functions]] suffers from the drawback that the type 

$$
  f \colon A \to B
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  qinv(f)
  \coloneqq
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \,,
$$

which may naively look like it merely detects whether $f$ is an equivalence, is in fact *not* a [[mere proposition]] ([UFP13, Thm. 4.1.3](#UFP13)).

This means that the type

\[
  \label{TheSubtlyWrongTypeOfEquivalences}
  \underset{
    f \colon A \to B
  }{\sum}  
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
\]

is --- despite its possible superficial appearance (cf. &lbrack;[Hofmann & Streicher (1998) --- §5.4](#HofmannStreicher98)&rbrack;), *not* in fact equivalent to the correct type of equivalences $Equiv(A,B)$, which is instead given by including a [[0-truncation]] ${[-]_{0}}$

