# Can AI be an effective tool for quizzing SWE Levels (junior/mid/senior)?

This is not really going to include code as I think coding is overrated when it comes to assessing junior/mid/senior level skill. There's also tons of resources out there that devs can use to improve their coding ability. I feel like AI doesn't really need to assist there. So where can we fit in AI? Over the years, I've noticed that the most helpful devs aren't necessarily the ones who can code the fastest, it's the ones who can help build the best understood picture that explains what we need to do. It's the dev who can point out common security issues but also knows when it's appropriate to bring in AppSec. The dev who doesn't agree with a design and leverages UX common practices as evidence. They don't just see coding problems, they see team, organizational, and business problems. More importantly they don't solve these problems with code, they solve them with whatever appropriate solution is necessary (asking for clarification, delegating tasks to other teams). The list goes on and on but I've essentially boiled this down to **Contextual Awareness**. 

Typically it's difficult to train this. You gradually build this up on the job by being exposed to hundreds of different problems during your career. It's a slow process and I'd argue you don't even recognize you need to do it until you ask for your first promotion. You feel like you got the coding skills but then the manager has a hard time articulating why that's not enough. But what if AI can make training this a lot easier? It can create scenarios that give you the opportunity to practice contextual awareness. It won't just gauge how many questions your asking, but how effective and relevant they are. At least that's the idea.

Let's take a look at how ChatGPT reasons the junior/mid/senior levels. 

## User Prompt
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Create a sample scenario where a PO suggests a feature and list out how a junior/mid/senior would answer these. Also include the reasoning as to why it's junior/mid/senior
</pre>

### AI Response
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🧪 Scenario: Feature Suggestion from Product Owner

    PO:
    “Let’s add a ‘Save for Later’ button next to each item on the checkout page so users can remove something from their cart but still easily find it later.”

🎓 Junior Developer Response

    Response:
    “Okay, I can add a button that stores the item in localStorage when clicked. Do you want me to also display it somewhere on the page?”

    Why This is Junior-Level:

    Focuses immediately on implementation details (tech solution).

    Assumes the feature is fully vetted; no pushback or clarification.

    Thinks in terms of UI mechanics, not user experience or backend implications.

    No mention of persistence scope (e.g., across devices/sessions).

🛠️ Mid-Level Developer Response

    Response:
    “Interesting idea. Just to clarify: should saved items persist across sessions or just temporarily in the browser? And where do you imagine the user accessing the saved list—on this page or somewhere else in the app? Also, should this trigger any analytics events for tracking user behavior?”

    Why This is Mid-Level:

    Begins to clarify scope and persistence.

    Starts thinking about user interaction flow and data tracking.

    Doesn't assume it’s a greenlight—asks for clarification before implementation.

    Still mostly focused on technical feasibility and user experience, not cross-team or broader product impact.

🧠 Senior Developer Response

    Response:
    “I see the value for users who want to save items for later. A few considerations before we scope this:

        From a user journey perspective, would this overlap with our existing Wishlist functionality? Could that cause confusion?

        Data-wise, should saved items be tied to user accounts, and if so, do we need auth or backend support to persist this?

        From a design perspective, do we have patterns elsewhere in the app we should follow for consistency?

        Any metrics or hypotheses you’re aiming to test with this? That could help us decide if this is worth prioritizing now vs later.”

    Why This is Senior-Level:

    Thinks about product cohesion (does this duplicate Wishlist?)

    Surfaces cross-functional concerns: backend, auth, UX, analytics

    Focuses on product strategy, not just user convenience

    Uses questions to align with business goals—not just implementation clarity

    Doesn’t just ask “what do you want?”—asks “why do we want this now?”
</pre>

The lines between junior/mid/senior get blurry at the boundaries but I think with this response it's enough to say that ChatGPT has a good enough baseline to trust somewhat. Nothing in the response stood out to me as just wrong. The one thing to be aware of though is that just because you're strong in one category doesn't mean your in the next level. Like if you are bringing in cross functional concerns but are still mid at clarifying scope then you're still probably still mid. You need to be strong in a lot of categories to move up. This is a side note but don't get caught up in categorizing these skills either. I've seen people try to improve skills in isolation but it doesn't work out because being "better" requires knowing how to use those skills cohesively. Like don't just study how to point out security issues. Learn how to point out issues because a lot of issues are common across domains it's just the details that shift.

So let's see if ChatGPT can run a simluation on gauging my level based on my questioning. We're creating a PO feature request scenario again.

## AI Question 1
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🎭 You’re the Developer. I’m the PO.

    PO:
    “We’ve been getting feedback that users sometimes hesitate at checkout because they’re not quite ready to buy certain items. I’m thinking we should add a ‘Save for Later’ button right next to the items in the cart so they can hold off without deleting them.

    Could you look into this?”

