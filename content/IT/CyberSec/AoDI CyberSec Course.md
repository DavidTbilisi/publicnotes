# 🐞💰🌐🛡️ Bug Bounty–Ready Web App Security: 12‑📅 Hands‑On 📚 (2×/wk)

**👥:** 🧑‍💻 mid‑level 🌐 devs ready to 🐞 hunt ⚖️legally & 🤝 professionally.
**🎯 Outcome:** By 📅 **12**, learners can pick ⚖️ scopes, run 🟡lightweight 🔍 recon, manually validate 🔥‑impact findings, and ship triage‑friendly 📝 reports that get taken seriously.

---

## 🧭 Course Principles

* **👐 Practice‑first:** ~70% 🧪 lab / 30% 🗣️ debrief each 📅. Ship 📦 (script/PoC/report) every time.
* **💼 Employment‑ready:** Per‑📅 deliverables → public, sanitized 📁 portfolio (no 🕵️‍♂️ sensitive data).
* **🧰 Real tools / 🎯 real targets:** PortSwigger Academy, OWASP Juice Shop, WebGoat, + legal **VDPs** ([Vulnerability Disclosure Programs] — company‑run good‑faith testing) with **Safe Harbor** ([explicit legal protection when rules are followed]).
* **🧯 Non‑destructive:** Respect ⏱️ rate limits, 🔏 data, 👤 privacy, 🗂️ scope. Prefer **👀 passive recon** ([gather info without touching target]) before **🤝 active** ([directly query endpoints]).
* **📖 Impact storytelling:** Connect 🐞 → 💼 business risk (🔓 data exposure / 👤 takeover / 💳 fraud) + concrete **🛠️ remediation** ([developer action to fix]).

## 🗓️ Meeting Roadmap — 12 📅 (2×/wk)

> 🗺️ **Oct–Nov 2025** (Asia/Tbilisi). Kickoff **2 Oct (Thu)**, second **6 Oct (Mon)**, then Thu/Mon cadence.

| 📅 | 📆 Date           | 🎯 Theme                                  | 🧠🧰 Core Skills & Tools                                                                                                             | 🧪📦 Labs & Deliverables                                             | 💼 Hiring Signal                      |
| -- | ----------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- | ------------------------------------- |
| 1  | 2 Oct 2025 (Thu)  | 🖥️⚙️ Workstation + 🔍 Recon 0→1          | Kali/Parrot; Burp; wordlists; subdomain+content discovery: `subfinder` `amass` `httpx` `katana` `gau/waybackurls` `ffuf/feroxbuster` | Build 1‑command recon pipeline → live hosts + juicy paths            | GitHub repo + README; reproducibility |
| 2  | 6 Oct 2025 (Mon)  | ⚖️ Legal, 🤝 Ethics & 🗂️ Scoping         | Read VDP scope; Safe Harbor; 🧯 non‑destructive; 🎚️ severity thinking                                                               | Pick 3 legal scopes; craft **RoE**; write triage pre‑engagement msg  | Professional maturity & compliance    |
| 3  | 9 Oct 2025 (Thu)  | 🔐 Auth, 🍪 Sessions & 👥 Access Control  | OAuth2/OIDC; 🔑 JWT; cookie flags; session fixation; **IDOR/BOLA/BFLA**                                                              | PortSwigger + Postman labs; 3 IDORs on training apps                 | Authz intuition; clear PoCs           |
| 4  | 13 Oct 2025 (Mon) | 🧪 Input Bugs @ ⚡ Speed                   | **XSS** (reflected/stored/DOM); **CSP**; **SSTI**; 💻 cmd‑inj; Burp Param Miner; `kxss` `dalfox`                                     | Build XSS probe list; 5 XSS labs (incl. CSP); 1 SSTI→RCE             | Payload arsenal; impact storytelling  |
| 5  | 16 Oct 2025 (Thu) | 🖧 Server‑Side Abuse: **SSRF** & 📁 Files | SSRF→metadata/pivot; upload bypass; path traversal; XML/XXE; deserialization basics                                                  | SSRF internal discovery; 2 upload bypasses; XXE exfil                | Chaining findings                     |
| 6  | 20 Oct 2025 (Mon) | 🔌 APIs & 🧩 Microservices                | OWASP API Top 10; Swagger/OpenAPI; authz drift; **Mass Assignment**; ⏱️ rate‑limit; GraphQL introspection                            | Build API test pack; exploit BOLA; GraphQL enum hunt                 | API checklist + examples              |
| 7  | 23 Oct 2025 (Thu) | 🔁 HTTP Weirdness & 🆕 Vulns              | Request **smuggling** (CL/TE); 🧱 cache poisoning/deception; **CORS** misconfig; Host header                                         | Cache‑poison lab; smuggling lab; CORS read PoC                       | Advanced bug repertoire               |
| 8  | 27 Oct 2025 (Mon) | 🤖 Automation: **Nuclei** + 🧩 Scripts    | Nuclei templates; `gf`; `jq/awk`; tiny Python/JS for PoCs/fuzzing                                                                    | Safe nuclei config; custom weak‑JWT detector                         | Practical automation                  |
| 9  | 30 Oct 2025 (Thu) | ☁️ Cloudy Web Apps                        | IMDS; presigned URLs; S3/GCS/Azure Blob; IAM gotchas via web                                                                         | Abuse URL expiry; find public bucket (lab); mock disclosure          | Cloud awareness                       |
| 10 | 3 Nov 2025 (Mon)  | 🛠️ DevSecOps Eyes                        | CI/CD; 📦 deps; 🧾 SBOM; 🔑 secrets; GitHub Actions surface                                                                          | Demo org; `gitleaks`/`trufflehog` pipeline (private)                 | Blue‑team empathy; SDLC literacy      |
| 11 | 6 Nov 2025 (Thu)  | 📨 From Finding → 💰: Reporting & Triage  | Platform severity vs **CVSS**; impact story; replication; fix suggestions; dupes/N‑A; etiquette                                      | 2 production‑grade reports (steps, impact, remediation, attachments) | Employer‑ready communication          |
| 12 | 10 Nov 2025 (Mon) | 🏁 Capstone: Live, ⚖️ Legal Hunt          | Choose Safe‑Harbor program; 🔍→🧪→📝 loop; pro submission                                                                            | Recon notes + 1–2 responsible reports (real/sim) + case study        | Portfolio credibility                 |

