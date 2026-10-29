---
tags:
---

# LING 2100 — Exam 2 Notes
### Morphology → Syntax → Semantics → Pragmatics

> [!abstract] How to use
> Read in order; each unit builds on the last (word parts → sentence structure → literal meaning → meaning in context). Covers all four decks, including the appendix slides and the image-only slides. **⚠️ = on the practice exam but not in the slides.** Answer key at the end. Exam 1 material: [[Ling 2100 Exam 1 Notes]].

## Table of Contents
- [[#Unit 5 — Morphology]]
- [[#Unit 6 — Syntax]]
- [[#Unit 7 — Semantics]]
- [[#Unit 8 — Pragmatics]]
- [[#Practice Exam Answer Key]]

---

# Unit 5 — Morphology

**Morphology** = the study of words and their parts: their structure, meaning, and rules of realization in context.

## Parts of speech
A word's **part of speech** (POS) determines **where it can go in a sentence** and **which inflectional/derivational morphology it can take**. It's diagnosed by **syntactic behavior** (where the word can appear), but it also has a **non-random relationship to meaning**.

| POS | Examples | Key facts |
|---|---|---|
| **Noun** | *cat, Alice* | subject/object; **common** (*cat*) vs. **proper** (*Alice*); inflect for **number** (*cats*); common nouns take determiners (*the/every/two cats*); often "people, places, things"; usually **time-stable entities**. Exceptions: ***explosion, earthquake*** (events) |
| **Pronoun** | *he, she, it, they, we* | stand in for **discourse-prominent nouns** (meaning depends on context); in English, inflect for **case** (below) |
| **Verb** | *run, swim, throw* | inflect for **tense** (*walk/walked*), **agree** in number with the subject (*she walks / they walk*); describe the main action; usually **dynamic** = **change over time involving their arguments** (the participants the verb needs: *I broke the window*). Exception: *I love movies* (a state) |
| **Adjective** | *red, cute, heavy* | **modify** a noun (*red dress*) or are the **predicate** with copula *is* (*the dress is red*); **gradable** (*tall*); **comparative/superlative** (*tall, taller, tallest*; *more/most beautiful*); can be **subjective** / emotional (*beautiful, horrible*) |
| **Adverb** | *quickly, very, really* | modify a **verb** (*ran quickly*) or **adjective** (*really tall*); often adjective + derivational ***-ly*** |
| **Determiner** | *the, a, some, all, every* | combine with a noun to pick out its referent: **new vs. familiar** (*a person / the cat*), **proximal/distal** (*this/that*), **possession** (*my*); includes **quantifiers** (*every, some, five*) |
| **Conjunction** | *and, or, so, but, because* | join words, phrases, clauses, sentences |
| **Preposition** | *of, for, with, to* | introduce a noun that **isn't a main argument** of the verb (*I saw him **at the party***) |
| **Modal auxiliary** | *can, may, would, should, might, will* | combine with a verb; describe **hypothetical** states of affairs (*I would go*) |

**Verb transitivity** = how many arguments a verb takes:

| Type | Args | Example |
|---|---|---|
| Intransitive | 1 | *I swam. / The window broke.* |
| Transitive | 2 | *I threw the ball. / I broke the window.* |
| Ditransitive | 3 | *I gave her the book.* (giver, recipient, thing given) |

**Case** = the form that shows a noun's **grammatical role**. In English, **only pronouns** show it:

| Case | Role | Forms |
|---|---|---|
| Nominative | subject | *she, he, I* |
| Accusative | object | *her, him, **me*** |
| Genitive | possessor | *her, his, my* |

- In **Latin** and **Russian**, *all* nouns inflect for case (WALS feature 51A; WALS = World Atlas of Language Structures).
- **Automatic POS tagging** (e.g. spaCy's displaCy demo) labels every word's POS; it's the first step of most NLP.

## Content vs. function words

| | Content (**open class**) | Function (**closed class**) |
|---|---|---|
| Categories | nouns, verbs, adjectives, adverbs | pronouns, determiners, conjunctions, prepositions, modals |
| Paraphrase meaning? | easy (*cat*) | very hard (*the, every, would*) |
| New ones? | all the time (*monoamorous*, *DM*) | rare, but it happens: conjunction ***slash*** ("You slash I will do it") |
| Frequency | mostly rare | the most frequent words (*the* is #1) |

Some words **straddle** the line: *want, cause, take (a bath)*.

## Inflection
**Inflection** = a word changes form to fit its **grammatical context** but **stays the same word and POS** (the same word in a different outfit):

| Form | Base | What changed |
|---|---|---|
| *dogs* | *dog* | plural |
| *walked* | *walk* | past tense |
| *walks* | *walk* | 3rd-person singular present |
| *her* | *she* | accusative case (case inflection is also called **declension**) |

| Kind | How | Examples |
|---|---|---|
| **Concatenative** (most common) | **add an affix** (a piece attached to the word, like *-s* or *-ed*): "chain it on" | *cat→cats*, *walk→walked*. **English plurals = concatenative suffix** |
| **Ablaut** (non-concatenative) | **change the vowel** | *man/men, woman/women; sing/sang, eat/ate* |
| **Suppletion** (non-concatenative) | **replace the whole root** with a substitute form | ***good/better/best***; *be/am/was* |

- **Irregulars cluster on frequent words** (*to be* = most common verb; *good*): maybe you must **hear a form often enough to preserve it**.
- Old ablaut pasts **vanished on rare verbs**: the past of *help* used to be ***holp***. Still varying today: *dived* vs. *dove*.

**French inflects more than English:**

| Part of speech | Inflects for | Example |
|---|---|---|
| Determiner | the noun's gender + number | *le chat* (the.MASC cat), *la maison* (the.FEM house), *les chats* (the.PL cat.PL) |
| Verb | person, number, tense, conditionality | *J'aimerais* (like.1SG.COND = "I would like") |
| Adjective | the noun's gender + number | *le beau chat*, *la belle maison* |

## Derivation
**Derivation** = make a **new word** by changing a root's **meaning or POS**.

| Affix | Attaches to → makes | Example |
|---|---|---|
| *-ize* | Adj/N → V | *popular → popularize* |
| *-er* | V → N | *teach → teacher* |
| *-able* | V → Adj | *wash → washable* |
| *-ness* | Adj → N | *silly → silliness* |
| *-ly* | Adj → Adv | *quick → quickly* |

Practice (find the root, its POS, the affix, and the result):

| Word | Root (POS) | Affix | Result | Note |
|---|---|---|---|---|
| *winterize* | *winter* (N) | *-ize* | V | |
| *clarify* | *clear* (Adj) | *-ify* | V | root changes to *clar-* |
| *I will **box** the supplies* | *box* (N) | none | V | POS change with **no affix** |
| *a guitar **pick*** | *pick* (V) | none | N | POS change with **no affix** |
| *antiqueness* | *antique* (Adj) | *-ness* | N | |
| *antiquity* | *antique* (Adj) | *-ity* | N | root changes to *antiqu-* |

| | Inflectional | Derivational |
|---|---|---|
| New word? | no, a form of the same word | **yes** |
| Changes POS? | **never** | often |
| Position | **outermost** | closer to the root |

## Morphemes
**Morpheme** = smallest piece of a word with a (somewhat consistent) meaning or function; it **can't be divided further**.

| Type | Definition | Examples |
|---|---|---|
| **Free** | can stand alone as a word | *car, tall, motion, wish, do, I* |
| **Bound** | can't stand alone | *-ing, un-, -s, -ed, re-, de-, -ize, -n't* |

Practice exam: *-es* in *cranberries* is **bound + inflectional**; *-ness* is **bound + derivational**.

**How meaningful are morphemes?** The slides' edge cases:

| Example | What it shows |
|---|---|
| *blue+berry, black+berry* | both parts free and meaningful |
| *goose+berry, straw+berry* | first part is a free word but adds no clear meaning |
| *rasp+berry, **cran**+berry* | first part never occurs alone: **cranberry morphemes** (bound, found in only one word) |
| *under+stand* | two free morphemes, but the meaning isn't "stand under" |
| *re+pay* vs. *re+pair* | transparent "pay again" vs. not "pair again" |
| *re+ceive, de+ceive, per+ceive* | *-ceive* recurs as a form, but has no statable meaning |
| *puffin+s, notic+ing, lazi+ness, silli+ness, walk+ed, nation+al+it+ies, natur+al+iz+ation, pulver+ize+s* | clean splits (note spelling changes); *pulver* = a bound root |

> [!example]- Bonus: "unpaired words" story (Jack Winter, *The New Yorker*, 1994)
> Built from words whose negative exists but the positive doesn't: *I was very **chalant**... appear **gruntled** and **consolate**... hair **kempt**, clothing **shevelled**, moved in a **gainly** way... manners couldn't be **peccable**... she was **committal**... she **requited** it.* The joke works because *dis-/un-/in-* are obviously separate morphemes, so we "expect" a base form that doesn't exist (a cranberry-like bound root).

## Word structure
A typical word = **root** (usually free) + **derivational affixes** + **inflectional affixes** (outermost):

*nation* (root, N) → *nation**al*** (derivational, → Adj) → *national**ize*** (derivational, → V) → *nationalize**s*** (inflectional, 3sg)


| Affix | Position | Example |
|---|---|---|
| **Prefix** | before the root | ***re**pay* |
| **Suffix** | after the root | *pay**ing*** |
| **Circumfix** | both sides at once | ***en**light**en*** |
| **Infix** | inside the root | none in English except *abso-**effing**-lutely* |

(WALS feature 26A maps prefixing vs. suffixing across languages.)

### Words have tree structure
**Key idea:** morphemes aren't "beads on a string"; they're **hierarchically structured** (trees). Each affix combines with a unit of a specific category. In the trees, **AFF** = affix.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\definecolor{cred}{RGB}{200,40,40}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.3cm,
  cat/.style={text=cblu,font=\large\bfseries},
  wd/.style={text=cgrn,font=\large\itshape},
  edge from parent/.style={draw,thick}]
\begin{scope}[level 1/.style={sibling distance=1.8cm}]
\node[cat] at (0,0) {Verb}
  child {node[cat] {N} child {node[wd] {nation}}}
  child {node[cat] {AFF} child {node[wd] {-al}}}
  child {node[cat] {AFF} child {node[wd] {-ize}}};
\node[cred] at (0,-4.3) {flat: wrong};
\node[font=\small, align=center] at (0,-5) {says nothing about which\\affix attaches to what};
\end{scope}
\begin{scope}[level 1/.style={sibling distance=3.2cm}, level 2/.style={sibling distance=1.8cm}]
\node[cat] at (7,0) {Verb}
  child {node[cat] {Adj}
    child {node[cat] {N} child {node[wd] {nation}}}
    child {node[cat] {AFF} child {node[wd] {-al}}}}
  child {node[cat] {AFF} child {node[wd] {-ize}}};
\node[cgrn] at (7,-4.9) {hierarchical: right};
\node[font=\small, align=center] at (7,-5.6) {N + -al = Adj; \ Adj + -ize = Verb};
\end{scope}
\end{tikzpicture}
\end{document}
```

The rules: *-al* needs a **noun** (→ Adj); *-ize* needs an **adjective or noun** (→ V); *-ation* needs a **verb** (→ N). So:
- ✓ *nationalize*, *nationalization* (*-ation* attaches to the verb *nationalize*)
- ✗ \**nationation*, \**nationational*: *-ation* can't attach to the noun *nation*
- ✗ \**nationizeal*: *-al* can't attach to a verb
- ? *nationize*: possible, since *-ize* can take nouns (cf. *fossil→fossilize*, *actual→actualize*). What would it mean?

(\* = ungrammatical, ? = questionable.)

### Hierarchy → ambiguity
**Ambiguity** = the same words/sounds/morphemes in the same order mean different things, because the **underlying structure** differs.

***Unlockable***: *-able* attaches to **verbs**; *un-* attaches to **verbs** (reverse: *unlock*) **or adjectives** (negate: *unhappy*).

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.3cm,
  cat/.style={text=cblu,font=\large\bfseries},
  wd/.style={text=cgrn,font=\large\itshape},
  edge from parent/.style={draw,thick},
  level 1/.style={sibling distance=3cm},
  level 2/.style={sibling distance=1.8cm}]
\node[cat] at (0,0) {Adj}
  child {node[cat] {Verb}
    child {node[cat] {AFF} child {node[wd] {un-}}}
    child {node[cat] {Verb} child {node[wd] {lock}}}}
  child {node[cat] {AFF} child {node[wd] {-able}}};
\node[align=center] at (0,-4.8) {(a) [[un-lock] -able]\\``\textbf{able to be unlocked}''};
\node[cat] at (7.5,0) {Adj}
  child {node[cat] {AFF} child {node[wd] {un-}}}
  child {node[cat] {Adj}
    child {node[cat] {Verb} child {node[wd] {lock}}}
    child {node[cat] {AFF} child {node[wd] {-able}}}};
\node[align=center] at (7.5,-4.8) {(b) [un- [lock-able]]\\``\textbf{not able to be locked}''};
\end{tikzpicture}
\end{document}
```

***Inflammable***: *in-* can mean "into/set on" (*inflame* = verb) or "not" (attaches to adjectives).

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.3cm,
  cat/.style={text=cblu,font=\large\bfseries},
  wd/.style={text=cgrn,font=\large\itshape},
  edge from parent/.style={draw,thick},
  level 1/.style={sibling distance=3cm},
  level 2/.style={sibling distance=1.8cm}]
\node[cat] at (0,0) {Adj}
  child {node[cat] {Verb}
    child {node[cat] {AFF} child {node[wd] {in-}}}
    child {node[cat] {N} child {node[wd] {flame}}}}
  child {node[cat] {AFF} child {node[wd] {-able}}};
\node[align=center] at (0,-4.8) {(a) [[in-flame]$_V$ -able]\\``\textbf{can be inflamed}'' = catches fire};
\node[cat] at (7.5,0) {Adj}
  child {node[cat] {AFF} child {node[wd] {in-}}}
  child {node[cat] {Adj}
    child {node[cat] {Verb} child {node[wd] {flame}}}
    child {node[cat] {AFF} child {node[wd] {-able}}}};
\node[align=center] at (7.5,-4.8) {(b) [in- [flamm-able]$_{Adj}$]\\``\textbf{not} flammable''};
\end{tikzpicture}
\end{document}
```

(a) is the real meaning (= catches fire). Because people misread it as (b), English **switched to *flammable***. "Can easily become inflamed" = tree **(a)**, where *inflame* is a Verb node.

Ambiguity happens at every level:

| Type | Example | Meaning 1 | Meaning 2 |
|---|---|---|---|
| **Lexical** (one word, two meanings) | *bank* | side of a river | financial institution |
| **Structural, inside a word** | *unlockable* | `[[un-lock] -able]` can be unlocked | `[un- [lock-able]]` can't be locked |
| **Structural, inside a phrase** | *American art teacher* | `[[American art] teacher]` teaches American art | `[American [art teacher]]` an art teacher who is American |
| **Structural, inside a sentence** | *Pope's Baby Steps on Gays* | the Pope's baby **steps on** gays | the Pope's **baby steps** (small progress) on gays |

(More sentence examples in [[#Ambiguity headlines]].)

## New words (neologisms)
New words appear constantly, mostly **content words** (*monoamorous*), rarely function words (*slash*). **The dictionary isn't the authority** on what's a word; it follows what people do (*deadass, eyebleach, yeet, ragebait, doomscroll, enshittification*).

| Process | What it is | Slide examples |
|---|---|---|
| **Derivational affixes** | add affixes | *monoamorous, girlbossification* |
| **Blend** | fuse **parts** of 2 words | *brunch, smog, motel, copaganda* |
| **Acronym** | initial letters | *NASA, radar, DM, BFF, AF* |
| **Clipping** | **shorten one** word | *gym, math, mic* |
| **Borrowing** | from another language | *karaoke* (Japanese), *sauna* (Finnish), *algebra* (Arabic), *tattoo* (Polynesian), *canoe* (Arawak/Taíno), *kayak* (Inuit) |
| **Back-formation** | strip what *looks like* an affix | *enthuse* (from *enthusiasm*) |
| **Genericization** | brand → general word | *Kleenex, Xerox, Uber* |
| **Words from names** | a name becomes a word | *sandwich* (Earl of Sandwich), *robot* (Čapek's play *R.U.R.*), *jumbo* (Barnum's elephant Jumbo) |
| **Compound** | combine 2 **whole** words | *desk chair, birthday cake, mother-in-law, sunglasses, work wife* |

**Tiffany lawsuit**: Costco sold "Tiffany" rings, arguing the name had been genericized to mean a pronged, raised stone setting. Tiffany said this cheapened its brand. Tiffany won one round, Costco appealed, and they settled.

> [!warning] ⚠️ Classifying the slang words (the slides list them but don't classify them)
> | Process | Words |
> |---|---|
> | **Compound** (2 whole words) | ***brainrot***, *doomscroll*, *ragebait*, *rawdog*, *babygirl*, *girl math*, *short king*, *dumpster fire*, *fancam*, *zoom bomb*, *hashtag*, *nepo baby* |
> | **Derivation** | ***enshittification*** (*en-…-ify-cation*), *unserious*, *yassify*, *unfriend*, *-splaining*, *-shaming* |
> | **Blend** (parts of 2 words) | ***Brexit*** (Britain+exit), *covidiot*, *mansplain*, *cronut*, *techlash*, *humblebrag*, *refudiate*, *hacktivist* |
> | **Clipping** (1 word cut down) | ***rizz*** (cha**ris**ma), *sus*, *vax*, *nepo*, *fam* |
> | **Acronym** | *NFT, FOMO, YOLO, MOOC, WAP* |
> | **POS change, no affix** | ***clock*** (N→V), *ghost* (N→V) |
> | **Old word, new meaning** | *slop, brat, hallucination, tweet, cloud* |
> | **Phrases, not word-formation** | *hold space, locked in, let someone cook, it's giving, 6-7* |

> [!example]- American Dialect Society Words of the Year (full slide lists)
> | Year | Word of the Year | Runners-up |
> |---|---|---|
> | 2025 | *slop* | ragebait, clock [verb], that's AI, chopped, 6-7, reheat nachos |
> | 2024 | *rawdog* | locked in, unserious, brainrot, brat, hold space |
> | 2023 | *enshittification* | ceasefire, babygirl, let someone cook, (derogatory), era, girl [dinner/math], millennial pause, hallucination |
> | 2022 | *-ussy* | Dark Brandon, quiet quitting, long-termism, nepo baby, it's giving, short king, -verse, chronically online, rizz |
> | 2021 | *insurrection* | antiwork, Big Lie, Great Resignation, Long Covid, Omicron, variant, vax, boosted, NFT, bussin', tone indicator, vibe, the ___ urge to, stonk, supply chain, yassify |
> | 2020 | *covid* | abolish/defund, dissent collar, freedumb, doomscrolling, fancam, sus, zoom fatigue, zoom bomb, covidiot, contact tracing, WAP, essential worker |
> | 2019 | *(my) pronouns* | ok boomer, plant-based, stan, Zoomer, Nobody:/Me:, quid pro quo, hot girl summer, VSCO girl, the squad |
> | 2018 | *tender-age shelter* | yeet, blue wave, nationalist, Individual 1, techlash, #nottheonion |
> | 2017 | *fake news* | alternative facts, #MeToo, persisterhood, take a knee, emergency podcast, shitpost, shooketh, unicorn, askhole, avocado toast |
> | 2016 | *dumpster fire* | woke, normalize, post-truth, deplorables, nasty woman, fam, -exit (Brexit), bigly, #blackgirlmagic, gaslight, slay, #OscarsSoWhite |
> | 2015 | *singular they* | ghost, mic drop, microaggression, shade, adulting, squad, yass, ammosexual, dadbod, trigger warning, AF, lit, Netflix & chill, swipe right/left, on fleek |
> | 2014 | *#BlackLivesMatter* | bae, columbusing, even ["I can't even"], ebola, basic, bye Felicia, salty, selfie stick, normcore, thirsty, manspreading |
> | 2013 | *because* [preposition: "because linguistics"] | slash, twerk, Obamacare, selfie, struggle bus, catfish, sharknado, underbutt, binge-watch, drone, -shaming, -splaining, cronut |
> | 2012 | *hashtag* | YOLO, fiscal cliff, Gangnam style, -pocalypse, hatewatching, mansplain, feels, ratchet, MOOC, cray-cray, binders full of women, meggings |
> | 2011 | *occupy* | FOMO, humblebrag, the 99%, tablet, kardash, put a bird on it, planking, job creator, cloud, tiger mother, brony |
> | 2010 | *app* | nom, Wikileaks, trending, prehab, refudiate, hacktivist, Obamacare, corn sugar, ironic mustache |
> | 2009 | *tweet* | H1N1, birther, blog, public option, rogue, un- [unfriend, unfollow], sea kitten, charging station, fail, sexting, death panel |

## Word frequency and length (corpus data)
A **corpus** = a large body of real text. The lecture used the **Brown Corpus** (1M words of edited American English) and 1M words of Reddit comments.


| Pattern | Statement | Shape |
|---|---|---|
| **Zipf's Frequency Law** | **a few very frequent words** (function words), **very many infrequent words** (content words) | **power law**: frequency plunges after the top few words, then flattens into a long tail. **Not** a bell curve |
| **Zipf's Brevity Law** | **more frequent words are shorter** (*the, of, a* vs. *oversimplification, mirthless*). **Language is efficient**: the words used most cost the least effort | negative frequency–length relationship |
| **Word length** | the most common length of an English word **type** (distinct word) is **7 characters** | roughly a **bell curve** |

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgry}{RGB}{150,150,150}
\begin{document}
\begin{tikzpicture}[font=\normalsize]
\draw[->,thick] (0,0) -- (12,0) node[below left] {frequency rank};
\draw[->,thick] (0,0) -- (0,6.6) node[above] {count per million};
\foreach \y in {10,20,30,40,50,60,70}
  {\draw[cgry] (-0.1,\y/11) -- (0.1,\y/11); \node[left,font=\small] at (-0.1,\y/11) {\y,000};}
\foreach \r in {5,10,15,20} {\draw (\r*0.55,-0.1) -- (\r*0.55,0.1); \node[below,font=\small] at (\r*0.55,-0.1) {\r};}
\draw[cblu,thick,smooth] plot coordinates {(0.55,6.36) (1.1,3.31) (1.65,2.62) (2.2,2.38) (2.75,2.12) (3.3,1.94) (3.85,0.96) (4.4,0.92) (4.95,0.89) (5.5,0.87) (6.05,0.86) (6.6,0.80) (7.15,0.66) (7.7,0.66) (8.25,0.64) (8.8,0.61) (9.35,0.58) (9.9,0.49) (10.45,0.48) (11,0.47)};
\foreach \r/\w/\f in {1/the/69.971,2/of/36.412,3/and/28.853,4/to/26.158,5/a/23.308,6/in/21.341,7/that/10.594,8/is/10.109,9/was/9.815,10/he/9.548,11/for/9.489,12/it/8.760,13/with/7.289,14/as/7.259,15/his/6.996,16/on/6.741,17/be/6.377,18/at/5.372,19/by/5.306,20/i/5.180}
  {\fill[cblu] (\r*0.55,\f/11) circle (2pt); \node[above right,rotate=45,font=\small] at (\r*0.55,\f/11) {\w};}
\node[align=left,font=\small] at (8,4.5) {a few huge-frequency\\function words, then a\\very long tail of rare words};
\end{tikzpicture}
\end{document}
```

| Rank | Brown (edited prose) | Reddit (comments) |
|---|---|---|
| 1 | *the* (6.97%) | *the* (3.34%) |
| 2–5 | *of, and, to, a* | *i, to, a, and* |
| Notable high ranks | *he, his, was* | *i, my, you* |

Genre matters: conversation puts *I/my/you* near the top.

```tikz
\definecolor{cgrn}{RGB}{60,170,80}
\definecolor{cgry}{RGB}{150,150,150}
\begin{document}
\begin{tikzpicture}[font=\normalsize]
\foreach \l/\c in {1/20,2/155,3/800,4/2320,5/4070,6/5620,7/6500,8/6050,9/5100,10/3870,11/2480,12/1550,13/900,14/460,15/220,16/115,17/60,18/25,19/10}
  \draw[fill=cgrn] (\l*0.6-0.3,0) rectangle (\l*0.6+0.3,\c/1000);
\draw[->,thick] (0,0) -- (12.5,0) node[below left] {length (characters)};
\draw[->,thick] (0,0) -- (0,7.2) node[above] {\# word types};
\foreach \y in {2000,4000,6000} {\draw (-0.1,\y/1000) -- (0.1,\y/1000); \node[left,font=\small] at (-0.1,\y/1000) {\y};}
\foreach \l in {1,5,7,10,15} \node[below,font=\small] at (\l*0.6,0) {\l};
\draw[<-,thick] (4.2,6.6) -- (6.2,7) node[right] {peak = \textbf{7 characters}};
\node[font=\small\itshape, align=left] at (9.5,4.8) {short: a, of, the\\middle: require, approval\\long: psychopharmacological};
\end{tikzpicture}
\end{document}
```

- **Types vs. tokens**: counting tokens (every occurrence) gives **shorter** typical lengths, because the frequent words are short.
- **Why log-scale the frequency axis** (on the slide's brevity-law plot)? Frequencies span orders of magnitude (*the* ≈ 70,000 per million; *mirthless* ≈ 1). On a linear axis almost every word would be squashed at zero.

## Morphological typology (word-to-morpheme ratio)
Languages differ in **how many morphemes are packed into a word** and **how many meanings each morpheme carries**.

**Reading glosses.** In the example tables below, the top row is the original, the middle row is the morpheme-by-morpheme gloss, and the bottom row is plain English. Grammatical labels used in glosses:

| Label | Meaning |
|---|---|
| **1SG / 3SG / 1PL** | 1st person singular / 3rd person singular / 1st person plural |
| **NOM / ACC** | nominative (subject) / accusative (object) |
| **LOC** | locative ("in/at") |
| **POSS** | possessive |
| **NEG** | negation |
| **DEM** | demonstrative ("this/that") |
| **PL** | plural |
| **MASC / FEM** | masculine / feminine |
| **ASP** | aspect: how an action unfolds (completed vs. ongoing) |
| **AOR** | aorist: completed/habitual action |
| **IMP** | imperfective: ongoing action |
| **COND** | conditional |
| **PRES** | present |
| **CL** | classifier: a word required between a number and a noun |
| **IND.INTR** | indicative intransitive |

| Type | Language | Key idea |
|---|---|---|
| **Isolating** | Yoruba (Nigeria) | each word stands alone: **~1 morpheme per word**, little inflection |
| **Agglutinating** | Turkish | root + affixes glued on like beads, **one meaning per affix** |
| **Polysynthetic** ("incorporating"; *poly* = many) | Yupik (Alaska) | **very long words**: root + many bound morphemes; **a whole sentence can be one word** |
| **Fusional** ("synthetic") | French | **several meanings fused into one affix**, so they can't be pulled apart |
| **Analytic** | English | **between isolating and agglutinating**: a little affixing (*kids, walked*), but much is carried by **free words** (prepositions) |

**Isolating (Yoruba)**: "I looked here, I looked there, but I did not see my mother." Every word is a single morpheme.

| mo | wò | èyí, | wò | èyí, | mo | kò | rí | ìyá | mi |
|---|---|---|---|---|---|---|---|---|---|
| 1SG | look | DEM | look | DEM | 1SG | NEG | see | mother | 1SG.POSS |
| I | looked | here | looked | there | I | not | see | mother | my |

**Agglutinating (Turkish)**: "Aytül always makes the tea in our family." Each hyphen marks a separate affix with one job.

| Bizim | ev-de | çay-ı | her zaman | Aytül | yap-ar |
|---|---|---|---|---|---|
| our | house-LOC | tea-ACC | always | Aytül | make-AOR |
| our | in the house | the tea (object) | always | Aytül | makes (habitually) |

The practice-exam word *ev-imiz-de* "in our house" works the same way: three pieces, three meanings.

| ev | -imiz | -de |
|---|---|---|
| house | our | in |

**Polysynthetic (Yupik)**: "We want to make a big house." The whole sentence is **one word**.

| Mangtegha | -ghlla | -ngllagh | -yug | -tu-kut |
|---|---|---|---|---|
| house | big | to make | to want | IND.INTR.1PL |
| house | big | make | want | we (statement) |

**Fusional (French)**: *était* "was" (from *Le sandwich que Sam a mangé était délicieux*, "The sandwich that Sam ate was delicious").

| ét- | -ait |
|---|---|
| be | 3SG.IMP |
| be | 3rd person + singular + imperfective, all fused into one ending |

**Analytic (English) vs. agglutinating (Turkish)**:

| Language | Form | Pieces |
|---|---|---|
| English | *in our house* | **3 separate words** |
| Turkish | *ev-imiz-de* | **1 word** (house + our + in) |

## Appendix topics
- **Reduplication**: repeat a root to change meaning. Often marks "distribution, plurality, repetition, customary activity, increase of size, added intensity, continuance" (Sapir 1921). Limited in English (*a red red rose*; "I'll bring the **salad salad**" = the prototypical salad), productive elsewhere (WALS feature 27A). **Iconic: "more is more."**
- **Compounds (Glass's research)**: a compound doesn't state how its **head** (main noun, usually last) and **modifier** relate. *water jug* = holds water; *water spinach* = grows in wet conditions (not really compositional).
  - **Artifact** heads (made by humans for a purpose, like *jug*) take modifiers about their **use/creation**.
  - **Natural-kind** heads (exist without humans, like *spinach*) take modifiers about **appearance, habitat, origin**, or borrowed ones (an attempt to capture the kind's "essence").
- **Pumpkin spice latte**: spice *for* pumpkin (pie), or spice *of* pumpkin? The compound doesn't say. Starbucks added real pumpkin after "shaming by the Food Babe," who missed the **morphological ambiguity**.
- **Adjectives as nouns (Glass's research)**: *The old are happier* (plural = **old people**) vs. *The old is never ordinary* (singular/mass = **oldness, old stuff**). The construction is very productive. Two readings, because a property can be construed as a **predicate of individuals** or as **the abstract thing those individuals share**.

---

# Unit 6 — Syntax

**Syntax** = the study of **word order**: which combinations of words are **grammatical** (possible) vs. **ungrammatical** (marked \*). Its rules let a **finite** set of words express **infinitely** many ideas.
- ✓ *The student read the book.* / ✗ \**Student the read book the.*
- ✓ *I threw the ball.* / ✗ \**The ball threw I.* / ✗ \**Her saw it.* (wrong case)

## Syntax vs. semantics

| Sentence | Grammatical? | Meaningful? |
|---|---|---|
| *Colorless green ideas sleep furiously* (Chomsky) | ✓ | ✗ |
| *Me love dog* / *Me eat cookie* | ✗ | ✓ (somewhat) |
| *?The toothbrush is pregnant* / *?The shoe poured the chair* | unclear | unclear |

So Chomsky argued **syntax and semantics are independent**. But where is the line between **ungrammatical** and **nonsensical**? There's no clear answer; it's as much theoretical as empirical.

## Syntactic facts about English (other languages differ!)
A **long-distance (non-local) dependency** = two words that belong together (e.g. a verb and its object) but are **separated** in the string. "___" marks the gap where the object "belongs."

| Sentence | Phenomenon |
|---|---|
| *The student read the book.* | declarative = **SVO** (Subject–Verb–Object) |
| *The book, the student read. The paper, she didn't.* | **object fronting**, only in **contrastive** contexts |
| *The clever student read the interesting book.* | **adjective before noun** |
| *Did the student read the book?* | **yes/no (polar) question**: **do-support** (*did* appears) + **inversion** (it goes to the front) |
| *Will the student read the book?* | **subject–auxiliary inversion** (existing auxiliary moves; no *do*) |
| *The student did not read the book.* | **negation** also uses do-support |
| *The student [who ___ read the book] is here.* | **subject relative clause** |
| *Who read the book?* | **subject wh-question** |
| *The book [that the student read ___] is on the table.* | **object relative clause**: long-distance dependency *read* ↔ *the book* |
| *What book did the student read ___?* | **object wh-question**: long-distance dependency *read* ↔ *what book* |
| *Which book did which student read ___?* | **multiple wh-question**: only one wh-phrase moves |

- Side note from the lecture: watch for **gender stereotypes in constructed example sentences**.

> [!warning] ⚠️ Agreement as a long-distance dependency
> *The **key** to the cabinets **is** on the table.* The verb agrees with the head noun ***key*** (singular), not the nearer *cabinets*, so ***key–is*** is a long-distance dependency across *to the cabinets*. Slips like "*...cabinets are*" show the dependency is non-local.

## Constituents
Words are **produced linearly** (one after another) but **mentally organized hierarchically** into chunks called **constituents**. In a tree, a constituent is any **subtree** (a set of words sharing a parent node).

**Constituency tests** (yes to any → it's a constituent):

| Test | Example |
|---|---|
| 1. **Can it answer a question?** | *Who begins the history of linguistics?* → "The Indian grammarian Panini." |
| 2. **Does it stick together when you reorder the sentence?** | "*The Indian grammarian Panini* begins *the history of linguistics*." |
| 3. **Can it be conjoined** with something else? | "*The history of linguistics*, and *scholarship on Sanskrit*, begins with..." |

| Sentence | ✓ Constituents | ✗ Not constituents |
|---|---|---|
| *The history of linguistics begins with the Indian grammarian Panini* | *the history of linguistics*, *of linguistics*, *linguistics*, *the Indian grammarian Panini*, *begins with the Indian grammarian Panini* | *linguistics begins with the*, *of linguistics begins with*, *begins with the Indian* |
| *The athlete tossed the ball* | *the athlete*, *the ball*, *tossed the ball* | *the athlete tossed*, *athlete tossed the*, *tossed the* |

## Lexical vs. phrasal categories

| | Lexical | Phrasal |
|---|---|---|
| Level | single word | phrase |
| Examples | Det, N, Adj, TransV, IntransV, Prep | **NP** = noun phrase (*every book, the red ball, two people*), **VP** = verb phrase (*ran, threw the ball*; may contain an NP), **AdjP** (*very tall, oddly funny*) |
| Determines | a **word's** distribution | a **phrase's** distribution |
| "Mad Libs" swap | another noun for *student*, another transitive verb for *read* | another NP for *the student*, another VP for *read the book* |

## Phrase Structure Grammar (Chomsky, ~1950s)
Goals:
1. capture the implicit **generative rules** that let us make and understand brand-new sentences
2. capture both **hierarchical structure** and **linear word order**
3. capture **grammaticality judgments** (which sentences are/aren't allowed)

Illustrated with a **grammar fragment** (a small toy model). **Rules** build the category nodes (**non-terminal** nodes); the **lexicon** supplies the words at the bottom (**terminal** nodes).

| Rule | Reads as |
|---|---|
| `S -> NP VP` | a sentence = noun phrase + verb phrase |
| `NP -> (Det) (Adj*) N` | optional determiner, any number of adjectives, then a noun |
| `NP -> NP (PP)` | a noun phrase, optionally followed by a prepositional phrase (recursive) |
| `PP -> Prep NP` | preposition + noun phrase |
| `NP -> Pronoun` | a pronoun alone |
| `VP -> TransV NP` | transitive verb + its object |
| `VP -> IntransV` | intransitive verb alone |
| `VP -> VP PP` | a verb phrase plus a prepositional phrase (recursive) |

| Lexicon category | Words |
|---|---|
| Det | *the, every, a, some* |
| N | *student, book, forest, reindeer, lunch, evening, game* |
| TransV | *throw, want, love, kick, eat, play* |
| IntransV | *swim, run, laugh, eat, dance* (*eat* is in both verb lists) |
| Adj | *red, blue, beautiful, interesting, tall* |
| Pronoun | *you, she, he, I, we, they* |
| Prep | *in, from, of* |

Notation: `( )` = optional, `*` = zero or more. Draw trees with mshang.ca/syntree, LaTeX/Overleaf, or by hand.

**Practice:**
- *Some reindeer eat lunch* = [S [NP [Det some] [N reindeer]] [VP [TransV eat] [NP [N lunch]]]]
- *Many beautiful reindeer dance in the evening* (treat *many* as Det):

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cred}{RGB}{200,40,40}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.3cm,
  cat/.style={text=cblu,font=\large\bfseries},
  wd/.style={text=cred,font=\large\itshape},
  edge from parent/.style={draw,thick},
  level 1/.style={sibling distance=7cm},
  level 2/.style={sibling distance=3.2cm},
  level 3/.style={sibling distance=2.4cm},
  level 4/.style={sibling distance=1.7cm}]
\node[cat] {S}
  child {node[cat] {NP}
    child {node[cat] {Det} child {node[wd] {many}}}
    child {node[cat] {Adj} child {node[wd] {beautiful}}}
    child {node[cat] {N} child {node[wd] {reindeer}}}}
  child {node[cat] {VP}
    child {node[cat] {VP} child {node[cat] {IntransV} child {node[wd] {dance}}}}
    child {node[cat] {PP}
      child {node[cat] {Prep} child {node[wd] {in}}}
      child {node[cat] {NP}
        child {node[cat] {Det} child {node[wd] {the}}}
        child {node[cat] {N} child {node[wd] {evening}}}}}};
\end{tikzpicture}
\end{document}
```

**Lecture quiz, *The author wrote the book*: which tree is right?**

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\definecolor{cred}{RGB}{200,40,40}
\begin{document}
\begin{tikzpicture}[font=\normalsize, level distance=1.1cm,
  cat/.style={text=cblu,font=\bfseries},
  wd/.style={text=cgrn,font=\itshape},
  edge from parent/.style={draw,thick}]
\begin{scope}[level 1/.style={sibling distance=3cm}, level 2/.style={sibling distance=1.4cm}]
\node[cat] at (0,0) {S}
  child {node[cat] {NP} child {node[cat] {Det} child {node[wd] {The}}} child {node[cat] {N} child {node[wd] {author}}}}
  child {node[cat] {VP} child {node[cat] {V} child {node[wd] {wrote}}} child {node[cat] {Det} child {node[wd] {the}}}}
  child {node[cat] {NP} child {node[cat] {N} child {node[wd] {book}}}};
\node[cred] at (0,-4.1) {Tree A: \textbf{wrong} (\emph{the} split from \emph{book})};
\end{scope}
\begin{scope}[level 1/.style={sibling distance=3.4cm}, level 2/.style={sibling distance=1.4cm}]
\node[cat] at (9,0) {S}
  child {node[cat] {S} child {node[cat] {Det} child {node[wd] {The}}} child {node[cat] {N} child {node[wd] {author}}} child {node[cat] {V} child {node[wd] {wrote}}}}
  child {node[cat] {NP} child {node[cat] {Det} child {node[wd] {the}}} child {node[cat] {N} child {node[wd] {book}}}};
\node[cred] at (9,-4.1) {Tree B: \textbf{wrong} (no subject NP, no VP)};
\end{scope}
\begin{scope}[level 1/.style={sibling distance=1.4cm}]
\node[cat] at (0,-5.5) {S}
  child {node[cat] {Det} child {node[wd] {The}}}
  child {node[cat] {N} child {node[wd] {author}}}
  child {node[cat] {V} child {node[wd] {wrote}}}
  child {node[cat] {Det} child {node[wd] {the}}}
  child {node[cat] {N} child {node[wd] {book}}};
\node[cred] at (0,-8.4) {Tree C: \textbf{wrong} (flat: no constituents)};
\end{scope}
\begin{scope}[level 1/.style={sibling distance=3cm}, level 2/.style={sibling distance=1.6cm}, level 3/.style={sibling distance=1.4cm}]
\node[cat] at (9,-5.5) {S}
  child {node[cat] {NP} child {node[cat] {Det} child {node[wd] {The}}} child {node[cat] {N} child {node[wd] {author}}}}
  child {node[cat] {VP} child {node[cat] {V} child {node[wd] {wrote}}}
    child {node[cat] {NP} child {node[cat] {Det} child {node[wd] {the}}} child {node[cat] {N} child {node[wd] {book}}}}};
\node[cgrn] at (9,-10.4) {Tree D: \textbf{right} (S $\to$ NP VP; VP $\to$ V NP)};
\end{scope}
\end{tikzpicture}
\end{document}
```

To check a tree, ask: does every real constituent (*the author, the book, wrote the book*) get its own node? Only **D** passes.

### Properties of PS rules

| Property | Meaning | Example |
|---|---|---|
| **Generative** | produce all (and only) the grammatical sentences, including new ones | |
| **One-to-many** | **one left side → several right sides** | **VP → V NP *and* VP → V** |
| **Recursive** | a rule can invoke itself → no longest sentence (infinite generative capacity) | NP → NP PP, PP → P NP (*the book of the student in the forest of...*) |
| **Language-specific** | they **must** be, because they encode **word order**, which varies | English Adj before N; French mostly after |

⚠️ PS rules are **not** language-general, **not** "binary, asymmetric, typed" (that's dependency grammar), **not** "cancelable" (that's implicatures), **not** "inflectional" (that's morphology). *NP → NP PP; PP → P NP* illustrates **recursion**, not one-to-many.

## Transformations / movement
PS rules only build local structure, so **long-distance dependencies** need extra rules: **transformations** or **movement** (a metaphor; it needn't be taken literally).
- *What did you eat ___?*: *what* sits at the front but is conceptually the **direct object of *eat***.
- *The book that I read ___ is on the table*: *the book* is the **subject** of *is* but also the **object of *read***.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\definecolor{cgry}{RGB}{130,130,130}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.25cm,
  cat/.style={text=cblu,font=\large\bfseries},
  wd/.style={text=cgrn,font=\large\itshape},
  edge from parent/.style={draw,thick},
  level 1/.style={sibling distance=3.2cm},
  level 2/.style={sibling distance=2cm},
  level 3/.style={sibling distance=1.7cm},
  level 4/.style={sibling distance=1.3cm}]
\node[cat] {CP}
  child {node[cat] {C} child {node[wd] (what) {What}}}
  child {node[cat] {C$'$}
    child {node[cat] {C} child {node[wd] {did}}}
    child {node[cat] {S}
      child {node[cat] {NP} child {node[wd] {you}}}
      child {node[cat] {VP}
        child {node[wd] {eat}}
        child {node[cat] {NP} child {node[text=cgry] (gap) {\_\_\_ (what)}}}}}};
\draw[-{Stealth[length=3mm]},dashed,very thick,cgry] (gap.south) .. controls +(-2,-1.5) and +(0,-3) .. (what.south) node[pos=0.35,below left,font=\normalsize] {movement};
\end{tikzpicture}
\end{document}
```

(CP = the layer above S that holds the fronted wh-word and the inverted *did*.)

## Dependency grammar
Used in **NLP** (natural language processing); demos: Stanford CoreNLP (corenlp.run), spaCy displaCy.
- **Origin**: French linguist **Lucien Tesnière**, inspired by **Latin and Slavic**, which have **free word order** and mark each noun's role with **case**.
- **Example**: *Puella canem amat / Canem puella amat / Amat puella canem* all mean "The girl loves the dog" (*puella* = girl.NOM, *canem* = dog.ACC, *amat* = loves). The order is chosen by discourse factors (**given before new**), so these languages need a framework that allows that flexibility.
- **Definition**: syntax as **binary, asymmetric, typed** relations between pairs of **POS-tagged** words. In each relation, the **head** is the word that governs, and the **dependent** is the word that attaches to it (an arrow points from head to dependent).

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgry}{RGB}{110,110,110}
\begin{document}
\newcommand{\dep}[4]{\draw[-{Stealth[length=2.2mm]},thick] (#1.north) .. controls +(0,#3) and +(0,#3) .. node[pos=0.5,above,font=\small\bfseries,text=cblu]{#4} (#2.north);}
\begin{tikzpicture}[font=\large]
\node (w1) at (0,0) {The}; \node[cgry,font=\small] at (0,-0.6) {DT};
\node (w2) at (2.2,0) {reindeer}; \node[cgry,font=\small] at (2.2,-0.6) {NN};
\node (w3) at (4.6,0) {played}; \node[cgry,font=\small] at (4.6,-0.6) {VBD};
\node (w4) at (6.8,0) {games}; \node[cgry,font=\small] at (6.8,-0.6) {NNS};
\dep{w2}{w1}{0.9}{DET}
\dep{w3}{w2}{1.2}{NSUBJ}
\dep{w3}{w4}{1.0}{OBJ}
\draw[-{Stealth[length=2.2mm]},thick] (4.6,2.3) node[above,font=\small\bfseries,text=cblu] {ROOT} -- (w3.north);
\end{tikzpicture}
\end{document}
```

(Phrase-structure version of the same sentence: [S [NP the reindeer] [VP played [NP games]]].)

| Property | In the graph above |
|---|---|
| **POS-tagged** | each word auto-labeled: DT determiner, NN noun, VBD past verb, NNS plural noun |
| **Binary** | each relation links **2 words** |
| **Asymmetric** | arrows have direction: *reindeer* is NSUBJ of *played*, not vice versa |
| **Typed** | each arc has a type: NSUBJ (subject) ≠ OBJ/DOBJ (object) |

The **verb is the root**: it depends on nothing. Syntactically, it determines **how many nouns** the sentence has; semantically, it describes the **main event** the nouns take part in.

### Advantages
1. **Works for any language and any word order**: the same relations hold; only the arc directions change. That's why it's used for **consistent cross-linguistic representations**: NLP tools for many languages, comparative syntax, and **Universal Dependencies** (Stanford; treebanks in **100+ languages**).

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\begin{document}
\newcommand{\dep}[4]{\draw[-{Stealth[length=2.2mm]},thick] (#1.north) .. controls +(0,#3) and +(0,#3) .. node[pos=0.5,above,font=\small\bfseries,text=cblu]{#4} (#2.north);}
\begin{tikzpicture}[font=\large]
\node (a1) at (0,0) {Puella}; \node (a2) at (2.2,0) {canem}; \node (a3) at (4.4,0) {amat.};
\dep{a3}{a2}{0.7}{OBJ}
\dep{a3}{a1}{2.2}{NSUBJ}
\node (b1) at (8,0) {Amat}; \node (b2) at (10.2,0) {puella}; \node (b3) at (12.4,0) {canem.};
\dep{b1}{b2}{0.7}{NSUBJ}
\dep{b1}{b3}{2.2}{OBJ}
\node[font=\small] at (2.2,-0.7) {girl.NOM \ dog.ACC \ loves};
\node[font=\small] at (10.2,-0.7) {loves \ girl.NOM \ dog.ACC};
\end{tikzpicture}
\end{document}
```

2. **Based on words** (*eat*), not phrases ("VP"), so there are **fewer invisible abstractions** and it stays closer to the text.
3. **No special rules for long-distance dependencies**: just draw a **longer arc**.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgry}{RGB}{110,110,110}
\begin{document}
\newcommand{\dep}[4]{\draw[-{Stealth[length=2.2mm]},thick] (#1.north) .. controls +(0,#3) and +(0,#3) .. node[pos=0.5,above,font=\small\bfseries,text=cblu]{#4} (#2.north);}
\begin{tikzpicture}[font=\large]
\node (w1) at (0,0) {What}; \node[cgry,font=\small] at (0,-0.6) {WP};
\node (w2) at (1.8,0) {did}; \node[cgry,font=\small] at (1.8,-0.6) {VBD};
\node (w3) at (3.4,0) {you}; \node[cgry,font=\small] at (3.4,-0.6) {PRP};
\node (w4) at (5,0) {eat}; \node[cgry,font=\small] at (5,-0.6) {VB};
\node (w5) at (7.2,0) {?}; \node[cgry,font=\small] at (7.2,-0.6) {.};
\dep{w4}{w3}{0.9}{NSUBJ}
\dep{w4}{w2}{1.8}{AUX}
\dep{w4}{w1}{2.8}{OBJ}
\dep{w4}{w5}{0.4}{PUNCT}
\end{tikzpicture}
\end{document}
```

4. **Shows that language is efficient.** **Dependency length** = how many words an arc spans. In parsed corpora (newspapers, etc.) across **37 languages**, **short dependencies are more common than random word order would predict**.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cred}{RGB}{200,40,40}
\begin{document}
\newcommand{\dep}[4]{\draw[-{Stealth[length=2mm]},thick] (#1.north) .. controls +(0,#3) and +(0,#3) .. node[pos=0.5,above,font=\small]{#4} (#2.north);}
\begin{tikzpicture}[font=\normalsize]
\foreach \i/\w in {1/John,2/threw,3/out,4/the,5/old,6/trash,7/sitting,8/in,9/the,10/kitchen}
  \node (c\i) at (\i*1.5,0) {\w};
\dep{c2}{c1}{0.6}{1} \dep{c2}{c3}{0.6}{1} \dep{c2}{c6}{2.2}{4}
\dep{c6}{c4}{1.2}{2} \dep{c6}{c5}{0.6}{1} \dep{c6}{c7}{0.6}{1}
\dep{c7}{c8}{0.6}{1} \dep{c8}{c10}{1.2}{2} \dep{c10}{c9}{0.6}{1}
\node[anchor=west] at (1,-0.8) {\textbf{C}: total dependency length = 1+1+4+2+1+1+1+2+1 = \textbf{14}};
\begin{scope}[yshift=-5cm]
\foreach \i/\w in {1/John,2/threw,3/the,4/old,5/trash,6/sitting,7/in,8/the,9/kitchen,10/out}
  \node (d\i) at (\i*1.5,0) {\w};
\dep{d2}{d1}{0.6}{1} \dep{d2}{d5}{1.8}{3}
\dep{d5}{d3}{1.2}{2} \dep{d5}{d4}{0.6}{1} \dep{d5}{d6}{0.6}{1}
\dep{d6}{d7}{0.6}{1} \dep{d7}{d9}{1.2}{2} \dep{d9}{d8}{0.6}{1}
\draw[-{Stealth[length=2mm]},thick,cred] (d2.north) .. controls +(0,3.6) and +(0,3.6) .. node[pos=0.5,above,font=\small]{8} (d10.north);
\node[anchor=west] at (1,-0.8) {\textbf{D}: total = 1+3+2+1+1+1+2+1+\textcolor{cred}{8} = \textbf{20} (worse: \emph{out} far from \emph{threw})};
\end{scope}
\end{tikzpicture}
\end{document}
```

### Phrase structure vs. dependency grammar

| | Phrase Structure | Dependency |
|---|---|---|
| Who | Chomsky | Tesnière |
| Units | phrases (abstract NP/VP nodes) | words + labeled arcs |
| Word order of a specific language | **captured** (language-specific rules) | **not captured** (works for any language) |
| Grammaticality judgments / rules for building sentences | **captured** | **not captured** |
| Long-distance dependencies | need **movement** | just a **longer arc** |
| Main use | theoretical syntax | **NLP**, cross-linguistic corpora |

## Ambiguity headlines

| Type | Headline | Reading 1 | Reading 2 |
|---|---|---|---|
| **Structural** (two trees) | *Pope's Baby Steps on Gays* | [Pope's baby] **steps on** gays | [Pope's **baby steps**] on gays |
| Structural | *MBA Studies Mushroom* | MBA studies **grow fast** | an MBA **studies a mushroom** |
| Structural | *Complaints about referees growing ugly* | the **complaints** grow ugly | the **referees** grow ugly |
| Structural | *Lawyers give poor free legal advice* | advice to **poor people** | **low-quality** advice |
| Structural | *Hospital sued by 7 foot doctors* | 7 **podiatrists** | doctors who are **7 feet tall** |
| Structural | *Time for football and meatball stew* | football, and meatball stew | a **football-and-meatball** stew |
| **Lexical** (word senses) | *Iraqi **Head** Seeks **Arms*** | leader seeks weapons | a head seeks limbs |
| **Event participation** (one structure, one sense per word) | *Pillars replaced by alumni* | alumni **funded** the replacement | alumni **are** the new pillars |
| Event participation | *Include your children when baking cookies* | as helpers | as **ingredients** |
| Event participation | *Kids make nutritious snacks* | kids **prepare** snacks | kids **are** snacks |
| Event participation | *Stolen painting found by tree* | found **near** a tree | a tree **found** it |

## Syntactic fieldwork
Elicit these from a speaker of another language: *Sam ate a sandwich. / Sam did not eat a sandwich. / Sam ate a delicious sandwich. / Did Sam eat a sandwich? / What did Sam eat? / The sandwich that Sam ate was delicious.*

| Question to answer | Mandarin | French |
|---|---|---|
| Basic word order | SVO | SVO (auxiliary + participle: *a mangé*) |
| Adj–N order | Adj **before** N, with *de* (*hǎo-chī de sāmíngzhì*) | Adj **after** N (*sandwich délicieux*) |
| Negation | *méi-yǒu* before the verb | *ne…pas* around the auxiliary |
| Past | **no tense**: aspect marker *le* | *avoir* + participle; *était* (imperfective "was") |
| Determiners | **none**; *yí-gè* "one-CL" | yes: *un, le* (gendered) |
| Polar question | particle ***ma*** at the end, no reordering | ***est-ce que*** at the front |
| Wh-question | *shénme* "what" **stays in place** | wh-word **fronted** (*qu'est-ce que*) |
| Relative clause | **before** the noun, with *de* | **after** the noun, with *que* |

> [!example]- Full glossed data: Mandarin
> DE = a linking particle (other labels: see the gloss table under Morphological typology).
>
> | English | Mandarin | Word-by-word |
> |---|---|---|
> | Sam ate a sandwich. | *Sàmǔ chī le yí-gè sāmíngzhì* | Sam · eat · ASP · one-CL · sandwich |
> | Sam did not eat a sandwich. | *Sàmǔ méi-yǒu chī yí-gè sāmíngzhì* | Sam · not-have · eat · one-CL · sandwich |
> | Sam ate a delicious sandwich. | *Sàmǔ chī le yí-gè hǎo-chī de sāmíngzhì* | Sam · eat · ASP · one-CL · good-eat · DE · sandwich |
> | Did Sam eat a sandwich? | *Sàmǔ chī le yí-gè sāmíngzhì ma?* | Sam · eat · ASP · one-CL · sandwich · QUESTION |
> | What did Sam eat? | *Sàmǔ chī le shénme?* | Sam · eat · ASP · what |
> | The sandwich that Sam ate was delicious. | *Sàmǔ chī le de sāmíngzhì shì hǎo-chī de* | Sam · eat · ASP · DE · sandwich · is · good-eat · DE |

> [!example]- Full glossed data: French
> | English | French | Word-by-word |
> |---|---|---|
> | Sam ate a sandwich. | *Sam a mangé un sandwich* | Sam · has · eaten · a · sandwich |
> | Sam did not eat a sandwich. | *Sam n'a pas mangé un sandwich* | Sam · NEG-has · not · eaten · a · sandwich |
> | Sam ate a delicious sandwich. | *Sam a mangé un sandwich délicieux* | Sam · has · eaten · a · sandwich · delicious |
> | Did Sam eat a sandwich? | *Est-ce que Sam a mangé un sandwich?* | is-it · that · Sam · has · eaten · a · sandwich |
> | What did Sam eat? | *Qu'est-ce que Sam a mangé?* | what-is-it · that · Sam · has · eaten |
> | The sandwich that Sam ate was delicious. | *Le sandwich que Sam a mangé était délicieux* | the.MASC.SG · sandwich · which · Sam · have.3SG.PRES · eaten · be.3SG.IMP · delicious.MASC.SG |

**Methods questions:**
- How many examples should be elicited per phenomenon?
- Should the speaker help with the analysis, or only provide data?
- Spoken, written (in which writing system?), or glossed?
- What language are the questions asked in?
- How do you know the speaker is answering the question the way the researcher intends?

**Ethics: "giving back."** This matters especially when a researcher takes data from a **minoritized community**, then publishes in **paywalled journals** for tenure. Ways to give back:
- partner with the community on **children's books, educational materials, accessible digital archives, writing systems, dictionaries**
- **documentaries** in the community's own voice (*Talking Black in America*, NC State)
- widen access to community-engaged linguistics (**MIT Indigenous Language program**)

**Unit review list**: English syntactic phenomena (cross-linguistically) · constituency tests · PS rules · dependency grammar · fieldwork (methods + ethics) · glossed examples · syntax vs. semantics.

---

# Unit 7 — Semantics

| Field | Studies |
|---|---|
| **Semantics** | meaning and the inferences drawn from morphemes, words, sentences, discourses (mostly **words and sentences**) |
| **Pragmatics** (next unit) | inferences drawn from **utterances** by **people in context** |

David Lewis (1972): to say what a meaning *is*, first ask what a meaning *does*.

If you know a **word's** meaning, you can:
1. identify its **referent** (the thing it picks out): *cat* → a furry feline; *unicorn* → a fictional horned horse (no real referent, still meaningful)
2. reason about its **relations** to other words: a cat is an **animal**; a cat is **not** a dog
3. use it in a sentence and know what it contributes

If you know a **sentence's** meaning, you can:
1. know its **truth conditions**: what the world must be like for it to be true (*Alice has a cat / a unicorn*)
2. reason about its relations to other sentences: *Alice has a cat* **entails** *Alice has a pet* (if the first is true, the second must be) and **contradicts** *Alice has no pets* (both can't be true)
3. know what it contributes to a discourse

| Branch | Studies | Examples |
|---|---|---|
| **Lexical semantics** | meaning of **open-class content words**; how nouns/verbs/adjectives differ in grammar and in the inferences they license | *cat, smile, beautiful* |
| **Compositional semantics** | meaning of **closed-class function words**; how word meanings **combine into sentence meanings** | *the, a, every, for, with, can, should, must* |

## Relations between words

| Relation | Meaning | Examples |
|---|---|---|
| **Synonyms** | same meaning | *couch/sofa, pretty/beautiful* |
| **Antonyms** | opposites; **mostly adjectives** (gradable scales have two ends) | *beautiful/ugly, tall/short* |
| **Homonyms** | **unrelated** meanings, **accidentally** same form; **not** expected to recur in other languages | *bank/bank*, *for/four* |
| **Polysemy** | **related** meanings; **potentially systematic**, **may recur** across languages | *head*, *dinner*, *book* (see below) |

Polysemy examples (one word, two related senses):

| Word | Sense 1 | Sense 2 |
|---|---|---|
| *head* | *my head* (body part) | *the head of the school* (leader) |
| *dinner* | *the dinner was delicious* (food) | *the dinner took two hours* (event) |
| *book* | *the book is heavy* (physical object) | *the book is interesting* (content) |
| *White House* | *the White House is in DC* (building) | *the White House knew about the meeting* (staff) |
| *mouse* | *Mickey mouse* (animal) | *computer mouse* (device) |
| ⚠️ *lamb* | the living animal | the meat (the same pattern recurs with *chicken, fish*, and in other languages) |

**Marked vs. unmarked antonyms:**

| Member | Examples | Effect |
|---|---|---|
| **Unmarked** (*tall*) | *How tall is she?*; *5 ft tall* ✓ | neutral; names the whole scale |
| **Marked** (*short*) | *How short is she?*; *?5 ft short* | carries extra meaning: assumes she's short |

## Lexical categories, semantically
- Do all languages have nouns, verbs, adjectives? How would we know (by syntax and morphology)?
- Some languages have **few adjectives**: English *I am hungry* (Adj) vs. French *J'ai faim* "I have hunger" (noun). Some languages do this for nearly all adjective-type concepts.
- Some languages (**Persian**) have **few verbs**: they use a **light verb** + a noun ("I did a shower / did a run / did a laugh").
- Which concepts become nouns, verbs, adjectives? Is there a language where *rice* or *joy* is a verb/adjective, or where *throw* is a noun?

⚠️ **The most astonishing gap would be a language without nouns.** Lacking tense (Mandarin), a word for "the" (Mandarin), or "purple" is common.

## Who decides what words mean?

| Word | Debated question | Who decides |
|---|---|---|
| *quark* | Is an electron a quark? (no) | **experts** |
| *carbohydrate* | Is butter a carb? (no) | **experts** |
| *whale* | Are orcas whales? | **experts** |
| ⚠️ *polygon* | Is a spiral a polygon? (no: polygons have straight, connected sides by definition) | **experts** |
| *soup* | Is cereal soup? | **everyone** |
| *sandwich* | Is a burrito a sandwich? | **everyone**, and courts (below) |
| *champagne* | Is all sparkling white wine champagne? | **everyone** |
| *woman* | Who counts? (Why is this asked less of *man*?) | **everyone** |
| *person* | Is a fetus a person? | **everyone** |
| *planet* | Used to cover all celestial bodies, including the sun and moon | changed with astrophysics |

**Burrito court case** (the slide cites *Quintana v. Fort Wayne Plan Commission*): Panera's mall lease banned rival **sandwich** shops, and Panera argued that Qdoba (burritos) couldn't open there.

**Words are tools to pick out meaningful categories**, and those categories can **change over time** and be **socially contentious**.
- Discussion prompt: find a social/political debate that hinges on a word's meaning. Do the people involved realize they're arguing about word meaning? How would reframing it change the debate?

**Wittgenstein on *game***: board games, card games, ball games, the Olympic games share no single common feature, only **"family resemblances"**: overlapping similarities, like how family members share build, eyes, or gait in criss-crossing ways. So **words don't all have strict boundaries**. This is related to, but distinct from, "who decides."
- Problem for law and policy: is a **borderline ovarian tumor** "cancer"? That can decide **life-insurance eligibility** or **public benefits**. Even **oncologists disagree** (work by **Jessica Rett**).

**Labov's cups**: people named drawings of containers that varied gradually in width, height, handles, and stems (cup / mug / bowl / vase...). Category **boundaries are fuzzy and gradient**.

## Distinctions among nouns

| Term | Definition | Examples / tests |
|---|---|---|
| **Relational** noun | needs a relatum (someone it's related to) | *sister*; *the sister of my friend* ✓; *A man walked in. His sister was with him* ✓ |
| **Sortal** noun | just names a kind | *sheep*; *?the sheep of my friend*; *?His sheep was with him* |
| **Count** noun | countable units | *so many books, two books, so many letters, so many apples* |
| **Mass** noun | stuff, not counted | *so much water, ?two waters, so much mail, so much apple* |

- The same stuff can be either: *letters* (count) vs. *mail* (mass).
- ***Furniture* is mass** (\**two furnitures*). Who has "more furniture," a table + a sofa or 3 little stools? People usually say **3 stools**: they count **pieces**, not volume.

| | Artifact | Natural kind |
|---|---|---|
| Definition | made by humans **for a purpose** | exists **independently of humans** |
| What makes something one? | its **function** (anything that staples = a stapler) | its **essence** (genetics makes a bear) |
| *start a ___* | *start a book* = start reading/writing it | *start a bear* = ?? |
| *my ___* | *my book* = the one I'm reading/writing | *my bear* = pet? study subject? |

So ***finish a sandwich*** = finish **making/eating** it: a sandwich is an **artifact**, so we infer the conventional ways of interacting with it. (No hidden *make/eat* sits in the tree or dependency graph.)

## Distinctions among verbs

| Term | Definition | Example |
|---|---|---|
| **Dynamic** | something happens/changes | *Alice threw the ball* |
| **Stative** | a state holds, no change | *Alice loved movies* |
| **Agentive** | the subject acts deliberately | *Alice ran*; *Alice sat on the chair* |
| **Non-agentive** | no intention | *Alice fell*; *The book sat on the table* |
| **Telic** | has a **built-in endpoint** (Greek *telos* = goal); takes "**in** X time" | *Alice ate **the** pizza **in** ten minutes* (done when the pizza is gone) |
| **Atelic** | no natural endpoint; takes "**for** X time" | *Alice ate pizza **for** ten minutes*; ***I watched TV*** |
| **Causative** | entails the object changes state | *The child **broke** the fence* → *The fence broke* ✓ |
| **Non-causative** | no change entailed | *The child **hit** the fence* → *?The fence hit* |

- *I did my homework **in** half an hour* = finished it; ***for** half an hour* = worked on it, maybe not finished.
- **Aspect orders events in a story**:
  - *Alice walked in. The book sat on the table.* → the book was **already there** (stative, overlaps in time).
  - *Alice walked in. The president sat down.* → he sat down **afterward** (event, in sequence).
- **Argument structure** = how many arguments a verb takes, and what role each plays:
  - *The submarine sank the ship* / *The ship sank*: the ship is the thing that **changes** in both.
  - *The athlete lifted the weight* / *The athlete lifted*: the athlete is still the **lifter**; the object is just left implicit.
  - Same "drop the object" surface pattern, different roles.

## Distinctions among adjectives

| Term | Definition | Examples |
|---|---|---|
| **Gradable** | allows degrees | *very tall, taller* |
| **Non-gradable** | either is or isn't | *?very dead, ?deader* |
| **Vague** | what counts depends on the comparison class | *expensive* coffee vs. car; *tall* man vs. building |
| **Objective** | if two people disagree, someone is wrong | *red, plastic, heavy* |
| **Subjective** | two people can disagree with neither wrong: **faultless disagreement** | *beautiful, cute, fun*. Prototype: ***"Roller coasters are fun."*** |

Test for subjectivity: A: *The box is {red / plastic / heavy / beautiful}.* B: *No it's not.* Is someone wrong?

- **Adjective ordering (Scontras et al. 2017)**: **more subjective adjectives go further from the noun**: *heavy red box* (not *?red heavy*), *beautiful wooden chair*, *cute red dress*. Confirmed in **corpora**, using human ratings of how subjective each adjective is.
- **Subjective adjectives prefer predicate position (Glass 2025)**: *The red dress is cute*, not *The cute dress is red*.

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{corg}{RGB}{220,110,20}
\begin{document}
\begin{tikzpicture}[font=\normalsize]
\begin{scope}
\fill[corg!35] (0,0) circle (1.3);
\fill[cblu!25] (1.5,0) circle (1.3);
\begin{scope}\clip (0,0) circle (1.3); \fill[green!50!black,opacity=0.55] (1.5,0) circle (1.3); \end{scope}
\draw[thick] (0,0) circle (1.3) (1.5,0) circle (1.3);
\node at (-0.5,1.6) {Swedish};
\node at (2,1.6) {musicians};
\node[align=center,font=\small] at (0.75,-1.9) {\textbf{intersective}: \emph{Swedish musician}\\= Swedish $\cap$ musician};
\end{scope}
\begin{scope}[xshift=6cm]
\fill[cblu!25] (0,0) circle (1.4);
\fill[green!50!black,opacity=0.55] (0.2,-0.2) circle (0.7);
\draw[thick] (0,0) circle (1.4) (0.2,-0.2) circle (0.7);
\node at (0,1.7) {musicians};
\node[font=\small,text=white] at (0.2,-0.2) {skillful};
\node[align=center,font=\small] at (0,-2) {\textbf{subsective}: \emph{skillful musician}\\$\subset$ musicians (skillful \emph{as} a musician)};
\end{scope}
\begin{scope}[xshift=11.5cm]
\fill[cblu!25] (0,0) circle (1.2);
\fill[green!50!black,opacity=0.55] (2.3,0) circle (0.8);
\draw[thick] (0,0) circle (1.2) (2.3,0) circle (0.8);
\node at (0,1.5) {musicians};
\node[font=\small] at (2.3,1.1) {former m.};
\node[align=center,font=\small] at (1,-2) {\textbf{privative}: \emph{former musician}\\is \textbf{not} a musician};
\end{scope}
\end{tikzpicture}
\end{document}
```

| Type | Rule | Examples |
|---|---|---|
| **Intersective** | Adj N = Adj things ∩ N things | *Swedish musician*, ***American*** |
| **Subsective** | Adj N ⊂ N, but not simply "Adj things" (a skillful musician isn't necessarily a skillful chef) | *skillful musician*, *important* |
| **Privative** | Adj N is **not** an N | *former musician*, *fake* |
| **Plastic** (??) | depends on the noun: *plastic chair* is a chair; *plastic flower* isn't a real flower | |

## Other word types

| Type | What it does | Examples |
|---|---|---|
| **Deixis** ("pointing," like the index finger) | referent depends on **who is speaking, when, and where** | *I, you, me, today, tomorrow, yesterday, here, now*. **Not** deictic: *beautiful* |
| **Expressives** | **same truth conditions**, plus the speaker's **emotional attitude** | *I lost my **damn** keys* vs. *I lost my keys* |
| **Slurs** | same descriptive content, plus a **derogatory attitude toward the group** | *Hermione is a **mudblood*** vs. *Hermione is from a non-wizard family* |

## Metaphor (Lakoff & Johnson 1980)
*Metaphors We Live By*: metaphors are **not decorative flourishes** (and not mainly literary); they're **fundamental to how we think**. We understand the **abstract** through the **concrete**. Each conceptual metaphor is named in the form *target is source*.

| Conceptual metaphor | Everyday expressions |
|---|---|
| Time is money | ***spent** an hour, **wasted** time* |
| Time is space | *move the meeting **up**, **back-to-back** meetings* |
| Good is up | ***higher**-level class, **raise** morale, **elevate** your style* |
| Understanding is vision | ***crystal-clear** speaker, I **see** your point, still **murky*** |
| Arguments are wars | ***cede/defend** a claim, **win** the argument* |
| Projects are meals/cooking | ***meaty** paper, **half-baked** idea, **back burner*** |
| Projects/ideas are buildings | ***laying the foundation, buttressing, supporting** a claim* |

**Language change runs concrete → abstract**: *You are **standing** on the floor* (concrete) → *What I said still **stands*** (abstract). The **Database of Semantic Shifts** (datsemshift.ru) catalogs many such shifts.

> [!warning] ⚠️ Metaphor vs. simile vs. allegory
> | Term | Definition | Example |
> |---|---|---|
> | **Metaphor** | understanding X **as** Y, with no "like" | *This is a **heavy** topic* (physical weight = seriousness) |
> | **Simile** | an explicit comparison **with "like" or "as"** | *a topic like a heavy rock* |
> | **Allegory** | a whole story whose parts stand for abstract ideas | *Animal Farm*: a story about farm animals overthrowing their farmer stands for the Russian Revolution |
>
> *"Morale is **low** because we've been **wasting** time **battling** silly problems"* uses **all of these**: *good is up*, *time is money*, *arguments are wars*.

## Compositional semantics
**Typed lambda calculus** treats word meanings as **functions** (machines that take an input and give an output).

| Type | Meaning | Example |
|---|---|---|
| ***e*** | an individual (entity) | *Lelia* |
| ***t*** | a truth value (true or false) | a whole sentence |
| ⟨*e,t*⟩ | a function from individuals to truth values | an intransitive verb like *swims* |

```tikz
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\begin{document}
\begin{tikzpicture}[font=\large, level distance=1.6cm,
  edge from parent/.style={draw,thick},
  level 1/.style={sibling distance=5cm}]
\node[align=center] {\textbf{S}\\\textcolor{cgrn}{swim(\textbf{Lelia})} : $t$}
  child {node[align=center] {\textbf{NP} (PropN)\\\textcolor{cgrn}{\textbf{Lelia}} : $e$}}
  child {node[align=center] {\textbf{VP} (V)\\\textcolor{cgrn}{$\lambda x\,[\mathrm{swim}(x)]$} : $\langle e,t\rangle$}};
\node[align=left,font=\normalsize] at (0,-4.2) {
1. $[\![\mathit{swim}]\!] = \lambda x[\mathrm{swim}(x)]$: takes an individual $x$, gives true if $x$ swims, false otherwise\\
2. $[\![\mathit{Lelia}]\!] = \textbf{Lelia}$: an individual\\
3. Combine (apply the function to the argument): $\lambda x[\mathrm{swim}(x)](\textbf{Lelia})$\\
4. Result: $\mathrm{swim}(\textbf{Lelia})$ = true if Lelia swims, false otherwise};
\end{tikzpicture}
\end{document}
```

**What *a* and *the* mean (Irene Heim)**: ***a*** = "**add a new referent**"; ***the*** = "**find an established referent**."

| Example | Interpretation |
|---|---|
| *A student walked in. **The** student sat down.* | the same student |
| *A student walked in. **A** student sat down.* | a different student |
| *I was in a car. **The seat** was comfortable.* | *the* for a new referent: no seat was mentioned, but cars have seats (a **bridging inference**) |
| *...introduced in 1865 during **the Reconstruction period**.* | *the* for a new referent: familiar from **general knowledge** of U.S. history |

---

# Unit 8 — Pragmatics

**Pragmatics** = the inferences drawn from **utterances by people in context**. It makes explicit our **implicit knowledge of how conversations work**. Linguists **have tried to identify general "rules"** of how conversations work.

## Speech acts (Austin 1962)
**J. L. Austin**, *How to Do Things with Words*: some utterances aren't true or false; they **make themselves true** when said **by the right person in the right context**.
- *"I **hereby** pronounce you a married couple."* · *"You are fired."*
- These are **performatives** (often marked with ***hereby***): they **change** the world rather than describe it.
- They only work with the right **authority** (an officiant, your boss), **circumstances**, and **procedure**. A stranger saying "You're fired" does nothing.

## Common Ground
**All** utterances "do something": they add to the **Common Ground (CG)** = the information (set of propositions) that we **mutually take for granted**, and know that we all take for granted (Paul Grice, Robert **Stalnaker**).
- Shared information requires **Theory of Mind**: your model of what's in other people's minds, and how it's similar to or different from yours.
- Our class's CG includes: we're at Georgia Tech, in the USA, speaking English, in a linguistics class, and the instructor's name is Lelia.
- ⚠️ CG ≠ all true facts in the world, ≠ all entailments of what's been said, ≠ only the presuppositions.

**Assertions are proposals to update the CG:**
- *I'm from Maryland*: I publicly commit to it, and I'm an authority on where I'm from, so you'll likely **accept** it. It's added: now we all know it, **and know that we all know it**. The CG grows as we talk.
- Assertions can be **rejected**: A: *The homework is due today.* B: *No, I think it's due Wednesday.* Nothing is added until they resolve it.

## Presupposition
**Presupposition** = information **assumed to already be in the CG** for an utterance to make sense. If a presupposition is false, the sentence isn't just false; it's **nonsensical (undefined)**.

**Strawson's example**: *The King of France is bald* (or *is not bald*). There's no King of France, so neither sentence is simply false. Replying "No he's not!" misses the real problem. You have to **"rewind"**: *"Hey, wait a minute, there **is** no King of France!"*

| Trigger | Example | Presupposes |
|---|---|---|
| *the* | *The King of France is bald* | there is a King of France |
| *stop* (change of state) | *Phil stopped smoking* | Phil used to smoke |
| ⚠️ **factive verbs** (*know, realize, regret*) | *Sam knows it's raining* | it's raining |

**Projection**: presuppositions are identified by the fact that they **project** = they **still hold when the sentence is embedded** under operators that cancel ordinary entailments (negation, *might*, questions):

| | There's a King? | He's bald? |
|---|---|---|
| *The King of France is bald.* | ✓ | ✓ |
| *...is **not** bald.* | ✓ | ✗ |
| *...**might** be bald.* | ✓ | ✗ |
| ***Is** the King of France bald?* | ✓ | ✗ |

Same with *Phil stopped smoking / Did Phil stop smoking? / Phil didn't stop smoking*: all still imply **he used to smoke**.

## Grice's Maxims
**H. Paul Grice** (1913–1988; Oxford, then Berkeley). Key idea: **communication is efficient**. We quickly and subconsciously infer **more than is said**.
- **Levinson's Rembrandt sketch**: from a few squiggly lines, viewers see a whole scene. An utterance is "just as sketchy," and listeners fill in the rest.
- **Point shared by Grice and Levinson**: we infer **lots of information beyond what's strictly said**.

| Maxim | Rule | Breaking it looks like |
|---|---|---|
| **Quality** | say only what you know is **true** | lying; unsupported claims |
| **Quantity** | be **as informative as required, no more, no less** | too much or too little info |
| **Manner** | be **understood**: organized, clear, audible, familiar words | rambling, mumbling, jargon |
| **Relevance** | stay **relevant** to the conversation's current purpose | randomly changing topic |

⚠️ **Politeness is not a maxim.**

Discussion questions from the lecture:
- **Descriptive or prescriptive?** They're phrased as commands, but they **describe** the assumptions listeners use to interpret speakers.
- **Eurocentric?** A real critique: norms of directness and informativeness vary by culture.

**Grice's key claim**: because we **assume everyone follows the maxims**, we can draw inferences beyond what was said.

| Exchange | Inference | Maxims |
|---|---|---|
| *I'm out of petrol.* — *There's a garage around the corner.* | it's open and sells gas | Relevance, Quantity |
| *How are your students?* — ***Some** are doing great.* | not all (or B hasn't finished grading) | Relevance, Quantity |
| Philosopher's recommendation letter: *penmanship excellent, attendance regular* | he's **not** a good philosopher | Quantity, Relevance |
| *Coming to the talk?* — ***Well**, I have to finish grading.* | B won't come (more **polite** than saying so; *well* marks a **dispreferred** reply) | Relevance |
| *Where does Jones live?* — *Somewhere in the South of France.* | B doesn't know (or won't say) exactly | Quantity, Relevance |
| *Do you speak Spanish?* — *I speak Portuguese.* | B doesn't speak Spanish | Quality, Quantity, Relevance |
| *Tickets cost $10.* — *I have $9.* | B doesn't have $10 | Quantity |
| *Tickets cost $9.* — *I have $9.* | **no** such inference (context changed) | — |

**Scalar implicature**: asserting a **weaker** claim implies the **stronger** one is false, because otherwise the speaker would have said it (*some → not all*).

## Conversational implicatures
These inferences are called **conversational implicatures**. ⚠️ The slides only name "cancelable"; the practice exam tests all four properties:

| Property | Meaning | Example |
|---|---|---|
| **Context-dependent** | same sentence, different implicature in a different context | $10 vs. $9 tickets |
| **Cancelable** | can be retracted without contradiction | *Somewhere in the South of France, oh right, in **Marseille**!* (now B clearly knows) |
| **Calculable** | the listener can work it out from what was said + the maxims | |
| **Reinforceable** | stating it outright isn't redundant | *some, but not all* |

They do **not** project through negation (that's presuppositions).

**Why they matter:**
- **Efficiency**: we don't have to spell everything out.
- **Plausible deniability**: it's more polite to implicate "I don't want to come," and more diplomatic to implicate "he's a bad philosopher," than to say either outright.

⚠️ **Searle's hamburger**: order a hamburger at a restaurant and you expect it cooked, on a plate, not raw and wrapped in plastic, even though you never said so. We expect listeners to **share our unstated background assumptions** and **infer beyond what's said**.

**Appendix: language and law (*Bronston v. United States*)**
> *Do you have any bank accounts in Swiss banks, Mr. Bronston?* — *No, sir.* — *Have you ever?* — *The **company** had an account for about six months in Zurich.*
- The implicature: Bronston **personally** never had one. In fact he did.
- The answer was **literally true**, and the Supreme Court held that **literally true but misleading testimony isn't perjury**. The law tracks what's **said**, not what's implicated.

## How conversations are organized
**Questions Under Discussion (QUD; Roberts 2012)**: a conversation is organized around implicit questions, which define what counts as "relevant" and "enough info."

| A says | B: *I have $9* answers the QUD "Can you afford it?" with... | So we infer |
|---|---|---|
| *Tickets cost $10.* | **No** | B has **only** $9 (with $10, B would have said so) |
| *Tickets cost $9.* | **Yes** | nothing more (having more than $9 is irrelevant to the QUD) |

**Adjacency pairs** = **conventional pairings of discourse moves**: a first move "scripts" the expected reply.

| First move | Expected reply |
|---|---|
| greeting | greeting |
| question | answer |
| invitation | acceptance, or refusal (a dispreferred reply) |
| farewell | farewell |
| compliment | varies by culture: accept? return the compliment? reject it? |
| apology | varies by culture: apologize back? accept? reject? |
| thanks | varies by culture: "you're welcome"? downplay ("it was nothing")? |

Compliments are socially fraught even though they're "positive": accepting can seem immodest, and rejecting can seem rude.

## Entailment vs. presupposition vs. implicature

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cblu}{RGB}{31,90,200}
\definecolor{cgrn}{RGB}{30,130,60}
\definecolor{corg}{RGB}{220,110,20}
\definecolor{cpur}{RGB}{140,50,170}
\begin{document}
\begin{tikzpicture}[font=\normalsize,
  q/.style={draw,thick,rounded corners,fill=cblu!10,align=center,minimum width=5cm,minimum height=1.1cm},
  a/.style={draw,very thick,rounded corners,align=center,minimum width=4.4cm,minimum height=1.3cm},
  arr/.style={-{Stealth[length=3mm]},thick}]
\node[q] (q1) at (0,0) {Can the inference be \textbf{cancelled}\\without contradiction?};
\node[a,fill=corg!15] (imp) at (6.5,0) {\textbf{Implicature}\\``It's late'' $\to$ ``I want to go home''\\(``...but I don't'' is fine)};
\node[q] (q2) at (0,-3) {Does it \textbf{project} (survive)\\under negation?};
\node[a,fill=cpur!15] (pre) at (6.5,-3) {\textbf{Presupposition}\\``The King is (not) bald''\\$\to$ ``There's a King''};
\node[a,fill=cgrn!15] (ent) at (0,-6) {\textbf{Entailment}\\``I ran'' $\Rightarrow$ ``I exercised''\\``I didn't run'' $\not\Rightarrow$ ``I exercised''};
\draw[arr] (q1) -- node[above]{yes} (imp);
\draw[arr] (q1) -- node[left]{no} (q2);
\draw[arr] (q2) -- node[above]{yes} (pre);
\draw[arr] (q2) -- node[left]{no} (ent);
\end{tikzpicture}
\end{document}
```

| | Entailment | Presupposition | Implicature |
|---|---|---|---|
| Example | *I ran → I exercised* | *The King is bald → there's a King* | *It's late → I want to go home* |
| Cancelable? | ✗ (\**I ran but didn't exercise*) | ✗ (\**...but there's no King*) | ✓ (*...but I don't want to go*) |
| Survives negation? | ✗ | ✓ | — |
| Source | literal meaning | assumed in the CG | inferred via the maxims |

**Language is efficient**, three ways across the units (practice exam: "all of these"):
- we infer more than is said (Grice), so we don't have to spell everything out
- corpus sentences favor **short dependencies** (syntax)
- frequent words are **short** (Zipf's Brevity Law)

---

# Practice Exam Answer Key
⚠️ = depends on material that isn't in the slides.

| # | Answer | Why |
|---|---|---|
| 1 | bound, inflectional | plural suffix |
| 2 | derivational, bound | Adj → N |
| 3 | systematically polysemous ⚠️ | animal/meat pattern recurs |
| 4 | "me" | accusative pronoun |
| 5 | tree with `[[in-flame]V -able]Adj` | *inflame* is a verb first |
| 6 | concatenative suffix | *-s* is added |
| 7 | brainrot ⚠️ | 2 whole words |
| 8 | enshittification ⚠️ | *en-…-ify-cation* |
| 9 | Brexit ⚠️ | Br(itain)+exit |
| 10 | earthquake | an event, not time-stable |
| 11 | politeness | not a maxim |
| 12 | 7 | histogram peak |
| 13 | language-specific | encode word order |
| 14 | language-general | they're language-specific |
| 15 | nouns ⚠️ | the other gaps are common |
| 16 | True ⚠️ | expert-defined term |
| 17 | Zipf's frequency law | few frequent, many rare |
| 18 | Zipf's Brevity Law | frequent = short |
| 19 | rizz ⚠️ | clipped *charisma* |
| 20 | dependency parsing | NLP standard |
| 21 | ungrammatical, but somewhat meaningful | like *Me love dog* |
| 22 | tried to identify general "rules" | Austin, Grice, Roberts |
| 23 | mentally organized with hierarchical structure | constituents |
| 24 | metaphor ⚠️ | weight → seriousness, no "like" |
| 25 | "project" through negation | survive *not* |
| 26 | context-dependent, cancelable, calculable, reinforceable ⚠️ | |
| 27 | changes involving their arguments | |
| 28 | atelic | no endpoint (*for an hour*) |
| 29 | furniture | \*two furnitures |
| 30 | carbohydrate | defer to experts |
| 31 | VP → V NP; VP → V | one left side, 2 right sides |
| 32 | key; is ⚠️ | agreement across the PP |
| 33 | good/better | root replaced |
| 34 | "for" / "four" | unrelated, accidental |
| 35 | agglutinating | 1 meaning per morpheme |
| 36 | "sandwich" is an artifact | conventional use (make/eat) |
| 37 | subjective adjectives occur further from the noun | Scontras |
| 38 | "Roller coasters are fun." | subjective → faultless disagreement |
| 39 | beautiful | not context-pointing |
| 40 | American | American ∩ N |
| 41 | all of these ⚠️ | good is up, time is money, arguments are wars |
| 42 | fundamental to our thinking | |
| 43 | "hereby" | performatives |
| 44 | information we all mutually take for granted | |
| 45 | presupposition ⚠️ | factive *know* survives negation/questions |
| 46 | implicature | cancelable (*...and a pencil too*) |
| 47 | conventional pairing of discourse moves | |
| 48 | we infer lots beyond what's strictly said | |
| 49 | all of these | inference, short dependencies, short frequent words |
| 50 | server shares our unstated assumptions ⚠️ | Searle |

**Distractor decoder** (what the wrong options actually belong to):

| Option wording | Belongs to |
|---|---|
| binary / asymmetric / typed | dependency grammar |
| cancelable | implicature |
| projects through negation | presupposition |
| time-stable entities | nouns |
| changes involving arguments | verbs |
| gradable / subjective properties | adjectives |
| vowel change · root swap · added affix | ablaut · suppletion · concatenative |
| ≈1 morpheme per word · 1 meaning per affix · many meanings per affix · sentence-length words | isolating · agglutinating · fusional · polysynthetic |
| accidental · systematic · abstract-via-concrete | homonymy · polysemy · metaphor |
| 3 arguments | ditransitive |
| repeated action | iterative (not a lecture term) |
