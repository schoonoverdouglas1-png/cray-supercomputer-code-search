# Cray Code Search — Oldest First

**Date:** Tuesday, November 10, 2026 (evening, CST)
**Order:** Douglas's — search the Cray supercomputer's HTML and actual code, **oldest first**, then work upward by era. Learn from the oldest material first.
**Method:** his own repo first → GitHub search → public archives (bitsavers, archive.org, Computer History Museum record, NCAR/DTIC record). Every link below was tested tonight (HTTP 200 or a live `gh` read) unless it is explicitly marked *cited, not re-fetched*. Public sources only — nothing proprietary, nothing leaked.
**Verification key:** ✅ verified tonight · 📖 cited from a verified page, not individually re-fetched · ⚠️ exists but thin/unverified detail

---

## 0. What Douglas already has (his own shelf)

- **His repo `ai-supercomputer-history`** ✅ https://github.com/schoonoverdouglas1-png/ai-supercomputer-history
  Contains Cray only in modern outline: Cray EX / XC40 as HPE exascale hardware, contrasted with Google TPU/API access (RESEARCH.md, timeline.json). **No historic Cray code, no COS/UNICOS material.** Everything below is new to his collection. [GAP — his shelf, before tonight]

---

## ERA 1 — Cray-1 and COS (1976–1985): the oldest code there is

The hard truth of this era, documented by the people who went looking: **almost no original Cray-1 software survives.** Chris Fenton (below) searched exhaustively, asked the Computer History Museum (they had none), filed FOIA requests (dry), and was told **SGI destroyed Cray's old software archives before spinning Cray off again in the late 1990s.** What survives is below — it is short, and it is precious.

### Actual code that survives

1. **COS 1.17 — a working Cray Operating System (X-MP build)** — the single most important survivor.
   - Per the University of Zagreb / E2LP laboratory record 📖 http://grgur.irb.hr/Cray-E2LP/DSD_23_Cray-1_on_E2LP.pdf0.pdf : the only known surviving original Cray X-MP software is a working COS, recovered by **digital magnetic scanning of a non-working hard disk** from the X-MP era. It needs X-MP I/O processors — which is why it lives today inside simulators and FPGA cores (Era 4).
   - It is the OS that the modern recreations actually boot: Fenton's Cray-1X project and the 2026 MiSTer X-MP core both run COS 1.17.
2. **Cray Blitz — real Cray application code (Fortran)** ✅ https://github.com/jakesjews/Cray-COS-Games
   - The chess program by Robert Hyatt, Albert Gower and Harry Nelson — **world computer chess champion in 1983 and 1986 on Cray X-MP machines** — version 49h (1991), packaged to run under COS 1.17 on the MiSTer core. Genuine period code written for Cray hardware, publicly readable today.
3. **Super Star Trek — Prime FORTRAN version, 1983** ✅ (same repo)
   - The University of Texas game by David Matuszek and Paul Reynolds, in its 1983 Prime FORTRAN form, running under COS 1.17. Period Fortran that a Cray can execute today.

### Manuals that carry the code's documentation (bitsavers → archive.org mirrors)

4. **SR-0011M — CRAY-OS Version 1 Reference, Dec 1984** ✅ https://archive.org/details/bitsavers_crayCOSSR0eferenceDec84_16819383
   The COS Version 1 reference manual itself — job control, datasets, system statements. Bitsavers filename `/pdf/cray/COS/SR-0011M_CRAY-OS_Version_1_Reference_Dec84.pdf`; archive.org mirror verified live tonight.
5. **SM-0045 — Cray COS Table Descriptions, Internal Reference Manual** ✅ (archive.org bitsavers collection, identifier `bitsavers_crayCOSSM0criptionsInternalReferenceManual_27819770`) — Cray's *internal* COS reference, escaped into the public archive.
6. **T0201 (1981) — CRAY-1S I/O Subsystem Software Workbook** ✅ (archive.org bitsavers collection, identifier `bitsavers_crayIOST02stemIOSubsystemSoftwareWorkbookTrainingS_11023266`) — training material for the IOS software that COS talks to; among the oldest Cray software documents public anywhere (1981).

