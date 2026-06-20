# XPMP — Experimental Metaphysics

*A process-ontology of perception, built in working code and carried across many bridges to the
empirical disciplines.*

**Status:** research sandbox · soft (conceptual + simulation) work · runs on CPU in an isolated venv.
**Implied reader:** a master's student in neuroscience or biology — someone fluent in predictive
coding, the Bayesian brain, and dynamical systems, and rightly allergic to metaphysics that cannot
be made to do any work. This README is written for you. Nothing here asks you to believe anything;
it asks you to check whether a structure is preserved.

---

## 1. What this repository is

This is a small, honest attempt to take a *monistic* account of perception — the kind associated with
Ernst Mach and Steven Lehar — and (a) make a piece of it run as a simulation, then (b) translate that
piece into vocabularies a STEM reader already trusts. The translations are the main intellectual
product. We call the method of building them the **Cobordic Programme** (§4). The metaphysics it
translates we call **XPMP** (§2).

If you read nothing else: there is a runnable toy model (`reality_vs_expectation.py`) that produced a
result none of us hand-coded — a prediction error that *refuses to reach zero* under quieting, and
reaches zero only under a structurally different operation. §3 is about why that small fact is
interesting to a neuroscientist. The rest is the apparatus for talking about it without category
errors.

---

## 2. What XPMP is

**XPMP = experimental metaphysics.** Its base commitment is **neutral / process monism**: perception
and reality are not two things standing in a correspondence (map vs. territory), but *one* process
under an equivalence. The world-as-experienced is the only world a system ever occupies. This is not
idealism ("it's all mind") and not eliminative physicalism ("it's all neurons"); it is the older,
stranger claim that *the felt world and the physical world are two aspects of a single happening.*

Four load-bearing terms, in your dialect:

- **Witness user (wu).** A perceptual process — "what it is like to be like something." Operationally,
  a generative-model-bearing system rolling out experience over time. Think of it as a Bayesian/
  active-inference agent, but with one extra commitment (below).
- **`3+1` — the roll-out.** The lived trajectory: three spatial degrees of freedom along one proper-
  time axis. In code it is a point `r(t) ∈ ℝ³` drifting toward an attractor under irreducible noise.
- **`3.d+1` — the emulator.** The wu does not only model the *world*; it models *its own roll-out.*
  The fractional `d ∈ [0,1]` (not a literal Hausdorff dimension — a pragmatic dial) is the **fraction
  of dynamics spent self-modeling.** `d = 0`: no self-model. Large `d`: heavy "model-based processing."
- **Dual-aspect nondualism.** One ground, two irreducible modes of presentation — first-person and
  third-person — that never collapse into each other. We call this the *symmetric asymmetry.*

The single extra commitment beyond standard predictive processing is the one worth your attention:
**the witness performs generative modeling of the *experience of the perceptual process itself*,** not
only of external causes. The object of the model includes the modeling.

**The self-evidencing argument.** You never perceive your own neural substrate first-person; it
appears only third-person, after the fact, on someone else's ECoG or fMRI. XPMP treats that *asymmetry
of access* not as a puzzle to be explained away but as the signature of the monism. You cannot see
your own brain for the same reason a Markov blanket's internal states do not appear to themselves as
objects: the substrate is the *condition* for there being a perceived world, not an item within it.
(§4 sharpens "condition, not item" into a precise statement physicists already accept.)

---

## 3. Why a neuroscientist or biologist might care

Not because XPMP is an empirical theory — it is not, and §5 says so plainly. Because it is a *stance*
that generates legible, sometimes sharp, sometimes testable structure:

1. **A principled reason for substrate-invisibility.** "The brain can't observe itself" usually gets
   waved at with words like *recursion* or *blind spot*. XPMP gives it a structural form (§4, the
   sheaf with no global section) identical to quantum contextuality — *there is no view from nowhere,
   only contextual local sections.* That is a non-mystical, importable way to state a fact you already
   half-believe.

