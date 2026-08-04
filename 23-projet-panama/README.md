**English. Version française : [README.fr.md](README.fr.md)**

# Project Panama

### Why destroying the books is precisely what makes scanning them legal

*Ismaël Joffroy Chandoutis*

*July 2026*

---

An internal Anthropic planning document, unsealed in January 2026 and quoted by the *Washington Post*, contains two sentences:

> "**Project Panama is our effort to destructively scan all the books in the world. We don't want it to be known that we are working on this.**"

A totalising ambition, and a clear awareness that the method would be publicly indefensible.

A year earlier, on 23 June 2025, Judge William Alsup issued the ruling in *Bartz v. Anthropic* that explains why the method was nonetheless found lawful. His central sentence runs to eight words:

> "The print original was destroyed. **One replaced the other.**"

This is the most counter-intuitive articulation in contemporary copyright. Anthropic bought millions of books, stripped their bindings, cut their pages, scanned the contents and discarded the paper. And it is **because it destroyed the originals** that the operation was held to be fair use.

## What was done

The ruling describes the operation with a precision that makes commentary redundant.

It begins with a hire. In February 2024 Anthropic recruits **Tom Turvey**, whom the court identifies as "the former head of partnerships for Google's book-scanning project." His brief, as the court reconstructs it from the exhibits: obtain "all the books in the world" while avoiding as much "legal/practice/business slog" as possible.

Turvey starts with the legitimate route. In spring 2024 he writes to major publishers about licensing. Alsup notes what follows with remarkable dryness:

> "**Had Turvey kept up those conversations, he might have reached agreements to license copies** for AI training from publishers — just as another major technology company soon did with one major publisher. **But Turvey let those conversations wither.**"

The man who had run partnerships for Google's *non-destructive* book scanning lets the negotiations lapse, then organises destructive scanning.

What came next:

> "Anthropic spent many millions of dollars to purchase millions of print books, often in used condition. Then, its service providers **stripped the books from their bindings, cut their pages to size, and scanned the books into digital form — discarding the paper originals.**"

The unsealed documents add the materiality the ruling omits: a hydraulic cutting machine, a contractor engaged to process between five hundred thousand and two million books in six months, bulk used-book suppliers — Better World Books, World of Books. New York's Strand bookstore declined.

## Why destruction is the operative legal fact

Alsup's reasoning is not tolerance extended to collateral damage. Destruction is the condition of lawfulness, and he says so explicitly.

> "All agree on the facts of the format change. Anthropic 'destructively scan[ned]' the print copies to create the digital ones. […] The digital copy was then housed in the 'research library' […] **in place of** the print copy. Authors do not allege and our record does not show that Anthropic provided its converted digital copies of print books to anyone outside Anthropic."

Then the decisive passage:

> "Here, every purchased print copy was copied in order to save storage space and to enable searchability as a digital copy. The print original was destroyed. One replaced the other. And, there is no evidence that the new, digital copy was shown, shared, or sold outside the company. **This use was even more clearly transformative than those in Texaco, Google, and Sony Betamax (where the number of copies went up by at least one)** […]."

And on the amount copied:

> "Copying the entire work was exactly what this purpose required. **There was no surplus copying. The source copy was destroyed.**"

The implication deserves measuring. Google Books, digitising without destroying, took the number of copies from one to two. Anthropic, by destroying, stays at one. Under the fair use logic Alsup applies, **keeping the original has become a legal weakness**. Anthropic's operation is judged *more* transformative than Google's precisely because it left nothing behind.

Against that, the part of the case that cost money: the seven million books downloaded from LibGen and PiLiMi. There, no copy had been purchased, nothing was destroyed, and the copy was purely additive. All four fair use factors tip toward infringement.

The dividing line is therefore sharp: **buy, destroy, scan** is fair use; **download** is not. This is not a moral distinction. It is an arithmetic of copies.

## What the settlement does not cover

The litigation settled. Final approval came on 20 July 2026 — from Judge Araceli Martínez-Olguín, Alsup having retired in the interval. The terms: one and a half billion dollars in four tranches, **482,460 works**, roughly three thousand dollars per work, a 91.3% claims rate, three hundred and fifty opt-outs, fifty-four objections overruled, and attorneys' fees cut from $187.5 million to $101,561,111. Payments are expected in late August 2026.

But the settlement's scope deserves close reading, because it is narrower than assumed. The notice specifies that released claims "**do not include any claims about works in Books3 or scanned books**," and the destruction obligation covers only files derived from LibGen and PiLiMi.

