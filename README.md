# Awesome AI Security Tools

> A curated list of the latest AI-powered security tools — offensive, defensive, and research-focused.
> Updated regularly. Contributions welcome.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Contents

- [Prompt Injection & LLM Testing](#prompt-injection--llm-testing)
- [AI-Assisted Penetration Testing](#ai-assisted-penetration-testing)
- [Vulnerability Research & Triage](#vulnerability-research--triage)
- [Malware Analysis](#malware-analysis)
- [SAST / Code Security](#sast--code-security)
- [Threat Intelligence](#threat-intelligence)
- [OT / ICS Security](#ot--ics-security)
- [Network Security](#network-security)
- [Cloud Security](#cloud-security)
- [Defensive / Blue Team](#defensive--blue-team)
- [Research & Datasets](#research--datasets)

---

## Prompt Injection & LLM Testing

| Tool | Description | Usage |
|------|-------------|-------|
| **[PIMap](https://github.com/iosec-shekhar/pimap)** | Automated black-box prompt injection scanner — sqlmap for LLMs. 8 attack modules, 33 payloads, HTML reports | `python3 pimap.py --url https://app.com/chat --param message --level 3` |
| **[Garak](https://github.com/leondz/garak)** | LLM vulnerability scanner — tests for prompt injection, jailbreaks, data leakage, hallucination | `python3 -m garak --model openai --model_type gpt-3.5-turbo --probes all` |
| **[PyRIT](https://github.com/Azure/PyRIT)** | Microsoft's Python Risk Identification Toolkit for LLMs. Red-teaming framework with attack strategies | `from pyrit.orchestrator import PromptSendingOrchestrator` |
| **[promptmap](https://github.com/utkusen/promptmap)** | Automatic prompt injection testing for ChatGPT plugins | `python3 promptmap.py --plugin-url https://plugin.example.com` |
| **[LLMFuzzer](https://github.com/mnns/LLMFuzzer)** | Fuzzing framework for LLM APIs — jailbreaks and prompt injection | `python3 llmfuzzer.py --target openai --model gpt-4` |
| **[Vigil](https://github.com/deadbits/vigil-llm)** | LLM prompt injection and jailbreak detection — defensive scanner | `python3 vigil.py --text "your prompt here"` |

---

## AI-Assisted Penetration Testing

| Tool | Description | Usage |
|------|-------------|-------|
| **[PentestGPT](https://github.com/GreyDGL/PentestGPT)** | GPT-powered penetration testing assistant — guides through recon, exploitation, and reporting | `python3 main.py` then describe your target |
| **[HackingBuddyGPT](https://github.com/ipa-lab/hackingBuddyGPT)** | LLM-powered autonomous privilege escalation agent — tested on Linux targets | `python3 wintermute.py --target 192.168.1.1 --user lowpriv` |
| **[AutoAttacker](https://github.com/xu-zhiyuan/autoattacker)** | Automated network penetration using LLMs as reasoning engine | Research tool — see repo for setup |
| **[Burp AI Extension](https://portswigger.net/burp/documentation/desktop/tools/ai-assistant)** | Built-in AI assistant in Burp Suite Pro — explains findings, generates payloads | Available in Burp Suite Pro UI |
| **[NightShade](https://github.com/t3l3machus/Nightshade)** | AI-augmented payload generator for web application testing | `python3 nightshade.py --target https://example.com` |

---

## Vulnerability Research & Triage

| Tool | Description | Usage |
|------|-------------|-------|
| **[COIT](https://github.com/iosec-shekhar/coit)** | CVE-to-OT Impact Translator — maps any CVE to OT/ICS operational context, MITRE ATT&CK for ICS, Purdue levels | `python3 coit.py CVE-2021-34527 --backend ollama` |
| **[VulnBot](https://github.com/Sckathach/VulnBot)** | AI-powered vulnerability analysis and CVE triage assistant | `python3 vulnbot.py --cve CVE-2024-1234` |
| **[ai-exploits](https://github.com/protectai/ai-exploits)** | Collection of real-world AI/ML exploits — MLflow, Jupyter, Ray vulnerabilities | Reference + PoC collection |
| **[Nuclei AI](https://github.com/projectdiscovery/nuclei)** | Nuclei templates now include AI-generated detection logic | `nuclei -t ai-templates/ -u https://target.com` |

---

## Malware Analysis

| Tool | Description | Usage |
|------|-------------|-------|
| **[Firmware Threat Model](https://github.com/iosec-shekhar/firmware-threat-model)** | Automated STRIDE threat modelling from firmware binaries — extracts filesystem, analyses strings, maps to ATT&CK | `python3 firmware_threat_model.py firmware.bin --backend ollama` |
| **[Malware Revealer](https://github.com/MansourSayedMalware/MalwareRevealer)** | LLM-based static malware analysis — explains obfuscated scripts in plain English | `python3 revealer.py --file suspicious.ps1` |
| **[gepetto](https://github.com/JusticeRage/Gepetto)** | IDA Pro plugin — uses GPT to explain decompiled functions and rename variables | IDA Pro plugin — F2 to query |
| **[BinGPT](https://github.com/ch3ck/BinGPT)** | Binary analysis with GPT — asks natural language questions about disassembled code | `python3 bingpt.py --binary target.exe --ask "what does this function do"` |
| **[CAPA + LLM](https://github.com/mandiant/capa)** | CAPA detects capabilities in executables — pair with LLM for explanation | `capa suspicious.exe --json \| python3 explain.py` |

---

## SAST / Code Security

| Tool | Description | Usage |
|------|-------------|-------|
| **[Semgrep AI](https://semgrep.dev/products/semgrep-assistant)** | Semgrep Assistant — AI triage and fix suggestions for SAST findings | Semgrep Cloud Platform |
| **[CodeShield](https://github.com/meta-llama/PurpleLlama/tree/main/CodeShield)** | Meta's LLM-based insecure code detector — identifies CWEs in Python, C, JavaScript | `python3 codeshield.py --file app.py` |
| **[Snyk Code AI](https://snyk.io/product/snyk-code/)** | DeepCode AI — AI-powered SAST with fix suggestions | `snyk code test` |
| **[insider](https://github.com/insidersec/insider)** | SAST tool with AI-enhanced pattern detection for mobile and web | `insider -tech javascript -target ./src` |

---

## Threat Intelligence

| Tool | Description | Usage |
|------|-------------|-------|
| **[OT CVE Research](https://github.com/iosec-shekhar/ot-cve-research)** | Maps all OT/ICS CVEs to MITRE ATT&CK for ICS — annual research dataset with HTML/PDF reports | `python3 ot_cve_research.py --vendor schneider --html report.html` |
| **[OpenCTI](https://github.com/OpenCTI-Platform/opencti)** | Open Cyber Threat Intelligence platform — AI-enriched IOC correlation and graph analysis | `docker-compose up -d` |
| **[MISP + AI](https://github.com/MISP/misp-modules)** | MISP threat sharing with AI enrichment modules | MISP modules — see docs |
| **[ThreatFox AI](https://threatfox.abuse.ch/)** | IOC repository with ML-based classification | REST API — `curl https://threatfox-api.abuse.ch/api/v1/` |

---

## OT / ICS Security

| Tool | Description | Usage |
|------|-------------|-------|
| **[COIT](https://github.com/iosec-shekhar/coit)** | CVE-to-OT Impact Translator — CVSS scores don't tell OT engineers what matters. COIT does | `python3 coit.py CVE-2023-38545` |
| **[Firmware Threat Model](https://github.com/iosec-shekhar/firmware-threat-model)** | Upload any firmware binary, get a STRIDE threat model with IEC 62443 mapping | `python3 firmware_threat_model.py plc_firmware.bin` |
| **[OT CVE Research](https://github.com/iosec-shekhar/ot-cve-research)** | Systematic 2024 OT CVE landscape — ATT&CK for ICS mapping, vendor rankings, research reports | `python3 ot_cve_research.py --json dataset.json --pdf report.pdf` |
| **[GrassMarlin](https://github.com/nsacyber/GRASSMARLIN)** | NSA passive ICS/SCADA network mapping tool — AI-assisted device classification | Standalone app — see releases |

---

## Network Security

| Tool | Description | Usage |
|------|-------------|-------|
| **[NetworkGPT](https://github.com/irgolic/NetworkGPT)** | Natural language network analysis — ask questions about PCAP files | `python3 networkgpt.py --pcap capture.pcap --ask "show me all DNS queries"` |
| **[Zeek + ML](https://github.com/zeek/zeek)** | Zeek network monitor with ML-based anomaly detection plugins | `zeek -r capture.pcap` |
| **[PacketWhisperer](https://github.com/jrecursive/PacketWhisperer)** | LLM-based PCAP analysis and threat hunting | `python3 packetwhisperer.py --pcap traffic.pcap` |

---

## Cloud Security

| Tool | Description | Usage |
|------|-------------|-------|
| **[CloudGPT](https://github.com/ustayready/cloudgpt)** | AI-powered cloud security analysis — reviews IAM policies, S3 buckets, security groups | `python3 cloudgpt.py --provider aws --resource iam-policy.json` |
| **[Cloudsplaining AI](https://github.com/salesforce/cloudsplaining)** | AWS IAM analysis with AI-generated risk explanations | `cloudsplaining scan --input policy.json` |
| **[Prowler AI](https://github.com/prowler-cloud/prowler)** | Cloud security assessment with AI-summarised findings | `prowler aws --ai-summary` |

---

## Defensive / Blue Team

| Tool | Description | Usage |
|------|-------------|-------|
| **[Vigil](https://github.com/deadbits/vigil-llm)** | Real-time LLM prompt injection detection for production apps | `pip install vigil-llm` then wrap your LLM calls |
| **[LLM Guard](https://github.com/protectai/llm-guard)** | Input/output sanitisation library for LLM apps — detects injection, PII, toxicity | `from llm_guard import scan_prompt` |
| **[Rebuff](https://github.com/protectai/rebuff)** | Prompt injection detector with canary tokens and heuristics | `from rebuff import Rebuff` |
| **[Microsoft Presidio](https://github.com/microsoft/presidio)** | PII detection and anonymisation for LLM outputs | `python3 -m presidio_analyzer analyze --text "text here"` |
| **[Wazuh + AI](https://github.com/wazuh/wazuh)** | SIEM/XDR with AI-driven anomaly detection and alert correlation | `docker-compose up -d` |
| **[HOL Guard](https://github.com/hashgraph-online/hol-guard)** | Local policy and approval controls for supported AI coding-agent actions, MCP tools and package installs | `hol-guard status` |

---

## Research & Datasets

| Resource | Description | Access |
|----------|-------------|--------|
| **[OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)** | The definitive LLM security risk classification | owasp.org |
| **[MITRE ATLAS](https://atlas.mitre.org/)** | Adversarial Threat Landscape for AI Systems — ATT&CK for ML | atlas.mitre.org |
| **[MITRE ATT&CK for ICS](https://attack.mitre.org/matrices/ics/)** | ICS/OT specific adversary techniques | attack.mitre.org |
| **[AI Incident Database](https://incidentdatabase.ai/)** | Real-world AI failure and incident reports | incidentdatabase.ai |
| **[HarmBench](https://github.com/centerforaisafety/HarmBench)** | Standardised evaluation framework for LLM red-teaming | Research benchmark |
| **[PromptBench](https://github.com/microsoft/promptbench)** | Microsoft's adversarial robustness benchmark for LLMs | Research benchmark |

---

## Contributing

Pull requests welcome. Please follow this format for new entries:

```
| **[Tool Name](link)** | One-line description | `usage command` |
```

Categories to consider: is it offensive or defensive? Is it LLM-specific or AI-assisted? Where does it fit?

---

## From the iosec.in Toolkit

Tools built and maintained by [iosec.in](https://iosec.in):

| Tool | Repo | Focus |
|------|------|-------|
| PIMap | [iosec-shekhar/pimap](https://github.com/iosec-shekhar/pimap) | Prompt injection testing |
| COIT | [iosec-shekhar/coit](https://github.com/iosec-shekhar/coit) | OT CVE impact translation |
| OT CVE Research | [iosec-shekhar/ot-cve-research](https://github.com/iosec-shekhar/ot-cve-research) | OT threat landscape research |

---

*Maintained by [iosec.in](https://iosec.in) · MIT License*