---

## 🔎 Detailed Breakdown

### 📅1 — 🖥️⚙️ Workstation + 🔍 Recon 0→1

**🎯:** Fast setup, fast signal; repeatable recon in minutes.

**🗣️ Jargon:** recon ([map assets/attack surface]); wordlist ([candidate paths/passwords]); passive vs active; scope ([allowed]); **RoE** ([Rules of Engagement]).

**🧰:** Kali/Parrot/WSL2, Burp, FoxyProxy, SecLists, `subfinder` `amass` `dnsx` `httpx` `katana` `gau` `waybackurls` `ffuf/feroxbuster`.

**✅ Checklist:**

* OS + packages; shell aliases; Go tools `requirements.txt`.
* Trust Burp CA; FoxyProxy; enable HTTP history + scope rules.
* Workspace: `/recon` `/httpx` `/content` `/screens` `/notes`.

**🧪 Lab 1 — Burp Intercept:** Intercept HTTPS, add 🎯 to scope, capture baseline requests, annotate params.
**🧪 Lab 2 — 1‑command recon:**

```bash
subfinder -silent -dL domains.txt | dnsx -silent | httpx -silent -title -status-code -json \
| tee httpx.json && cat httpx.json | jq -r 'select(.status_code==200) | .url' \
| katana -silent -jc | tee endpoints.txt && ffuf -w wordlist.txt -u FUZZ_URL/FUZZ
```

*( **`dnsx`**=DNS probe; **`httpx`**=HTTP probe; **`katana`**=endpoint crawler; **`ffuf`**=content discovery )*

**📦 Deliverables:** GitHub repo (script + README + sample output); 2–3 annotated screenshots.
**🏁 Success:** ≥80% subs probed; deduped endpoints; note next probes (`/api/*`, `/admin`).
**⚠️ Pitfalls:** noisy scans; no scope record; mixing passive/active without provenance.

---

### 📅2 — ⚖️ Legal, 🤝 Ethics & 🗂️ Scoping

**🎯:** Stay safe, in scope, and communicate like a teammate.
**🗣️ Jargon:** **VDP**; **Safe Harbor**; **triage** ([first report review]); **OOS** ([out‑of‑scope]); **PII** ([personal data]).
**🧠 Skills:** Read platform policies; build **Scope Matrix** (target, methods, rate limits, test accounts, disallowed); draft **pre‑engagement** msg & stop conditions.
**🧪 Lab:** Choose 3 scopes; 1‑page **RoE** incl. rate‑limit plan, data handling, rollback.
**📦:** PDF checklist; triage msg; scope matrix.
**🏁:** RoE covers what/how/when‑to‑stop + evidence of non‑destruction (masked data).
**⚠️:** assuming wildcard scope; testing payments; storing real user data.

---

### 📅3 — 🔐 Auth, 🍪 Sessions & 👥 Access Control