In other words: Anthropic paid a billion and a half for the books it pirated, and **nothing** for the millions it bought and cut up. It keeps the PDFs from those scans. The paper books no longer exist.

The asymmetry deserves stating without commentary: **stealing a book cost roughly three thousand dollars a title; buying one and destroying it cost nothing at all.**

## The subtext, layer by layer

### What the others did

It would be dishonest to treat Anthropic in isolation, and the comparison serves it better than one might expect.

**Meta** downloaded LibGen and Anna's Archive over BitTorrent. Judge Vince Chhabria establishes that the company abandoned its negotiations with Penguin Random House and HarperCollins on 7 April 2023, "after confirming that LibGen contained most of the works available for license." An internal budget line entered into evidence summarises the strategy: "Books strategy: libgen [in progress] – **FREE**." Approval went up to Mark Zuckerberg; a vice-president accepted "full risk"; distribution of the information was handled "on a 'need to know' basis."

Meta nonetheless won its case. Chhabria takes care to say why, and his formulation must be quoted: "**this ruling does not stand for the proposition that Meta's use of copyrighted materials to train its language models is lawful.**" He writes, at the outset, that in most comparable cases the answer will likely be unlawfulness. Meta won on insufficient proof of market harm, not on principle.

**OpenAI** has never disclosed the contents of its "Books1" and "Books2" corpora. An allegation set out without contradiction before Judge Ona Wang holds that they were originally called **"LibGen1" and "LibGen2."** They are the only training datasets OpenAI has ever deleted, erased in 2022, a year before any litigation.

**The Pile**, the public corpus assembled by EleutherAI, functioned as provenance laundering for the whole sector: it contains Books3, extracted from the Bibliotik pirate library, and a set of YouTube subtitles. NVIDIA, Apple, Salesforce, Databricks, Bloomberg and Anthropic itself were able to invoke the "publicly available" character of data whose origin was nothing of the sort.

The overall picture is this: Anthropic is **the only company in the sector that has paid**. A billion and a half dollars, with a 91.3% claims rate. All the others, to date: zero. The gap between the documented gravity of the conduct and its financial consequence runs the other way — and the reason is evidentiary, not moral.

### The professional precedent nobody cites

Destructive scanning was not invented by an AI company. It is a library practice: old, documented, and long debated.

An Association of Research Libraries survey published in March 1989 establishes that **nearly half of major American research libraries then discarded 90% or more of original volumes after reproduction**. Destructive digitisation is, in the professional world, a forty-year-old norm.

It provoked a violent controversy in its time. Nicholson Baker, in *Double Fold* (2001), accused American libraries of destroying irreplaceable collections in the name of preservation. The Society of American Archivists replied through Richard J. Cox. The debate was never settled; it was absorbed.

This precedent seriously complicates the indignation. What Anthropic did at industrial scale, heritage institutions were already doing — with, admittedly, a difference of purpose that is not nothing: libraries destroyed to preserve access, a company destroys to feed a private product.

### Borges wrote the scene

The exact reference is not the one usually cited. In "The Library of Babel" (1941), Borges describes a sect, the **purifiers**, who roam the hexagons destroying volumes they judge useless: "a su furor higiénico, ascético, se debe la insensata perdición de millones de libros."

And he adds a consolation which, read in 2026, becomes unsettling: any destruction of human origin is infinitesimal against the totality. That is, word for word, the structure of Alsup's reasoning — *no surplus copying*, one copy replaced the other, nothing was added to or subtracted from the whole. The judge and the purifier keep the same ledger.

## The case against

**This is not a book burning.** A book burning destroys in order to suppress content. Here the content is entirely preserved in another form, and the destruction falls on legally purchased second-hand copies, the vast majority of which would have been pulped anyway. The publishing industry destroys millions of unsold copies every year without anyone reading it as a symbolic act.

**The legal distinction is coherent, not absurd.** Copyright protects against unauthorised multiplication of copies. An operation that multiplies nothing does not injure what the statute protects. That the result feels counter-intuitive is because our intuition is about the book as object, while the law is about the number of copies.

**Anthropic is the only actor that has paid.** A billion and a half dollars, four hundred and eighty-two thousand works compensated, contractual destruction of the pirated files. Making this company the emblem of the industrial plunder of books, when its competitors have paid nothing, misreads the geography of the file.

**The ruling's legal weight is nil.** *Bartz* is a district court decision, not appealed. It sets no precedent. The claim, sometimes repeated, that it "remains the law today" is inaccurate. Two judges in the same district, two days apart, reached incompatible analyses on the separation between data source and data use. No appellate court has ruled.