Your turn. Respond however you'd like—as if you're a dev on the team. You can ask questions, propose an approach, push back, or anything else.

Once you respond, I’ll give structured feedback on whether your reasoning aligns with junior, mid, or senior level thinking—and why.
</pre>

## User Response 1
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Sure. Does any of the analytics data indicate why they're hesitating? I know you said not quite ready but can you shed some light on what that means? I wanna make sure that "Save for later" would actually be used. I'm worried about a situation where we create "save for later" and it adds stuff that just sits there forever or its never used at all. Also how often is this happening?
</pre>

## AI Response 1
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🔥 Great response. Let’s evaluate this step-by-step.
🧠 Your Response:

    “Does any of the analytics data indicate why they're hesitating? … I wanna make sure that ‘Save for later’ would actually be used… I'm worried about a situation where we create 'save for later' and it adds stuff that just sits there forever or is never used at all. Also, how often is this happening?”

🧩 Evaluation: Mid-Level with Senior Tendencies
✅ Strengths:

    Root Cause Thinking
    → You didn’t accept the surface narrative. You asked for underlying evidence of the user problem.
    → That shows you’re thinking beyond build tasks and into why the feature exists.

    Impact-Oriented Skepticism
    → Concern about adding features that go unused shows product ownership mindset, not just engineering.
    → You’re subtly questioning feature bloat and future maintenance debt.

    Metric-Based Framing
    → Asking “how often is this happening?” hints at quantitative prioritization, not just intuition.

🧠 Why Not Quite Senior Yet (but close):

    You didn’t yet connect to broader system overlap or product strategy. A senior might also ask:

        “Do we already have Wishlist functionality that could be extended?”

        “Would this impact logged-in vs guest experiences?”

        “Should we test interest in this with a soft feature before full dev (e.g., via design prototype or AB test)?”

In short, you're one or two questions away from a senior-level diagnostic sweep, which usually covers:

    User problem validation

    Cross-feature overlap

    Technical scope

    Business tradeoffs

🏷️ Final Verdict:

Mid+ level — strong ownership and product instincts, nearly senior. Keep asking “why now?” and “how does this fit with everything else?” and you’re solidly there.
</pre>

For context, I'm a senior dev. But this thing flagged me as mid. So it's trash at gauging. JK... No let's breakdown what happened cause there's a lesson in contextual awareness here. Although ChatGPT understood the premise of what I was doing, we didn't contextually align on how. ChatGPT expected the user to be senior level in one prompt, that means ask every question a senior would at once. I took it as, let's start a dialogue. I'll ask a starting question that's most relevant to me and we'll go from there. This is why you gotta really be careful with AI and not just trust it. Cause nothing it said was wrong, but the mechanism of how it was executed was wrong. ChatGPT should have recognized that humans don't have conversations in one shot and conducted the experiment accordingly. But it didn't. And I should have known that ChatGPT doesn't understand human conversations like I do and improved the initial prompt. But I didn't. That's ok though because now we know. We're now contextually aware that AI is not some super intelligence (yet) and that it's still got a long way to go. That means I can't just turn my brain off when talking to this thing. I gotta check it every now and then. 

Ok so I clarified the ask a bit and continued the assessment. Let's see where I end up now. We're picking up as if it were responding to my first set of questions.

### AI response 1
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Yeah, fair question. From what we’ve seen in session recordings, users often remove an item and then scroll around a bit more, sometimes even re-adding it. We’ve had a few support tickets where people asked if there was a way to save something without buying it now.

We haven’t run a formal study on it or anything, so I don’t have exact usage stats. But it seems like a recurring theme in feedback over the last couple quarters. It’s come up enough that I figured it might be worth exploring.
</pre>

### User response 2
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Makes sense. Can we do a formal study on it? Seems important enough if it's a reoccurring theme. And by we I mean "not the dev team". Feels like this falls more on business requirement gathering at the moment.
</pre>

### AI response 2
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
That’s fair. I think we could do something lightweight—maybe a quick survey or check with UX to run a user test. But that might delay the feature a bit.

Do you think it’s worth holding off implementation entirely until we have that? Or could we do a quick version and iterate later?
</pre>

### User response 3
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Yeah it boils down to demand but I don't have the data to determine that. I can tell you that we can do a quick version and iterate. Depending on how much risk we wanna take we can deploy to all users or we can set something up where only a certain subset of users get the feature. From my perspective, there does seem to be enough demand to go ahead and put something in. It's also a secondary flow, meaning not every one is going to use it so that mitigates some of the risk. My preference though is to wait for a more formal assessment but that's just a personality thing. If business wants us to push forward I wouldn't be opposed. 
</pre>

At this point, ChatGPT terminated the experiement and just gave me an evaluation.

