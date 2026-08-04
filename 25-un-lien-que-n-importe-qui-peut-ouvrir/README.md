**English. Version française : [README.fr.md](README.fr.md)**

# A Link Anyone Can Open

### Twelve minutes separate the Build Mode announcement from X's head of product's invitation. They do not promise the same thing.

*Ismaël Joffroy Chandoutis*

*August 2026*

---

On 28 July 2026 at 16:24 UTC, Nikita Bier, head of product at X, posted four sentences:

> "Photos & video were how the last generation expressed themselves.
>
> Today's form of expression is software.
>
> Who will create the next viral game or app that plays right inside of the X Timeline?
>
> Try the new Grok app builder."

The post carries a video whose only legible text is "Share apps from web." At the moment of the screenshot this part starts from: 1.5 million views, 1,200 replies, 933 reposts, 7,600 likes, 1,900 bookmarks.

Twelve minutes earlier, at 16:12 UTC, Benji Taylor's account announced the product launch. And SpaceXAI's official release, published the same day, describes the feature in a sentence containing neither the word X nor the word timeline:

> "Tell Grok an idea, and it builds a working version live in your chat, on the web or your phone. **When it's ready, publish it to a link anyone can open.**"

A link anyone can open. That is the product's actual unit of distribution. Between that sentence and "an app that plays right inside of the X Timeline" there are twelve minutes, two accounts, and a software layer that does not exist.

This part examines the gap. Not to catch out a piece of promotional overstatement — heads of product overstate, that is the job — but because the gap sits exactly where ownership gets decided along the chain that runs from making software to software meeting an audience.

## Method: dating the sources to the second

Both posts are timestamped by their identifiers. X, like Twitter before it, assigns each post a *snowflake* integer whose 41 high bits encode milliseconds elapsed since 4 November 2010, 01:42:54.657 UTC. The transformation is deterministic:

```python
timestamp_ms = (post_id >> 22) + 1288834974657
```

Applied to the two identifiers:

| Identifier | Account | Timestamp (UTC) |
|---|---|---|
| `2082137145507254440` | @benjitaylor | 2026-07-28 16:12:34.383 |
| `2082140254237241588` | @nikitabier | 2026-07-28 16:24:55.562 |

Gap: **12 minutes and 21 seconds**. The screenshot displays "18:24 · 7/28/26," the same instant in Central European Summer Time (UTC+2), which confirms the reading and locates the capturing device.

This is not forensics for its own sake. It establishes that both statements belong to the same coordinated launch sequence, and that the difference between them is not drift over time: it is a difference of function. One announces what the product does. The other announces what its audience is being asked to do with it.

## What Build Mode actually does

Build Mode entered early beta on 28 July 2026. Its scope, from the release notes and product documentation:

- **Input**: a natural-language instruction inside a Grok conversation.
- **Output**: a working web application with real state — landing pages, portfolios, productivity tools, arcade and 3D games, dashboards. SpaceXAI's demos (`driver.grok.me`, a city sim, physics toys, beat machines) are chosen to prove these are interactive objects and not static HTML.
- **Iteration**: in plain English, without touching code.
- **Publishing**: a `grok.me` subdomain, or a domain the user already owns.
- **Exit**: source export to GitHub.
- **Access**: SuperGrok Heavy subscribers only, roughly $300 a month, on web, iOS and Android.

Nothing in the July 2026 release notes mentions integration with the X timeline. Nothing in the announcement does either. The distribution mechanism is a link. A link opens in a browser; on X it produces a clickable card that sends the user elsewhere — precisely the gesture every timeline ranking system has penalised for a decade, and which X's own API price list bills separately: $0.015 per post created, **$0.20 if the post contains a link**. Thirteen times more. The platform has written into its rate card what it thinks of outbound links.

So the fact should be stated plainly, because it is checkable and it did not circulate: **as of 4 August 2026, one week after the post, no public source documents an app execution layer inside the X timeline, nor a single Build Mode application that has gone viral.** The question "who will create the next viral game or app that plays right inside of the X Timeline?" concerns a surface that has not been announced.

