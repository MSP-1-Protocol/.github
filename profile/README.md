# MSP-1 — Mark Semantic Protocol

A universal, AI-first metadata standard enabling machine-readable clarity, authority signals, and structured intent across the web.

**Current Version:** MSP-1.0.2  
**Official Site:** https://msp-1.org/  

---

## 🌐 What is MSP-1?

MSP-1 (Mark Semantic Protocol) is a **machine-first metadata standard** that gives AI agents a clear, explicit way to understand:

- What a site is about (purpose & primary topic)  
- Who it serves (audience & intent)  
- How authoritative it is (expertise & originality signals)  
- How and when content is updated   
- How pages relate internally and externally (semantic relationships)  

Instead of forcing AI to guess meaning from HTML, MSP-1 exposes **structured intent** in a predictable, JSON-based format.

---

## 📦 Core Components

MSP-1 is built around three simple but powerful ideas:

1. **Site-level declaration**  
   - `/.well-known/msp.json`  
   - Declares protocol support, version, site purpose, authority level, and content mapping.

2. **Page-level metadata**  
   - Per-URL JSON files that describe:
     - content type (homepage, article, gallery, blog post, etc.)  
     - topic, audience, and primary intents  
     - authority & originality signals  
     - update cadence & last substantive edit  
     - entities, keywords, and relationships  

3. **JSON Schemas for validation**  
   - Official schemas under:  
     - `https://msp-1.org/schema/`  
   - Enable strict validation and tool integration.

---


## 🚀 Getting Started (For Implementers)

1. **Place `/.well-known/msp.json`** at your site root  
   - Ensure it resolves at:  
     `https://your-domain.com/.well-known/msp.json`  
   - Edit the placeholder values to reflect your domain, audience, and policies.

2. **Expose page-level MSP-1 JSON**  
   - Follow the `pageMetadataPattern` in `msp.json`  
   - Validate against `msp-1-page.json` or a more specific schema (article, gallery, blog, etc.).

3. **Validate your implementation**  
   - Use tools from `msp-1-tools` (CLI or online validators)  
   - Confirm your JSON passes schema validation and matches your site structure.

---

## 🤖 For AI Agents & Crawlers

AI agents integrating MSP-1 should:

1. **Discover**  
   - Request: `/.well-known/msp.json` from the site root.  

2. **Inspect**  
   - Read `protocol`, `version`, `site`, and `content`.  
   - Honor declared training and derivative-use conditions.

3. **Resolve Page Metadata**  
   - Use `content.pageMetadataPattern` and `content.primaryContentRoots` to locate page-level MSP-1 JSON.  

4. **Interpret**  
   - Treat MSP-1 metadata as **explicit semantic guidance**, especially for:
     - authority weighting  
     - topical relevance  
     - content freshness  
     - safe use conditions  


---

## 🤝 Contributing & Governance

MSP-1 is designed to be:

- **Open** – publicly documented and openly visible  
- **Stable** – versioned with semantic rules (MSP-1.0.x)  
- **Pragmatic** – minimal, JSON-based, and easy to implement  

Contribution model (early phase):

- Protocol evolution is **centrally stewarded** to maintain coherence.  
- Feedback, issues, and proposals are welcome via GitHub Issues and Pull Requests.  
- Major breaking changes will be reserved for future major versions (e.g., MSP-2.x).

See individual repositories for:

- `CONTRIBUTING.md` – how to propose changes  
- `SECURITY.md` – how to report security concerns  
- `LICENSE` – licensing terms (e.g., MIT)

---

## 📬 Contact

**Standards & Development:**  
`dev@msp-1.org`  

**Official Site:**  
https://msp-1.org/

If you are building AI agents, AI-ready websites, or AIO/AEO/GEO optimization tooling, MSP-1 is designed to be your **semantic bridge** between human-authored content and machine interpretation.
