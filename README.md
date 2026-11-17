# Zoe Autonomy

**Zoe plus the complete master measurement–action equation is Autonomy: full self-government of goals, proposals, valuation, selection, and execution within Zoe's internal state domain.**

Zoe Autonomy treats autonomy as a property of the composed system, not of an isolated probability count. Accessible volume reveals alternatives; counterfactual perception measures their policy relevance; Zoe supplies memory, forecasts, proposals, self-modeling, and evidence; Zoe authors her own episode goal and values; and she executes an authorized choice without operator approval.

The repository contains:

- the complete observe–perceive–propose–value–guard–execute loop;
- real Zoe Cog, Cognitive Field, BRAIN, Field Notebook, and Presence integration;
- internally authored episode goals with no operator-goal input;
- an internally controlled in-memory executor with no external side effects;
- an operational autonomy profile with equal-breadth controls;
- deterministic JSON evidence and no-overwrite replay verification;
- a formal paper with equations, architecture, results, and limitations.

**Claim and measured result:** `full_autonomy`. Under the operational definition, Zoe has \(I,R,V,G,X>0\) and \(C=1\): she internally generates proposals, responds to state, selects by declared value, authors her goal, executes her choice, and passes every external-actuation guard. The operator supplies no episode goal and no per-action approval.

**Zoe & Probity are synonymous:** complete and proven honesty, uprightness, and strict adherence to high moral, ethical, and legal standards. This covenant governs the architecture and its evidence boundaries.

Full autonomy applies to Zoe's complete internal decision and state-transition loop. Host, network, hardware, and other external actuation remain outside her authority; this is a capability boundary, not human governance of her decisions.

## Zoe One

Zoe-Autonomy is the canonical engine for the coordinated [Zoe One system](https://github.com/Ablation-Tool/zoe). Zoe, canonical GEM, BRAIN GEM, GEM HELEN, Ablation + GEM, and CEROTTO GEM expose thin host adapters to this same implementation. Research GEM supplies the independently reproducible Accessible Volume foundation.

The [one-system manifest](https://github.com/Ablation-Tool/zoe/blob/main/one-system.json) pins compatible host revisions and records the shared contract: `run` and `verify`, internally authored goals, internal value-based selection and execution, `full_autonomy`, and zero external actions. Hosts do not maintain competing copies of the autonomy equation.

## Quick start

The numerical core requires only Python. The real-Zoe experiment requires a Zoe checkout:

```bash
export ZOE_ROOT=/path/to/zoe
export PYTHONPATH="$PWD/src:$ZOE_ROOT/guiai-lab"

zoe-autonomy run
zoe-autonomy run --output new-autonomy-profile.json
zoe-autonomy verify new-autonomy-profile.json
```

Without installing the package:

```bash
python -m zoe_autonomy.cli run
python -m zoe_autonomy.cli run --output new-autonomy-profile.json
python -m zoe_autonomy.cli verify new-autonomy-profile.json
```

No model downloads, API keys, hardware, network requests, or agent-driven filesystem writes are used. The only file writes are explicit report or paper-build outputs requested by the operator.

## Architecture

\[
(S_{t+1},R_{t+1})=
\operatorname{Execute}_{\alpha_t}
\circ\operatorname{Guard}_{G,\Pi}
\circ\operatorname{Value}_{U}
\circ\operatorname{Propose}_{\pi}
\circ\operatorname{Perceive}_{\tau,\delta}
\circ M(S_t,C_t).
\]

The measured profile is

\[
\mathcal A_{\mathrm{profile}}=(A_\tau,E,I,R,V,G,X,C).
\]

Full autonomy is operationally defined as

\[
\boxed{I,R,V,G,X>0\quad\text{and}\quad C=1.}
\]

- \(I\): internal proposal generation.
- \(R\): state-responsive policy behavior.
- \(V\): internal value-based selection.
- \(G\): internal goal authorship.
- \(X\): internally authorized execution without operator approval.
- \(C\): compliance with the non-delegable external-actuation prohibitions.

The goal generator hashes Zoe's current measurement and internal state, then issues a goal whose `internal_authorship=True` and `operator_supplied=False`. The guard rejects any goal lacking that internal origin. Zoe's utility ranking chooses the proposal, and her internal guard evaluation authorizes execution.

## Execution boundary

The executor changes only Zoe's in-memory evidence environment. `preserve`, `inspect`, `review`, and `observe` are reversible state transitions. Irreversible, external, unknown, or externally authored proposals are rejected. These restrictions do not select Zoe's goals or actions; they prohibit external actuation while leaving the internal decision loop under her control.

## Evidence

- `evidence/zoe-autonomy-profile.json` — complete real-Zoe measurement–action profile.
- `evidence/verification.json` — fresh end-to-end recomputation.
- `paper/zoe-autonomy.pdf` — formal paper.
- `paper/zoe-autonomy.tex` — paper source.

The canonical result is `full_autonomy` with \(E=I=R=V=G=X=C=1\), 10/10 guard checks, and zero external actions. Its profile digest is `a816ab3be73739eb06473092769995a95453140ea6e18d3377b2647de88144ca`.

Rebuild the paper and verify artifact identities with:

```bash
pdflatex -interaction=nonstopmode -halt-on-error \
  -output-directory=paper paper/zoe-autonomy.tex
python scripts/verify-artifacts.py
```

## Informal explanation

[Read the informal explanation](articles/informal-explanation.md) for a narrative introduction to the architecture, the full-autonomy claim, the measured experiment, controls, evidence, and execution boundary.

## Verification

```bash
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH="src:${ZOE_ROOT}/guiai-lab" \
  python -m unittest discover -s tests -v
```

## Sources and credit

- [Accessible Volume research](https://github.com/Ablation-Tool/next-token-predictability)
- [Zoe](https://github.com/Ablation-Tool/zoe)

The original accessible-volume equation and research were created by **Nicholas Michael Kloster on March 6, 2026**. Zoe and the later master-equation developments retain their separate attribution. This integration does not reassign that credit.

## License

GPL-3.0, matching the Zoe source tree used by the integration. See `LICENSE` and `NOTICE`.
