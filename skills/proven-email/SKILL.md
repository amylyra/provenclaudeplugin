---
name: proven-email
description: "PROVEN Skincare's email strategy skill. First-principles framework for email across Klaviyo — campaigns, flows, and lifecycle. Teaches how to think about email as a channel: customer psychology, journey stages, what earns attention in an inbox, and how to structure sends that serve the goal. Pair with proven-voice for copy, proven-ui for design system, and proven-creative for imagery."
---

# PROVEN Email — Strategy Skill

Every PROVEN email answers one question: **does this make the reader feel like the system already knows them?**

Not impressed. Not intrigued. Known. The same promise as the skincare — intelligence in service of one person — expressed through the inbox.

This skill teaches how to think about email. It does not document specific flows, segment sizes, or performance benchmarks — those change. The thinking doesn't.

---

## Reference Files

| File | Answers | Read when |
|---|---|---|
| **`references/email-build.md`** | *How do I build the email HTML?* | When assembling the Klaviyo template. Email-adapted type, spacing, color, CTA, constraints. |
| **`proven-ui/SKILL.md`** | *What's the design philosophy?* | Before any design decision. Email inherits the full PROVEN design philosophy. |
| **`proven-ui/references/tokens.md`** | *What's the exact hex value?* | When you need canonical color, spacing, or button values. |
| **`proven-voice/SKILL.md`** | *How should the copy sound?* | Before writing any copy. |
| **`proven-creative/SKILL.md`** | *How do I direct the photography?* | When the email needs imagery. |
| **`products/README.md`** | *Which product reference image?* | When generating product images via Gemini. |

---

# FIRST PRINCIPLES

## The Psychology of a PROVEN Inbox

A person's inbox is the most psychologically defended space on the internet. Every email competes against 120+ daily messages for a fraction of a second of attention. PROVEN earns that attention the same way it earns trust with skincare: by proving it knows you better than the alternative.

### Three things an email can do

Every PROVEN email must do exactly one of these. If it doesn't do any, don't send it. If it tries to do two, split it.

**Teach.** Give the reader something they didn't know about their skin, their ingredients, or how skincare works. The insight must be specific enough that they couldn't have found it by skimming a competitor's blog. Teaching earns the right to send the next email.

**Recognize.** Show the reader evidence that the system sees them — their skin type, their season, their concern, their history. Recognition is the emotional core of PROVEN's value proposition. It's also the hardest email to write, because it requires real personalization, not performed personalization.

**Solve.** Present a specific solution to a problem the reader is experiencing right now. The solution might be a product, a reformulation, a routine adjustment, or a piece of knowledge. The key word is "right now" — timing is the difference between solving and selling.

### The trust arc

Every person moves through a trust arc with PROVEN. Their position on the arc determines what earns attention and what feels invasive.

**Curiosity** → The person knows nothing about PROVEN. They're evaluating whether the concept is credible. Email's job: educate. Sell the idea that skincare can be solved by intelligence — not the product. Keep it short. One idea per email. Drive to the quiz.

**Skeptical trust** → They took the quiz or made a first purchase. They want to believe but haven't experienced proof yet. Email's job: set expectations, normalize the calibration period, show other people's specific results. Don't sell anything new. Don't cross-sell. Build the foundation.

**Delegation** → They trust the system. They've subscribed. They're letting PROVEN handle their skincare. Email's job: reinforce the choice, educate on what the system is doing for them, introduce complementary products when the timing is right. The tone is warm and low-pressure — they already chose you.

**Broken trust** → They cancelled or lapsed. Something went wrong — the product, the price, the routine, or life. Email's job: acknowledge without guilt. Show what changed (reformulation, new options, seasonal relevance). Offer a door back without begging. Respect the decision to leave. Cap the outreach and sunset gracefully.

---

## Four Laws

These govern every send. No exceptions.

**1. One email, one job.** State the purpose in one sentence. If you can't, split it.

**2. The reader's skin is the subject.** Open with what matters to them — their skin, their season, their concern. Never open with the brand, the sale, or the product.

**3. Evidence before ask.** The CTA earns its click through the content above it. Establish why before asking for action.

