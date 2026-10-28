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
A word's **part of speech** (POS) determines **where it can go in a sentence** and **which inflectional/derivational morphology it can take**. It's diagnosed by **syntactic behavior**, but it also has a **non-random relationship to meaning**.

| POS | Examples | Key facts |
|---|---|---|
| **Noun** | *cat, Alice* | subject/object; **common** (*cat*) vs. **proper** (*Alice*); inflect for **number** (*cats*); common nouns take determiners (*the/every/two cats*); often "people, places, things"; usually **time-stable entities**. Exceptions: ***explosion, earthquake*** (events) |
| **Pronoun** | *he, she, it, they, we* | stand in for **discourse-prominent nouns** (meaning depends on context); in English, inflect for **case** (below) |
| **Verb** | *run, swim, throw* | inflect for **tense** (*walk/walked*), **agree** in number with the subject (*she walks / they walk*); describe the main action; usually **dynamic** = **change over time involving their arguments** (*I broke the window*). Exception: *I love movies* (a state) |
| **Adjective** | *red, cute, heavy* | **modify** a noun (*red dress*) or are the **predicate** with copula *is* (*the dress is red*); **gradable** (*tall*); **comparative/superlative** (*tall, taller, tallest*; *more/most beautiful*); can be **subjective** / emotional (*beautiful, horrible*) |
| **Adverb** | *quickly, very, really* | modify a **verb** (*ran quickly*) or **adjective** (*really tall*); often adjective + derivational ***-ly*** |
| **Determiner** | *the, a, some, all, every* | combine with a noun to pick out its referent: **new vs. familiar** (*a person / the cat*), **proximal/distal** (*this/that*), **possession** (*my*); includes **quantifiers** (*every, some, five*) |
| **Conjunction** | *and, or, so, but, because* | join words, phrases, clauses, sentences |
| **Preposition** | *of, for, with, to* | introduce a noun that **isn't a main argument** of the verb (*I saw him **at the party***) |
| **Modal auxiliary** | *can, may, would, should, might, will* | combine with a verb; describe **hypothetical** states of affairs (*I would go*) |

**Verb transitivity** = number of **arguments** (participant nouns):

| Type         | Args | Example                                   |
| ------------ | ---- | ----------------------------------------- |
| Intransitive | 1    | *I swam. / The window broke.*             |
| Transitive   | 2    | *I threw the ball. / I broke the window.* |
| Ditransitive | 3    | *I gave her the book.*                    |

**Case** = the form that shows a noun's **grammatical role**. In English, **only pronouns** show it:

| Case | Role | Forms |
|---|---|---|
| Nominative | subject | *she, he, I* |
| Accusative | object | *her, him, **me*** |
| Genitive | possessor | *her, his, my* |

