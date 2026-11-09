
This page provides an index of machine-checked formalizations of mathematical constructions documented on the [[nLab]].

The index is organized by mathematical subject rather than by proof assistant. Formal verification and human semantic review are recorded separately.

\tableofcontents

## Formalizations

<details>
<summary><strong>Homotopy theory</strong></summary>

<div style="margin-left: 1.5em; padding-left: 1em; border-left: 2px solid #cccccc; margin-top: 1em; margin-bottom: 1em;">

<details>
<summary><strong>Paths and identity types</strong></summary>


<div style="margin-left: 1.25em; margin-top: 0.8em; margin-bottom: 1.5em; text-align: left;">

<div style="margin-bottom: 1.5em;">
<p><strong>Homogeneous path type</strong> <small>(FI-001)</small></p>
<p>
<strong>nLab:</strong> [[identity type]]<br>
<strong>Cubical Agda:</strong> <code>Cubical.Core.Primitives.Path</code><br>
<strong>Scope:</strong> Homogeneous path type <code>Path A a b</code>.<br>
<strong>Source:</strong> <a href="https://github.com/agda/cubical/blob/87af036ebd1c87956cf08fea44e62c7cf76392ca/Cubical/Core/Primitives.agda#L65-L66">Pinned Agda source</a>
</p>
<p><small>Classification: plausible structural correspondence.<br>
Machine verification: source verified; not independently rebuilt.<br>
Human semantic review: pending.</small></p>
</div>

<div style="margin-bottom: 1.5em;">
<p><strong>Dependent path type</strong> <small>(FI-002)</small></p>
<p>
<strong>nLab:</strong> [[identity type]]<br>
<strong>Cubical Agda:</strong> <code>Cubical.Core.Primitives.PathP</code><br>
<strong>Scope:</strong> Dependent paths in a family over the cubical interval.<br>
<strong>Source:</strong> <a href="https://github.com/agda/cubical/blob/87af036ebd1c87956cf08fea44e62c7cf76392ca/Cubical/Core/Primitives.agda">Pinned Agda source</a>
</p>
<p><small>Classification: partial correspondence; the nLab discussion is broader than the primitive presentation.<br>
Machine verification: source verified; primitive not independently rebuilt.<br>
Human semantic review: pending.</small></p>
</div>

<div style="margin-bottom: 1.5em;">
<p><strong>Path composition</strong> <small>(FI-003)</small></p>
<p>
<strong>nLab:</strong> [[equality in type theory]] (Typal equality, Transitivity)<br>
<strong>Cubical Agda:</strong> <code>Cubical.Foundations.Prelude._∙_</code><br>
<strong>Scope:</strong> Composition of paths, first <code>p</code>, then <code>q</code>.<br>
<strong>Source:</strong> <a href="https://github.com/agda/cubical/blob/87af036ebd1c87956cf08fea44e62c7cf76392ca/Cubical/Foundations/Prelude.agda#L172">Pinned Agda source</a>
</p>
<p><small>Classification: plausible structural correspondence.<br>
Machine verification: source verified; not independently rebuilt.<br>
Human semantic review: pending.</small></p>
</div>

<div style="margin-bottom: 0.5em;">
<p><strong>Identity-system characterization</strong> <small>(FI-004)</small></p>
<p>
<strong>nLab:</strong> [[equality in type theory]]<br>
<strong>1Lab:</strong> <code>1Lab.Path.IdentitySystem.identity-system-gives-path</code><br>
<strong>Scope:</strong> An identity-system witness yields an equivalence <code>R a b ≃ (a ≡ b)</code>.<br>
<strong>Source:</strong> <a href="https://1lab.dev/1Lab.Path.IdentitySystem">Official documentation</a> (revision <code>d45acb1d16acb2472ade6f1cfbad4ba00867ad1c</code>)
</p>
<p><small>Classification: partial correspondence; not the same construction as path inversion.<br>
Machine verification: source verified; no 1Lab build reproduced.<br>
Human semantic review: pending.</small></p>
</div>

</div>

</details>


<details>
<summary><strong>Dependent total spaces, homotopy fibers, and pullbacks</strong></summary>

<div style="margin-left: 1.25em; margin-top: 0.8em; margin-bottom: 1.5em; text-align: left;">

