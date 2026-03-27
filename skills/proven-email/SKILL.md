---
name: proven-email
description: "PROVEN Skincare's email strategy and execution skill for Klaviyo. Use when creating, reviewing, or optimizing any PROVEN email — campaigns, flows, templates, subject lines, or email strategy. Covers email architecture, segment-specific messaging, campaign blueprints, flow sequence design with timing and branching logic, Klaviyo template HTML structure, personalization tokens, and performance optimization. Triggers on any request involving PROVEN emails, Klaviyo campaigns, email templates, email copy, subject lines, email flows, email reporting, email strategy, drip sequences, abandoned cart flows, welcome series, or win-back flows. Also use when asked to build, edit, or review email HTML for PROVEN, or when analyzing email performance data. This skill handles the *what*, *when*, *to whom*, and *structure* of email. Pair with proven-voice for copy tone and proven-fe-designer for visual design decisions."
---

# PROVEN Email — Klaviyo Execution Skill

Build PROVEN emails the way the brand builds skincare: every element chosen for a reason, nothing generic, nothing wasted.

This skill has three parts:
1. **Shared Foundations** — what applies to every email, campaign or flow
2. **Campaign Playbooks** — editorial sends: seasonal, educational, sales, UGC, brand
3. **Flow Playbooks** — behavioral sequences: quiz abandon, welcome, cart abandon, one-time buyer conversion, churned win-back

It does not duplicate the brand voice (use `proven-voice`) or the visual design system (use `proven-fe-designer`). It tells you *what* to send, *to whom*, *when*, and *how to structure it*.

---

# PART 1: SHARED FOUNDATIONS

## How to Think

Before building any email, answer one question: **Does this email make the reader feel like we already know them?**

PROVEN's emails are not broadcasts. They are evidence that the system is paying attention. Every email should feel like it was written by someone who knows the reader's skin, their history with the brand, and where they are in their journey.

**Four laws that govern every send:**

**1. One email, one job.** State the purpose in one sentence. If you can't, split it. This is absolute — no email does two things.

**2. The reader's skin is the subject.** Open with what matters to them — their skin, their season, their concern. Never open with the brand, the sale, or the product. Those come second.

**3. Evidence before ask.** Establish why before asking for action. The CTA earns its click through the content above it, not through button color or urgency language.

**4. Respect the inbox.** PROVEN sends ~37 email variations per month — 2-3x the industry average. Every email must teach, recognize, or solve something specific. If it doesn't do one of those three things, don't send it.

---

## Audience Architecture

Every campaign and flow targets a specific audience. Never send to "everyone."

### System Subscribers (~17,500)
**Stage:** Delegation — they trust the system.
**Role:** Retention, cross-sell, seasonal education, reformulation awareness.
**Benchmarks:** 1.5-2.5% CTR, $0.70-$2.40 RPR, 65-72% open rate.
**Tone:** Warm, low-pressure. Reinforce the choice they already made.
**Key segments:** `Opened 30 Days - System Subscribers` (highest engagement), `Opened 70 Days - System Subscribers` (standard window), `System Subscribers (opened ever)` (broadest).

### Eye Duo Subscribers (~2,600)
**Stage:** Committed but narrow product relationship.
**Role:** Upsell to full system, eye-area science, cross-sell.
**Benchmarks:** 4-5% CTR, $2.00-$2.40 RPR — smallest but highest-converting segment.
**Tone:** Specific. Lead with eye-area evidence.

### Churned Subscribers (~13,400)
**Stage:** Post-delegation — trust broke.
**Role:** Win-back through reformulation messaging, seasonal triggers, new launches.
**Tone:** No guilt. No "we miss you." Instead: "Your skin changed. So did we."
**Key segments:** `Opened 30/90 Days - Churned Subscribers`, `Churned Subscribers (opened ever)`.

### One-Time Buyers (~1,200)
**Stage:** Skeptical trust — tried it, didn't commit.
**Role:** Subscription conversion. Show the system advantage.
**Tone:** Evidence-forward. Results timelines. Compounding effect.
**Key segments:** `Opened 30/90/120 Days One Time Buyers`.

### Prospects (~103,000+)
**Stage:** Awareness to consideration. Many quiz-abandoned.
**Role:** Education, social proof, quiz completion, first purchase.
**Benchmarks:** 0.1-0.4% CTR, $0.01-$0.13 RPR. Open rates 77-83% (higher than subscribers).
**Tone:** Educational, curiosity-driven. Sell the idea that skincare can be solved — not the product.
**Key segments:** `New Prospects`, `Opened 30 Days - Prospects` (warm), `Opened 90 Days - Prospects` (standard), `90/210 Day Openers - Lapsed Prospects`, `Prospects (opened ever)`.