### AI response 3
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🧠 Round-by-Round Evaluation
✅ Round 1: You Asked

    “Can we look at analytics? How often does this happen?”

    Level: Mid+

    Focus: Root cause validation, demand assessment

    Strength: You initiated the "why are we building this?" lens.

✅ Round 2: You Escalated

    “Can we do a formal study? This seems more like a business requirement.”

    Level: Borderline Senior

    Focus: Role clarity + strategic prioritization

    Strength: You clearly drew a line: this isn’t a dev-led initiative yet.

    Tone: Respectful boundary-setting (“not the dev team”)—very senior.

✅ Round 3: You Negotiated

    “We can build it fast, limit rollout, or wait. Personally prefer waiting, but open to moving forward.”

    Level: Senior

    Focus:

        Tradeoff navigation (speed vs validation)

        Risk mitigation strategies (subset rollout)

        Business-aligned flexibility ("if business wants us to push… I’m not opposed")

    Strength: You’re not just building features—you’re acting as a steward of decision-making under uncertainty. You:

        Framed risk clearly

        Offered multiple implementation paths

        Voiced your preference without obstructing momentum

🏁 Final Verdict (Across Arc):

You’ve shown senior-level contextual awareness through:

    Disciplined pacing of questions

    Clarifying role boundaries (dev vs product)

    Offering risk-adjusted implementation paths

    Showing strategic humility (“just a personality thing” vs digging in)

    Staying product-aware without overstepping

This is the kind of reasoning AI could evaluate if it's trained to look not just for "smart answers," but for conversational leadership.
</pre>

Yay got senior. Now here's where I feel a bunch of people get caught up. They get the happy result and stop here. But notice how ChatGPT didn't tell me where I screwed up or how I can improve. I think that's cause ChatGPT is built to be more positive so we gotta override that. We need ChatGPT to tell us what it thinks our weak points are and how we can improve because that's just as important.

### User Response 4
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
Can you list out some strengths to my approach? List some obvious ones and subtle ones if they exist. Also do the same with weaknesses.
</pre>

### AI Response 4 (Strengths)
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🔹 Obvious Strengths

    Validates Assumptions

        You didn’t jump to build—you questioned whether the feature is truly needed. This shows product thinking.

    Cross-Functional Thinking

        You explicitly referenced that this falls under business/UX responsibility, showing clear understanding of role boundaries.

    Risk Mitigation Mindset

        Instead of "yes/no", you offered scoped options (subset rollout, quick version, wait for data), which shows you’re thinking in terms of risk tolerance and incremental delivery.

    Aligns with Stakeholders

        You expressed a personal preference while still making it clear you'd defer to business needs—a key trait in collaborative senior engineers.

🔸 Subtle Strengths

    Conversation Pacing Discipline

        You asked a few highly targeted questions per exchange. This shows you're managing cognitive load and understand real-world communication dynamics. It prevents overwhelming stakeholders.

    Signals Without Demands

        You never said “this must be validated first” or “we shouldn’t do this.” Instead, you used phrases like:

            “Seems important enough...”

            “Feels like this falls more on...”

            “My preference is…”

        That’s a diplomatic, facilitative tone, common in effective tech leads and architects.

    Recognizes Feature Scope as Secondary Flow

        You noticed that this isn’t part of the primary checkout flow, reducing its user impact. That’s a systems-thinking signal—you're seeing how this slots into the broader product experience.

    Anticipates Feature Decay

        Mentioning the potential of items “just sitting there forever” shows foresight around feature lifecycle and product debt, which juniors/mids rarely account for.
</pre>

### AI Response 4 (Weaknesses)
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
🔹 Obvious Weaknesses

    Lack of Concrete Recommendation

        You presented options well, but never closed the loop with a firm proposal (e.g., “I suggest we do a limited rollout while UX runs a fast validation study”).

        In decision-heavy orgs, this may feel too neutral.

    No Explicit Technical Framing Yet

        You haven't brought up engineering implications: e.g., auth logic, persistence, backend impact, analytics instrumentation. That would round out your ownership.

🔸 Subtle Weaknesses

    Preference Framed as Personality

        “That’s just a personality thing” may undercut your strategic reasoning. If you think the product needs validation, own that as a logic-driven position, not a personal quirk.

    Soft Language Could Be Misread

        Your style is diplomatic, which is good, but some stakeholders (especially less mature PMs) might mistake it for indecision. A stronger framing might be:

            “I’m not against moving forward, but I recommend we get at least lightweight validation to ensure it solves the real issue.”

    No Explicit Timeline Framing

        You didn’t ask “how soon do we need this?” or “do we have space in this sprint?” which would help position the risk of delay vs value more concretely.
</pre>