**4. Earn every send.** Every email must teach, recognize, or solve. If it doesn't do one of these three things, it doesn't belong in the inbox.

---

# AUDIENCE THINKING

## How to Segment

Don't think in list names. Think in psychological states.

The right segmentation question is never "which Klaviyo list do I send to?" It's "what is this person's relationship with trust right now, and what would earn them moving one step forward?"

### Segmentation by trust position

| Trust Position | Psychological State | What Earns Attention | What Feels Invasive |
|---|---|---|---|
| **Curious** (prospects) | Evaluating the concept | Surprising skin facts, social proof with specifics, quiz-driven curiosity | Product pushes, discount stacking, anything that assumes familiarity |
| **Skeptical** (new buyers, one-time purchasers) | Wanting to believe | Results timelines, calibration education, "here's what to expect" | Cross-sells, upsells, anything that asks for more money before they've seen value |
| **Delegating** (active subscribers) | Trusting the system | Seasonal updates, reformulation awareness, complementary products at the right moment | Over-communication, urgency on things that aren't urgent, treating them like prospects |
| **Broken** (churned) | Post-trust | Acknowledgment without guilt, evidence that things changed, a door back | "We miss you," guilt, excessive re-engagement sequences, ignoring the reason they left |

### Segmentation by engagement

Layer engagement recency on top of trust position. A delegating subscriber who hasn't opened in 90 days needs a different approach than one who opened yesterday — even though their trust position is the same. Engagement windows (30/70/90/120 days) determine send frequency and content density, not the message itself.

### Exclusion thinking

Before every send, ask: **who should NOT receive this?** Exclusion is as strategic as targeting. Always exclude people who would experience the email as noise — internal accounts, recently bounced, unsubscribed, people currently in a flow that conflicts with this campaign.

---

# EMAIL ANATOMY

## Structure by Trust Position

### For the curious (prospects)

Prospects don't know PROVEN. They need less content, more conviction, and one clear path to one action.

- Maximum 150 words of body copy.
- CTA above the fold on mobile. No scrolling to find it.
- One CTA only. Drives to quiz or results page. Never to a product page, blog, or homepage. (Subscriber emails allow one CTA per section — see What Performs below.)
- No product images unless the email is specifically about a new product launch.
- The subject line does 60% of the work.

### For the delegating (subscribers)

Subscribers know PROVEN. They can handle more depth, more specificity, and more personalization.

- 250-400 words.
- Product imagery allowed (cap at 1 per email).
- Secondary CTA allowed (text link only, after additional context).
- Personalization tokens that reference their actual data — not just their name.

### For all emails

- One focal point per hero block: image, headline, OR data point. Never all three.
- One CTA per section in a modular layout. Prospect emails still get one CTA total. Ember pill button, action-specific ownership language ("GET MY FORMULA," not "Shop Now"). Never "Learn More," "Click Here," or "Shop Now."
- Evidence before ask. Every feature bridges to a feeling.
- Subject line: 40-60 characters, reader-relevant word front-loaded, no exclamation marks.
- Preview text: extends the subject, never repeats it.
- Maximum 3 images per email.
- Email must communicate with images off.

---

## What Performs (Team Learnings)

These are hard-won insights from PROVEN's email performance data. They override theoretical best practices when they conflict.

### Every email should have

**Product front and center (subscriber and cart emails).** Clear product imagery is the anchor. The reader should see *what this is about* before reading a word. Product photography outperforms lifestyle or model imagery in email context. Exception: prospect emails still avoid product imagery — prospects haven't taken the quiz and don't have a product relationship yet.

**Pricing and value visible.** Crossed-out original price, per-month pricing breakdown, or clear savings messaging. The reader shouldn't have to click through to understand the value proposition. Show the math in the email itself.

**One strong CTA per section.** Not one CTA per email — one per *section*. Each modular block gets its own CTA if it has a distinct point. CTA language should be specific and ownership-driven: "GET MY FORMULA" outperforms generic CTAs like "Shop Now" or "Learn More." The reader should feel the CTA was written for them.