2. **A model that distinguishes equanimity from cessation — quantitatively.** The toy model sweeps the
   self-modeling fraction `d` and measures prediction error `PE = ‖e − r‖`. Two regimes fall out that
   the contemplative literature usually blurs:
   - **Quieting** (`d → 0`, self-model attenuated but present): `PE` drops but hits a **nonzero floor**.
     The act of *observing* a noisy roll-out costs a residual lag no matter how silent the model goes.
   - **Dissolution** (no emulator at all, `e ≡ r`): `PE` is **identically zero** — a structurally
     different operation, not the limit of the first.

   The model handed us `lim_{d→0} PE > 0` while `PE|_{dissolved} = 0`. If you work in contemplative
   neuroscience (jhana, "cessation," non-dual states), that is a concrete, *qualitative* prediction:
   the neural signature of deep equanimity should differ in kind, not merely in degree, from the
   signature of a self-model going offline. One is a near-identity transformation; the other is the
   identity. (See §4, Figures in `blog.md`.)

3. **A clean, runnable intuition pump for active inference** — observation vs. enaction as a *two-way*
   coupling (the model writes back onto the world it models), prediction error as divergence, precision
   as a knob — in ~150 lines, with every parameter annotated as the metaphysical commitment it encodes.

4. **A meta-skill: relating first-person frameworks to third-person measurement without category
   errors.** This is the Cobordic Programme, and it is arguably the most exportable thing here.

---

## 4. The Cobordic Programme — the justifiable bridge

Here is the heart of it, and the part to read slowly.

XPMP's phenomenality is, by its own lights, **intellectually imperceptible** from the empirical
outside: you cannot hand a skeptic the first-person ground directly. So XPMP needs *bridges* — ways to
carry its structure into domains a STEM audience already trusts. But a bridge that made mathematics
(or semiotics, or neurology) the **foundation** of XPMP would betray the monism: it would smuggle the
territory inside one of its maps. The programme's whole discipline is to build bridges that **translate
without subordinating.**

We borrow a word from topology. A **cobordism** is a structure `W` whose boundary is two separate
spaces `M ⊔ N`; it *joins* them while letting neither contain the other. A **Cobordic bridge** is, by
analogy, a structure-preserving correspondence whose two boundaries are *phenomenal XPMP* and *some
empirical domain*, joined with genuine passage across and **no collapse of one into the other.**

> **The bridgeless bridge.** The joke, and the teaching, is that the two shores were never actually
> two — that is what monism *means*. So every bridge is provisional: a raft, not a foundation; a finger
> pointing, not the moon. And because there is *no global section* — no view from nowhere — there can
> be **no single master-bridge** that subsumes the rest. What you get instead is an **atlas of partial
> charts.** The programme *is* that atlas. Its plurality is not a weakness to be unified away; it is
> forced by the metaphysics it serves.

**Category theory is exactly one chart.** It is a good one — rigorous, current, and already used by
physicists for contextuality — which is why we built it first (`blog.md §II`). In that chart the bridge
is literally a **profunctor** (a relation between categories that privileges neither), the witness is a
**lens** (`get` = observation, `put` = enaction: one morphism, two irreducible aspects), the self-
modeling fraction `d` lives in a **Para** wrapper (the home of learning / active inference), and "you
cannot see your own brain" becomes "**a sheaf can be locally seamless yet have no global section**"
(structurally the Kochen–Specker theorem). But none of this is XPMP's foundation. It is one frame of
the bridgeless bridge — one chart in the atlas. Swap the chart and the same phenomenality reappears
under different, equally non-foundational coordinates:

| Bridge | Empirical/intellectual frame it speaks to | Status |
|---|---|---|
| **II. Category-theoretic** | profunctors, lenses, sheaves/topoi, operads; categorical cybernetics | **built** (`blog.md §II`, `category_theory_bridge.md`) |
| **III. Semiotic** | Peirce's signs and indices — perception as sign-action | planned |
| **IV. Scale-invariant** | renormalization, fractal/scale-free structure; the fractional `d` revisited | planned |
| **V. Neurological** | predictive coding, active inference, Markov blankets, what ECoG can/can't see | planned |
| **VI. Geometry processing** | the roll-out as a manifold; discrete differential geometry of the witness | planned |
| **VII. "Hippie"** | direct first-person contemplative report — the vernacular of experience | planned |