In **Latin** and **Russian**, *all* nouns inflect for case (WALS feature 51A). **Automatic POS tagging** (e.g. spaCy's displaCy demo) labels every word's POS; it's the first step of most NLP.

## Content vs. function words

| | Content (**open class**) | Function (**closed class**) |
|---|---|---|
| Categories | nouns, verbs, adjectives, adverbs | pronouns, determiners, conjunctions, prepositions, modals |
| Paraphrase meaning? | easy (*cat*) | very hard (*the, every, would*) |
| New ones? | all the time (*monoamorous*, *DM*) | rare, but it happens: conjunction ***slash*** ("You slash I will do it") |

*The* is the most common English word. Some words **straddle** the line: *want, cause, take (a bath)*.

## Inflection
**Inflection** = a word changes form to fit its **grammatical context** but **stays the same POS**: *dog→dogs* (plural), *walk→walked* (past), *walk→walks* (3rd-person singular present), *she→her* (accusative; inflection of nouns/pronouns for case is also called **declension**).

| Kind | How | Examples |
|---|---|---|
| **Concatenative** (most common) | **add an affix** | *cat→cats*, *walk→walked*. **English plurals = concatenative suffix** |
| **Ablaut** (non-concatenative) | **change the vowel** | *man/men, woman/women; sing/sang, eat/ate* |
| **Suppletion** (non-concatenative) | **replace the whole root** | ***good/better/best***; *be/am/was* |

- Irregular forms cluster on **frequent words** (*to be* = most common verb; *good*). Maybe you must **hear a form often enough to preserve it**: old ablaut pasts **vanished on rare verbs** (the past of *help* was ***holp***). Ongoing: *dived* vs. *dove*.
- **French inflects more**: determiners match noun gender/number (*le chat* the.MASC cat, *la maison* the.FEM house, *les chats* the.PL cat.PL); verbs mark person, number, tense, conditionality (*J'aimerais* like.1SG.COND); adjectives agree (*le beau chat*, *la belle maison*).

## Derivation
**Derivation** = make a **new word** by changing a root's **meaning or POS**.

| Affix | Attaches to → makes | Example |
|---|---|---|
| *-ize* | Adj/N → V | *popular → popularize* |
| *-er* | V → N | *teach → teacher* |
| *-able* | V → Adj | *wash → washable* |
| *-ness* | Adj → N | *silly → silliness* |
| *-ly* | Adj → Adv | *quick → quickly* |

Practice (root, POS, affix → result):
- *winterize*: *winter* (N) + *-ize* → V
- *clarify*: *clear* (Adj) + *-ify* → V (root changes to *clar-*)
- *I will **box** the supplies*: *box* (N) → V with **no affix**
- *a guitar **pick***: *pick* (V) → N with **no affix**
- *antiqueness*: *antique* (Adj) + *-ness* → N
- *antiquity*: *antique* (Adj) + *-ity* → N

| | Inflectional | Derivational |
|---|---|---|
| New word? | no, a form of the same word | **yes** |
| Changes POS? | **never** | often |
| Position | **outermost** | closer to the root |

## Morphemes
**Morpheme** = smallest piece of a word with a (somewhat consistent) meaning/function; **can't be divided further**.
- **Free**: can stand alone (*car, tall, motion, wish, do, I*).
- **Bound**: can't stand alone (*-ing, un-, -s, -ed, re-, de-, -ize, -n't*).

**How meaningful are morphemes?** The slides' edge cases:
- *blue+berry, black+berry*: both parts meaningful.
- *goose+berry, straw+berry*: the first part is a free word but adds no clear meaning.
- *rasp+berry, **cran**+berry*: the first part never occurs alone. These are **cranberry morphemes**: bound pieces found in only one word.
- *under+stand*: two free morphemes, but the meaning isn't "stand under."
- *re+pay* (transparent) vs. *re+pair* (not "pair again") vs. *re+ceive, de+ceive, per+ceive*: *-ceive* recurs as a form, but has no statable meaning.
- Clean splits (note spelling changes): *puffin+s, notic+ing, lazi+ness, silli+ness, walk+ed, nation+al+it+ies, natur+al+iz+ation, pulver+ize+s* (*pulver* = bound root).

> [!example]- Bonus: "unpaired words" story (Jack Winter, *The New Yorker*, 1994)
> Built from words whose negative exists but the positive doesn't: *I was very **chalant**... appear **gruntled** and **consolate**... hair **kempt**, clothing **shevelled**, moved in a **gainly** way... manners couldn't be **peccable**... she was **committal**... she **requited** it.* The joke works because *dis-/un-/in-* are obviously separate morphemes, so we "expect" a base form that doesn't exist (a cranberry-like bound root).

## Word structure
A typical word = **root** (usually free) + **derivational affixes** (bound) + **inflectional affixes** (bound, **outermost**).
*nationalizes* = *nation* (free root, N) + *-al* (derivational → Adj) + *-ize* (derivational → V) + *-s* (inflectional, 3sg).

| Affix | Position | Example |
|---|---|---|
| Prefix | before | ***re**pay* |
| Suffix | after | *pay**ing*** |
| Circumfix | both sides at once | ***en**light**en*** |
| Infix | inside | none in English except *abso-**effing**-lutely* |

(WALS feature 26A maps prefixing vs. suffixing across languages.)

### Words have tree structure
**Key idea:** morphemes aren't "beads on a string"; they're **hierarchically structured** (trees). Each affix combines with a unit of a specific category.

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
\node[cred] at (0,-4.3) {flat: WRONG};
\node[font=\small, align=center] at (0,-5) {says nothing about which\\affix attaches to what};
\end{scope}
\begin{scope}[level 1/.style={sibling distance=3.2cm}, level 2/.style={sibling distance=1.8cm}]
\node[cat] at (7,0) {Verb}
  child {node[cat] {Adj}
    child {node[cat] {N} child {node[wd] {nation}}}
    child {node[cat] {AFF} child {node[wd] {-al}}}}
  child {node[cat] {AFF} child {node[wd] {-ize}}};
\node[cgrn] at (7,-4.9) {hierarchical: RIGHT};
\node[font=\small, align=center] at (7,-5.6) {N + -al = Adj; \ Adj + -ize = Verb};
\end{scope}
\end{tikzpicture}
\end{document}
```

Rules: *-al* needs a **noun** (→ Adj); *-ize* needs an **adjective or noun** (→ V); *-ation* needs a **verb** (→ N). So:
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
\node[align=center] at (7.5,-4.8) {(b) [in- [flamm-able]$_{Adj}$]\\``\textbf{NOT flammable}''};
\end{tikzpicture}
\end{document}
```

(a) is the real meaning (= catches fire). Because people misread it as (b), English **switched to *flammable***. "Can easily become inflamed" = tree **(a)**, where *inflame* is a Verb node.

| Ambiguity type | Example |
|---|---|
| **Lexical** (one word, two meanings) | *bank* (river / financial) |
| **Structural, in a word** | *unlockable* |
| **Structural, in a phrase** | *American art teacher*: [[American art] teacher] = teaches American art; [American [art teacher]] = an art teacher who is American |
| **Structural, in a sentence** | *Pope's Baby Steps on Gays* (see [[#Ambiguity headlines]]) |

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
> - **Compound** (2 whole words): ***brainrot***, *doomscroll*, *ragebait*, *rawdog*, *babygirl*, *girl math*, *short king*, *dumpster fire*, *fancam*, *zoom bomb*, *hashtag*, *nepo baby*
> - **Derivation**: ***enshittification*** (*en-…-ify-cation*), *unserious*, *yassify*, *unfriend*, *-splaining*, *-shaming*
> - **Blend** (parts of 2 words): ***Brexit*** (Britain+exit), *covidiot*, *mansplain*, *cronut*, *techlash*, *humblebrag*, *refudiate*, *hacktivist*
> - **Clipping** (1 word cut down): ***rizz*** (cha**ris**ma), *sus*, *vax*, *nepo*, *fam*
> - **Acronym**: *NFT, FOMO, YOLO, MOOC, WAP*
> - **POS change with no affix**: ***clock*** (N→V), *ghost* (N→V)
> - **Old word, new meaning**: *slop, brat, hallucination, tweet, cloud*
> - **Phrases, not word-formation**: *hold space, locked in, let someone cook, it's giving, 6-7*

> [!example]- American Dialect Society Words of the Year (full slide lists)
> - **2025** *slop* (ragebait, clock [verb], that's AI, chopped, 6-7, reheat nachos)
> - **2024** *rawdog* (locked in, unserious, brainrot, brat, hold space)
> - **2023** *enshittification* (ceasefire, babygirl, let someone cook, (derogatory), era, girl [dinner/math], millennial pause, hallucination)
> - **2022** *-ussy* (Dark Brandon, quiet quitting, long-termism, nepo baby, it's giving, short king, -verse, chronically online, rizz)
> - **2021** *insurrection* (antiwork, Big Lie, Great Resignation, Long Covid, Omicron, variant, vax, boosted, NFT, bussin', tone indicator, vibe, the ___ urge to, stonk, supply chain, yassify)
> - **2020** *covid* (abolish/defund, dissent collar, freedumb, doomscrolling, fancam, sus, zoom fatigue, zoom bomb, covidiot, contact tracing, WAP, essential worker)
> - **2019** *(my) pronouns* (ok boomer, plant-based, stan, Zoomer, Nobody:/Me:, quid pro quo, hot girl summer, VSCO girl, the squad)
> - **2018** *tender-age shelter* (yeet, blue wave, nationalist, Individual 1, techlash, #nottheonion)
> - **2017** *fake news* (alternative facts, #MeToo, persisterhood, take a knee, emergency podcast, shitpost, shooketh, unicorn, askhole, avocado toast)
> - **2016** *dumpster fire* (woke, normalize, post-truth, deplorables, nasty woman, fam, -exit (Brexit), bigly, #blackgirlmagic, gaslight, slay, #OscarsSoWhite)
> - **2015** *singular they* (ghost, mic drop, microaggression, shade, adulting, squad, yass, ammosexual, dadbod, trigger warning, AF, lit, Netflix & chill, swipe right/left, on fleek)
> - **2014** *#BlackLivesMatter* (bae, columbusing, even ["I can't even"], ebola, basic, bye Felicia, salty, selfie stick, normcore, thirsty, manspreading)
> - **2013** *because* [preposition: "because linguistics"] (slash, twerk, Obamacare, selfie, struggle bus, catfish, sharknado, underbutt, binge-watch, drone, -shaming, -splaining, cronut)
> - **2012** *hashtag* (YOLO, fiscal cliff, Gangnam style, -pocalypse, hatewatching, mansplain, feels, ratchet, MOOC, cray-cray, binders full of women, meggings)
> - **2011** *occupy* (FOMO, humblebrag, the 99%, tablet, kardash, put a bird on it, planking, job creator, cloud, tiger mother, brony)
> - **2010** *app* (nom, Wikileaks, trending, prehab, refudiate, hacktivist, Obamacare, corn sugar, ironic mustache)
> - **2009** *tweet* (H1N1, birther, blog, public option, rogue, un- [unfriend, unfollow], sea kitten, charging station, fail, sexting, death panel)

## Word frequency and length (corpus data)
A **corpus** = a large body of real text. Examples: the **Brown Corpus** (1M words of edited American English) and 1M words of Reddit comments.

**Zipf's Frequency Law**: there are **a few very frequent words** (function words) and **very many infrequent words** (content words). It's a **power law** (long tail), not a bell curve.

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

- Brown corpus top 5: *the* (6.97%), *of, and, to, a*. Reddit top 5: *the* (3.34%), *i, to, a, and*.
- Reddit ranks *i, my, you* high; Brown ranks *he, his, was* high. **Genre matters.**

**Word length roughly follows a bell curve.** Length of word **types** (distinct words) in Brown:

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

- **Most common length of an English word type ≈ 7 characters.** (Counting tokens instead gives shorter lengths, because the frequent words are short.)

**Zipf's Brevity Law**: **more frequent words are shorter** (*the, of, a* top the chart; *oversimplification, mirthless* sit at the bottom). **Language is efficient.**
- **Why log-scale the frequency axis?** Frequencies span orders of magnitude (*the* ≈ 70,000 per million; *mirthless* ≈ 1). On a linear axis, almost every word would be squashed at zero.

## Morphological typology (word-to-morpheme ratio)

| Type | Definition | Example |
|---|---|---|
| **Isolating**: Yoruba (Nigeria) | little inflection; **~1 morpheme per word** | *mo wò èyí, wò èyí, mo kò rí ìyá mi* = 1SG look DEM, look DEM, 1SG NEG see mother 1SG.POSS ("I looked here, I looked there, but I did not see my mother") |
| **Agglutinating**: Turkish | root + **string of affixes, each = one meaning** | *ev-de* house-LOC; *çay-ı* tea-ACC; *yap-ar* make-AOR (AOR = completed/habitual action). ***ev-imiz-de*** = house-our-in "in our house" |
| **Polysynthetic** ("incorporating"): Yupik (Alaska) | **very long words**, root + many bound morphemes (each may carry several meanings); **a whole sentence can be one word** | *Mangtegha-ghlla-ngllagh-yug-tu-kut* = house-big-make-want-IND.INTR.1PL ("We want to make a big house") |
| **Fusional** ("synthetic"): French | one affix **fuses several meanings** | *était* = "be" + 3rd person + singular + imperfective in one form |
| **English** ("analytic") | **between isolating and agglutinating**: a little affixing (*kids, walked*), but much is carried by **free words** (prepositions) | *in our house* = 3 words vs. Turkish *ev-imiz-de* = 1 word |

Agglutinating vs. fusional: in Turkish you can point to the "our" piece and the "in" piece separately. In French *-ait*, person, number, and aspect can't be pulled apart.

## Appendix topics
- **Reduplication**: repeat a root to change meaning. Often marks "distribution, plurality, repetition, customary activity, increase of size, added intensity, continuance" (Sapir 1921). Limited in English (*a red red rose*; "I'll bring the **salad salad**" = the prototypical salad). Productive in other languages (WALS feature 27A). **Iconic: "more is more."**
- **Compounds (Glass's research)**: a compound doesn't state how **head** and **modifier** relate. *water jug* = holds water; *water spinach* = grows in wet conditions (not really compositional).
  - **Artifacts** (made by humans for a purpose, e.g. *jug*) take modifiers about their **use/creation**.
  - **Natural kinds** (exist without humans, e.g. *spinach*) take modifiers about **appearance, habitat, origin**, or borrowed modifiers (an attempt to capture the kind's "essence").
- **Pumpkin spice latte**: spice FOR pumpkin (pie) or spice OF pumpkin? The compound doesn't say. Starbucks added real pumpkin after "shaming by the Food Babe," who missed the **morphological ambiguity**.
- **Adjectives as nouns (Glass's research)**: *The old are happier* (plural = **old people**) vs. *The old is never ordinary* (singular/mass = **oldness, old stuff**). The construction is very productive. The two readings come from properties being construable as **predicates of individuals** or as **the abstract thing those individuals share**.

---

# Unit 6 — Syntax

**Syntax** = the study of **word order**: which combinations of words are **grammatical** (possible) vs. **ungrammatical** (\*, impossible). Its rules let a **finite** set of words express **infinitely** many ideas.
- *The student read the book.* ✓ / \**Student the read book the.*
- *I threw the ball.* ✓ / \**The ball threw I.* / \**Her saw it.* (wrong case)

## Syntax vs. semantics
- *Colorless green ideas sleep furiously* (Chomsky): **grammatical but meaningless**.
- *Me love dog* / *Me eat cookie*: **ungrammatical but (somewhat) meaningful**.
- So Chomsky argued **syntax and semantics are independent**.
- But where is the line between **ungrammatical** and **nonsensical**? *?The toothbrush is pregnant. ?The shoe poured the chair.* There's no clear answer; it's as much theoretical as empirical.

## Syntactic facts about English (other languages differ!)

| Sentence | Phenomenon |
|---|---|
| *The student read the book.* | declarative = **SVO** |
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

- **Long-distance (non-local) dependency** = two words that belong together (verb + its object) but are **separated** in the string. "___" marks the gap.
- Side note from the lecture: watch for **gender stereotypes in constructed example sentences**.

> [!warning] ⚠️ Agreement as a long-distance dependency
> *The **key** to the cabinets **is** on the table.* The verb agrees with the head noun ***key*** (singular), not the nearer *cabinets*, so ***key–is*** is a long-distance dependency across *to the cabinets*. Slips like "*...cabinets are*" show the dependency is non-local.

## Constituents
Words are **produced linearly** (one after another) but **mentally organized hierarchically** into chunks called **constituents**.

**Constituency tests** (YES to any → constituent):
1. **Answers a question**: *Who begins the history of linguistics?* → "The Indian grammarian Panini."
2. **Sticks together when reordered**: "*The Indian grammarian Panini* begins *the history of linguistics*."
3. **Can be conjoined**: "*The history of linguistics*, and *scholarship on Sanskrit*, begins with..."

*The history of linguistics begins with the Indian grammarian Panini*:
- ✓ *The history of linguistics*, *of linguistics*, *linguistics*, *The Indian grammarian Panini*, *begins with the Indian grammarian Panini*
- ✗ *Linguistics begins with the*, *of linguistics begins with*, *begins with the Indian*

*The athlete tossed the ball*:
- ✓ *the athlete*, *the ball*, *tossed the ball*
- ✗ *the athlete tossed*, *athlete tossed the*, *tossed the*

**Constituents share a parent in the tree: every subtree is a constituent.**

## Lexical vs. phrasal categories
- **Lexical** (word-level: Det, N, Adj, TransV, IntransV, Prep) determine a **word's** distribution. Swap within a category, "Mad Libs" style: another noun for *student*, another transitive verb for *read*.
- **Phrasal** determine a **phrase's** distribution: **NP** (*every book, the red ball, two people*), **VP** (*ran, threw the ball*; may contain an NP), **AdjP** (*very tall, oddly funny*). Swap one NP for another, one VP for another.

## Phrase Structure Grammar (Chomsky, ~1950s)
**Goals:** (1) capture the implicit **generative rules** for making/understanding new sentences; (2) capture both **hierarchical structure** and **linear order**; (3) capture **grammaticality judgments**. Illustrated with a **grammar fragment** (a small toy model).

```
Phrase structure rules (non-terminal nodes)   Lexicon (terminal nodes = words)
S  -> NP VP                                    Det      -> the, every, a, some
NP -> (Det) (Adj*) N                           N        -> student, book, forest, reindeer,
NP -> NP (PP)                                              lunch, evening, game
PP -> Prep NP                                  TransV   -> throw, want, love, kick, eat, play
NP -> Pronoun                                  IntransV -> swim, run, laugh, eat, dance
VP -> TransV NP                                Adj      -> red, blue, beautiful, interesting, tall
VP -> IntransV                                 Pronoun  -> you, she, he, I, we, they
VP -> VP PP                                    Prep     -> in, from, of
```
- `X -> Y Z` = "an X can be a Y followed by a Z." `( )` = optional. `*` = zero or more.
- *eat* is both TransV and IntransV.
- To draw trees: mshang.ca/syntree, LaTeX/Overleaf, or by hand.

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
\node[cgrn] at (9,-10.4) {Tree D: \textbf{RIGHT} (S $\to$ NP VP; VP $\to$ V NP)};
\end{scope}
\end{tikzpicture}
\end{document}
```

Check a tree by asking: does every real constituent (*the author, the book, wrote the book*) get its own node? Only **D** passes.

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
- *What did you eat ___?*: *what* is at the front, but it's conceptually the **direct object of *eat***.
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
- **Origin**: French linguist **Lucien Tesnière**, inspired by **Latin and Slavic**, which have **free word order** and mark roles with **case**. *Puella canem amat / Canem puella amat / Amat puella canem* all mean "The girl loves the dog" (*puella* = girl.NOM, *canem* = dog.ACC, *amat* = loves). The order is chosen by discourse factors (**given before new**). These languages need a framework that allows that flexibility.
- **Definition**: syntax as **binary, asymmetric, typed** relations between pairs of **POS-tagged** words: a **head** → a **dependent**.

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

The **verb is the root** (depends on nothing). Syntactically, it determines **how many nouns** the sentence has; semantically, it describes the **main event** the nouns take part in.

### Advantages
1. **Works for any language and any word order**: the same relations hold, only the arc directions change. That's why it's used for **consistent cross-linguistic representations**: NLP tools for many languages, comparative syntax, and **Universal Dependencies** (Stanford; treebanks in **100+ languages**).

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

**Dependency length** = how many words an arc spans. In parsed corpora (newspapers, etc.) across **37 languages**, **short dependencies are more common than random word order would predict**. That's another way language is efficient.

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

### Disadvantages
Dependency grammar does **not** capture a specific language's **word order**, its **grammaticality judgments**, or its **rules** for building grammatical sentences.

| | Phrase Structure | Dependency |
|---|---|---|
| Who | Chomsky | Tesnière |
| Units | phrases (abstract NP/VP nodes) | words + labeled arcs |
| Word order / grammaticality | **captured** (language-specific) | **not captured** (works for any language) |
| Long-distance dependencies | need **movement** | just a **longer arc** |
| Main use | theoretical syntax | **NLP**, cross-linguistic corpora |

## Ambiguity headlines
**Structural** (two trees):
- *Pope's Baby Steps on Gays*: [Pope's baby] **steps on** gays / [Pope's **baby steps**] on gays
- *MBA Studies Mushroom*: MBA studies **grow fast** / an MBA **studies a mushroom**
- *Complaints about referees growing ugly*: the **complaints** grow ugly / the **referees** grow ugly
- *Lawyers give poor free legal advice*: advice to **poor people** / **low-quality** advice
- *Hospital sued by 7 foot doctors*: 7 **podiatrists** / doctors who are **7 feet tall**
- *Time for football and meatball stew*: football, and meatball stew / a **football-and-meatball** stew

**Lexical** (word senses): *Iraqi **Head** Seeks **Arms*** (leader seeks weapons / a head seeks limbs).

**Underspecified participation** (one structure, one sense per word, but several ways to take part in the event):
- *Pillars replaced by alumni*: alumni **funded** the replacement / alumni **are** the new pillars
- *Include your children when baking cookies*: as helpers / as **ingredients**
- *Kids make nutritious snacks*: kids **prepare** snacks / kids **are** snacks
- *Stolen painting found by tree*: found **near** a tree / a tree **found** it

## Syntactic fieldwork
Elicit: *Sam ate a sandwich. / Sam did not eat a sandwich. / Sam ate a delicious sandwich. / Did Sam eat a sandwich? / What did Sam eat? / The sandwich that Sam ate was delicious.*

Then ask: basic word order? Adj–N order? How are negation and past tense expressed? Are there determiners? What's the word order of polar questions, wh-questions, and relative clauses?

| | Mandarin | French |
|---|---|---|
| Word order | SVO | SVO (auxiliary + participle: *a mangé*) |
| Adj–N | Adj **before** N, with *de* (*hǎo-chī de sāmíngzhì*) | Adj **after** N (*sandwich délicieux*) |
| Negation | *méi-yǒu* before the verb | *ne…pas* around the auxiliary |
| Past | **no tense**: aspect marker *le* | *avoir* + participle; *était* (imperfective "was") |
| Determiners | **none**; *yí-gè* "one-CL" (CL = classifier) | yes: *un, le* (gendered) |
| Polar question | particle ***ma*** at the end, no reordering | ***est-ce que*** at the front |
| Wh-question | *shénme* "what" **stays in place** | wh-word **fronted** (*qu'est-ce que*) |
| Relative clause | **before** the noun, with *de* | **after** the noun, with *que* |

> [!example]- Full glossed data
> **Mandarin** (ASP = aspect, CL = classifier, DE = linker)
> 1. *Sàmǔ chī le yí-gè sāmíngzhì* — Sam eat ASP one-CL sandwich
> 2. *Sàmǔ méi-yǒu chī yí-gè sāmíngzhì* — Sam not-have eat one-CL sandwich
> 3. *Sàmǔ chī le yí-gè hǎo-chī de sāmíngzhì* — Sam eat ASP one-CL good-eat DE sandwich
> 4. *Sàmǔ chī le yí-gè sāmíngzhì ma?* — ... sandwich QUESTION
> 5. *Sàmǔ chī le shénme?* — Sam eat ASP what
> 6. *Sàmǔ chī le de sāmíngzhì shì hǎo-chī de* — Sam eat ASP DE sandwich is good-eat DE
>
> **French**
> 1. *Sam a mangé un sandwich* — Sam has eaten a sandwich
> 2. *Sam n'a pas mangé un sandwich* — Sam NEG-has NOT eaten a sandwich
> 3. *Sam a mangé un sandwich délicieux* — Sam has eaten a sandwich delicious
> 4. *Est-ce que Sam a mangé un sandwich?* — Is-it that Sam has eaten a sandwich?
> 5. *Qu'est-ce que Sam a mangé?* — What-is-it that Sam has eaten?
> 6. *Le sandwich que Sam a mangé était délicieux* — The.MASC.SG sandwich which Sam have.3SG.PRES eaten be.3SG.IMP delicious.MASC.SG

**Methodological questions**: How many examples per phenomenon? Should the speaker help analyze, or only give data? Spoken, written (in which writing system?), or glossed? What language are the questions asked in? How do you know the speaker understood the question as intended?

**Ethics, "giving back"**: this matters especially when taking data from **minoritized communities** and then publishing in **paywalled journals** for tenure. Options:
- Partner with the community on **children's books, educational materials, accessible archives, writing systems, dictionaries**
- **Documentaries** in the community's own voice (*Talking Black in America*, NC State)
- Widen access to community-engaged linguistics (**MIT Indigenous Language program**)

**Unit review list**: English syntactic phenomena (cross-linguistically) · constituency tests · PS rules · dependency grammar · fieldwork (methods + ethics) · glossed examples · syntax vs. semantics.

---

# Unit 7 — Semantics

- **Semantics** = meaning/inferences from morphemes, words, sentences, discourses (mostly **words and sentences**).
- **Pragmatics** = inferences from **utterances** by **people in context** (next unit).
- David Lewis (1972): to say what a meaning *is*, first ask what a meaning *does*.

**Knowing a word's meaning** lets you:
1. identify its **referent** (*cat* → furry feline; *unicorn* → a fictional horned horse)
2. reason about its **relations** to other words (a cat is an **animal**; a cat is **not** a dog)
3. use it in a sentence

**Knowing a sentence's meaning** lets you:
1. know its **truth conditions** (what the world must be like for it to be true: *Alice has a cat / a unicorn*)
2. reason about relations: *Alice has a cat* **entails** *Alice has a pet* and **contradicts** *Alice has no pets*
3. know what it contributes to a discourse

| **Lexical semantics** | **Compositional semantics** |
|---|---|
| meaning of **open-class content words** (*cat, smile, beautiful*): how nouns/verbs/adjectives differ in grammar and in the inferences they license | meaning of **closed-class function words** (*the, a, every, for, with, can, should, must*); how word meanings **combine into sentence meanings** |

## Relations between words

| Relation | Meaning | Examples |
|---|---|---|
| **Synonyms** | same meaning | *couch/sofa, pretty/beautiful* |
| **Antonyms** | opposites | *beautiful/ugly, tall/short* |
| **Homonyms** | **unrelated** meanings, **accidentally** same form; **not** expected to recur in other languages | *bank/bank*, *for/four* |
| **Polysemy** | **related** meanings; **potentially systematic**, **may recur** across languages | *my head / head of the school*; *the dinner was delicious / took two hours* (food/event); *the book is heavy / interesting* (object/content); *the White House is in DC / knew about the meeting* (building/staff); *computer mouse / Mickey mouse* |

- **Antonyms are mostly adjectives**, because adjectives sit on **gradable scales** with two ends.
- **Marked vs. unmarked**: *How **tall** is she?* is neutral; *How **short** is she?* assumes she's short. *5 ft tall* ✓ vs. *?5 ft short*. The unmarked member (*tall*) names the whole scale.
- ⚠️ ***lamb*** (animal/meat) is **systematic polysemy**: the pattern recurs (*chicken, fish*) and across languages.

## Lexical categories, semantically
- Do all languages have nouns, verbs, adjectives? How would we know (by syntax/morphology)?
- **Few adjectives** in some languages: *I am hungry* (Adj) vs. French *J'ai faim* "I have hunger" (N). Some languages do this for nearly all adjective-type concepts.
- **Few verbs** in Persian: **light verb** + noun ("I did a shower / did a run / did a laugh").
- Which concepts become N/V/Adj? Is there a language where *rice* or *joy* is a verb/adjective, or *throw* is a noun?

⚠️ **The most astonishing gap would be a language without nouns.** Lacking tense (Mandarin), a word for "the" (Mandarin), or "purple" is common.

## Who decides what words mean?
- **Defer to experts**: *quark* (is an electron one? no), *carbohydrate* (is butter one? no), *whale* (orcas?), ⚠️ *polygon*: straight connected sides by definition, so a spiral is **not** a polygon (True).
- **Everyone debates**: *soup* (is cereal soup?), *sandwich*, *champagne* (any sparkling white wine?), *woman* (who counts? why is this asked less of *man*?), *person* (is a fetus a person?).
- **Meaning changes**: *planet* once covered all celestial bodies, including the sun and moon; astrophysics changed it.
- **Burrito case** (the slide cites *Quintana v. Fort Wayne Plan Commission*): Panera's mall lease banned rival **sandwich** shops; Panera argued Qdoba (burritos) couldn't open. Is a burrito a sandwich?
- **Words are tools to pick out meaningful categories**, which can **change over time** and be **socially contentious**.
- Discussion prompt: find a political debate that hinges on a word's meaning. Do the people involved realize that? How would reframing it change the debate?

**Wittgenstein on *game***: board games, card games, ball games, the Olympic games share no single common feature, only **"family resemblances"** (overlapping similarities, like a family's build, eyes, gait). So **words don't all have strict boundaries**. That's related to, but distinct from, "who decides." Problem: law and policy need boundaries. Is a **borderline ovarian tumor** "cancer" (life-insurance eligibility, public benefits)? Even **oncologists disagree** (work by **Jessica Rett**).

**Labov's cups**: people named drawings of containers that varied gradually in width, height, handles, and stems (cup / mug / bowl / vase...). Category **boundaries are fuzzy and gradient**.

## Distinctions among nouns
- **Relational vs. sortal**: relational nouns need a relatum (*sister* = someone's sister); sortal nouns just name a kind (*sheep*). Tests: *the sister of my friend* ✓ / *?the sheep of my friend*; *A man walked in. His {sister / ?sheep} was with him.*
- **Mass vs. count**:
  - count: *so many books, two books, so many letters, so many apples*
  - mass: *so much water, ?two waters, so much mail, so much apple*
  - The same stuff can be either: *letters* vs. *mail*.
  - ***Furniture* is mass** (\**two furnitures*). Who has "more furniture," 2 big pieces or 3 little stools? People typically say **3 stools**: they count individual pieces.
- **Artifact vs. natural kind**:

| | Artifact | Natural kind |
|---|---|---|
| Definition | made by humans **for a purpose** | exists **independently of humans** |
| Membership | by **function** (anything that staples = stapler) | by **essence** (genetics = bear) |
| *start a ___* | *start a book* = start reading/writing it | *start a bear* = ?? |
| *my ___* | *my book* = the one I'm reading/writing | *my bear* = pet? study subject? |

So ***finish a sandwich*** = finish **making/eating** it: a sandwich is an **artifact**, so we infer the conventional ways of interacting with it. (No hidden *make/eat* sits in the tree or dependency graph.)

## Distinctions among verbs
- **Dynamic vs. stative**: *Alice threw the ball* (change) / *Alice loved movies* (state).
- **Agentive vs. non-agentive**: *Alice ran*, *Alice sat on the chair* (deliberate) / *Alice fell*, *The book sat on the table* (no intention).
- **Telic vs. atelic**:
  - **Telic** = has a **built-in endpoint**: *ate **the** pizza **in** ten minutes*.
  - **Atelic** = no endpoint: *ate pizza **for** ten minutes*; ***I watched TV***.
  - *I did my homework **in** half an hour* = finished it; ***for** half an hour* = worked on it.
- **Aspect orders events in a story**:
  - *Alice walked in. The book sat on the table.*: the book was **already there** (stative).
  - *Alice walked in. The president sat down.*: he sat down **afterward** (event).
- **Argument structure** (how many arguments, and their roles):
  - *The submarine sank the ship* / *The ship sank*: the ship **changes** in both.
  - *The athlete lifted the weight* / *The athlete lifted*: the athlete is still the **lifter**; the object is just left implicit.
  - Same surface pattern, different roles.
- **Causative vs. not**: *The child **broke** the fence* (fence changes) → *The fence broke* ✓. *The child **hit** the fence* (no change) → *?The fence hit*.

**Verbs typically describe changes involving their arguments.**

## Distinctions among adjectives
- **Gradable** (*very tall, taller*) vs. **non-gradable** (*?very dead, ?deader*).
- **Vagueness**: what counts as *expensive* coffee vs. car, a *tall* man vs. building depends on the comparison class.
- **Subjective vs. objective**: A: *The box is {red / plastic / heavy / beautiful}.* B: *No it's not.* For *red / plastic / heavy*, someone is wrong. For *beautiful*, neither is: that's **faultless disagreement**, the mark of **subjective** adjectives. Prototype: ***"Roller coasters are fun."***
- **Adjective ordering (Scontras et al. 2017)**: **more subjective adjectives go further from the noun**: *heavy red box* (not *?red heavy*), *beautiful wooden chair*, *cute red dress*. This was confirmed in **corpora**, using human subjectivity ratings. Subjective adjectives are also more often **predicative** (Glass 2025): *The red dress is cute*, not *The cute dress is red*.
- **Intersective / subsective / privative**:

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
\node[align=center,font=\small] at (1,-2) {\textbf{privative}: \emph{former musician}\\is NOT a musician};
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
- **Deixis** ("pointing," like the index finger): *I, you, me, today, tomorrow, yesterday, here, now*. The referent depends on **who/when/where** the speaker is. *Beautiful* is **not** deictic.
- **Expressives**: *I lost my **damn** keys* has the **same truth conditions** as *I lost my keys*, plus the speaker's **emotional attitude**.
- **Slurs**: *Hermione is a **mudblood*** carries the same descriptive content as *...from a non-wizard family*, plus a **derogatory attitude toward the group**.

## Metaphor (Lakoff & Johnson 1980)
*Metaphors We Live By*: metaphors are **not decorative flourishes**; they're **fundamental to how we think**. We understand the **abstract** through the **concrete**.

| Conceptual metaphor | Expressions |
|---|---|
| TIME IS MONEY | ***spent** an hour, **wasted** time* |
| TIME IS SPACE | *move the meeting **up**, **back-to-back** meetings* |
| GOOD IS UP | ***higher**-level class, **raise** morale, **elevate** your style* |
| UNDERSTANDING IS VISION | ***crystal-clear** speaker, I **see** your point, still **murky*** |
| ARGUMENTS ARE WARS | ***cede/defend** a claim, **win** the argument* |
| PROJECTS ARE MEALS/COOKING | ***meaty** paper, **half-baked** idea, **back burner*** |
| PROJECTS/IDEAS ARE BUILDINGS | ***laying the foundation, buttressing, supporting** a claim* |

- **Language change runs concrete → abstract**: *standing on the floor* → *what I said still **stands***. The **Database of Semantic Shifts** (datsemshift.ru) catalogs many such shifts.

> [!warning] ⚠️ Metaphor vs. simile vs. allegory
> - **Metaphor** = understanding X **as** Y, with no "like": *a **heavy** topic* (weight = seriousness).
> - **Simile** = explicit comparison **with "like/as"**.
> - **Allegory** = a whole story whose parts stand for abstract ideas.
> - *"Morale is **low** because we've been **wasting** time **battling** silly problems"* uses **all of these**: GOOD IS UP, TIME IS MONEY, ARGUMENTS ARE WARS.

## Compositional semantics
**Typed lambda calculus** treats word meanings as **functions**. Types: ***e*** = individuals, ***t*** = truth values, plus mappings between them (⟨*e,t*⟩ = a function from individuals to truth values).

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
1. $[\![\mathit{swim}]\!] = \lambda x[\mathrm{swim}(x)]$: takes an individual $x$, gives TRUE if $x$ swims, FALSE otherwise\\
2. $[\![\mathit{Lelia}]\!] = \textbf{Lelia}$: an individual\\
3. Combine (apply the function to the argument): $\lambda x[\mathrm{swim}(x)](\textbf{Lelia})$\\
4. Result: $\mathrm{swim}(\textbf{Lelia})$ = TRUE if Lelia swims, FALSE otherwise};
\end{tikzpicture}
\end{document}
```

**What *a* and *the* mean (Irene Heim)**: ***a*** = "**add a new referent**," ***the*** = "**find an established referent**."
- *A student walked in. **The** student sat down.* → the same student.
- *A student walked in. **A** student sat down.* → a different student.
- But *the* often introduces new referents:
  - *I was in a car. **The seat** was comfortable.*: a **bridging inference** (cars have seats).
  - *The idea of a technology school in Georgia was introduced in 1865 during **the Reconstruction period**.*: familiar from context or **general knowledge**.

---

# Unit 8 — Pragmatics

**Pragmatics** = inferences drawn from **utterances by people in context**. It makes explicit our **implicit knowledge of how conversations work**. Linguists **have tried to identify general "rules" of conversation**.

## Speech acts (Austin 1962)
**J. L. Austin**, *How to Do Things with Words*: some utterances aren't true or false; they **make themselves true** when said **by the right person in the right context**. *"I **hereby** pronounce you a married couple." "You are fired."*
- These **performatives** (marked by ***hereby***) **change** the world rather than describe it.
- They need the right **authority** (an officiant, your boss), **circumstances**, and **procedure**. A stranger saying "You're fired" does nothing.

## Common Ground
- **All** utterances "do something": they add to the **Common Ground (CG)** = the propositions we **mutually (know we) take for granted** (Grice, **Stalnaker**).
- Mutual knowledge requires **Theory of Mind**: modeling what's in others' minds, and how it differs from yours.
- Example of our class's CG: we're at Georgia Tech, in the USA, speaking English, in a linguistics class, and the instructor is Lelia.
- **Assertions = proposals to update the CG.**
  - *I'm from Maryland*: I publicly commit to it; I'm an authority on it, so you accept it, and it's added. Now we all know it, **and know that we all know it**. The CG grows as we talk.
  - Assertions can be **rejected**: A: *The homework is due today.* B: *No, I think it's due Wednesday.* Nothing is added until A and B resolve it.
- ⚠️ CG ≠ all true facts, ≠ all entailments, ≠ only presuppositions.

## Presupposition
**Presupposition** = info **assumed to already be in the CG** for an utterance to make sense. If it's false, the sentence is **not just false but nonsensical (undefined)**.
- **Strawson**: *The King of France is (not) bald*. There's no King of France, so "No he's not!" misses the problem. You must **rewind**: *"Wait a minute, there **is** no King of France!"*
- Triggers on the slides: *the* (there is one), *stop* (*Phil stopped smoking* → he used to smoke). ⚠️ **Factive verbs** like ***know*** (also *realize, regret*): *Sam knows it's raining* → it's raining.

**Projection** = presuppositions **survive** under entailment-canceling operators (negation, *might*, questions). That's how you identify them:

| | There's a King? | He's bald? |
|---|---|---|
| *The King of France is bald.* | ✓ | ✓ |
| *...is **not** bald.* | ✓ | ✗ |
| *...**might** be bald.* | ✓ | ✗ |
| ***Is** the King of France bald?* | ✓ | ✗ |

*Phil stopped smoking / Did Phil stop smoking? / Phil didn't stop smoking*: all still mean **he used to smoke**.

## Grice's Maxims
**H. Paul Grice** (1913–1988; Oxford, then Berkeley). **Communication is efficient**: we quickly and subconsciously infer **more than is said**.
- **Levinson's Rembrandt sketch**: from a few squiggly lines, viewers see a whole scene. An utterance is "just as sketchy," and listeners fill in the rest.
- **Point shared by Grice and Levinson**: we infer **lots of information beyond what's strictly said**.

| Maxim | Rule |
|---|---|
| **Quality** | say only what you know is **true** (don't lie; don't say unsupported things) |
| **Quantity** | be **as informative as required, no more, no less** |
| **Manner** | be **understood** (organized, clear, audible, familiar words) |
| **Relevance** | stay **relevant** to the conversation's current purpose |

⚠️ **Politeness is NOT a maxim.**

Discussion questions:
- **Descriptive or prescriptive?** Phrased as commands, but they **describe** the assumptions listeners use.
- **Eurocentric?** A real critique: norms of directness and informativeness vary by culture.

**Grice's key claim**: because we **assume everyone follows the maxims**, we draw inferences beyond what's said.

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
These inferences are **conversational implicatures**. They're **cancelable**: retractable without contradiction. *Somewhere in the South of France, oh right, in **Marseille**!* (now we don't infer B doesn't know).

⚠️ Full list of properties: **context-dependent** ($9 vs. $10), **cancelable**, **calculable** (you can work them out from the maxims), **reinforceable** (saying them outright isn't redundant: *some, but not all*). They do **not** project through negation.

**Why they matter**:
1. They explain **efficiency**: we don't spell everything out.
2. **Plausible deniability**: it's more polite to implicate "I don't want to come," and more diplomatic to implicate "he's a bad philosopher."

⚠️ **Searle's hamburger**: order a hamburger and you expect it cooked, on a plate, not raw in plastic. We expect listeners to **share our unstated background assumptions** and **infer beyond what's said**.

**Appendix, *Bronston v. United States***:
> *Do you have any Swiss bank accounts?* — *No, sir.* — *Have you ever?* — *The **company** had an account for about six months in Zurich.*

- Implicature: Bronston **personally** never had one. In fact he did.
- The answer was **literally true**, and the Supreme Court held that **literally true but misleading testimony isn't perjury**. The law tracks what's **said**, not what's implicated.

## How conversations are organized
**Questions Under Discussion (QUD; Roberts 2012)**: conversations address implicit questions, and these define what's "relevant" and "enough info."
- *Tickets cost $10* → *I have $9* implicitly answers **"No"** to the QUD "Can you afford it?" (If B had $10, B would have said so.)
- *Tickets cost $9* → *I have $9* answers **"Yes"**. Having more is irrelevant to the QUD, so we don't infer B has only $9.

**Adjacency pairs** = **conventional pairings of discourse moves** (a first move scripts the reply):
- greeting/greeting · question/answer · invitation/acceptance or refusal · farewell/farewell
- **Cross-cultural variation**:
  - compliment → accept? return? reject? (Compliments are socially fraught because accepting can seem immodest and rejecting can seem rude.)
  - apology → reciprocal apology? acceptance? rejection?
  - thanks → "you're welcome"? downplay ("it was nothing")?

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
\node[a,fill=corg!15] (imp) at (6.5,0) {\textbf{IMPLICATURE}\\``It's late'' $\to$ ``I want to go home''\\(``...but I don't'' is fine)};
\node[q] (q2) at (0,-3) {Does it \textbf{project} (survive)\\under negation?};
\node[a,fill=cpur!15] (pre) at (6.5,-3) {\textbf{PRESUPPOSITION}\\``The King is (not) bald''\\$\to$ ``There's a King''};
\node[a,fill=cgrn!15] (ent) at (0,-6) {\textbf{ENTAILMENT}\\``I ran'' $\Rightarrow$ ``I exercised''\\``I didn't run'' $\not\Rightarrow$ ``I exercised''};
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

**Language is efficient** (all three): we infer beyond what's said (Grice), corpora favor **short dependencies**, and frequent words are **short** (Zipf).

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
| 41 | all of these ⚠️ | UP IS GOOD, TIME IS MONEY, WARS |
| 42 | fundamental to our thinking | |
| 43 | "hereby" | performatives |
| 44 | information we all mutually take for granted | |
| 45 | presupposition ⚠️ | factive *know* survives negation/questions |
| 46 | implicature | cancelable (*...and a pencil too*) |
| 47 | conventional pairing of discourse moves | |
| 48 | we infer lots beyond what's strictly said | |
| 49 | all of these | inference, short dependencies, short frequent words |
| 50 | server shares our unstated assumptions ⚠️ | Searle |

**Distractor decoder**
- **Binary/asymmetric/typed** = dependency grammar.
- **Cancelable** = implicature.
- **Projects through negation** = presupposition.
- **Time-stable** = nouns · **change** = verbs · **gradable/subjective** = adjectives.
- **Ablaut** = vowel change · **suppletion** = root swap · **concatenative** = affix.
- **Isolating** ≈ 1 morpheme/word · **agglutinating** = 1 meaning per affix · **fusional** = many meanings per affix · **polysynthetic** = sentence-words.
- **Homonymy** = accidental · **polysemy** = systematic · **metaphor** = abstract via concrete.
- **Ditransitive** = 3 arguments · **iterative** = repeated action (not a lecture term).