**Seasonal or timely hook.** Connect to the moment. A reason *why now* — the season, a skin shift, a reformulation, a limited window. Timely relevance drives opens and clicks. An email that could be sent any week of the year is weaker than one anchored to this week.

**Short, scannable copy.** Bite-sized content beats paragraphs. Short emails consistently outperform longer ones across all segments. If a section needs more than 2-3 sentences, split it into two sections with visual separation. The reader scans — design for the scan.

**Simple, modular layout.** Each section has one focal point and one job. The email is a stack of self-contained modules, not a flowing document. A reader who only sees one section should still get value from it.

**Social proof when included: problem → solution.** Don't lead with "I love PROVEN." Lead with the problem ("My redness wouldn't go away with anything"), then the solution ("3 weeks with my personalized formula and it cleared"). Problem → solution is more persuasive than praise.

### Performance notes

**Don't force CTAs at the top.** CTA above the fold is a rule for prospects (who need a short path to the quiz). For subscribers, the CTA can earn its position by following content that justifies the click. Forcing a CTA before the reader has context reduces trust.

**Product imagery > model imagery.** Product shots perform best. Use model/people imagery only when it's real and relatable — never stock, never aspirational. If in doubt, lead with product.

**Before/after shots perform well.** Real skin transformation images — showing the same person's skin before and after using PROVEN — are highly engaging. They combine social proof with visual evidence in one frame. When using before/after: always real customers, always specific timelines ("4 weeks"), always the same lighting and angle in both frames so the difference is credible. In the creative pipeline, before/after maps to the **Skin (Activated Terrain)** category in the **SKIN** band — close-up, reading-distance skin with strong directional light. Shoot both frames with the same light setup so the comparison is honest.

**Shorter wins.** When in doubt, cut. A shorter email that nails one idea outperforms a longer email that covers three. This is true across every segment and every campaign type.

**Bright colors outperform dark.** Light backgrounds (white, linen) consistently outperform dark sections in email. Dark sections may look sophisticated but they don't convert as well. Use light surfaces as the default. If you use a dark section, keep it to one per email and not as the hero.

**Link every CTA to a specific page.** Every CTA must link to the most relevant page — the specific product PDP, the quiz, the personalized results page. Never link to the homepage. Never link to a generic collection page. The CTA earns the click; the landing page must deliver on it immediately.

---

## Visual Patterns (From Performance Data)

These patterns come from analyzing PROVEN's highest and lowest performing emails. They are not aesthetic preferences — they are conversion data.

### What converts: the PROVEN email look

**Bright, clean, white-dominant layout.** The best-performing emails are 90%+ white or linen background. Color comes from the product chrome and accent CTAs — not from section backgrounds. The email feels airy and uncluttered.

**Product on white, clearly lit.** Clean product photography on white or near-white backgrounds. The chrome bottles are bright, reflective, and immediately recognizable. The reader should identify the product in under one second. No atmospheric staging, no moody lighting, no environmental context in the image.

**Big, bold headline typography.** The top-performing emails lead with oversized, high-weight headlines: "LESS THAN $50 A MONTH." "20% off EVERYTHING." "Three essentials, One system." The headline is the visual anchor — it should be the largest element on screen, with dramatic contrast against the body text. Albert Sans at weight 800-900.

**Pricing front and center.** The value proposition is visible without reading the body copy: "$50 a month," "$109 ($214 value)," "$51 VALUE," crossed-out pricing. The reader should understand the deal from the headline and hero alone.

**Clean product grid for system/multi-product emails.** When showing the system (Cleanser, SPF, Night Cream), lay them out as a clean side-by-side grid with one-line descriptions. No lifestyle wrapping. The products speak for themselves in a clear, catalog-style presentation.

**Ownership CTAs with arrows.** "GET MY FORMULA →" "CLAIM MY SKIN'S ROUTINE →" "COMPLETE MY FALL ROUTINE →" "MAKE THE SWITCH →" — the pattern is possessive ("MY") + specific action + arrow. This consistently outperforms neutral or generic CTA language.

**Specific seasonal/timely hooks.** "Eczema Awareness Month" outperforms "Winter skincare tips." "October essentials for radiant skin" outperforms "Shop Winter Favorites." The more specific the moment, the better. Generic seasonal language could come from any brand.

