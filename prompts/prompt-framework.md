# Prompt Framework: AI Website Copy Generator for Local Businesses
**Task 1 | Future Interns Prompt Engineering Internship**

---

## Overview

This document outlines the structured prompt system designed to generate high-quality, conversion-focused website copy for local businesses using AI tools (Claude / ChatGPT / Gemini).

The framework is modular and reusable, each prompt block targets a specific section of a business website and can be adapted to any local business type by swapping the variables.

---

## Prompt Architecture

The system uses a **3-layer prompt structure**:

```
Layer 1: Context Injection     -> Who the business is, who the customer is
Layer 2: Section-Specific Task -> What copy to generate (homepage, services, CTA)
Layer 3: Tone & Constraint     -> How to write it (voice, length, style rules)
```

This separation makes prompts **reusable, testable, and easy to iterate on** : a core principle of good prompt engineering.

---

## Master Context Prompt (Run First)

This prompt is sent once at the start to establish the business identity. All subsequent prompts reference this context.

```
You are a professional website copywriter specialising in local businesses.

I need you to write website copy for the following business:

Business Name: [BUSINESS_NAME]
Type: [BUSINESS_TYPE] (e.g., café, salon, clinic)
Location: [CITY, NEIGHBOURHOOD]
Target Audience: [PRIMARY CUSTOMER PROFILE]
Unique Selling Proposition: [WHAT MAKES THEM DIFFERENT]
Tone: [TONE — e.g., warm and neighbourly / professional / playful]
Price Range: [PRICE POSITIONING, e.g., mid-range, premium, affordable]

Keep all copy:
- Benefit-driven, not feature-driven
- Conversational but polished
- Free of jargon
- Ready to publish on a real website (no placeholders like [INSERT NAME])

Acknowledge this brief and wait for my section-specific instructions.
```

---

## Prompt 1: Homepage Copy

```
Using the business context above, write the homepage copy. Include:

1. HEADLINE
   - One powerful sentence that communicates the core value proposition
   - Should answer: "Why should I care?" in under 10 words
   - Avoid generic openers like "Welcome to..." or "The best..."

2. SUB-HEADLINE
   - 1–2 sentences explaining who this is for and what they get
   - Should feel like a natural follow-on to the headline

3. INTRO SECTION
   - 3–4 sentences introducing the business
   - Emphasise feeling and experience, not just facts
   - End with a soft invitation to explore or visit

Format each section with a clear label. Do not add explanations — output only the copy.
```

---

## Prompt 2: Services Page Copy

```
Now write the Services page copy for the same business. Include:

For each of the 4–5 core services/offerings:
- SERVICE NAME (short, clear)
- ONE-LINE DESCRIPTION (what it is)
- BENEFIT STATEMENT (why the customer will love it - 1 sentence)
- MICRO-CTA (a 4–6 word action phrase, e.g., "Reserve your table today")

Then write a short SERVICES INTRO paragraph (2–3 sentences) that sits above the service list, explaining the overall experience the customer can expect.

Keep tone consistent with the homepage. Avoid bullet-point overload (write like a human, not a product catalogue).
```

---

## Prompt 3: CTA Sections

```
Write three separate CTA (Call-to-Action) sections for the business website:

CTA 1: PRIMARY CTA (above the fold / hero section)
- Action-oriented headline (5–8 words)
- Supporting line (1 sentence, reduces friction)
- Button text (2–4 words)

CTA 2: TRUST-BUILDER CTA (mid-page, after services)
- Lead with a social proof or reassurance statement
- Follow with an invitation to visit or get in touch
- Button text (2–4 words)

CTA 3: FOOTER / CLOSING CTA
- Warm, community-feel closing message (2–3 sentences)
- Location mention for local SEO relevance
- Button text (2–4 words)

Each CTA should feel distinct in energy: urgent, reassuring, and warm respectively.
```

---

## Prompt 4: Tone Adaptation (Reusability Layer)

This prompt demonstrates how the same framework adapts to different business types. Swap the tone instruction to instantly shift the voice.

```
Rewrite the homepage headline and sub-headline from the previous output,
but this time adapt the tone for a [NEW TONE] business.

Tone options:
- "friendly and approachable" -> for salons, cafes, bakeries
- "clinical and trustworthy" -> for clinics, diagnostic labs, pharmacies
- "confident and results-driven" -> for agencies, coaches, consultants
- "fun and energetic" -> for gyms, youth brands, event spaces

Keep the core value proposition the same. Only the voice and word choice should change.
Show the original and the adapted version side by side for comparison.
```

---

## Prompt Engineering Notes

| Principle | How It's Applied |
|---|---|
| **Role prompting** | "You are a professional website copywriter" sets expert behaviour |
| **Context injection** | Master prompt pre-loads all business variables before tasks begin |
| **Constraint setting** | Rules like "no placeholders", "under 10 words" prevent common AI failures |
| **Modular structure** | Each prompt is independent, easy to re-run, test, or swap |
| **Output formatting** | Section labels requested explicitly to make outputs parse-ready |
| **Tone as a variable** | Tone is extracted into its own layer, enabling reuse across client types |

---

## Tool Used
**Claude (claude.ai):** Anthropic's conversational AI, selected for its instruction-following consistency and nuanced tone control.

---

*Task 1: Future Interns Prompt Engineering Internship Program*