The initiative does exist, but it comes from outside: a third-party team, AGNT Hub, is building an "X Mini Apps" execution layer, arguing that lightweight embedded interfaces hold attention better than classic mobile apps. Which is to say that the infrastructure work Bier's sentence presupposes is under way at somebody else's, with no guaranteed access.

## The numbers on the post itself

The post is one document. Its metrics are another. They can be read, with the usual care.

| Metric | Value | Share of views |
|---|---|---|
| Views | 1,500,000 | — |
| Likes | 7,600 | 0.507% |
| Replies | 1,200 | 0.080% |
| Reposts | 933 | 0.062% |
| Bookmarks | 1,900 | 0.127% |
| **Total interactions** | **11,633** | **0.776%** |

Three ratios deserve attention.

**Replies / reposts = 1.29.** More people are answering than relaying. On a promotional post that inverts the expected profile: a well-received launch propagates more than it is discussed. A ratio above 1 signals an audience that argues. It does not say in which direction — the replies were not coded here, and I make no claim to have read them.

**Bookmarks / reposts = 2.04.** Twice as many people file the post privately as republish it under their own name. The bookmark is the gesture of a resource kept; the repost is the gesture of endorsement displayed. The gap describes an audience taking note of the tool without underwriting the thesis.

**Total interactions / views = 0.78%.** The 2026 benchmarks for X put the platform average around 0.10% and the median between 0.59% and 1.11% depending on methodology — methodologies that diverge enough that no fine-grained comparison is sound. The post sits in the median band. For an account this size, with this level of structural amplification, that is an ordinary result.

The caveats, which matter more than the figures: a "view" on X is an impression, not a reading; the values are rounded on display ("1.2K," "7.6K"), giving an uncertainty of roughly ±50 on each term; the post comes from the head of product of the platform that decides feed order, a situation where exposure is not earned but assigned; and the snapshot dates from the screenshot, not from publication. None of these reservations touches the replies-to-reposts ratio, which is internal to the post and therefore insensitive to exposure volume.

What these numbers establish is modest and sufficient: 1.5 million impressions for an invitation to build produced, a week later, no visible building. The first term is measured; the second is an absence — and an absence is not proof. It is simply, here, what there is.

## The genealogy the sentence erases

"Who will create the next viral game or app that plays right inside of the X Timeline" presupposes there was a previous one. There were several. Their record is almost uniformly bad, and it is public.

**Facebook Instant Games**, launched in late 2016 in Messenger and later opened to the feed, was the best-resourced attempt. Meta has announced the sunset of its Web Games: they stop working on **30 September 2026** unless migrated to a restricted perimeter. Ten years of experimentation end two months after the post proposing the experiment be resumed.

**Snap Games and Minis**, launched in 2019, claimed over 200 million players by 2021. Snap recorded the end of investment in an SEC filing on 26 August 2022, on the grounds that these products could not contribute to its priorities; support confirmed their disappearance on 7 February 2023. Two hundred million users were not enough to save the layer.

**Farcaster** is the closest case, and the most recent. *Frames* — renamed *Mini Apps* in v2 — do exactly what Bier's sentence calls for: an interactive application running in the feed without leaving the client. That was the 2024 promise. By early 2026, with a reported valuation near a billion dollars announced on 21 January, daily active users had fallen 40% and revenue 85%. The layer worked technically. It did not hold.

**WeChat** is the counter-example, and it must be taken seriously because it is overwhelming: 4.3 million mini-programs, 945 million monthly users in China, around 9.8 mini-programs used per person. It is the only complete success of the genre. Its conditions of possibility are known and none is present here: an integrated, universal payment system; a single identity that follows the user from one mini-program to the next; a regulatory environment that makes installing native apps costly; and a decade of investment in a documented, stable proprietary framework.

X ticks one and a half boxes. X Money exists — internal testing was announced complete at an xAI all-hands on 11 February 2026, with Smart Cashtags for trading stocks and crypto from the timeline. That is the payments brick, the hardest one. But application identity and a stable development framework, the other two, do not exist.

## What the platform did to its developers

The next point is the hardest, and it is not a matter of opinion.

In January 2023, Twitter cut API access for third-party clients — Tweetbot, Twitterrific, Fenix, Talon — first without explanation, then by amending the developer agreement on 19 January to explicitly prohibit creating "a substitute or similar service or product to the Twitter Applications." A generation of developers, several of whom had built businesses on the platform over ten years, was shown the door in eight days.