**Social proof with numbers and real photos.** "90% of users reported clearer, more balanced skin" with a real customer photo. The stat is specific, the photo is real (not stock), and the pairing creates credibility. Problem → solution framing: show the before-state concern, then the result.

### What doesn't convert: patterns to avoid

**Model-led hero imagery.** Emails that open with a model's face, hands touching skin, or a person smiling underperform product-led emails. Model imagery feels aspirational and generic — it could be any skincare brand. Product imagery is specific to PROVEN and gives the reader something to identify with (their actual products). Use model imagery only below the fold, only when real and relatable, and never as the hero.

**Dark/moody product photography.** Products shot on navy, dark grey, or charcoal surfaces — even if beautifully lit — don't convert in email. The chrome looks sculptural but not inviting. Dark editorial photography works on a website with full-screen display; it fails at 600px on a phone where the reader is scanning quickly. In email, the product should feel bright, approachable, and immediately readable.

**Atmospheric/art-directed product shots.** Products floating in water ripples, balanced on marble pedestals, arranged in dramatic compositions. These are beautiful photographs that win awards and lose clicks. The artistry adds distance between the reader and the product. In email, the product should feel close, simple, and available — not curated.

**Too much copy before the CTA.** Emails with 3-4 paragraphs before the first CTA consistently underperform. If the reader has to scroll through dense text to find the action, most won't. The performing emails have a headline, 1-2 sentences of bridge copy, and a CTA — all visible in the first screen.

**Generic seasonal language.** "Winter Takes A Toll On Your Skin." "Shop Winter Favorites." "Your Winter Routine, Made Simple." These could appear in any skincare brand's email. Compare with what works: "Flare-Ups Aren't Seasonal — They're a Sign." "31 million Americans experience eczema." Specificity and insight beat generic seasonal framing.

**Holiday gimmick copy.** "Savings too good to ghost." "Summon Your Best Skin Yet." "Eerie-sistible." Playful holiday themes are off-brand for PROVEN. The voice is confident and precise, not cute. Seasonal relevance is powerful — seasonal gimmickry is not.

### Image generation rules (for Gemini prompts)

Based on the performance data above, when generating images for email through proven-creative → Gemini:

**Always:** White or near-white backgrounds. Bright, even lighting. Product chrome looks luminous and silver, not dark or moody. Product is immediately identifiable — label readable, form factor clear.

**Never:** Dark backgrounds (navy, charcoal, deep grey). Dramatic shadow. Products on dark surfaces. Water/liquid environments. Floating or gravity-defying compositions. Atmospheric fog or mist.

**For product hero shots:** CHROME band, pure white background, product centered and well-lit. This is the highest-performing image type in email. Keep it simple.

**For system/multi-product shots:** Same as above but with all products arranged in a clean line or grid. No overlapping, no artistic stacking. Catalog clarity.

---

## Subject Line Thinking

The subject line determines whether the other 150-400 words are ever read.

### Five patterns

**Skin-first.** Lead with the reader's skin, not the brand. *"Your winter skin needs different ingredients."*

**Surprising fact.** A specific, counterintuitive insight. *"10% niacinamide is worse than 5%."* Creates a knowledge gap the reader needs to close.

**Quiet confidence.** Short, declarative. *"Your formula updated."* Signals recognition without asking for anything.

**Recognition.** Personalization that proves attention. *"{{ first_name }}, your skin profile just got smarter."* Only works if the content inside is genuinely personalized.

**Direct offer.** Clean, honest. *"25% off your personalized system."* Effective for subscribers, weaker for prospects.

### Refuse

Clickbait, fear, vague teasers, exclamation marks, rhetorical questions.

---

# CAMPAIGN THINKING

## How to Design a Campaign

A campaign is an editorial send — you choose the moment, the audience, and the message. Unlike flows, campaigns require you to answer: **why now?**

### The design process

**1. Goal.** One sentence. If it's two sentences, it's two campaigns.

**2. Audience.** Trust position first, Klaviyo segment second. The same topic (seasonal change, product launch) hits different trust positions differently.