Each row is a *cobordism*: phenomenal boundary on one side, an empirical boundary on the other, joined
without either swallowing the other. No row is privileged. The atlas is the point.

The name nods, deliberately, to the Erlangen and Langlands programmes — research programmes that unify
by exhibiting bridges rather than by reduction. The difference: those seek a deeper *common* structure.
The Cobordic Programme denies there is a single one to seek, and makes that denial — the missing global
section — its organizing principle.

---

## 5. Honest disclaimers (read these)

- **XPMP is metaphysics, not an empirical theory.** The bridges give it *legible structure*, not
  *empirical confirmation.* A preserved structure is not evidence; it is intelligibility.
- **The simulations are toy models.** Arbitrary-but-meaningful numbers chosen to *illustrate* a
  framework, not to fit data. The residual-gap result is a property of the model's construction — which
  is exactly why it is interesting (we did not put it there by hand), and exactly why it is not proof
  of anything about brains. Treat it as a hypothesis generator.
- **The strongest objection — "you have described, not explained" — is correct.** It was the
  commission. The programme claims only constraint-bearing *description that travels*. The line between
  that and crackpottery is the entire reason the bridges are built carefully.
- **A broken bridge does not refute XPMP.** Because each bridge is a non-faithful translation, breaking
  the model breaks the *map*, not the territory. This is a feature of the method, stated honestly, not
  an escape hatch invented after the fact — it is the precise meaning of "XPMP does not presuppose
  mathematics (or any frame) as a subset of itself."

---

## 6. What's in the repo

| File | What it is |
|---|---|
| `reality_vs_expectation.py` | The core toy model: reality `3+1` vs. expectation `3.d+1`, coupled, with the `d`-sweep. Produces Figure I.1. |
| `emusim3p1.py` | The same witness *retyped* as a `Para(Lens)`; measures hom-distance to the identity lens and proves the residual-gap-as-near-identity claim. Produces Figure I.2. |
| `ct_diagrams.py` | The six category-theory diagrams (Figures 1–6), each with a baked-in caption. |
| `blog.md` | The essay: §I the residual gap, §II the category-theoretic bridge (with figures), §III–VII the other bridges (forthcoming). |
| `category_theory_bridge.md` | Long-form notes behind §II — the rigorous version of Bridge II. |
| `figures.md` | Standalone index of the diagrams. |
| `chatlog.md` | The working transcript the essay grew out of. |

### Quickstart

Everything runs CPU-only inside an isolated environment named `experimental_metaphysics` (so your
system/global packages stay untouched):

```bash
python3 -m venv experimental_metaphysics
./experimental_metaphysics/bin/pip install numpy matplotlib

./experimental_metaphysics/bin/python reality_vs_expectation.py   # -> reality_vs_expectation.png
./experimental_metaphysics/bin/python emusim3p1.py                # -> emusim3p1.png  (+ prints the proof)
./experimental_metaphysics/bin/python ct_diagrams.py              # -> fig1..fig6 .png
```

---

## 7. Mini-glossary

- **Witness user (wu)** — a perceptual process; an experiencing system that rolls out a world.
- **`3+1` / `3.d+1`** — the lived roll-out / the roll-out *plus* a self-model, `d` = how much self-model.
- **Prediction error (`PE`)** — `‖e − r‖`, the divergence between expectation and reality (Active Inference).
- **Residual gap** — the nonzero `PE` floor that survives quieting; the "cost of still looking."
- **Dual-aspect nondualism** — one ground, two irreducible aspects (first/third person): the *symmetric asymmetry.*
- **Cobordism / Cobordic bridge** — a structure joining phenomenal and empirical boundaries without subordinating either.
- **Bridgeless bridge** — the reminder that the two shores were never two, and that no master-bridge exists; hence an atlas of partial charts, not one foundation.

---

*Soft research lives here on the Mac; the biophysics (GPU) work lives elsewhere. Numbers are arbitrary
but meaningful — every parameter is a metaphysical commitment written down as a float.*