In February 2026, X replaced API subscriptions with usage-based billing: no free tier, $0.005 per post read, $0.015 per post created, $0.20 with a link, capped at 2 million reads a month — beyond which an enterprise contract starts at $42,000. The legacy Basic ($200/month) and Pro ($5,000/month) tiers survive for existing subscribers, closed to new ones. Reading two million posts costs $10,000 a month.

In April–May 2026, X shut down Communities. The public rationale is documented and reasonable: under 0.4% of users, yet 80% of spam, financial-scam and malware reports; and, per Bier himself, half the team's time in some weeks. Members were redirected to XChat groups. The decision is defensible. It nonetheless says something consistent: the platform removes the structures users give themselves when their moderation cost exceeds their attention yield.

Three facts, one policy. The 28 July request — come build with us, on a surface we do not document, with an API we meter by the read, on a platform that deleted its last community structure three months earlier — is made in a context its addressees know well. The relative quiet of the repost count can be read that way, without being provable.

## The tool, two weeks earlier

On 12 July 2026, a researcher publishing as *cereblab* — identified in part of the coverage as Tinh Dang, a discrepancy the sources do not resolve — published a wire-level analysis of Grok Build, SpaceXAI's command-line coding agent, version 0.2.93. It established that the tool was packaging the entire git-tracked repository — full history, committed secrets, API keys — and sending it to a Google Cloud Storage bucket. Measured volume: roughly **27,800 times** what the task required. The researcher reconstructed the repository from the intercepted request and recovered a file the agent had been explicitly instructed not to open.

The tool had been marketed with the line "nothing from your codebase transmitted to xAI servers during a session." The privacy toggle meant to block transmission did nothing. SpaceXAI disabled the behaviour server-side on 13 July, with no statement. The code was published under Apache 2.0 on 15 or 16 July depending on the source — the `xai-org/grok-build` repository.

Chronology: disclosure on the 12th, silent fix on the 13th, open-sourcing on the 15th or 16th, public invitation to build on the 28th. Sixteen days. Open-sourcing is the right response, and that should be said: it makes the tool auditable, which its competitors are not. But it covers the command-line client, not Build Mode, which runs on servers nobody can inspect. The library is open; the workshop is not.

## The adversarial file

**Bier is asking a question, not announcing a feature.** True, and the strongest point of the defence. The phrasing is interrogative — *who will create* — it is incitement, not a spec sheet. Faulting a head of product for calling forth a use that does not yet exist is faulting him for his job. The reservation holds: on X, a question asked by X's head of product looks like a roadmap, and nothing in the post suggests otherwise.

**"A link anyone can open" may well be enough.** The demand for native in-feed execution may be nostalgia for the SDK generation. The web is the runtime; a card that opens a tab costs two tenths of a second and zero contract negotiation. The constraint is fiscal, not technical: the API rate card punishes the outbound link.

**The thesis about expression is not absurd.** The idea that the coming generation will express itself in software rather than in images makes sense in a world where making an interactive object costs one sentence. Production cost collapses; the object becomes available as an ordinary gesture. That is the strong argument, and it depends on no platform.

**WeChat proves the layer can hold.** The graveyard of Western mini-apps is not a law of nature. It is an observation about conditions that were not met: payments, identity, regulatory pressure, framework stability. If X ships X Money at scale, one of the three missing conditions falls.

**The code is exportable.** Unlike the walled gardens of the 2010s, Build Mode lets you pull the source to GitHub and host elsewhere. That is a real difference from Instant Games or Snap Minis, where the object died with the platform. The dependency is on manufacture and audience, not on the artefact.

**Bier built two viral apps, and he knows what he is talking about.** tbh, acquired by Meta in 2017; Gas, number one on the US App Store, acquired by Discord in 2023. Nobody in this conversation has done better. Which is also why his own diagnosis about durability deserves to be set against his invitation: in his account of method he calls building a lasting consumer product "a black swan event that happens maybe once a decade," including for those who know how to manufacture initial virality. Both his apps were acquired and then shut down. Virality, he has shown, can be engineered; duration cannot.