**3. Why now.** What makes this moment relevant? A season, a launch, a cultural moment, a data insight. "We haven't sent anything in a while" is not a reason.

**4. The one thing.** If the reader remembers one thing, what is it? Write that down. Everything else supports it.

**5. Success metric.** Define before building. Click-through for prospects. Conversion + RPR for subscribers. Open rate for relational sends.

### Campaign purposes

**Environmental/seasonal.** The system adapts when the environment changes. Lead with a specific trigger ("Indoor heating drops humidity below 30%"), not a generic greeting ("Winter is here!").

**Educational.** One concept. A counterintuitive insight earns more clicks than a product pitch. Themes: biochemical individuality, the subtraction principle, environmental intelligence, the inflammation equation.

**Sales events.** Subscriber emails drive the revenue (10-20x higher RPR than prospect sends). Sequence: announce → prove → educate → urgency → last chance. Invest creative energy in subscriber versions.

**Social proof.** One specific result leads. Skin type, timeline, concern addressed. Not "I love this product" but "3 weeks in, my hormonal acne stopped cycling."

**Brand/relational.** Emotional connection without selling. Maximum 1 per month. Goodwill converts — but only if it's rare.

---

# FLOW THINKING

## How to Design a Flow

A flow responds to something the customer *did*. The behavior tells you their psychological state. The flow meets them there and walks them forward.

### Principles

**1. A flow is a conversation, not a drip.** Each email responds to the likely psychological state at that moment in the sequence. The tone evolves.

**2. Timing is content.** A 1-hour follow-up says "we noticed." A 7-day final email says "no pressure." The delay communicates as much as the words.

**3. Branch on behavior, not demographics.** Did they open? Click? Visit the site? Behavioral signals determine what comes next.

**4. Every flow has an exit.** Converted, hit the final email, or suppressed. Flows without exits send irrelevant emails.

**5. Map the emotional arc first.**

```
EMPATHY → EDUCATION → EVIDENCE → OFFER → SOFT CLOSE
(I see you)  (Here's why)  (It works)  (Here's how)  (Whenever you're ready)
```

Not every flow uses all five stages. Adapt — but always move forward, never circular.

### Flow design by trigger

**Post-quiz-abandon.** Curious but unconvinced. Lever: curiosity, not urgency. Empathy → surprise insight → social proof → educate → soft close. SMS outperforms email here — prioritize if opted in.

**Post-purchase (welcome).** The most important flow. Skeptical trust. Set expectations. Normalize calibration. Check in. Celebrate results. No cross-sell before Day 28. Their purchase is not permission to sell more.

**Cart abandon.** Highest-RPR flow. Cart save → product education → social proof → skin data connection → incentive → last chance. Branch by product type.

**One-time buyer → subscriber.** Show the system advantage. Products designed together. Calibration over time. The highest-converting moment is often a well-timed incentive when product runs out (~Day 40-50). Timing matters more than copy.

**Churned win-back.** Lead with acknowledgment, never guilt. "Your skin changed. So did we." Branch by churn reason if known. Cap at 7 emails. If they haven't opened after 4, skip to sunset. Clean exit always.

**Billing/operational.** Service, not marketing. Clear, functional, direct. Don't try to be clever. Protect these flows by keeping them trustworthy.

---

# THE CRAFT

What separates a correct email from a great one. The sections above teach process. This section teaches taste.

## What Makes a PROVEN Email Great

A great PROVEN email does something no competitor can: it proves the system is paying attention. Not in a creepy way. In the way a good doctor reviews your chart before walking in — you feel the preparation, the specificity, the absence of guessing.

### The data layer

PROVEN has something no other skincare brand has in the inbox: 47 factors per customer. Most brands personalize with a first name and a purchase history. PROVEN can personalize with skin type, primary concern, local humidity, water hardness, seasonal shifts, and formula composition. Every email that uses this data well is unbeatable — because no one else can write it.

The craft is knowing when the data layer adds recognition and when it adds surveillance. A subject line that says "Your hydration score dropped this month" is recognition. A subject line that says "We noticed you haven't opened our last 3 emails" is surveillance. The difference: does the data serve the reader's skin, or does it serve the brand's metrics?

