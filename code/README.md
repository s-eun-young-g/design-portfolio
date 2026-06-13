# Computational design — definitions as code

Parametric design studies in Rhino + Grasshopper, presented as **code, not binary
`.gh` files**. Each definition is run through my own
[**pythongrasshopperinterp**](https://github.com/s-eun-young-g/pythongrasshopperinterp)
translator, which reads a Grasshopper definition and prints both the *parametric
system* (its driving inputs and the component pipeline) and a best-effort Python
transcription. Every study is paired with a render of the output.

<p>
  <img src="truss/truss2d.png" width="220" alt="truss canopy">
  <img src="staircase/staircase.png" width="135" alt="spiral staircase">
  <img src="icetent/icetent.png" width="135" alt="ice-shelter dome">
  <img src="branching/branching.png" width="200" alt="branching willow">
</p>

| Study | What it is | Scale |
|---|---|---|
| [truss/](truss/) | a truss canopy generated over a freeform surface | 45 components |
| [staircase/](staircase/) | a spiral staircase from 12 named parameters | 171 components |
| [icetent/](icetent/) | a faceted ice-shelter dome | 467 components |
| [branching/](branching/) | a recursive fractal tree (recursion via a loop construct) | 41 components |

Each folder holds the render, a `.describe.txt` (the parametric system read off the
definition), a `.py` (Python transcription), and the source `.ghx`.