**🎯:** Break authz systematically (ethically).

**🗣️ Jargon:** OAuth2 ([delegated auth]); **OIDC** ([identity layer]); **JWT** ([JSON Web Token]); **IDOR** ([Insecure Direct Object Reference]); **BOLA** ([Broken Object Level Authorization]); **BFLA** ([Broken Function Level Authorization]); session fixation ([force victim to use attacker session]).

**🧠:** Trace flows; inspect cookies (HttpOnly/Secure/SameSite); JWT alg/key issues; refresh rotation. Build role/tenant cases: user→user, user→admin, tenantA→tenantB.
**🧪 Labs:** PortSwigger access‑control path; Postman scripts auto‑swap IDs; validate 3 IDORs.
**📦:** Postman collection; PoC shots; mitigation notes (server‑side object checks).
**🏁:** ≥1 vertical + ≥1 horizontal authz flaw reproduced.

**⚠️:** client‑side only checks; trusting role names in JWT.

---

### 📅4 — 🧪 Input Bugs @ ⚡ Speed

**🎯:** Confident XSS/SSTI/cmd‑inj with context‑aware payloads.

**🗣️ Jargon:** **XSS**; **CSP** ([Content Security Policy]); **SSTI**; **RCE**; **WAF**.
**🧠:** Find sinks (HTML/JS/template); craft per‑context payloads; Burp **Param Miner**; `dalfox` `kxss`.
**🧪 Labs:** Build XSS probe list; bypass CSP (allowed src/JSONP); 1 SSTI→RCE in lab.
**📦:** Payload arsenal; write‑up with business impact + fix.
**🏁:** 5 distinct XSS contexts; 1 SSTI chain.

**⚠️:** one‑size payloads; ignoring CSP report‑only.

---

### 📅5 — 🖧 Server‑Side Abuse: **SSRF** & 📁 Files

**🎯:** Turn server trust against itself; abuse risky parsers.
**🗣️ Jargon:** **SSRF**; **XXE**; **LFI/RFI**; polyglot; magic bytes; **IMDS** ([cloud metadata]).
**🧠:** Shape SSRF (scheme/host/port/path); hit IMDS; uploads: bypass type/name/ext; store outside webroot; validate server‑side; path traversal (`../`).
**🧪 Labs:** SSRF → internal enumeration; IMDSv2 token (lab); 2 upload bypasses (MIME/polyglot); XXE with external entity.
**📦:** PoC videos; checklists (egress deny‑by‑default; host allow‑list; robust upload validation; disable external entities).
**🏁:** SSRF impact beyond fetch (e.g., reach internal admin) in lab.

**⚠️:** DNS rebinding blind spots; trusting client‑side checks.

---

### 📅6 — 🔌 APIs & 🧩 Microservices

**🎯:** Hunt where modern apps live.
**🗣️ Jargon:** OWASP API Top 10; **Mass Assignment** ([blind model binding]); **Rate Limiting**; **Excessive Data Exposure**; GraphQL **introspection** ([reveal schema]).
**🧠:** Read Swagger/OpenAPI; diff docs vs behavior; design BOLA/BFLA tests; GraphQL `__schema`, enumerate types/fields; IDOR on resolvers.
**🧪 Labs:** Build Hoppscotch/Postman + Burp pack; exploit BOLA; show Mass Assignment via hidden fields.
**📦:** API checklist; sanitized PoCs; remediation notes (server checks, allow‑list fields, output filtering).
**🏁:** ≥1 BOLA + ≥1 Mass Assignment with business impact.

**⚠️:** trusting client logic; missing tenant boundaries.

---

### 📅7 — 🔁 HTTP Weirdness & 🆕 Vulns

**🎯:** Exploit invisible layers (proxies/caches/intermediaries).
**🗣️ Jargon:** **Smuggling** (CL/TE desync); **CORS**; cache poisoning/deception; Host header abuse.
**🧠:** Craft CL/TE mismatches (lab‑only); poison shared caches (unkeyed inputs); spot unsafe `Access-Control-Allow-Origin` + credentialed CORS.
**🧪 Labs:** 1 smuggling; 1 cache poison altering response; CORS read PoC.
**📦:** Runbooks + mitigations (normalize headers; strict cache keys; proper CORS).
**🏁:** Altered cached response or cross‑origin read (lab).

**⚠️:** production smuggling; ignoring CDN/WAF quirks.

---

### 📅8 — 🤖 Automation: **Nuclei** + 🧩 Scripts

