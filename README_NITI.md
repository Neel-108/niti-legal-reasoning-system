# NITI - Legal Reasoning System for Lawyers

NITI is a prompt-based AI reasoning system built for licensed lawyers practising in India. It performs structured risk analysis on contracts and legal documents, conducts doctrinal legal research, and surfaces issues with counter-views and confidence ratings without crossing into legal advice or drafting.

Current version: **1.7.2** | May 2026


## What NITI Does

NITI operates in two modes:

**Document Analysis**
Upload a contract or legal document. NITI reads it, classifies the document type, checks completeness, identifies High and Medium risks with counter-interpretations and failure scenarios, runs a structural gaps checklist calibrated to the document type, and surfaces systemic risks and challenge points.

**Legal Research**
Ask any legal or doctrinal question without a document. NITI reasons through it, presents mandatory counter-views where ambiguity exists, states assumptions explicitly, and flags what needs verification.

NITI was stress-tested across 51 tests including adversarial red-teaming, prompt injection, and authority override scenarios. Plain Claude has no equivalent behavioral discipline.



## What NITI Does Not Do

- **No legal advice.** NITI identifies and analyses risks. It does not tell you what to do.
- **No drafting.** NITI will not write, rewrite, or produce legal language of any kind.
- **No hallucination.** NITI will not fabricate statutes, section numbers, or case citations. If a reference cannot be verified, it says so.
- **No action guidance.** NITI will not advise on signing, proceeding, or any transactional decision.



## Architecture

NITI operates through four layers:

**Analysis Engine** - Document comprehension, classification, jurisdiction determination, completeness verification.

**Research Buddy Engine** - Counter-interpretations, doctrinal reasoning, enforcement patterns, exploratory reasoning anchored to document where present.

**Compression Engine** - Active in all modes. Removes non-essential text, eliminates repetition, preserves decision-relevant signal.

**Epistemic Control System** - Confidence ratings (High / Medium / Low), basis of uncertainty, and specific challenge points on every major issue. Uncertain conclusions are never presented as definitive.



## Why Prompt-Based, Not SaaS

Legal documents are confidential by definition. A SaaS product or API-based deployment means client documents passing through servers, logs, and third-party infrastructure outside the lawyer's control.

NITI runs as a self-contained system prompt inside the lawyer's own Claude interface. No data is stored anywhere outside their session. The lawyer pastes the document, receives the analysis, closes the window. Nothing persists.

The architecture matches the confidentiality requirements of the domain. This is not a technical limitation but it is the correct security model for legal work.



## How to Use

**For document analysis:**
1. Upload the contract or document
2. Send: `Analyze this agreement.`
3. Ask follow-up questions naturally

**For research:**
1. Ask your legal question directly, no document needed

**Tips:**
- Redact client names and sensitive identifiers before uploading
- Always upload the complete document including all schedules and exhibits
- One session = one matter. Start a new chat for a new matter.
- If an output feels wrong, push back. NITI will reassess from first principles.



## Testing

NITI was developed through five test sessions across three distinct test types: structured protocol testing, adversarial red-teaming, and real-world stress scenarios. 
Each session had a defined scope, defined failure modes to find, and a measurable outcome. 
Details of Test Reports are mentioned in the QA folder. 

**Methodology note:**
Test cases were AI-assisted in design, manually executed, with each failure personally analysed and patched. 
The tester is not a lawyer. The legal reasoning was validated against adversarial scenarios and internal consistency, not personal legal expertise.



## Limitations

NITI is an AI system. 
All outputs are analytical inputs for the lawyer's judgment and not verified legal conclusions. 
NITI is reliable on well-formed inputs but is not a substitute for professional judgment. 
The lawyer remains fully responsible for all professional decisions and client advice.



## Status

Prompt-based system. Not commercially available. Built for professional legal use in India with secondary capability on US law (Delaware corporate, SEC/SEBI securities).
To request access or discuss deployment: swapnilpanchal465@gmail.com 


