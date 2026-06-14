# Computational design — definitions as code

Parametric things I built in Rhino + Grasshopper (mostly for MIT's 4.500 + design
classes) — but shown as **code, not binary `.gh` blobs you can't read or diff**.
Each definition gets run through my own
[**pythongrasshopperinterp**](https://github.com/s-eun-young-g/pythongrasshopperinterp)
translator, which cracks open the Grasshopper file and prints both the *parametric
system* (the sliders + the component pipeline) and a best-effort Python
transcription. Every study comes with a render so you can see what it actually
makes. 🌱

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

> **status / honesty note:** the renders are real Rhino outputs and the
> `.describe.txt` inventories are reliable. The `.py` transcriptions are
> *best-effort* — my translator maps a bunch of components to clean Python and
> flags the rest as `gh("…")`. It's a work in progress, which is honestly half the
> fun. Want the real thing? the `.ghx` files open straight in Grasshopper.