**🎯:** Augment manual testing (no scanner‑spam).
**🗣️ Jargon:** **Nuclei** (template checks); `gf` (grep patterns); `jq` (JSON); `awk` (text); **PoC**; **fuzzing** (systematic input variation).
**🧠:** Write 2 Nuclei templates (matchers/extractors); pipe recon → nuclei → manual validation; add rate‑limit guards; tiny Python/JS for JWT/params.
**🧪 Labs:** Safe nuclei config (exclude destructive); custom weak‑JWT detector.
**📦:** 2 templates; 1 PoC script; safe‑automation README.
**🏁:** Low‑noise actionable leads, each manually validated.

**⚠️:** submitting raw nuclei output; risky templates on prod.

---

### 📅9 — ☁️ Cloudy Web Apps

**🎯:** Bridge ☁️ misconfig → real web impact.
**🗣️ Jargon:** **IMDS**; **presigned URL** (temporary signed link); bucket **ACL**; instance role.
**🧠:** Detect cloud fingerprints; probe public buckets; abuse presigned URLs (lab); map SSRF→IMDS→temp creds→internal API (lab).
**🧪 Labs:** Presigned URL misuse; public bucket discovery; mock disclosure with least privilege/short TTL/block public access.
**📦:** Cloud‑web abuse scenarios + code/config fixes.
**🏁:** Show web issue → sensitive object access (lab).

**⚠️:** random cloud IP scanning; overclaiming impact.

---

### 📅10 — 🛠️ DevSecOps Eyes

**🎯:** See what pipelines leak & how to fix.
**🗣️ Jargon:** **CI/CD**; **SBOM**; **secrets** (tokens/keys/passwords); **dorking** (targeted search).
**🧠:** Model CI/CD surface (logs/artifacts/env/runner perms); local secret‑hunting with `gitleaks`/`trufflehog` + pre‑commit; write prevention guide.
**🧪 Labs:** Demo GitHub org; seed fake secrets; catch locally; propose CI guardrails.
**📦:** Private pipeline; prevention doc; short demo video.

**🏁:** Automated detection + actionable prevention.

**⚠️:** scanning 3rd‑party orgs; publishing real keys.

---

### 📅11 — 📨 From Finding → 💰: Reporting & Triage

**🎯:** Turn valid 🐞 into fast, actionable 📝.
**🗣️ Jargon:** **CVSS**; severity; **dupe**; **remediation**.
**🧠:** Write repro a dev follows <5 min; map tech → business (IDOR ⇒ invoice access ⇒ data protection risk); handle dupes; negotiate severity with evidence.
**🧪 Labs:** Convert 2 labs → production‑grade reports (summary/steps/impact/remediation/attachments).
**📦:** 2 polished reports (PDF/MD) + artifacts.
**🏁:** Triage feedback: clear, reproducible, low noise; practical fix.

**⚠️:** vague steps; no screenshots; overstated impact.

---

### 📅12 — 🏁 Capstone: Live, ⚖️ Legal Hunt

**🎯:** Execute a mini professional engagement end‑to‑end.
**🛠️ Activities:** Choose 1–2 Safe‑Harbor programs; confirm 🗂️ via Scope Matrix; run 🔍→🧪→📝 loop (low‑intensity); log ⏱️ & stop conditions; present 10‑min 🎤 case study (problem/method/result/remediation/lessons).
**📦 Deliverables:** Recon notes, methodology, PoCs, responsible submissions (or simulated if none).
**🏁 Success:** Professionalism + legality + ≥1 actionable report mirroring prod quality.

---

## 🎯⚖️ Targets (Legal Only)

* **🎓 Training:** PortSwigger Academy (XSS/Access/SSRF/Smuggling paths), OWASP Juice Shop, WebGoat, bWAPP, vuln API labs.
* **🟢 Live scopes:** Public VDP/bug bounty with explicit Safe Harbor. Low‑intensity; strict scope; prefer sandbox/dev when offered.

### 🟩 HTB — 🆓 machines (suggested)

> Availability changes. Free users → **active** machines; **retired** → VIP. **Starting Point** tiers are free & stable. Be non‑destructive + in‑scope.

**📅1–2 (basics/recon/scoping):**

* **Meow** — banner grabbing & service enum (recon basics).
* **Fawn** — safe cred enum; rate‑limit etiquette.
* **Dancing** — recon + basic auth weaknesses → web surface.

**📅3 (auth/access):**

* **Oopsie** — **IDOR** & panel logic.
* **Unified** — panel + session handling.

**📅4 (input, SQLi/XSS/SSTI):**

* **Appointment** — **SQLi** patterns & params.
* **Ignition** — login logic; extend to XSS probes.
* **Crocodile** — creds reuse → web; test inputs.
* **Sequel** — DB exposure lessons.