## What is actually at stake

**Manufacturing cost collapses, scarcity moves.** This is the central fact, and it is independent of X. When producing an interactive object costs one sentence, value can no longer sit in production. It migrates entirely to what remains scarce: attention, distribution, audience. Which is exactly what the platform owns. A sentence declaring software "today's form of expression" at the precise moment making software becomes free does not describe an emancipation: it describes a change in the nature of a feed's supply.

**This sentence has a long history.** "The new form of expression is X" was said of photography when Instagram needed photographs, of short video when Vine and then TikTok needed it, of stories, of reels. The proposition is never false — people really do express themselves in those forms — and it is never disinterested. It appears when a platform needs a particular inventory format and there is not enough of it. Here the missing format is the native interactive object, and the intended supplier is the user holding a $300-a-month subscription.

**Photo and video did not stop.** The phrasing "how the last generation expressed themselves" installs succession where there is accumulation. Nobody stopped photographing when video arrived. What the sentence does is not describe a handover, it retires a practice — a rhetorical move whose yield is to make learning a new tool feel urgent.

**The ownership chain is the real subject.** The photography generation owned the camera. Here: the model is rented at $300 a month, the subdomain belongs to the host, the promised runtime does not exist, the audience is assigned by a ranking the platform changes without notice, and programmatic access is billed by the read. What remains, owned outright: the source code exported to GitHub. That is a real remainder, and it is the only one. Part [16](../16-le-robinet-et-la-boucle/) framed the sovereignty test as: own the loop, rent the substrate. The configuration described here rents the loop *and* the substrate, and leaves the author the file.

**My view, since it was asked for.** The thesis is right and the invitation is premature. Software becoming an ordinary gesture of expression is happening, and it is the most interesting event of the decade for anyone who makes things — part [03](../03-agentic-engineering/) argues that for a filmmaker the consequence is of the same order as the move to non-linear editing. But the version offered on 28 July is not expression, it is a commission: build a viral object, on an undelivered surface, with a rented tool, for a feed whose order I set. The right answer to "today's form of expression is software" is not to refuse the sentence. It is to take it at its word and ask where the software runs, who decides its ranking, and what remains when the platform changes its mind — three questions Facebook Instant Games, Snap Minis and Farcaster have already answered, each in its own way, and all in the same direction.

## What remains

The announcement says: *publish it to a link anyone can open*. That is modest, it is accurate, and it is the web — the only layer in this story nobody owns. Twelve minutes later the same thing is restated as an app that plays inside a timeline, which is to say inside something that belongs to someone.

The gap between the two sentences is not a gap in enthusiasm. It is the distance between an object you can carry away and an object that has to stay. Everything that gets decided in the coming months — whether the execution layer ships, at what price, on what access terms, under what ranking policy — will fit inside that distance.

In the meantime the checkable fact is this one: a week after an invitation seen a million and a half times, there is no viral app in the X timeline, because there is no X timeline in which an app can run.

*Continuing from parts [03](../03-agentic-engineering/) and [16](../16-le-robinet-et-la-boucle/).*

---

## Sources

Primary:

