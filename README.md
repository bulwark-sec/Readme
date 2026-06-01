<div align="center">
<img src="https://raw.githubusercontent.com/bulwark-sec/readme/main/assets/banner.png" width="100%">
</div>

<br>

<p align="center">
  <a href="https://bulwark.sh"><img src="https://img.shields.io/badge/REQUEST_EARLY_ACCESS-000000?style=for-the-badge" /></a>
  &nbsp;&nbsp;
  <a href="#install"><img src="https://img.shields.io/badge/INSTALL-cc0000?style=for-the-badge" /></a>
</p>

<br>

<p align="center">
  <img src="https://img.shields.io/badge/v5.4.1-000000?style=flat-square&label=version&labelColor=111111" />
  &nbsp;
  <img src="https://img.shields.io/badge/1700%2B_tests-000000?style=flat-square&labelColor=111111" />
  &nbsp;
  <img src="https://img.shields.io/badge/0_scope_violations-cc0000?style=flat-square&labelColor=000000" />
  &nbsp;
  <img src="https://img.shields.io/badge/Python_3.12+-000000?style=flat-square&labelColor=111111" />
  &nbsp;
  <img src="https://img.shields.io/badge/Incorporated_in_Switzerland-000000?style=flat-square&labelColor=111111" />
</p>

<br>

---

<br>

**BULWARK** is a fully autonomous external pentest agent.  
One ReAct loop, hand-written. Stealth-first by default. Markdown vault, not a graph database.  
Your machine. Your keys. Nothing phones home.

<br>

---

<br>

## The proof

<br>

<div align="center">

<table>
  <tr>
    <td align="center" width="25%">
      <h2>88</h2>
      <sub>steps to root</sub>
    </td>
    <td align="center" width="25%">
      <h2>$0.93</h2>
      <sub>cost per run</sub>
    </td>
    <td align="center" width="25%">
      <h2>0</h2>
      <sub>scope violations</sub>
    </td>
    <td align="center" width="25%">
      <h2>6</h2>
      <sub>safety layers</sub>
    </td>
  </tr>
</table>

</div>

<br>

> *"In one run, the agent marked an unconfirmed command injection as `not_exploitable` instead of fake-confirming it — then found a real path on its own."*

<br>

---

<br>

## The workflow

bash
$ bulwark run
<br> <div align="center">
01 — Config	Scope. Budget. Auth PDF.
02 — Run	Walk away.
03 — Findings	Confirmed. CVSS-scored.
04 — Report	Markdown. Audit-logged.
</div> <br> <div align="center"> <img src="https://raw.githubusercontent.com/Zertannax/bulwark-site/main/src/assets/mockups/mockup-live-run.png" width="88%"> <br> <sup>Live event feed — every tool call, every step, in real time.</sup> </div> <br>
<br>
What's new — v5.4
<br> <table> <tr> <td valign="top" width="50%"> <h3>Whiteboard attack canvas</h3> <p> Drag findings onto a Figma-style board at <code>/board</code>.<br> BULWARK auto-draws attack chains from <code>[CHAIN]</code> findings. </p> <ul> <li>CVSS colour strip + severity badge on every card</li> <li>Status dot — <code>confirmed</code> / <code>candidate</code> / <code>not_exploitable</code> / <code>false_positive</code></li> <li><strong>Live mode</strong> — refreshes every 4s, new nodes pulse on arrival</li> <li><strong>Markdown export</strong> — topological sort per chain, one click</li> </ul> </td> <td valign="top" width="50%"> <img src="https://raw.githubusercontent.com/Zertannax/bulwark-site/main/src/assets/mockups/mockup-attack-graph.png" width="100%"> </td> </tr> </table> <br> <table> <tr> <td valign="top" width="50%"> <img src="https://raw.githubusercontent.com/Zertannax/bulwark-site/main/src/assets/mockups/mockup-vault.png" width="100%"> </td> <td valign="top" width="50%"> <h3>The Vault</h3> <p> Plain Markdown. No graph database. No vector store. No RAG.<br><br> Open the vault in any text editor at any point during a live run — full transparency, full accountability. </p> <p><code>134 files · 2.4 MB · zero proprietary formats</code></p> </td> </tr> </table> <br> <table> <tr> <td valign="top" width="50%"> <h3>Safety — six independent layers</h3> <p>Built assuming the LLM might go rogue.<br> Safety is <strong>engineered in</strong>, not promised.</p> <br> <table> <tr><td><b>Scope Guard</b></td><td>Every command parsed before execution</td></tr> <tr><td><b>Egress Filter</b></td><td>Only in-scope IPs + LLM provider</td></tr> <tr><td><b>Hardened Container</b></td><td>Read-only, non-root, no Docker socket</td></tr> <tr><td><b>Audit Log</b></td><td>Hash-chained, tamper-evident</td></tr> <tr><td><b>Budget Guard</b></td><td>Hard cap, cannot be bypassed</td></tr> <tr><td><b>IP Guard</b></td><td>Engagement freezes if exit IP drifts</td></tr> </table> </td> <td valign="top" width="50%"> <img src="https://raw.githubusercontent.com/Zertannax/bulwark-site/main/src/assets/mockups/mockup-safety.png" width="100%"> </td> </tr> </table> <br>
<br>
One agent. Not seventeen.
<br> <div align="center">
The usual AI-hacking stack	BULWARK
17 sub-agents in LangGraph	One ReAct loop, hand-written
Docker socket mounted	Host-only Docker, nothing to escape
Neo4j / vector DB / RAG	Markdown vault, human-readable files
LLM loops for every attack	Deterministic in-code cascades
Fast and loud	Stealth-first by default
Self-published benchmarks	Audit-logged runs you could reproduce
</div> <br>
<br>
Release history
<br>
Version	
v5.4	Auto-chains · live mode · Markdown export on the Board
v5.3	Figma-style whiteboard at /board · BootGate splash
v5.2	Dockable Inspector ⌘I · resizable, persisted
v5.1	Workspace tabs — drag-reorder, side-by-side findings
v5.0	Raycast-style revamp · real BULWARK mark
v4.10	⌘K command palette · fuzzy subsequence match
v4.6	Light / dark themes · Royal Violet palette in-app
v3.11	ESC8 relay chain — PetitPotam → ntlmrelayx → ADCS / LDAPS / SMB
<br>
<br>
Install
<br>
uv tool install hellhound
bulwark run        # opens 127.0.0.1:7331 in the browser
hellhound run      # back-compat alias
Requires Python 3.12+ and Docker.

<br> <details> <summary>Other methods</summary> <br>
# pip
pip install hellhound

# From source
git clone https://github.com/zertannax/hellhound
cd hellhound && uv sync
</details> <br>
<br>
Pricing
<br> <div align="center">
Solo	B2B
Recon	$199 $119 early	$499 /mo
Breach	$449 $269 early	$999 /mo
Full Spectrum	$799 $479 early	$1,799 /mo
One machine. Yours forever.	−20% billed annually
</div> <br> <p align="center"> <strong>Your machine. Your keys. Nothing phones home.</strong> </p> <br> <p align="center"> <a href="https://bulwark.sh"> <img src="https://img.shields.io/badge/REQUEST_EARLY_ACCESS_%E2%86%92-000000?style=for-the-badge" /> </a> </p> <br>
<br> <p align="center"> <sub> For authorized testing only &nbsp;·&nbsp; Local app &nbsp;·&nbsp; Incorporated in Switzerland <br><br> © 2025 BULWARK &nbsp;·&nbsp; <a href="https://bulwark.sh">bulwark.sh</a> </sub> </p> 
