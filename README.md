# FUTURE_PE_01
## Task 1: AI Website Copy Generator for Local Businesses
Most businesses lose customers, not because their services are bad, but rather because their website copy is unclear, generic or outdated. Hiring a professional copywriter is expensive. This task explores how structured prompt engineering can solve that problem at scale.

**Goal:** To design a reusable prompt framework that generates high-quality, conversion-focused website copy for any local business.

**Tools used:** Claude, Lovable

### Business chosen: Ember & Lily Café 
#### Location: Al Mankhool, Dubai, UAE
A fictional neighbourhood café targeting residents and remote workers in Dubai who are tired of loud, rushed chain cafés. 

The name Ember & Lily evokes warmth(ember) and lightness(lily), the two feelings the café is built around.

**Why this business?**

- Dubai has a massive café culture but is dominated by chains
- The "cozy neighbourhood" gap is a genuine market need
- It's relatable to a local audience while being portfolio-friendly

### Prompt Logic
The framework uses a 3-layer architecture:

Layer 1: Context Injection
- Establishes business identity, audience, tone, and USP
- Run once at the start (all other prompts reference this)

Layer 2: Section-Specific Prompts
- Homepage Copy (headline, sub-headline, intro)
- Services Page (offerings with benefit statements + micro-CTAs)
- CTA Sections (primary, trust-builder, footer)

Layer 3: Tone Adaptation
- Demonstrates prompt reusability across business types
- Same structure, swapped tone variable (completely different voice)

### Repository consists of:
README.md

prompts/prompt-framework.md (Full prompt system with documentation)

outputs/website-copy-ember-lily-cafe.md (AI-generated website copy + tone comparison)
    
### How to Reuse This Framework
- Open prompts/prompt-framework.md
- Fill in the Master Context Prompt with your client's details
- Run Prompt 1 -> 2 -> 3 in sequence in Claude or ChatGPT
- Use Prompt 4 to adapt tone for a different business type
- Copy outputs directly into Framer AI, Lovable, or any website builder

### Website made using Lovable AI : https://ember-and-lily-local.lovable.app/

*Future Interns — Prompt Engineering Internship Program 2026*