I mean I agree with most of these. In fact the 1st major weakness I've indentifed myself. I don't like answering yes or no because there are 100000 other edge cases that will sway me one way or the other. It's not that I can't it's that I usually default to leaving it open ended. Luckily for me, I'm in an env where that's acceptable because our team dynamic is around the entire team agreeing. But if that changed, I would definetly need to work on giving more concrete recommendations. So far so good with ChatGPT

But why stop there? I don't agree with #2 being an obvious weakness. I'm talking to a PO, why would I talk about technical framing when we're still confirming solution? And it's a PO, I'm not expecting them to know what I'm talking about. Let's ask.


### User Prompt 5
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
I agree with most of these but I'm challenging #2 obvious weakness "No Explicit Technical Framing Yet". The conversation is with a PO. So 2 things come up for me. 1 we haven't closed the loop on confirming what the overall solution is going to be. So bringing in technical implementation might be a bit too soon. 2, it's a PO. PO doesn't really need to know the engineering implications. That's a conversation with me and the dev team or architect which from my understanding are not part of this conversation. It's not that I wouldn't bring them up though, it's that in this line of conversation I would argue that there was no need to. Now if the PO asked me for an estimate then it might have come up. 

Don't just accept my answer. I want to see you reason through it. Challenge it and see if your assessment still holds. If it doesn't then accept my response. If it does then challenge me back.
</pre>
Important Note: I had to reprompt with that 2nd part of not just accepting my answer. Becuase I'm **contextually aware** that AI has a tendency to just concede when challenged, I have to explicitly tell it not to. I'm asking it to provide reasoning so that at the very least I can check if it matches its result.

### AI Prompt 5
<pre style="white-space:pre-wrap; word-wrap:break-word; padding:1em; border-radius:5px; border:1px solid #d0d7de;">
⚖️ Argument For It Being a Weakness (Original Reasoning)

    Senior engineers are expected to pre-empt downstream blockers.

        Even with non-engineering stakeholders, a light mention like:

            “Just to flag, depending on how we store this, auth or persistence might affect delivery scope,”
            …can avoid misaligned expectations down the line.

    POs often don't know what they're asking for in terms of effort.

        Giving some technical framing helps anchor feasibility and complexity, especially when proposing multiple options (e.g., localStorage vs server-side save).

    It establishes cross-functional credibility.

        When seniors bring in just enough technical insight, it shows ownership without going full low-level. It reassures the PO that the dev is not just a feature-taker.

    It affects prioritization.

        If “Save for Later” requires backend persistence vs local storage, that absolutely might shift where it lands in a sprint. A high-level nudge could help the PO triage.

🧠 Now, Let’s Weigh Your Counterpoints

    “The solution wasn’t locked in yet, so implementation talk is premature.”

✔ Valid.

    Premature implementation often traps teams into bad solutions. Holding it back keeps the discussion open.
    Counterweight: Still, even uncertainty can be scoped. A quick “this could range from trivial to complex depending on direction” might help PO understand what they’re signing up for.

    “The PO doesn’t need engineering detail—that’s for internal dev discussions.”

✔ Mostly valid, but here’s the tension:
POs don’t need tech details, but they do benefit from guardrails. Otherwise, you risk scope creep later.

Example of a good middle ground:

    “If this turns into a persistent, account-tied feature, we’ll probably need backend support and user auth, just something to keep in mind.”
    → This doesn’t derail the convo but subtly frames impact.

    “If they asked for an estimate, then it would’ve come up.”

✔ Totally fair, and it proves you’re reacting to cues, not over-injecting technicalities.
But a senior dev often adds early signal framing before being asked—precisely to help set up accurate future estimates. That can prevent surprises later.

🧩 Final Judgment

    🟨 Not a weakness in this particular flow, but…
    🟩 It could be a missed opportunity, depending on how fast the org moves.

You showed strong reasoning by:

    Matching your depth to the conversation’s stage

    Deferring technical details until the business case was more solid

    Avoiding premature solutioning

BUT—

If the org has a history of running with half-validated ideas and scoping later, you might regret not flagging the potential backend/app layer implications earlier.
🤝 Conclusion:

Your challenge holds. It was not a weakness given the pacing and audience, but in a different org context (e.g., fast-sprint pressure, low-product-maturity teams), it could become one.

You made a reasoned tradeoff, not a blind omission.
I withdraw the original critique. 🧠
</pre>

Again I agree with its reasoning and it goes along a point I brought up earlier. My style is an advantage because of my environment. ChatGPT correctly calls out that although what I'm saying is true, it would be a weakness in a different context. And that's what it's all about, **contextual awareness**. You not only have to learn different techniques, you have to learn when to apply them. You can't just consider the technical aspects, you have to consider the people aspect as well. It's hard, it's annoying, and it's not what most devs sign up for. But hey next time your manager tells you why you can't get a promotion, this is probably what they're talking about.