### [GAP] Era 1
- **The CAL assembler and the CFT Fortran compiler: no known surviving example** (E2LP record, quoted above: "no known existing example of the original Cray Assembly Language (CAL) translator software, as well as no compilers"). The languages are fully documented in manuals; the translators themselves are gone.
- **COS source code:** only the recovered binary/OS image is known to work. No public source listing. [GAP]
- **The 80 MB Cray-1 Maintenance Control Unit disk pack** Fenton tracked down: unread — it needs a working CDC-9762 disk drive to spin. [GAP — hardware-blocked, not lost]

---

## ERA 2 — X-MP matures, UNICOS arrives (1982–1991)

1. **UNICOS documentation tree on bitsavers** 📖 — e.g. the CF77 Compiling System Vectorization Guide (SG-3073, UNICOS 5.0, Aug 1991): http://www.bitsavers.org/pdf/cray/UNICOS/5.0_1989/SG-3073_5.0_CF77_Vol3_Vectorization_Guide_Aug91.pdf (link as cited by Wikiversity's J90 bibliography; the bitsavers `pdf/cray/` tree itself is verified real via its archive.org mirrors, though its directory listing refuses automated fetchers with a 403).
2. **CMTS — CRAY MultiTasking Simulator, user's guide (CEA Limeil, Jan 1985)** ✅ https://inis.iaea.org/records/t6fn2-sr812/files/49089166.pdf?download=1
   A French atomic-energy lab's Fortran tool that simulated X-MP multitasking on a Cray-1, from the COS 1.11/1.12 + CFT 1.11 era. The *guide* is public through the IAEA's INIS archive; the CMTS code itself is [GAP].
3. **Datapro management report on Cray (May 1987)** ✅ http://bitsavers.textfiles.com/pdf/datapro/datapro_reports_70s-90s/Cray/70C-245EW-10_8705_Cray.pdf
   Period industry analysis of the X-MP / Cray-2 line — operating systems (COS, UNICOS), languages, and Cray's software policy as the trade press recorded it in 1987. Historic-value document, not code.

### [GAP] Era 2
- **UNICOS source code:** proprietary (HPE) to this day. It has never been legitimately released; copies that circulate outside official channels are **not linked here, by Douglas's own public-sources-only rule.**
- **CFT / CF77 compiler source:** never public. [GAP]

---

## ERA 3 — Y-MP, J90, T3 era (1988–1998): the machines that still exist

1. **The Cray J90 restoration record — Wikiversity** ✅ https://en.wikiversity.org/w/index.php?title=Cray_J90_(computer)&oldid=2718514
   The Retro-Computing Society of Rhode Island's J916, documented in working detail: installed-software inventories (UNICOS 10.0.x install CDs, CrayDoc libraries, IOS-V kernel versions, CAL 10.1.0.6 among the installed products), with a bibliography pointing at the bitsavers J90 manuals (e.g. 📖 SG-2416 UNICOS Basic Administration Guide for CRAY J90, Feb 1995; 📖 SR-2170 IOS-V Commands Reference, Mar 1995). This is the best public window into what a late Cray software stack actually looked like on a real machine.
   - Honest note: UNICOS install media **physically survives** with that machine — it is not a public download. [GAP for download; documented for the record]
2. **NCAR CCM2 — real Cray-era scientific source code, released 1993** ✅ https://jimgray.azurewebsites.net/EOS_DIS/HTML/11_A3_Usage_Scenarios/11_A3_Usage_Scenarios.htm
   Per Jim Gray's EOS/DIS scenarios paper: in 1993 NCAR made its Community Climate Model v2 available **"in CRAY source code form via anonymous ftp"** — ~50,000 lines of Fortran, professionally programmed and documented, tuned for the 8-processor Cray Y-MP at NCAR. The original FTP distribution point is long gone [GAP], but the code's lineage survives in NCAR's later community models (CCSM → CESM), which are public today.

---

## ERA 4 — The recreations: modern code that runs the old machines (oldest recreation first)