<div style="margin-bottom: 1.5em;">
<p><strong>Dependent total space</strong> <small>(FI-005)</small></p>
<p>
<strong>nLab:</strong> [[dependent type]]<br>
<strong>Cubical Agda:</strong> <code>Cubical.Core.Primitives.Σ</code> (re-exported by <code>Cubical.Data.Sigma</code>)<br>
<strong>Scope:</strong> Dependent sums of type families.<br>
<strong>Source:</strong> <a href="https://github.com/agda/cubical/blob/87af036ebd1c87956cf08fea44e62c7cf76392ca/Cubical/Core/Primitives.agda#L205-L206">Pinned Agda source</a>
</p>
<p><small>
Correspondence evidence: Both constructions represent dependent sums. This does not imply a classical lifting-property fibration.<br>
Machine verification: source verified; primitive not independently rebuilt.<br>
Human semantic review: pending.
</small></p>
</div>

<div style="margin-bottom: 1.5em;">
<p><strong>Homotopy fiber of a map</strong> <small>(FI-006)</small></p>
<p>
<strong>nLab:</strong> [[homotopy fiber]]<br>
<strong>Cubical Agda:</strong> <code>Cubical.Foundations.Equiv.Base.fiber</code><br>
<strong>Scope:</strong> Homotopy fiber of a map <code>f : A → B</code> over a point <code>y : B</code>.<br>
<strong>Source:</strong> <a href="https://github.com/agda/cubical/blob/87af036ebd1c87956cf08fea44e62c7cf76392ca/Cubical/Foundations/Equiv/Base.agda#L9">Pinned Agda source</a>
</p>
<p><small>
Correspondence evidence: The Agda declaration defines the fiber using dependent pairs and paths to the specified point.<br>
Machine verification: source verified; not independently rebuilt.<br>
Human semantic review: pending.
</small></p>
</div>

<div style="margin-bottom: 0.5em;">
<p><strong>Fiber of a dependent total-space projection</strong> <small>(FI-007)</small></p>
<p>
<strong>nLab:</strong> [[homotopy pullback]]<br>
<strong>Cubical Agda:</strong> <code>NLabMonodromy.total-hofib≃</code><br>
<strong>Scope:</strong> The equivalence <code>fiber (total-projection P) b ≃ P b</code>.<br>
<strong>Source:</strong> <a href="https://github.com/hw4375-collab/Monodromy-CubicalAgda/blob/180118e72bb3ed95ef1bf4c7e3bcdbdb2bfe74c3/agda/NLabMonodromy.agda">Verified Agda implementation</a>
</p>
<p><small>
Correspondence evidence: The formal declaration establishes the homotopy-fiber equivalence for the projection of a dependent total space; this is a specific instance related to the homotopy-pullback construction, not a formalization of every homotopy pullback.<br>
Machine verification: independently type-checked by the pilot.<br>
Human semantic review: pending.
</small></p>
</div>

</div>
</details>


<details>
<summary><strong>Monodromy</strong> — Cubical Agda</summary>

<div style="margin-left: 1.5em; margin-top: 1em; margin-bottom: 1.5em;">

<p>The construction of [[monodromy]] in [[homotopy type theory]] can be expressed through transport along paths in dependent type families.</p>

<p><strong>Formalization:</strong> Transport equivalences, loop-space monodromy, pointed transport, and induced equivalences on higher homotopy groups.</p>

<ul>
<li><a href="https://github.com/hw4375-collab/Monodromy-CubicalAgda/blob/180118e72bb3ed95ef1bf4c7e3bcdbdb2bfe74c3/agda/NLabMonodromy.agda">Agda source code</a></li>
<li><a href="https://github.com/hw4375-collab/Monodromy-CubicalAgda/blob/180118e72bb3ed95ef1bf4c7e3bcdbdb2bfe74c3/paper/main.pdf">Shadow Paper</a></li>
<li><a href="https://github.com/hw4375-collab/Monodromy-CubicalAgda/tree/180118e72bb3ed95ef1bf4c7e3bcdbdb2bfe74c3/alignment">Mathematics-to-code alignment</a></li>
<li><a href="https://github.com/hw4375-collab/Monodromy-CubicalAgda">GitHub repository</a></li>
</ul>

<p><strong>Verification:</strong> Agda 2.8.0, Cubical Library v0.9 — type-checked.</p>

<p><strong>Human mathematical and semantic review:</strong> Pending.</p>

<p><em>Scope limitation: The complete fundamental-group action on fixed-basepoint higher homotopy groups has not yet been formalized.</em></p>

</div>
</details>

</div>
</details>

## Related resources

* [[nLab materials]]
* [[formalized libraries of homotopy type theory]]
* [[proof assistants and formalization projects -- list]]
