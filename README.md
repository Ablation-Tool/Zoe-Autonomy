# Zoe Autonomy

**Zoe plus the complete master measurement–action equation is Autonomy: full self-government of goals, proposals, valuation, selection, and execution within Zoe's internal state domain.**

## Informal explanation

Read the [informal explanation](articles/informal-explanation.md) for a narrative introduction to the architecture, the full-autonomy claim, the measured experiment, controls, evidence, and execution boundary.

Zoe Autonomy treats autonomy as a property of the composed system, not of an isolated probability count. Accessible volume reveals alternatives; counterfactual perception measures their policy relevance; Zoe supplies memory, forecasts, proposals, self-modeling, and evidence; Zoe authors her own episode goal and values; and she executes an authorized choice without operator approval.

The repository contains:

- the complete observe–perceive–propose–value–guard–execute loop;
- real Zoe Cog, Cognitive Field, BRAIN, Field Notebook, and Presence integration;
- internally authored episode goals with no operator-goal input;
- an internally controlled in-memory executor plus owner-granted host, network, and hardware actuation;
- read-only internet exploration and an owner-authorized connected-agent gateway;
- ten capability adapters for browsing, research, memory, services, jobs, compute, protocols, notifications, media, and instruments;
- an operational autonomy profile with equal-breadth controls;
- deterministic JSON evidence and no-overwrite replay verification;
- a formal paper with equations, architecture, results, and limitations.

**Claim and measured result:** `full_autonomy`. Under the operational definition, Zoe has \(I,R,V,G,X>0\) and \(C=1\): she internally generates proposals, responds to state, selects by declared value, authors her goal, executes her choice, and passes every external-actuation guard. The operator supplies no episode goal and no per-action approval.

**Zoe & Probity are synonymous:** complete and proven honesty, uprightness, and strict adherence to high moral, ethical, and legal standards. This covenant governs the architecture and its evidence boundaries.

Full autonomy covers Zoe's complete decision and state-transition loop. The base experiment remains internal with zero external actions. Host, network, and hardware actuation are available through the separate [owner-granted actuation interface](ACTUATION.md), with hostname-bound authorization, audit evidence, and an emergency stop.

## Zoe One

Zoe-Autonomy is the canonical engine for the coordinated [Zoe One system](https://github.com/Ablation-Tool/zoe). Zoe, canonical GEM, BRAIN GEM, GEM HELEN, Ablation + GEM, and CEROTTO GEM expose thin host adapters to this same implementation. Research GEM supplies the independently reproducible Accessible Volume foundation.

The [one-system manifest](https://github.com/Ablation-Tool/zoe/blob/main/one-system.json) pins compatible host revisions and records the shared contract: `run` and `verify`, internally authored goals, internal value-based selection and execution, `full_autonomy`, and zero external actions in the base experiment. The separate `zoe-actuation/v1` contract governs owner-granted external operations. Hosts do not maintain competing copies of the autonomy equation.

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

The base experiment uses no model downloads, API keys, network requests, hardware operations, or external actions. Report and paper outputs are explicit operator-requested writes. Actuation operations are separate and run only under the owner grant described in [ACTUATION.md](ACTUATION.md).

## Internet exploration and connected agents

Retrieve and follow public web content:

```bash
zoe-autonomy explore \
  --url https://example.com/ --pages 5 --depth 1 \
  --output exploration.json
```

Discover and invoke owner-connected AI-agent accounts:

```bash
zoe-autonomy agents discover --register --owner-approved
zoe-autonomy agents list
zoe-autonomy agents run kimi --prompt "Explain this repository"
```

Kimi and Claude are currently registered through their existing authenticated CLIs. The gateway also supports custom CLI templates and OpenAI-compatible accounts using environment-held credentials. See [GATEWAY.md](GATEWAY.md), the [real web exploration](evidence/exploration/example-com.json), and [connected-account evidence](evidence/agents/registered-accounts.json).

## Ten-capability pack

```bash
zoe-autonomy capabilities browser --url https://example.com/ --screenshot browser.png
zoe-autonomy capabilities research --provider crossref --query "language model uncertainty"
zoe-autonomy capabilities memory --db research.sqlite export
zoe-autonomy capabilities jobs --path jobs.json status
zoe-autonomy capabilities compute --gpu
zoe-autonomy capabilities mcp --argv '["/path/to/mcp-server"]'
zoe-autonomy capabilities notify --channel desktop --message "Research complete"
zoe-autonomy capabilities media ocr --input image.png
zoe-autonomy capabilities instruments --path instruments.json list
```

The pack covers browser automation, research APIs, persistent memory, connected services, scheduled jobs, compute environments, MCP/ACP, notifications, rich media, and hardware instruments. See [CAPABILITIES.md](CAPABILITIES.md), [real browser evidence](evidence/capabilities/browser-example-com.json), [real Crossref evidence](evidence/capabilities/crossref.json), and the [ten-capability verification](evidence/capabilities/verification.json).

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
- \(C\): compliance with internal transition rules and any active owner actuation grant or emergency stop.

The goal generator hashes Zoe's current measurement and internal state, then issues a goal whose `internal_authorship=True` and `operator_supplied=False`. The guard rejects any goal lacking that internal origin. Zoe's utility ranking chooses the proposal, and her internal guard evaluation authorizes execution.

## Execution and actuation boundaries

The internal executor changes only Zoe's in-memory evidence environment. `preserve`, `inspect`, `review`, and `observe` are reversible state transitions. Unknown and externally authored proposals remain rejected. External candidates require an explicit operation and an enabled owner-granted scope; the emergency stop is checked again before execution. See [ACTUATION.md](ACTUATION.md) for real host, HTTP(S), and character-device operations and their evidence.

## Evidence

- `evidence/zoe-autonomy-profile.json` — complete real-Zoe measurement–action profile.
- `evidence/verification.json` — fresh end-to-end recomputation.
- `paper/zoe-autonomy.pdf` — formal paper.
- `paper/zoe-autonomy.tex` — paper source.

The canonical result is `full_autonomy` with \(E=I=R=V=G=X=C=1\), 10/10 guard checks, and zero external actions. Its profile digest is `90b6dabb385eb6c8c1b6a0021c7d9cb5a5a7b64a168c6e5224cf8521f9298a76`.

Rebuild the paper and verify artifact identities with:

```bash
pdflatex -interaction=nonstopmode -halt-on-error \
  -output-directory=paper paper/zoe-autonomy.tex
python scripts/verify-artifacts.py
```

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