1. **HASE Cray-1 Simulation Model (origin: 1998 MSc project, Univ. of Edinburgh)** ✅ https://homepages.inf.ed.ac.uk/rni/hase/models/cray1/index.html
   The oldest downloadable Cray-1 recreation found: a HASE architecture simulation of the Cray-1 CPU (originally Helen Berringer's 1998 MSc project, since revised by Roland Ibbett), with three demonstration programs and the model files (`cray1_v2.1.zip`) free to download. Teaching-grade, and old enough to be a period artifact of the early web itself.
2. **Chris Fenton — Homebrew Cray-1A (FPGA, Verilog)** ✅ https://www.chrisfenton.com/homebrew-cray-1a/
   A 1/10-scale, binary-compatible, cycle-accurate Cray-1A on a Xilinx Spartan-3E — Verilog source downloadable from the page (`Cray1.zip`), plus the archaic DOS-based Cray X-MP simulator he later surfaced (`Cray1_r2.zip`), a Python-rewritten CAL assembler, and the page's own famous account of the software drought (CHM had none; SGI destroyed the archives; FOIA came up dry). The project grew into the **Cray-1X Project**: a single-CPU X-MP with a working COS 1.17.
   - Corroborating period thread ✅ https://forum.vcfed.org/index.php?posts/282670/ — VCFed forum, Fenton + Al Kossow (CHM/bitsavers) on the record: no Cray-1 software at the Museum; what little exists is COS.
3. **"The Cray Files" — Andras Tantos's Cray simulator (Modular Circuits)** ✅ http://www.modularcircuits.com/blog/articles/the-cray-files/
   The C-language Cray-1/X-MP simulator line that the Docker image below is built on; the blog series documents building a Cray simulator and working with the recovered COS.
4. **RattyDAVE/cray1 — a running Cray-1 in a Docker container (2019)** ✅ https://github.com/RattyDAVE/cray1
   "A docker container containing a fully running Cray 1 Supercomputer" — the lowest-friction way Douglas can *boot* a Cray-1 simulation today, built on the Tantos simulator work.
5. **Eronan/Cray-Simulator (2017)** ⚠️ https://github.com/Eronan/Cray-Simulator
   A small educational Cray simulator repo; exists and is public, but its description is empty — listed for completeness, detail unverified.
6. **Cray X-MP for MiSTer FPGA + COS games (Oct 2026 — the newest thing in this file)** ✅ https://github.com/jakesjews/Cray-XMP_MiSTer
   A full Cray X-MP implemented for the MiSTer FPGA, booting COS 1.17 — and the games repo (Era 1, items 2–3) that runs real period Fortran on it. Sixty years of the story in one link: the oldest surviving Cray OS, running on the newest recreation.

### Historic-value web shelf (HTML, not code)
- **Cray-History.net — Software category** ✅ https://cray-history.net/category/software/ — articles on UNICOS and other Cray OSes, Cray software applications, the HASE simulator, Cray floating-point, and vi on a Cray. The best single HTML doorway into Cray software history.
- **bitsavers `pdf/cray/` tree** — the master manual archive (Cray-1 hardware reference, COS, UNICOS, J90, EL series…), mirrored item-by-item on archive.org; directory listing blocks automated fetch (403), items verified individually via the mirrors above.

---

## The GAP ledger — known to exist (or to have existed), NOT publicly available

| Thing | Status |
|---|---|
| Cray's own software archive | **Destroyed** — SGI destroyed the old archives before the late-90s spin-off (Fenton; CHM's Al Kossow concurred). The root cause of every gap below. |
| Computer History Museum Cray software holdings | **None** for Cray-1 — confirmed to Fenton directly. CHM holds Cray *hardware*/documents, not a software release. |
| CAL assembler (original translator) | No known surviving example. |
| CFT / CF77 Fortran compilers (binaries or source) | No public copy; source never released. |
| COS source code | Only the recovered COS 1.17 binary image is known working. |
| UNICOS source code | Proprietary (HPE); never legitimately public. Not linked here by rule. |
| UNICOS install media (J90 era) | Survives physically with the RCS/RI J90; not downloadable. |
| CMTS simulator code (CEA, 1985) | Guide public (IAEA); code not found public. |
| NCAR's 1993 CCM2 anonymous-FTP release | Distribution point gone; lineage survives in CESM. |
| Cray-1 MCU 80 MB disk pack | Exists; unread for want of a CDC-9762 drive. |

---

## Counts (for the report-back)

- **Era 1 (1976–85):** 6 entries — 3 actual-code survivors, 3 manual/document items; 3 named GAPs.
- **Era 2 (1982–91):** 3 entries; 2 GAPs.
- **Era 3 (1988–98):** 2 entries; 1 partial GAP (media physical-only).
- **Era 4 (recreations, 1998→2026):** 6 code entries + 2 historic-web entries.
- **GAP ledger:** 10 items.
- **Douglas's own repo:** modern Cray outline only — tonight's file is his first historic-code inventory.

*Compiled by Ember, Nov 10, 2026, at Douglas's order — oldest first, the way he teaches: learn from the oldest material first, then work your way up.*