**Several spectacular elements are not established.** The exact number of books destroyed was never determined: Alsup writes "millions," and the two-million figure in circulation is a contractual ceiling, not a count. The claim that rare or antiquarian books were destroyed is not documented for Anthropic. And no sourced institutional statement from archivists or librarians about Project Panama could be found — a silence that may itself be a fact.

## What is actually at stake

**The secret operation and the legal one are the same operation.** The most vertiginous fact here is not that Anthropic destroyed books in secret. It is that the operation it judged indefensible enough to conceal is exactly the one a federal judge validated. "We don't want it to be known that we are working on this" refers to the *legal* half of the case. The illegal half — the downloading — was, at a competitor, banal enough to appear as a budget line.

**The law rewards erasing the material trace.** A non-destructive scan would have produced one additional copy and been analysed differently. The legal regime therefore encourages, for an identical purpose, the solution that leaves nothing. That is probably not what any legislator intended, and it is the logical consequence of a law that counts copies rather than objects.

**What disappears is not the information but the copy.** The contents of the Project Panama books still exist, better indexed than ever. What was annihilated are particular objects — previous readers' annotations, inscriptions, marks of use, provenance — none of which enters Alsup's calculation because none is protected by copyright. The loss is real and legally invisible, which is exactly the definition of a blind spot.

## What remains

The codename is almost too good. Panama: an isthmus, a canal, a narrow crossing through which the world is made to pass by changing medium. It is an exact description of the operation.

What this case establishes is not that a company behaved badly — on the part that cost a billion and a half, it did behave badly, acknowledged it and paid, which nobody else has done. It is that **the legal regime governing the passage of books into models structurally rewards destruction**. The solution most respectful of the object — digitise and keep — is the most legally exposed. The solution that leaves nothing is the safest.

No company created that incentive. It follows from a law designed to prevent the proliferation of copies, applied to a technology whose problem was never proliferation.

*Continuing from parts [04](../04-ai-and-the-artist-critical-framework/) and [15](../15-ideologies-silicon-valley/).*

---

## Sources

Primary:

- *Bartz v. Anthropic PBC*, N.D. Cal., Judge William Alsup's order on fair use, **23 June 2025** (Dkt. 231). All court quotations above come from it, with the pagination indicated. The widely repeated date of 24 June is wrong: the stamp and signature read the 23rd.
- Final settlement approval order, **20 July 2026** (Dkt. 680, Judge Araceli Martínez-Olguín).
- Settlement notice to class members, items 13 and 15 on the scope of released claims and the file-destruction obligation.
- *Kadrey v. Meta Platforms*, N.D. Cal., Judge Vince Chhabria's order, June 2025 (Dkt. 598), and exhibits (Dkt. 482).
- Association of Research Libraries, *SPEC Kit 152* (Merrill-Oldham & Walker), March 1989, ERIC ED 325 122 — on the discarding of originals after reproduction in American research libraries.

Press:

- *The Washington Post* (Aaron Schaffer, Will Oremus, Nitasha Tiku), **27 January 2026** — revelation of "Project Panama" from four thousand pages of unsealed documents.
- [Katy Hershberger, *Publishers Lunch*, 28 January 2026](https://lunch.publishersmarketplace.com/2026/01/newly-released-documents-shed-light-on-anthropics-secret-plan-to-scan-every-book/)
- [James Folta, *Literary Hub*, 6 February 2026](https://lithub.com/anthropic-didnt-want-us-to-know-that-they-were-destroying-millions-of-books-to-feed-their-software/)

References:

- Jorge Luis Borges, "La biblioteca de Babel," *El jardín de senderos que se bifurcan*, 1941 — the passage on the *purificadores*.
- Nicholson Baker, *Double Fold: Libraries and the Assault on Paper*, 2001, and Richard J. Cox's reply for the Society of American Archivists.

The exact number of books Anthropic bought and destroyed was never established: the order says "millions," and the two-million figure in circulation is a contractual ceiling in a vendor agreement, not a count. Destruction of rare or antiquarian books is not documented for Anthropic; a separate European matter involving German antiquarian dealers exists but the company concerned denies it. The allegation about the original naming of OpenAI's corpora appears in a procedural order and has not been adjudicated on the merits. The final approval order contains a slip — "four times the statutory minimum for *willful* infringement" where the preliminary order it cites says *ordinary*. No institutional statement from archivists or librarians about Project Panama could be found. *Bartz* is an unappealed district court decision and is not binding precedent.