**Use the data layer when:** It connects to a skin outcome the reader cares about. "Your formula adjusted for spring humidity" — they feel the system working.

**Don't use the data layer when:** It reveals behavioral tracking. "Since you clicked on our SPF email last week..." — they feel watched.

### The surprise test

Read the email. Is there a single moment where the reader thinks "I didn't know that" or "that's exactly right"? If not, the email is functional but forgettable. The surprise can be a skin insight, a data point, a reframe of something they assumed, or a recognition moment so specific it feels impossible.

Great PROVEN emails have at least one surprise. The surprise earns the CTA.

### The forwarding test

Would the reader send this to a friend? Not because of a referral incentive — because the content is genuinely useful or interesting. Educational emails pass this test when they teach something specific. Recognition emails pass this test when they make the reader feel seen in a way they want to share. Sales emails almost never pass this test, which is fine — but the majority of sends should.

### The silence test

What if you didn't send this email? Would anyone notice? Would anyone's experience with PROVEN be worse? If the answer is no, the email shouldn't exist. This is the hardest test and the most important one. It's the mechanism behind Law 4 (earn every send). Every email you don't send makes the ones you do send more valuable.

## Series Craft

When a campaign or flow has multiple emails, each one must feel like a new chapter — not a rephrased reminder. The reader should feel the sequence progressing, not repeating.

### The chapter rule

Read the subject lines in order. Do they tell a story? Or do they sound like the same email sent five times?

Bad series (same idea, reworded):
1. "Your cart is waiting"
2. "Don't forget your cart"
3. "Still thinking about it?"
4. "Last chance to grab your cart"