**The prospect paradox:** Prospect open rates are the *highest* in the account but click-through is 10-50x lower than subscribers. The subject lines work. The email body doesn't. Every prospect email must be structurally optimized for click-through — see Prospect Email Architecture below.

### Exclusion Logic (Every Send)

Always exclude: `PROVEN AF`, `Unsubscribed From Marketing Emails`, `Bounced`, `Proven Skincare`, `Proven Skincare Emails`.

Prospect campaigns: also exclude `System Subscribers`.
Subscriber campaigns: optionally exclude `Eye Duo Subscribers` (they get their own sends).

---

## Prospect Email Architecture

Prospect emails require a structurally different design from subscriber emails. Prospects don't know PROVEN yet — they need less content, more conviction, and a clearer path to one action.

**The Prospect Email Formula:**

```
┌─────────────────────────────────┐
│ LOGO (small, centered)          │
├─────────────────────────────────┤
│ HEADLINE                        │
│ One sentence. Surprising or     │
│ personally relevant. No brand   │
│ name in the headline.           │
├─────────────────────────────────┤
│ BRIDGE (2-3 sentences max)      │
│ Connect the headline to PROVEN. │
│ One evidence point. One feeling.│
├─────────────────────────────────┤
│ CTA BUTTON                      │
│ "Take the 3-Minute Quiz"        │
│ or "See What Your Skin Needs"   │
├─────────────────────────────────┤
│ SINGLE PROOF POINT (optional)   │
│ One testimonial with specifics  │
│ OR one stat with context        │
├─────────────────────────────────┤
│ FOOTER                          │
└─────────────────────────────────┘
```

**Rules:**
- **Maximum 150 words** of body copy (before footer). Prospects skim — every word above 150 reduces click probability.
- **CTA appears above the fold** on mobile. No scrolling to find it.
- **One CTA only.** Always drives to quiz or results page. Never to a product page, blog, or homepage.
- **No product images** unless the email is specifically about a new product. Prospects haven't taken the quiz — showing products they don't have a relationship with doesn't convert.
- **Subject line does the heavy lifting.** With only 150 words of body copy, the subject line must carry the hook. It's 60% of the work.

**Contrast with subscriber emails:**
Subscriber emails can be longer (250-400 words), include product imagery, have secondary CTAs, and assume familiarity. Prospect emails cannot assume anything.

---

## Email Anatomy (All Emails)

### Required Elements

**1. Subject Line**
- 40-60 characters. Front-load the reader-relevant word.
- No ALL CAPS (except one word for emphasis, rarely). No exclamation marks.
- No emoji unless testing shows clear lift.
- Personalization when it adds meaning: `{{ first_name|default:'Your' }}`.

**2. Preview Text**
- Extends the subject line. Never repeats it.
- 40-90 characters visible. Must make sense as a fragment.

**3. Header**
- PROVEN logo, minimal. No navigation bar.

**4. Hero Block**
- One focal point: image, headline, OR data point. Never all three.

**5. Body**
- One idea per section. Short paragraphs (2-3 sentences).
- Evidence before ask.
- Every feature bridges to a feeling (per `proven-voice`).

**6. Primary CTA**
- One per email. Non-negotiable.
- Ember button (`#C26A4A`, white text, pill shape).
- Action-specific: "Take the Quiz" / "Shop Your Routine" / "Update Your Formula."
- Never: "Learn More," "Click Here," "Shop Now" (generic).

**7. Unsubscribe**
- `{% unsubscribe 'Unsubscribe' %}`. Clean. Visible.

### Optional Elements (One Per Email Maximum)

- **Evidence block:** 1-3 data points with context.
- **Testimonial:** One quote with skin type, timeline, concern.
- **Product block:** Image + 1-2 sentences on why it was chosen.
- **Secondary CTA:** Text link only, after additional context.

---

## Subject Line Patterns

**Skin-first:** "Your winter skin needs different ingredients"
**Surprising fact:** "10% niacinamide is worse than 5%"
**Quiet confidence:** "Your formula updated."
**Recognition:** "{{ first_name }}, your skin profile just got smarter"
**Direct offer:** "25% off your personalized system"

**Refuse:** Clickbait ("You won't believe..."), fear ("Your skin is aging faster than..."), vague ("Big news inside"), exclamatory ("SALE!!!"), rhetorical questions ("Ready for better skin?").

