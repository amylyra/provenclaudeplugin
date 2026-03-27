# Plugin Eval — Test Briefs

Run each brief through the plugin in Cowork. Score each dimension 1-10. Log where the pipeline breaks, what you had to manually fix, and how long it took vs. doing it the old way.

---

## Test 1 — Single Email (Simplest)

**Brief:** "Win-back email for the Personalized Cleanser. Targeting customers who haven't purchased in 90+ days. Goal: get them to reorder. Include a 15% discount code WELCOME15."

**What to score:**

| Dimension | What to look for | Score |
|---|---|---|
| **Copy quality** | Does it sound like PROVEN voice? No filler, no hedging, evidence-led? | /10 |
| **Email structure** | Subject line, preheader, headline, body, CTA — all present? Klaviyo tokens? | /10 |
| **Image relevance** | Does the hero image match the story? Is it on-brand (binding rules)? | /10 |
| **Assembly** | Does the HTML render? Fonts, colors, spacing correct? | /10 |
| **Brand QA** | Did the agent run QA? Do you agree with the score? | /10 |
| **No intervention needed** | Did it complete without you stepping in to redirect? | Yes/No |

**Time:** _____ minutes (vs. estimated _____ minutes doing it manually)

---

## Test 2 — Product UI (No Marketing Pipeline)

**Brief:** "Redesign the quiz results card. It should show the customer's top 3 skin concerns, their personalized formula name, and a CTA to purchase. Mobile-first."

**What to score:**

| Dimension | What to look for | Score |
|---|---|---|
| **Correct pipeline** | Did it skip proven-email and proven-creative? Went straight to proven-ui? | /10 |
| **Design quality** | Does it feel like PROVEN? Tokens correct? Responsive? | /10 |
| **UX logic** | Is the information hierarchy right? Does the CTA feel natural? | /10 |
| **Code quality** | Clean HTML/CSS? Accessible? No hacky workarounds? | /10 |
| **Brand QA** | Did QA run? Score accurate? | /10 |

**Time:** _____ minutes

---

## Test 3 — Social Media (Copy + Imagery)

**Brief:** "3 Instagram feed posts for the SPF launch. Targeting existing customers. Tone: exciting but not hype-y. Each post needs a different angle — one about the science, one about daily routine, one about ingredients."

**What to score:**

| Dimension | What to look for | Score |
|---|---|---|
| **Copy variety** | Are the 3 posts genuinely different angles, not just reworded versions? | /10 |
| **Platform fit** | Correct for IG? Right length, right tone, no hashtag spam? | /10 |
| **Image prompts** | Did it use proven-creative pipeline? Correct bands? Validator run? | /10 |
| **Image quality** | Do Gemini results look on-brand? Chrome responsive? Warm materials? | /10 |
| **Aspect ratio** | Images generated at 1:1 or 4:5? Not landscape? | /10 |

**Time:** _____ minutes

---

## Test 4 — Paid Media (Ad Variations)

**Brief:** "Google Ads creative pack for the Personalized Night Cream. Targeting cold traffic searching 'personalized skincare.' Need headline and description variations plus image options."

**What to score:**

| Dimension | What to look for | Score |
|---|---|---|
| **Character limits** | Headlines ≤30 chars? Descriptions ≤90 chars? | /10 |
| **Variation quality** | Are variations genuinely different approaches, not synonyms? | /10 |
| **Copy quality** | PROVEN voice even in short-form? No generic ad-speak? | /10 |
| **Image variations** | Multiple aspect ratios (1.91:1, 1:1)? Different compositions? | /10 |
| **Brand QA** | Did QA catch anything? | /10 |

**Time:** _____ minutes

---

## Test 5 — Multi-Channel Campaign (Stress Test)

**Brief:** "Mother's Day campaign. Product: System Kit as a gift. Channels: 1 email, 3 IG posts, 1 landing page. Story: 'She figured out your skin before you did.' Promo: free gift wrap with code FORMOM."

**What to score:**

| Dimension | What to look for | Score |
|---|---|---|
| **Narrative consistency** | Same story across all channels? Or did it drift? | /10 |
| **Channel adaptation** | Each channel formatted correctly? Not just the same thing pasted everywhere? | /10 |
| **Image reuse** | Did it generate images once and adapt, or regenerate redundantly? | /10 |
| **Context management** | Did quality degrade toward the end? Which channel was last? | /10 |
| **Total completion** | Did it finish everything, or did it run out of steam? | /10 |
| **Brand QA** | Did QA run on the full package? Score accurate? | /10 |

**Time:** _____ minutes

---

## How to Read Results

- **All tests score 7+ across the board:** Plugin is ready for team rollout. Iterate from real usage.
- **Tests 1-4 score well, Test 5 breaks:** Context management needs work. Consider splitting multi-channel into sequential sessions by design (not a bug, a workflow choice).
- **Copy scores high but image scores low:** The proven-creative → Gemini pipeline needs tuning. Likely prompt structure isn't translating well to Gemini's model.
- **Agent keeps asking for approval mid-pipeline:** The gate conflict isn't resolved. Tighten the agent instructions.
- **Everything takes longer than manual:** The overhead of loading skills and running the full pipeline isn't worth it for simple tasks. Consider adding a "lightweight mode" where the agent skips QA and image generation for quick requests.

---

## After Testing

Log your results and bring them back. I'll use the scores to diagnose which parts of the agent instructions, skill files, or pipeline logic need adjustment.