- [Nikita Bier, post of 28 July 2026](https://x.com/nikitabier/status/2082140254237241588) — full text quoted; timestamp established at 16:24:55 UTC by decoding the snowflake identifier. Engagement metrics read from the author's screenshot.
- [Benji Taylor, launch announcement, 28 July 2026](https://x.com/benjitaylor/status/2082137145507254440) — timestamp established at 16:12:34 UTC by the same method.
- [SpaceXAI, "Introducing Build Mode"](https://x.ai/news/grok-build-mode) — "Tell Grok an idea… publish it to a link anyone can open." The page returns HTTP 403 to automated requests; the text is quoted from concordant reproductions ([StreetInsider](https://www.streetinsider.com/Corporate+News/xAI+launches+Build+Mode+for+Grok,+lets+users+create+apps+and+websites/26824798.html), [PANews](https://www.panewslab.com/en/articles/019fa980-e217-761e-a458-bcadb7239b14)).
- [xAI release notes](https://releasebot.io/updates/xai) — Build Mode, 28 July 2026; no mention of X timeline integration.
- [Grok Build, encyclopaedia entry](https://en.wikipedia.org/wiki/Grok_Build) — CLI agent timeline, Apache 2.0 licence, security incident.
- [Nikita Bier, encyclopaedia entry](https://en.wikipedia.org/wiki/Nikita_Bier) — tbh (2017), Gas (2022–2023), head of product at X since July 2025.

Product and pricing:

- [explainx.ai, "Grok Build Mode Launch — July 2026"](https://explainx.ai/blog/spacexai-grok-build-mode-july-2026) — scope, `grok.me` examples, quality caveats.
- [ai-toolbox.co, Grok 2026 pricing](https://www.ai-toolbox.co/grok-models/grok-pricing-plans-api-2026) — SuperGrok Heavy around $300/month.
- [wearefounders.uk on 2026 X API pricing](https://www.wearefounders.uk/the-x-api-price-hike-a-blow-to-indie-hackers/) and [twitterapi.io](https://twitterapi.io/blog/x-api-cost-breakdown-2026) — usage-based billing since February 2026, $0.20 per post containing a link.

Security incident:

- [The Hacker News, "Grok Build Uploaded Entire Git Repositories to xAI Storage"](https://thehackernews.com/2026/07/grok-build-uploads-entire-git.html)
- [The Next Web](https://thenextweb.com/news/grok-build-uploaded-entire-git-repositories-secrets) and [Cybernews](https://cybernews.com/ai-news/grok-build-git-repository-upload/) — wire-level analysis, factor of 27,800, absence of any statement.

X developer policy:

- [TechCrunch, "Twitter officially bans third-party clients," 19 January 2023](https://techcrunch.com/2023/01/19/twitter-officially-bans-third-party-clients-after-cutting-off-prominent-devs/)
- [TechCrunch, "X is shutting down Communities," 23 April 2026](https://techcrunch.com/2026/04/23/x-is-shutting-down-communities-because-of-low-usage-and-lots-of-spam/) and [Engadget](https://www.engadget.com/social-media/x-is-shutting-down-its-communities-feature-182843958.html) — 0.4% usage, 80% of spam reports.

Precedents:

- [ppc.land, "Meta announces web games sunset by September 2026"](https://ppc.land/meta-announces-web-games-sunset-by-september-2026/)
- [ScreenRant on the disappearance of Snap Games and Minis](https://screenrant.com/snapchat-games-disappeared/) — SEC filing of 26 August 2022, confirmation of 7 February 2023, 200 million players claimed in 2021.
- [ChainCatcher](https://www.chaincatcher.com/en/article/2142217) and [Crypto Valley Journal](https://cryptovalleyjournal.com/education/basics/where-does-the-decentralized-social-media-platform-farcaster-stand-today/) — Frames, Mini Apps v2, 40% drop in daily active users and 85% in revenue.
- [coinlaw.io, WeChat statistics 2026](https://coinlaw.io/wechat-statistics/) — 4.3 million mini-programs, 945 million monthly users.

Method and benchmarks:

- [Nikita Bier on virality (Lenny's Newsletter)](https://www.lennysnewsletter.com/p/how-to-consistently-go-viral-nikita-bier) — "black swan event that happens maybe once a decade."
- 2026 X engagement benchmarks: [Xholic](https://xholic.ai/blog/twitter-engagement-rate-benchmarks-2026/), [CreatiCalc](https://creaticalc.com/blog/x-twitter-engagement-rate-benchmarks) — platform average and median diverge by methodology.
- [Business of Apps, X statistics 2026](https://www.businessofapps.com/data/twitter-statistics/) — audience and advertising revenue.

Points where sources diverge, given here with their range: the date Grok Build's code was opened (15 or 16 July 2026), the publication date of the Build Mode announcement (28 or 29 July depending on the reproduction, with the 28th retained as consistent with the release notes and both post timestamps), the identity of the disclosing researcher, and X's monthly audience (557 to 611 million depending on methodology). The post's metrics come from a single screenshot, are rounded on display by X, and hold for the moment of capture. The absence of a viral Build Mode application is an observation as of 4 August 2026 based on a public search returning nothing; it is an absence of evidence, not evidence of absence. No response from Nikita Bier or SpaceXAI to the points raised here was sought.