---

## Klaviyo Email Template

### Technical Constraints

Email HTML is not web HTML. These constraints are mandatory:

- **600px max content width.** Table-based layout. No flexbox, no grid, no CSS variables.
- **Inline styles required** for Outlook and older clients. `<style>` blocks for Gmail and Apple Mail, but always duplicate critical styles inline.
- **Fonts degrade gracefully.** Import Albert Sans and Source Serif 4 via `@import` for Gmail/Apple Mail. Always include fallbacks: `'Albert Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif` and `'Source Serif 4', Georgia, 'Times New Roman', serif`.
- **Images blocked by default** in many clients. Never rely on images alone to communicate the message. Every image needs alt text. Every email must make sense with images off.
- **Dark mode handling:** Test that navy (#162743) backgrounds don't invert. Use `color-scheme: light dark;` in `<meta>` and `@media (prefers-color-scheme: dark)` for critical overrides. Ember (#C26A4A) and linen (#FAF6F2) need explicit dark mode values or they wash out.
- **CTA buttons must be bulletproof.** Use the VML/table hybrid pattern — it renders as a styled button even in Outlook where `border-radius` fails.
- **Mobile responsive.** `@media` queries for `max-width: 620px`: content fills 100% width, hero text drops to 28px, body to 15px, CTA buttons are full-width and 56px tall (thumb-friendly).
- **Maximum 3 images per email.** More than 3 increases load time on mobile and triggers aggressive image-blocking in corporate clients.

### Color Palette (Email-Safe)

```
Canvas:             #FFFFFF
Warm section:       #FAF6F2 (linen)
Cool section:       #F5F9FB (lighter sky — better contrast)
Text primary:       #000000
Text secondary:     #4A6D7C (teal-dark — safe on white and linen)
Metadata:           #7295A2 (teal — on pure white only)
CTA fill:           #C26A4A (ember)
CTA text:           #FFFFFF
CTA hover:          #A85A3E
Dark section bg:    #162743 (navy)
Dark section text:  #FFFFFF
Dark section accent: #8CAEB9 (teal-light)
Divider:            #E6DED4 (sand)
```

### CTA Button (Bulletproof)

```html
<table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin: 0 auto;">
  <tr>
    <td align="center" style="background-color: #C26A4A; border-radius: 50px; padding: 14px 32px;">
      <a href="{{ cta_url }}" style="color: #FFFFFF; font-family: 'Albert Sans', Helvetica, Arial, sans-serif; font-size: 15px; font-weight: 600; text-decoration: none; display: inline-block; letter-spacing: 0.02em;">
        Take the Quiz
      </a>
    </td>
  </tr>
</table>
```

### Personalization Tokens

| Token | Use Case | Rule |
|-------|----------|------|
| `{{ first_name\|default:'there' }}` | Greeting | Use only when followed by personalized content. "Hi Sarah" + generic body = fake personalization. |
| `{{ first_name\|default:'Your' }}` | Possessive | "{{ first_name }}'s updated formula" — only in subscriber emails. |
| `{{ person\|lookup:'Skin Type' }}` | Quiz data | Only if profile has this property populated. |
| `{{ person\|lookup:'Primary Concern' }}` | Concern targeting | Use to select content blocks dynamically. |

---

## A/B Testing Framework

PROVEN A/B tests most campaigns. Focus tests on the highest-leverage variable for each audience.

**For prospects (problem = click-through):**
- Test body length: 100 words vs. 200 words
- Test CTA position: above-fold vs. below-fold
- Test CTA copy: action-specific ("Take the 3-Minute Quiz") vs. benefit ("See Your Custom Formula")
- Test content type: stat-led vs. testimonial-led vs. myth-bust-led

**For subscribers (problem = cross-sell/upsell):**
- Test offer structure: percentage off vs. dollar amount vs. free gift
- Test content depth: short product feature vs. ingredient education
- Test CTA: "Add to Your Routine" vs. "Shop Your Formula"

**Rules:**
- Test one variable at a time.
- Minimum 1,000 recipients per variant for email. Minimum 500 for SMS.
- Run for at least 4 hours before selecting a winner. 24 hours preferred.
- Track clicks as primary metric for prospects. Track conversion + RPR for subscribers.

---

## Campaign Build Checklist

- [ ] Single purpose stated in one sentence
- [ ] Target audience selected with engagement window
- [ ] Exclusions applied (always: PROVEN AF, unsubs, bounced, internal)
- [ ] Subscriber/prospect versions built separately (if applicable)
- [ ] Subject line: 40-60 chars, reader-first, no exclamation marks
- [ ] Preview text: extends subject, doesn't repeat it
- [ ] Body follows one-email-one-job rule
- [ ] Prospect email ≤150 words. Subscriber email ≤400 words.
- [ ] Copy reviewed against `proven-voice`
- [ ] One primary CTA, ember, action-specific language
- [ ] CTA above fold on mobile (prospect emails — mandatory)
- [ ] Evidence cited with specifics
- [ ] Unsubscribe present
- [ ] Mobile responsive (test in Klaviyo preview)
- [ ] Images have alt text. Email works with images off.
- [ ] Smart sending enabled
- [ ] Naming: `ba_YYYYMMDD_[theme]_[series#]_[audience]`

---

# PART 2: CAMPAIGN PLAYBOOKS

Six campaign types. Each has a structure, audience strategy, and blueprint.

## 1. Seasonal / Environmental

**Purpose:** Reinforce the adaptive system — PROVEN changes when your environment does.
**Frequency:** 2-4 sends per seasonal transition.
**Audience:** All — but split angles.
**Performance:** Best-performing seasonal sends: `winter_formula_1_subs` (1.2% CTR, $0.78 RPR).

### Subscriber Blueprint
```
Subject: Your winter formula just updated
Preview: Here's what changed — and why

Body:
- Open: Environmental trigger specific to season (not "winter is here" — instead "Indoor heating drops air humidity below 30%. Your skin noticed.")
- Bridge: What PROVEN adjusted (1-2 sentences)
- Evidence: "40% of customers receive seasonally adaptive skincare"
- CTA: "See Your Updated Formula" or "Explore What Changed"
```

### Prospect Blueprint
```
Subject: Why your moisturizer stops working every winter
Preview: It's not the product. It's the season.

Body:
- Open: Surprising environmental fact (e.g., "85% of US households have hard water. Your skin is reacting to your pipes, not your products.")
- Bridge: "PROVEN analyzes 47 factors — including your local climate and water quality — to create a formula that adapts with you." (1 sentence)
- CTA: "Take the 3-Minute Quiz"
```

### Seasonal Calendar

| Period | PROVEN Angle |
|--------|-------------|
| Jan | "Your system is already adapting to the new year." |
| Feb | Winter peak. Barrier repair science. Self-care (not gift-giving). |
| Mar-Apr | Spring transition. Reformulation awareness. "Your skin is shifting." |
| May | UV education. Day Moisturizer SPF emphasis. |
| Jun-Aug | Humidity, travel, environmental changes. Adaptive proof. |
| Sep | Back-to-routine. "3 products. 2 minutes." Simplicity. |
| Oct | Fall transition. Recovery. Barrier repair. |
| Nov | Black Friday / Cyber Monday (see Sales Events). |
| Dec | Boxing Day. Year-in-review. |

---

## 2. Product Education

**Purpose:** Teach ingredient science, debunk myths, position PROVEN's approach.
**Frequency:** 2-3 per month. Protect the 44% educational content ratio.
**Audience:** All. Prospects get "why personalization matters." Subscribers get "what's in yours."

### Blueprint
```
Subject: [Surprising fact or myth-bust]
Preview: [One-sentence expansion]

Body:
- Open: Counterintuitive insight (from knowledge base science section)
  Examples:
  • "10% niacinamide causes more irritation than 5% — with no additional efficacy."
  • "The 'glow' from over-exfoliation is actually low-grade inflammation."
  • "34% of people who quit retinoids were actually purging and should have continued."
- Educate: One concept, explained in 2-3 sentences
- Bridge: How PROVEN handles this
- CTA: Prospects → "Take the Quiz" / Subscribers → "Explore Your Ingredients"
```

**Content themes (rotate monthly):**
1. Biochemical individuality — why copying routines doesn't work
2. The subtraction principle — 3 calibrated products > 12 random ones
3. Environmental intelligence — water hardness, climate, circadian rhythms
4. The inflammation equation — reducing inflammation > adding actives
5. Purging vs. irritation — how to tell the difference

---

## 3. Sales Events

**Purpose:** Revenue during promotional windows.
**Frequency:** 3-6 sends per event.
**Audience:** All, split by segment. Subscriber emails drive the actual revenue (10-20x higher RPR than prospect sends).

### Series Arc (5-Email Sale)

| # | Timing | Job | Audience Width |
|---|--------|-----|---------------|
| 1 | Day 1 | Announce the offer. Clean, direct. | Broadest |
| 2 | Day 2 | Social proof. Why now. | Standard |
| 3 | Day 3 | Education + offer. Ingredient or system angle. | Standard |
| 4 | Day 5 | Urgency. "Ends tomorrow." | Narrow (engaged) |
| 5 | Day 6 | Last chance. Shortest email. | Narrowest |

**Subscriber sale emails:** Lead with savings on their existing routine. "Your 3-step system — $40 less this week."
**Prospect sale emails:** Lead with the offer as a reason to try. "Start your custom routine at 25% off."

**Performance reference (Black Friday):**
- `bf_5_sub`: 1.1% CTR, $1.27 RPR (urgency + subscriber relationship)
- `bf_5_pros`: 0.09% CTR, $0.01 RPR (same urgency, 100x less effective on prospects)
- Takeaway: invest creative energy in subscriber sale emails.

---

## 4. Social Proof / UGC

**Purpose:** Let customers do the convincing.
**Frequency:** 1-2 per month.
**Audience:** Prospects and churned subscribers.

### Blueprint
```
Subject: "[Specific result]" — [Name], [skin type/concern]
Preview: [Timeline] with PROVEN

Body:
- Lead with one specific customer result (not "I love this product" — instead "3 weeks in, my hormonal acne stopped cycling")
- 1-2 additional testimonials, each with: skin type, timeline, specific concern addressed
- Bridge: "Every formula is different because every skin is different."
- CTA: "See What Your Formula Could Look Like" → quiz
```

---

## 5. Brand / Relational

**Purpose:** Emotional connection without selling.
**Frequency:** 1 per month maximum. More than this and it stops feeling special.
**Audience:** Engaged subscribers and warm prospects.

**Structure:** Founder note, behind-the-scenes, company milestone, seasonal reflection. No hard CTA required. Soft: "Reply and tell us how your skin is doing."

**Performance proof:** Thanksgiving note (`thanksgiving_note_all`): 68.7% open rate, $0.77 RPR with minimal CTAs. Goodwill converts.

---

# PART 3: FLOW PLAYBOOKS

Flows are behavioral sequences. They respond to something the customer *did*. They require timing, branching, emotional arcs, and exit conditions — not just content.

## Flow Design Principles

**1. Every flow is a conversation, not a drip.** Each email in the sequence responds to the psychological state the customer is likely in *at that moment* in the sequence. Email 1 after quiz abandon is empathetic. Email 3 is educational. Email 5 is a soft close. The tone evolves.

**2. Timing is content.** The delay between emails communicates as much as the words. A 1-hour first follow-up says "we noticed." A 7-day final email says "no pressure." Get the delays wrong and the right words feel wrong.

**3. Branch on behavior, not demographics.** Did they open the last email? Did they visit the site? Did they click but not convert? These behavioral signals determine which email comes next.

**4. Every flow has an exit.** Define when someone leaves the flow: they converted, they hit the final email, or they were suppressed. Flows without exits send irrelevant emails to people who already bought or fully disengaged.

**5. The emotional arc is the strategy.** Map the feeling progression before writing a single word:

```
EMPATHY → EDUCATION → EVIDENCE → OFFER → SOFT CLOSE
(I see you)  (Here's why)  (It works)  (Here's how)  (Whenever you're ready)
```

---

## Flow 1: Quiz Abandon

**Trigger:** Added to quiz abandon list.
**Current state:** Live (flow `XhUJeH`).
**Current performance:** Email 1: 2.6% CTR, $0.94 RPR. Emails 2-5 decay to 0.5-1.0% CTR.
**SMS in this flow:** 7.8% CTR, $3.72 RPR — SMS dramatically outperforms email for quiz abandon.

### Sequence Design

| # | Delay | Name | Emotional State | Job | CTA |
|---|-------|------|----------------|-----|-----|
| 1 | 1 hour | The Nudge | Curious but distracted | Remind them their results are waiting. Empathy, not pressure. | "Finish Your Quiz" |
| 2 | 24 hours | The Insight | Still considering | One surprising skin fact they didn't know. Create "I need to know more" feeling. | "See What Your Skin Needs" |
| 3 | 3 days | The Proof | Skeptical | One specific customer result with skin type, timeline, and concern match. | "Take the Quiz — 3 Minutes" |
| 4 | 7 days | The Education | Lukewarm | Debunk a skincare myth from the knowledge base. Position PROVEN as the alternative. | "Start Your Custom Formula" |
| 5 | 14 days | The Soft Close | Take it or leave it | Short. Warm. "Whenever you're ready, your formula is waiting." No urgency. | "Take the Quiz" |

**SMS (if opted in):** Send SMS version of Email 1 at 30 minutes. SMS has 3.7x higher RPR than email in this flow — prioritize it.

**Branch logic:**
- After Email 1: If clicked but didn't complete quiz → send Email 2 as "Pick up where you left off" variant.
- After Email 3: If opened none of emails 1-3 → skip to Email 5 (soft close). Don't exhaust the sequence on someone not reading.
- **Exit:** Completed quiz, placed order, or received all 5 emails.

**Optimization note:** The current flow shows steep decay from Email 1 (2.6% CTR) to Email 4 (0.5% CTR). This is normal for abandonment flows, but the gap suggests Emails 2-4 may be too similar in approach. Each email should feel like a different *angle*, not a different *reminder*.

---

## Flow 2: Welcome (Post-Purchase)

**Trigger:** Order Created metric (flow `TNt87K` / `XzDhw6`).
**Current state:** Live. Multiple messages by product type (system, serum, eye).
**Current performance:** Order confirmation: 9-11% CTR, $0.67-$2.50 RPR. Later emails decay: reviews email at 0% CTR, promo emails at 0-0.5% CTR.

This is the most psychologically important flow. The customer just made a purchase and is in **Skeptical Trust** (Phase 2 of the customer lifecycle). The first 48 hours and first product experience determine whether they become a long-term subscriber or churn.

### Sequence Design (System Subscribers)

| # | Delay | Name | Emotional State | Job |
|---|-------|------|----------------|-----|
| 1 | Immediate | Order Confirmation | Excited but nervous | Confirm the purchase. Set expectations: what arrives, when, what to expect in Week 1. |
| 2 | Day 1 | Welcome | Anticipation | Introduce the system. Brief: how to use the 3 products, morning/night. Make it feel simple, not like homework. |
| 3 | Day 5 | First Check-In | Products arrived, trying them | "How's your skin feeling?" Normalize adjustment. Explain calibration phase (Week 1-2). No sell. |
| 4 | Day 14 | The Why | Calibrating, possibly impatient | Explain what's happening under the surface. Reference the Expected Results Timeline. "Week 3-4 is when clearing begins." |
| 5 | Day 28 | Results + Reformulation | Should be seeing results | "One month in." Celebrate. Introduce reformulation as a feature, not a failure. "If something isn't right, we adjust." |
| 6 | Day 45 | Cross-Sell | Trusting the system | Introduce one complementary product (eye cream, serum). Personalized to their profile if possible. |

**Critical rule for this flow:** Emails 1-4 are NOT selling. They are building trust. The current flow has promo emails too early (emails 5 and 6 in the existing flow are promo-focused with 0% CTR). Don't offer discounts or cross-sells before Day 28.

**Branch logic:**
- After Email 3 (Day 5): If they replied or submitted a support ticket → pause the flow, let CX handle.
- After Email 5 (Day 28): If they haven't opened emails 3-5 → they're disengaged. Don't cross-sell. Send a "We're here if you need us" and exit.
- **Exit:** Reached Email 6, or purchased again (they've graduated to the subscriber segment and campaign emails take over).

**Optimization note:** The current Welcome Flow shows a significant drop from Email 1 (5.8% CTR) to Email 4 (0% CTR on reviews email). The reviews email (system message 4) is likely too generic. Replace with personalized check-in content tied to the customer's primary concern.

---

## Flow 3: Abandoned Cart

**Trigger:** Added to Cart / Checkout Started metric (flow `WJxFLu`).
**Current state:** Live. Highly branched by product type (system, serum, eye, SPF, cleanser, night cream).
**Current performance:** Best performers: `cart_save` variants at 10-12% CTR, $5.60-$9.28 RPR. Product-specific emails: 2.5-7.7% CTR. Later promo emails: 2.8-6.6% CTR.

This is PROVEN's highest-RPR flow. The product-specific branching is working — preserve it.

### Sequence Design

| # | Delay | Name | Job | CTA |
|---|-------|------|-----|-----|
| 1 | 1 hour | Cart Save | "You left something behind." Show the specific product(s). Keep it short. | "Complete Your Order" |
| 2 | 24 hours | Product Education | Explain *why* this product was recommended for them. Specific to the product they carted. | "Get Your [Product]" |
| 3 | 3 days | Social Proof | One testimonial specific to the product category they abandoned. | "See Why [X] Customers Love This" |
| 4 | 5 days | Skin Stats | Reference their profile. "Your skin has [X] — this is why we recommended [product]." | "Built for Your Skin" |
| 5 | 7 days | Promo | Offer an incentive if available. "Complete your order and save [X]." | "Save [X]% Today" |
| 6 | 10 days | Gift / Last Chance | Final touch. Free gift with order or last-chance framing. | "Last Chance — Your Cart Expires" |

**Product-specific branching (preserve this — it's working):**
The current flow branches by product type after Email 1. This is correct. SPF abandoners get SPF-specific education. Serum abandoners get serum science. Keep this structure.

**SMS integration:** Cart abandon SMS at 30 minutes has the highest RPR in the entire account ($12.06 RPR on small sample). Prioritize SMS for cart abandon over email when the customer has an SMS opt-in.

**Branch logic:**
- After Email 1: If purchased → exit. If clicked but didn't purchase → fast-track to Email 5 (promo).
- After Email 3: If hasn't opened any email → skip to Email 6 (last chance, then exit).
- **Exit:** Purchased, or received Email 6, or 14 days elapsed.

**A/B test insight:** The current flow has `promo_a` vs. `promo_b` variants. `promo_b` (3.4% CTR) slightly outperforms `promo_a` (0% CTR). Review and kill the underperformer.

---

## Flow 4: One-Time Buyer → Subscription

**Trigger:** Placed Order metric, filtered to non-subscribers (flow `TLL5FW`).
**Current state:** Live. 6 emails.
**Current performance:** Email 1 (results): 3.9% CTR, $1.39 RPR. Email 3 (running low): 5.4% CTR, $0.99 RPR. Email 4 (promo): 0.4% CTR but 7.1% conversion rate, $9.31 RPR — likely a well-timed promo hitting when product runs out.

### Sequence Design

| # | Delay | Name | Emotional State | Job |
|---|-------|------|----------------|-----|
| 1 | Day 14 | Early Results | Trying the product | "How are your first two weeks?" Share what to expect next. Plant the subscription seed gently. |
| 2 | Day 30 | The System Advantage | Seeing results, considering reorder | "Products designed together work differently." Explain calibration across the system. |
| 3 | Day 40 | Running Low | Product running out | "Time to restock? Subscribe and never run out." Practical. Subscription savings front and center. |
| 4 | Day 50 | Promo | May have already reordered or lapsed | Offer a subscription incentive. This is the highest-converting email in the flow ($9.31 RPR) — timing is everything. |
| 5 | Day 65 | Social Proof | Needs convincing | "Here's what subscribers experience over 3 months" — long-term results stories. |
| 6 | Day 80 | Survey / Soft Close | Make or break | "How was your experience?" Whether they subscribe or not, capture feedback. |

**Branch logic:**
- After any email: If subscribed → exit immediately.
- After Email 3: If clicked but didn't subscribe → fast-track to Email 4 (promo).
- **Exit:** Subscribed, completed all 6, or 90 days elapsed.

**Key insight:** Email 4 (promo) has a 7.1% conversion rate despite only 0.4% CTR. This suggests people are clicking through from *other* channels (SMS, direct site visit) after seeing the email subject line — the email may be acting as a reminder trigger rather than a direct conversion path. Preserve its timing.

---

## Flow 5: Churned Win-Back

**Trigger:** Subscription cancelled metric (flow `RBbEV5`).
**Current state:** Live. 7 stages of messaging, branched by churn reason (price, product, usage, other, catchall).
**Current performance:** Early emails (1-2): 1.5-1.9% CTR. Best: `winback_product` at $2.07 RPR. Most later emails: <0.5% CTR, $0 RPR. The `catchall` branch (no known reason) performs worst.

### Sequence Design

| # | Delay | Name | Job | Churn Reason Branch |
|---|-------|------|-----|-------------------|
| 1 | Day 3 | Acknowledgment | "We see you cancelled." No guilt. Acknowledge. Ask why if we don't know. | All |
| 2 | Day 10 | The Update | "Here's what changed since you left." New products, formula improvements, seasonal relevance. | All |
| 3 | Day 21 | Reformulation Hook | "Your next formula would be different from your last." PROVEN's strongest win-back message — the system learned from their experience. | Product / Catchall |
| 3a | Day 21 | Price Variant | "We have new options." Introduce smaller bundles, one-time purchase, or promotional pricing. | Price |
| 3b | Day 21 | Usage Variant | "Simpler than you think." 2-minute routine, morning/night guide. Reduce friction. | Usage |
| 4 | Day 35 | Social Proof | "Customers who came back saw [specific result]." Win-back testimonial. | All |
| 5 | Day 50 | Final Offer | One incentive. Direct. "Come back and save [X]%." | All |
| 6 | Day 70 | Soft Close | "We're here whenever your skin needs us." Warm, zero pressure. | All |
| 7 | Day 90 | Sunset | "We'll stop emailing you about this. If you ever want to restart, [link]." Clean exit. | All |

**Critical rule:** The current flow sends 7 rounds of messages across ALL branches — that's potentially 20+ emails to a churned customer. This is too many. **Cap at 7 total emails per person regardless of branch path.** Respect the decision to leave. The goal is to offer a door back, not to beg.

**Branch logic:**
- If churn reason is known (from Skio data or survey): route to reason-specific variant at Email 3.
- If churn reason is unknown: use catchall path (reformulation hook).
- After Email 4: If hasn't opened any email → skip to Email 7 (sunset). Stop wasting sends.
- **Exit:** Resubscribed, completed Email 7, or 90 days elapsed.

**Optimization note:** The current flow's `catchall` branch (no known churn reason) has the worst performance — 0% CTR on several messages. These customers are the hardest to win back because you don't know what went wrong. Consider adding a one-question survey email as Email 1 for catchall: "One question: what made you leave? [Product didn't work] [Too expensive] [Didn't use it enough] [Other]." Use the answer to route them to the right branch.

---

## Flow 6: Charge Upcoming (Preserve and Protect)

**Trigger:** Billing reminder metric (flow `RigLxv`).
**Current state:** Live. Highest-volume flow.
**Current performance:** 23-25% CTR, $1.59-$1.72 RPR across 35,000+ recipients.

This flow is PROVEN's operational backbone. It drives massive click volume (8,000+ unique clicks per 90 days) and significant revenue. **Do not redesign this flow.** Optimize incrementally:

- Ensure the email clearly shows what's being charged and when.
- Include a "Manage your subscription" link (the high CTR suggests people are clicking to manage, not just to browse).
- Consider adding a cross-sell element below the billing info: "Add [recommended product] to your next order?"
- Test adding a reformulation nudge: "Your skin profile was last updated [date]. Update it before your next order?"

---

## Draft Flows to Activate (Priority Order)

**1. Card Expiration Notification** (flow `RYvjpm`, draft)
- Prevents involuntary churn from expired payment methods.
- Simple: "Your card ending in [XXXX] expires soon. Update it to keep your routine coming."
- One email, sent 14 days before expiration. Follow up at 7 days if not updated.

**2. Failed Billing Attempt** (flow `X74sRk`, draft)
- Recovers failed payments before they become cancellations.
- Email 1 (immediate): "We couldn't process your payment. Update your card to keep your next shipment on track."
- Email 2 (3 days): "Your payment still needs attention."
- Email 3 (7 days): "Last chance before we pause your subscription."
- These are high-urgency, low-design emails. Clear, functional, direct.

---

## What This Skill Refuses

**Content:**
- Emails with more than one primary CTA
- Prospect emails longer than 150 words of body copy
- Subject lines with exclamation marks
- "We miss you" in win-back messaging
- Fear-based language anywhere (subject, body, CTA)
- Generic copy any skincare competitor could send
- Educational emails that are ads wearing a lab coat
- Product launches that lead with the product instead of the problem
- Testimonials without specifics (skin type, timeline, concern)

**Structure:**
- Sending to "all subscribers" without segment-specific messaging
- Sending without exclusions applied
- Flows without defined exit conditions
- Flows that send more than 7 emails to churned customers
- More than 3 images per email
- CTA below the fold on prospect mobile emails
- Promo or cross-sell in the first 28 days of a welcome flow

**Technical:**
- Relying on images to communicate (email must work with images off)
- Using base teal (#7295A2) on linen backgrounds
- Skipping dark mode testing for navy sections
- Body text that fails WCAG AA contrast (4.5:1 for small, 3:1 for large)

---

## Companion Skills

| Skill | Use For |
|-------|---------|
| `proven-voice` | All copy: subject lines, body text, CTAs, preview text |
| `proven-fe-designer` | Visual decisions: layout, color, typography, imagery |
| Knowledge Base | Facts: data points, science, products, psychology, positioning |

This skill provides email strategy and structure. The others provide voice and visual materials. Use all three together.

---

*The goal is not a good email. The goal is an inbox where every PROVEN message feels like it was written for one person — because the system behind it actually knows them. That's the same promise as the skincare. The email should deliver on it too.*