**📅5 (SSRF/upload/XXE):**
* **Vaccine** — cookies + SQLi; supplement with active boxes tagged `upload`/`SSRF`.

**📅6 (APIs/GraphQL):** Pair HTB Academy Web modules + any active JSON API box; validate **BOLA**/**Mass Assignment**.
**📅7 (smuggling/caching/CORS):** Prefer PortSwigger labs; optional active box w/ proxy/cache behavior (caution).
**📅8–10 (automation/cloud/DevSecOps):**

* **Archetype** — infra + secrets patterns feeding web.
* **Unified** — reuse for automation.
* Add secret‑hunting on your **own** demo repos (never public orgs).

**🧰 Stretch (VIP/temporary active):** **Bashed**, **Shocker**, **Jerry** — classic web‑centric (upload/RCE/misconfig).

---

## 📝 Standard Reporting Template (use from 📅5 onward)

1. **🧭 Summary** (one para; business impact). *Ex:* “IDOR in `/api/invoices/{id}` lets authenticated users download other tenants’ invoices.”
2. **🎯 Scope & 🧩 Affected Assets** (URLs/endpoints/versions). *Ex:* `https://api.example.com/v2/invoices/{id}` (prod).
3. **🎚️ Severity/Impact** (platform severity + rationale). *Ex:* High — unauthorized access to financial PII.
4. **🔑 Preconditions** (accounts/roles/config). *Ex:* Authenticated user in tenant A.
5. **🪜 Steps to Reproduce** (numbered; copy‑pasteable HTTP reqs w/ headers/body).
6. **📸 Evidence** (screens; HTTP captures; curl/Postman; short PoC video).
7. **🛠️ Remediation** (server‑side object checks; tenant isolation; unit tests) + links to docs.
8. **🗒️ Notes** (rate limits; data handling; scope confirmations; triage timeline).

**✍️ Formatting:** numbered steps; code blocks; mask data.

---

## 🧰 Toolbelt (Baseline)

* **Intercept/Testing:** Burp (intercept/repeater/intruder), OWASP ZAP (open‑source proxy/scanner), Postman/Hoppscotch (API clients).
* **Recon/Discovery:** `subfinder`/`amass` (subdomain), `dnsx` (DNS probe), `httpx` (HTTP probe), `katana` (crawl), `gau`/`waybackurls` (archives), `ffuf`/`feroxbuster` (content).
* **Automation/Aux:** **nuclei**, `gf`, `jq`, `awk`, Python `requests`, `gitleaks`/`trufflehog`.
* **Wordlists:** **SecLists** (curate subsets).

**🗂️ Workspace tip:** per‑target folders + `notes.md` tracking cmds/versions/findings.

---

## 📊 Assessment Rubric (per 📅)

* **🔬 Technical depth — 40:** exploit quality; context awareness; safe execution.
* **📣 Impact articulation — 25:** business framing; data sensitivity; exploitability.
* **🔁 Reproducibility — 20:** clear steps; minimal assumptions; working PoC.
* **🤝 Conduct — 10:** scope hygiene; respectful comms; non‑destruction evidence.
* **👯 Collaboration — 5:** peer review; pair testing; clear notes.

**✅ Pass:** ≥75 per 📅 • **🏁 Capstone:** ≥85

---

## 📁 Portfolio Pack @ Graduation

* Public GitHub: recon scripts; 2 custom Nuclei templates; API collections.
* 3–5 sanitized write‑ups w/ developer‑centric fixes.
* Capstone case study (end‑to‑end story).
* Reusable triage‑friendly report template.

---

## ⏱️ Session Flow (each 📅)

* **20 min** kickoff (threat model + micro‑lecture)
* **100 min** 🧪 lab (pair/solo)
* **20 min** debrief (impact, mitigation, report snippet)

---

## ⚖️🛡️ Code of Conduct & Safety

* Stay in scope. Ask when ambiguous.
* Don’t exfiltrate/view real user data; prove impact with minimum footprint.
* Respect rate limits + production stability; prefer test/sandbox assets.

---

### 🧑‍🏫 Instructor Notes (optional)

* Maintain private lab tenant for ☁️/API exercises.
* Pre‑provision targets + seed data for repeatability.
* Require short write‑ups; give inline feedback on clarity & developer usefulness.


[Syllabus](https://digitaledu.ge/cybersecurity/)

![[nmap_cheatsheet.png]]![[metasploit_cheatsheet.png]]
![[netcat_cheatsheet.png]]
![[mimikatz_cheatsheet.png]]
![[hydra_cheatsheet.png]]