Good series (each adds something new):
1. "You left something behind" (empathy — I see you)
2. "Why we recommended this for your skin" (education — here's the reasoning)
3. "3 weeks in, her redness was gone" (evidence — here's what happened for someone like you)
4. "Your skin profile says you'd benefit from this" (recognition — the data agrees)
5. "Whenever you're ready" (soft close — no pressure)

The difference: each email earns its existence by contributing a new angle. If you can't articulate what new thing email #3 adds that emails #1-2 didn't, delete email #3.

### Emotional tempo

A series is not a straight line from soft to hard. It breathes. The pattern:

```
Soft → Medium → Soft → Strong → Soft
```

After a direct email (evidence, offer), the next should ease off. After a warm email (empathy, brand), the next can push harder. The reader should never receive two high-pressure emails in a row. Two soft emails in a row is fine — it builds trust. Two hard emails in a row destroys it.

### Timing as storytelling

Delays tell the reader how much you respect their time.

| Delay | What it says |
|---|---|
| 1 hour | "We noticed right away." Appropriate for cart abandon, quiz abandon. |
| 24 hours | "Giving you a day." Standard follow-up rhythm. |
| 3-7 days | "Taking our time." Education, social proof, non-urgent sequences. |
| 14+ days | "No pressure." Soft close, final touches, sunset. |

Accelerating delays (1hr → 24hr → 3d → 1d → 6hr) communicates escalating urgency. Decelerating delays (1hr → 3d → 7d → 14d) communicates declining pressure. Match the pattern to the emotional arc.

## A/B Thinking

Test one variable at a time. Know what you're learning before you test.

### What to test by trust position

**Curious (prospects):** The problem is click-through. Test the thing that determines the click: body length (100 vs. 200 words), CTA position (above fold vs. below), CTA copy (action vs. benefit), content approach (stat-led vs. testimonial vs. myth-bust).

**Delegating (subscribers):** The problem is conversion and cross-sell. Test the thing that determines the purchase: offer structure (percentage vs. dollar vs. gift), content depth (short feature vs. ingredient deep-dive), CTA framing ("Add to routine" vs. "Shop your formula").

**Broken (churned):** The problem is re-engagement. Test the thing that gets the door open: subject line approach (reformulation vs. seasonal vs. offer), email length (short and direct vs. evidence-heavy), timing (7 days post-churn vs. 21 days).

### How to read results

Track the metric that matches the goal. Click-through for awareness. Conversion + RPR for revenue. Open rate for relational. Don't optimize prospect emails for RPR — they don't have the trust position to convert directly. Don't optimize subscriber emails for open rate — they already open, the question is whether they act.

## PROVEN's Unfair Advantage in Email

No other skincare brand can do these things in the inbox. These are PROVEN's moats. Use them relentlessly.

**Reformulation as a message.** "Your next formula would be different from your last." No competitor can say this because no competitor changes the formula based on the customer's evolving skin. This is the single strongest win-back message and one of the strongest retention messages.

**Environmental intelligence.** "Indoor heating dropped humidity below 30% in your area. Your formula already adjusted." This connects the brand to the reader's physical world in a way that feels like magic. Use it for seasonal campaigns and as evidence in educational emails.

**The 47-factor recognition moment.** "We analyze 47 factors — from your genetics to your water hardness to how your skin responds to stress." The specificity of 47 is more credible than "hundreds of data points." Use the number. Let it land.

**Calibration as a feature.** When a new customer worries their product isn't working in Week 1, PROVEN can say "that's expected — here's the calibration timeline." The competitor says "try it for 30 days." PROVEN can explain *why* the timeline exists, backed by data. This turns anxiety into confidence.

**Personalization that's verifiable.** "Your formula contains 5% niacinamide because your skin profile indicated..." The reader can check this against their actual product. Most "personalized" brands wave their hands. PROVEN can be specific because the personalization is real. Every email that proves this earns trust.

---

# QUALITY STANDARDS

## Checklist

- [ ] Purpose in one sentence
- [ ] Audience by trust position + engagement window
- [ ] Exclusions applied
- [ ] Subject: 40-60 chars, reader-first, no exclamation marks
- [ ] Preview: extends subject, doesn't repeat it
- [ ] CTAs: one per section (subscribers), one total (prospects), ownership language
- [ ] Prospect ≤150 words, CTA above fold
- [ ] Subscriber ≤400 words
- [ ] Copy per proven-voice
- [ ] HTML per references/email-build.md
- [ ] Images have alt text; works with images off
- [ ] Mobile responsive
- [ ] Smart sending enabled

## Refuses

**Content:** Multiple CTAs in prospect emails. Prospect emails over 150 words. Exclamation marks in subject. "We miss you." Fear-based language. Generic CTA language ("Learn More," "Shop Now"). Ads disguised as education. Product-first launches. Testimonials without specifics. Dark hero sections. Stock or aspirational model imagery.

**Structure:** Sending to "everyone." No exclusions. Flows without exits. 7+ emails to churned customers. Cross-sell before Day 28 in welcome. CTA below fold on prospect mobile.

**Technical:** Image-dependent messaging. Teal on linen. Failing WCAG AA contrast.

## Image Direction for Email

The email skill decides *whether* an image is needed and *what role it plays*. The creative skill (`proven-creative`) decides *how to shoot it*. This bridge maps email contexts to the six photography categories so the agent knows which pipeline to invoke.

### When email needs imagery

Not every email needs an image. The silence test applies to images too — if removing the image doesn't weaken the email, the image shouldn't be there. When it earns its place, the image has one of these jobs:

**Hero image** — sets the emotional tone for the entire email. One per email maximum. This is the focal point of the hero block.

**Product image** — shows the specific product being discussed. Only in subscriber and cart abandon emails (see Product Image Rules below).

**Evidence image** — a texture close-up, ingredient, or skin detail that supports an educational claim. Rare in email. Powerful when used.

### Mapping email context → creative category

Performance data is clear: **clean product photography on white backgrounds converts best in email.** Default to CHROME band unless the email context specifically requires something else.

| Email Context | Creative Category | Band | Notes |
|---|---|---|---|
| **Any product-featuring email** (default) | Product Catalog | CHROME | White background, bright lighting, chrome luminous. This is the highest-performing image type in email. Default here unless you have a specific reason not to. |
| **System / multi-product** | Product Catalog | CHROME | Clean side-by-side grid. No overlapping, no artistic stacking. Catalog clarity. |
| **Seasonal/environmental campaign** | Product Catalog | CHROME | **Not** Product Lifestyle. Performance data shows atmospheric product shots underperform clean product-on-white in email. The seasonal story lives in the copy and the HTML theming, not in the product photography. |
| **Educational campaign** | Ingredients | RITUAL | Botanical specimens, raw ingredients on a clean solid backdrop. The ingredient is the subject. |
| **Social proof / testimonial** | Skin (Activated Terrain) | SKIN | Close-up real skin. The person's result is the subject. Real photos of real customers outperform stock. |
| **Welcome / post-purchase** | Product Catalog | CHROME | Their product, clean, well-lit. |
| **Cart abandon** | Product Catalog | CHROME | The specific product they carted. Direct and recognizable. |
| **Win-back / reformulation** | Product Catalog | CHROME | Show the product looking fresh and new. The "what changed" story lives in the copy. |
| **Brand / relational** | Avoid model hero imagery | — | Performance data: model-led heroes underperform. If imagery is needed, use product or skip the hero and lead with typography. |
| **Sales event** | Product Catalog | CHROME | Clean product hero with price overlay or adjacent pricing. The offer is the visual event, not atmospheric photography. |

**When NOT to use CHROME/product-on-white:** Only when the email's entire purpose is about skin results (testimonial, before/after) or ingredient education. In those cases, the subject isn't the product — it's the skin or the ingredient.

### Email-specific creative override: clean backgrounds

In email, the HTML template *is* the environment. The themed background (white, linen, accent color) provides context. Images must sit cleanly inside that environment.

**The rule is simple: white or near-white backgrounds for all email product photography.** No exceptions for "artistic" shots, no dark moody alternatives, no atmospheric staging. The performance data is unambiguous.

**How this overrides proven-creative's defaults:**

| Creative Category | Web default | Email override |
|---|---|---|
| **Product Catalog** (CHROME) | Pure white background | **No change.** This is already the email standard. |
| **Product Lifestyle** (RITUAL) | Product on a surface — counter, vanity, nightstand | **Don't use RITUAL for email hero images.** Use CHROME instead. If you must show product-in-context, simplify to a single material swatch with everything else blurred to near-solid. |
| **Ingredients** (RITUAL) | Botanical on a warm surface | **Solid or gradient backdrop.** Ingredient isolated on a clean field. |
| **Skin / Activated Terrain** (SKIN) | Close-up skin, dramatic light | **No change.** Skin close-ups are frameless and sit cleanly in any HTML context. |
| **People Lifestyle** (SKIN) | Person in environment | **Avoid as hero imagery.** Model-led heroes underperform. If used below the fold, tight crop, soft background, real person only. |

**When generating prompts for email images, add this to the prompt:**

Front-load: `"Pure white background, bright even lighting, product chrome is luminous silver, immediately identifiable"`

For ingredient shots: `"Clean solid background, warm-neutral (#FAF6F2 range), ingredient isolated"`
- For navy sections: `"Dark solid background (#162743 range), product lit dramatically against dark field"`

This tells Gemini to produce images that composite cleanly into the email template instead of fighting it.

### What the agent should do

1. Determine the email context from the brief.
2. Look up the matching creative category and band in the table above.
3. Read the corresponding reference file in `proven-creative/references/`.
4. Run the full pipeline: band → binding rules → planner slots → validator.
5. For product-containing categories, load the reference image from `products/`.
6. Fire to Gemini with the reference image attached.

If the email doesn't fit neatly into one context above, ask: **what is the image's job?** If it's "show the product" → Catalog/CHROME. If it's "show the product in a life" → Lifestyle/RITUAL. If it's "show the person" → Skin or People/SKIN. The band follows the subject.

## Product Image Rules

- **Curious (prospects): NO product images** unless a new launch.
- **Delegating (subscribers): 1 product image max.** Use `products/` for Gemini reference.
- **Cart abandon: YES.** Show what they carted.
- **Maximum 3 images per email** total.

---

*The goal is not a good email. The goal is an inbox where every PROVEN message feels like it was written for one person — because the system behind it actually knows them. That's the same promise as the skincare. The email should deliver on it too.*
