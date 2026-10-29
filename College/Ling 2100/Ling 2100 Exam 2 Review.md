---
tags: [linguistics, ling2100, exam-prep]
---

# LING 2100 — Exam 2 Review

> [!abstract] Exam at a glance
> **Units:** 5 Morphology · 6 Syntax · 7 Semantics · 8 Pragmatics.
> **Format (practice exam):** multiple choice, heavy on definitions, classifying examples, and "which one is NOT..."
> **⚠️** = on the practice exam but not in the slides.
> Full explanations and diagrams: [[Ling 2100 Exam 2 Notes]].

---

## Unit 5 — Morphology

### Parts of speech

| POS | Must-know facts |
|---|---|
| Noun | subject/object; inflects for number; takes determiners; **time-stable entities** (exceptions: *explosion, **earthquake***) |
| Pronoun | stands in for a discourse-prominent noun; **only English words with case**: nominative *I/she/he*, accusative ***me**/her/him*, genitive *my/her/his* (Latin and Russian mark case on all nouns) |
| Verb | tense + subject agreement; describes **changes involving its arguments** (exception: *love*) |
| Adjective | modifies (*red dress*) or predicates (*is red*); gradable; *-er/-est*; can be subjective |
| Adverb | modifies V or Adj; often Adj + *-ly* |
| Determiner | *the/a/this/my/every/five*: new vs. familiar, near vs. far, possession, quantity |
| Preposition | introduces a non-main argument (*at the party*) |
| Modal | *can/would/might*: hypothetical states of affairs |

- **Transitivity**: intransitive = 1 argument (*I swam*) · transitive = 2 (*I threw the ball*) · **ditransitive = 3** (*I gave her the book*).
- POS is diagnosed by syntactic behavior and determines available morphology. **Automatic POS tagging** (spaCy displaCy) labels every word's POS; it's the first step of NLP.
- **Content (open class)** = N, V, Adj, Adv: easy to paraphrase, coined constantly. **Function (closed class)** = pronouns, determiners, conjunctions, prepositions, modals: hard to paraphrase, rarely new (*slash*), most frequent. Words that straddle the line: *want, cause, take a bath*.

### Inflection vs. derivation

| | Inflection | Derivation |
|---|---|---|
| Result | same word, new form | **new word** |
| POS change | **never** | often |
| Position | **outermost** | inside |
| Examples | *-s* (plural), *-s* (3sg), *-ed*, *-ing*, *-er/-est*, *she→her* (case = **declension**) | ***-ness***, *-ize*, *-er* (agent), *-able*, *-ly*, *-ity*, *un-*, *re-* |

- *-es* in *cranberries* = **bound, inflectional**. ***-ness*** = **derivational, bound**.
- POS change with **no affix**: *to **box*** (N→V), *a guitar **pick*** (V→N).
- Root changes shape: *clear→**clar**ify*, *antique→**antiqu**ity*.

| Inflection type | How | Example |
|---|---|---|
| **Concatenative** | add affix (**English plurals**) | *cat→cats* |
| **Ablaut** | change vowel | *man/men, sing/sang* |
| **Suppletion** | replace root | ***good/better/best***, *be/am/was* |

⚠️ **Not suppletion**: *child/children*, *sheep/sheep*, *chair/furniture*.

- Irregulars survive on **frequent** words; *holp* → *helped*; *dived/dove* still varies.
- French: determiners, adjectives, and verbs all inflect (*la belle maison*; *J'aimerais* = like.1SG.COND).

### Morphemes and word structure
- **Morpheme** = smallest meaningful unit. **Free** (*car, I*) vs. **bound** (*-ing, un-, -s*).
- **Cranberry morphemes** (*cran-, rasp-*) occur in only one word. *-ceive* (*re/de/perceive*) recurs as a form with no clear meaning. *Under+stand* isn't compositional. *Pulver-* is a bound root.
- **Unpaired words** (Jack Winter, *New Yorker*): *chalant, gruntled, kempt, shevelled* are funny because the base never exists alone (a cranberry-like bound root).
- **Word** = root + derivational affixes + inflectional affixes (outermost). *nation+al+ize+s*.
- **Affixes**: prefix *repay* · suffix *paying* · **circumfix** ***en**light**en*** · infix (English only *abso-effing-lutely*). WALS maps case (51A), prefixing vs. suffixing (26A), and reduplication (27A).
- **Words are hierarchical** (trees), not beads on a string: *-al* needs a N, *-ize* an Adj/N, *-ation* a V → \**nationation*, \**nationizeal*; ?*nationize*.
- **Ambiguity from structure**:
  - *unlockable* = `[[un-lock]V -able]` "can be unlocked" / `[un- [lock-able]Adj]` "can't be locked"
  - ***inflammable*** = `[[in-flame]V -able]` **"can become inflamed"** (the real meaning; pick the tree with *inflame* as a Verb) / `[in- [flammable]Adj]` "not flammable" → hence *flammable*
  - *American art teacher* = `[[American art] teacher]` / `[American [art teacher]]`

### New words

| Process | Slide examples | ⚠️ Slang examples |
|---|---|---|
| **Compound** (2 whole words) | *desk chair, sunglasses, work wife* | ***brainrot**, doomscroll, ragebait, short king, girl math* |
| **Derivation** | *monoamorous, girlbossification* | ***enshittification**, unserious, yassify* |
| **Blend** (parts of 2) | *brunch, smog, motel, copaganda* | ***Brexit**, covidiot, mansplain, cronut* |
| **Clipping** (1 word cut) | *gym, math, mic* | ***rizz** (charisma), sus, vax* |
| **Acronym** | *NASA, radar, DM, BFF, AF* | *NFT, FOMO, YOLO* |
| **Borrowing** | *karaoke, sauna, algebra, tattoo, canoe, kayak* | |
| **Back-formation** | *enthuse* (← *enthusiasm*) | |
| **Genericization** | *Kleenex, Xerox, Uber*; the Tiffany vs. Costco ring lawsuit | |
| **From names** | *sandwich, robot, jumbo* | |

⚠️ *clock* (N→V) = no-affix POS change; *hold space / locked in / 6-7* = phrases, not word formation. The dictionary follows usage; it isn't the authority.

### Zipf and corpora
- **Frequency Law**: a few very frequent (function) words, very many rare (content) words → **power law**, not normal.
- **Brevity Law**: **frequent words are shorter** (language is efficient).
- **Word-type length ≈ bell curve, peak = 7 characters.** (Counting tokens gives shorter lengths, since frequent words are short.)
- Log axis because frequencies span orders of magnitude. *The* is #1 (Brown 7%, Reddit 3%); Reddit ranks *i/my/you* high.

### Typology

| Type | Key | Language |
|---|---|---|
| **Isolating** | ~1 morpheme/word | Yoruba |
| **Agglutinating** | many affixes, **1 meaning each** (*ev-imiz-de* "house-our-in") | Turkish |
| **Polysynthetic** | sentence = one word | Yupik |
| **Fusional** | one affix = **several meanings** (*était*) | French |
| **Analytic** | between isolating & agglutinating | English |

### Appendix bits
- **Reduplication**: *salad salad*; iconic ("more is more"); Sapir 1921.
- **Compounds**: artifact heads → use relations (*water jug*); natural-kind heads → appearance/habitat (*water spinach*).
- **Pumpkin spice**: FOR vs. OF pumpkin is ambiguous (the Food Babe missed this).
- **"The old"**: plural = old people / mass = oldness.

---

## Unit 6 — Syntax

- **Syntax** = word order; grammatical vs. \*ungrammatical; finite rules → infinite sentences.
- **Independent of semantics** (Chomsky): *Colorless green ideas sleep furiously* = **grammatical, meaningless**; ***Me eat cookie*** = **ungrammatical, somewhat meaningful**. The line is fuzzy (*?The toothbrush is pregnant*).
- **English facts**:
  - SVO
  - object fronting only when contrastive
  - Adj before N
  - polar question = **do-support + inversion**; *Will...?* = subject–auxiliary inversion
  - negation uses do-support
  - subject/object relative clauses; subject/object/multiple wh-questions
- **Long-distance dependency** = related words separated (*What did you eat ___?*; *the book that I read ___*). ⚠️ Agreement counts too: ***key** ... **is*** in *The key to the cabinets is on the table*.
- Watch for gender stereotypes in constructed example sentences.

### Constituents
- Language is **produced linearly but mentally organized hierarchically**.
- **Tests** (any YES = constituent):
  1. it can answer a question
  2. it sticks together when reordered
  3. it can be conjoined
- *The history of linguistics begins with the Indian grammarian Panini*: ✓ *the history of linguistics, of linguistics, the Indian grammarian Panini, begins with...Panini* · ✗ *linguistics begins with the, begins with the Indian*.
- Constituent = **subtree**. *The athlete tossed the ball*: ✓ *the athlete, the ball, tossed the ball* · ✗ *athlete tossed the, tossed the*.
- **Lexical categories** (Det, N, TransV...) vs. **phrasal categories** (NP, VP, AdjP); swap within a category ("Mad Libs").

### Phrase Structure Grammar (Chomsky, 1950s)
```
S -> NP VP     NP -> (Det)(Adj*) N     NP -> NP (PP)     NP -> Pronoun
PP -> Prep NP  VP -> TransV NP         VP -> IntransV    VP -> VP PP
```
- Rules = **non-terminals**; **lexicon** = terminals (words). `()` optional, `*` = 0 or more. Draw trees with mshang.ca/syntree, LaTeX/Overleaf, or by hand.
- Correct tree for *The author wrote the book*: **[S [NP the author] [VP wrote [NP the book]]]** (a flat tree, or a split *the / book*, is wrong).

| PS rules ARE | PS rules are NOT |
|---|---|
| **generative**, **recursive** (NP→NP PP, PP→P NP), **one-to-many** (**VP→V NP; VP→V**), **language-specific** | language-general · binary/asymmetric/typed (that's dependency) · cancelable (implicature) · inflectional |

- **Transformations/movement** = extra rules for long-distance dependencies (a metaphor, not literal): *what* moves from object position to the front, into a CP layer above S.

### Dependency grammar
- **Tesnière**; inspired by free-word-order **Latin/Slavic** (*Puella canem amat* in any order; case marks roles; given before new).
- **Binary, asymmetric, typed** head→dependent relations between **POS-tagged** words (DET, NSUBJ, OBJ, AUX). **Verb = root**.
- **Pros**:
  - works for any word order → **NLP**, **Universal Dependencies** (100+ languages)
  - word-based, fewer abstractions
  - long-distance dependency = just a longer arc
  - corpora (37 languages) favor **short dependencies** (efficient)
- **Cons**: doesn't capture a language's word order, grammaticality judgments, or rules.
- **NLP uses dependency parsing** (not PS trees, not Grice).

### Ambiguity types
- **Structural**: *Pope's Baby Steps on Gays, MBA Studies Mushroom, Hospital sued by 7 foot doctors, Lawyers give poor free legal advice, Complaints about referees growing ugly, Time for football and meatball stew*.
- **Lexical**: *Iraqi Head Seeks Arms*.
- **Event participation**: *Kids make nutritious snacks, Include your children when baking cookies, Pillars replaced by alumni, Stolen painting found by tree*.

### Fieldwork

| | Mandarin | French |
|---|---|---|
| Adj–N | before (*de*) | after |
| Negation | *méi-yǒu* | *ne...pas* |
| Past | aspect *le*, no tense | aux + participle |
| Articles | none (numeral + classifier) | *un/le* |
| Yes/no question | final *ma* | *est-ce que* |
| Wh-question | in place | fronted |
| Relative clause | before N | after N (*que*) |

- **Ethics**: give back to minoritized communities (books, archives, dictionaries, writing systems, documentaries like *Talking Black in America*, MIT Indigenous Language program), not just paywalled papers.
- **Methods questions**: how many examples? speaker's role? spoken/written/glossed? language of elicitation? did the speaker understand the question?

---

## Unit 7 — Semantics

- **Semantics** = meaning of words and sentences; **pragmatics** = inferences from utterances in context. Lewis: ask what meaning *does*.
- Word meaning = referent (if any; *unicorn* has none but is still meaningful) + relations (*cat* ⊂ *animal*) + use in sentences.
- Sentence meaning = **truth conditions**, **entailment** (*cat → pet*), **contradiction** (*cat* vs. *no pets*).
- **Lexical** (content words) vs. **compositional** (function words; combining meanings).

### Word relations

| | Key |
|---|---|
| Synonym / antonym | *couch/sofa*; *tall/short* (antonyms are mostly adjectives because of gradable scales) |
| Marked / unmarked | *How tall* (neutral) vs. *How short* (assumes short); *?5 ft short* |
| **Homonymy** | unrelated, **accidental**, won't recur cross-linguistically: *bank*, ***for/four*** |
| **Polysemy** | related, **systematic**, may recur: *head*, *dinner* (food/event), *book* (object/content), *White House*; ⚠️ ***lamb*** (animal/meat) |

- Languages differ in categories: French *J'ai faim* (noun for "hungry"); Persian light verbs ("do a run").
- ⚠️ **Most astonishing**: a language with **no nouns** (lacking tense, "the," or "purple" is common).

### Who decides meaning?
- **Experts**: ***carbohydrate***, *quark*, *whale*; ⚠️ *polygon* (spirals aren't polygons = **True**).
- **Everyone**: *sandwich* (burrito case: Panera v. Qdoba), *soup*, *woman*, *person*, *champagne*. *Planet* changed with astrophysics.
- **Wittgenstein's *game*** = **family resemblance**, no strict boundaries; a problem for law (is a borderline tumor "cancer"? Jessica Rett).
- **Labov's cups** show fuzzy, gradient category boundaries.

### Nouns
- **Relational** (*sister*) vs. **sortal** (*sheep*): *?the sheep of my friend*.
- **Mass** (*water, mail, **furniture***) vs. **count** (*books, letters*). "More furniture" is judged by **number of pieces**.
- **Artifact** (purpose; *stapler*, *start a book*) vs. **natural kind** (essence; *bear*). ***Finish a sandwich* = make/eat it, because a sandwich is an artifact.**

### Verbs
- **Dynamic** (*threw*) vs. **stative** (*loved*); **agentive** (*ran*) vs. **non-agentive** (*fell*).
- **Telic** (endpoint; *in an hour*: *ate the pizza*) vs. **atelic** (*for an hour*: *ate pizza*, ***watched TV***). Stative sentences overlap in time; events follow in sequence.
- **Argument structure**: *the ship sank* (patient as subject) vs. *the athlete lifted* (agent, object dropped).
- **Causative**: *broke → the fence broke* ✓; *hit → ?the fence hit*.

### Adjectives
- **Gradable** (*taller*) vs. not (*?deader*). **Vague**: depends on comparison class.
- **Subjective → faultless disagreement**: ***"Roller coasters are fun."***
- **Scontras et al. 2017**: **more subjective adjectives sit further from the noun** (*cute red dress*). Glass 2025: subjective adjectives prefer predicate position.
- **Intersective** (***American**, Swedish*) · **subsective** (*skillful, important*) · **privative** (*former, fake*) · *plastic* depends on the noun.

### Other word types
- **Deixis** (context-pointing): *I, me, you, here, now, today, tomorrow*. **Not** *beautiful*.
- **Expressives** (*damn*) and **slurs** add attitude without changing truth conditions.

### Metaphor (Lakoff & Johnson 1980)
- **Fundamental to thought**, not decoration: abstract via concrete.
- TIME IS MONEY · TIME IS SPACE · GOOD IS UP · UNDERSTANDING IS VISION · ARGUMENTS ARE WARS · PROJECTS ARE MEALS / BUILDINGS.
- History runs concrete → abstract (*stands*); see the Database of Semantic Shifts (datsemshift.ru).
- ⚠️ *heavy topic* = **metaphor** (simile uses *like*; allegory = extended story). *Morale is **low**... **wasting** time **battling**...* = **all of these**.

### Composition
- **Lambda calculus**: types *e* (individuals), *t* (truth values); *swim* = λx[swim(x)] : ⟨e,t⟩, applied to **Lelia** : e → swim(Lelia) : t.
- **Heim**: *a* = add a new referent; *the* = find a familiar one. **Bridging**: *a car... the seat*.

---

## Unit 8 — Pragmatics

- Linguists **have tried to identify general rules** of conversation.
- **Speech acts (Austin)**: **performatives** make themselves true when said by the right person in the right context; marked by ***hereby*** (*I now pronounce you...*, *You're fired*).
- **Common Ground** = info **mutually taken for granted** (Stalnaker, Grice), e.g. we're at Georgia Tech, speaking English. It requires Theory of Mind. **Assertions = proposals** to update it: *I'm from Maryland* gets accepted and added; *No, it's due Wednesday* rejects one.

### Presupposition
- Assumed to be in the CG; if false, the sentence is **nonsensical** (Strawson's *King of France*: you have to "rewind").
- **Projects through negation**, modals, and questions.
- Triggers: *the*, *stop* (*Phil stopped smoking* → he used to smoke), ⚠️ **factive *know*** (*Sam knows it's raining* → it's raining).

### Grice
- **Maxims**: **Quality** (truth) · **Quantity** (as informative as needed) · **Manner** (clarity) · **Relevance**. ⚠️ **Politeness is NOT one.** They're phrased as commands but are descriptive (the assumptions listeners use). Critique: they may be Eurocentric.
- By assuming cooperation, we **infer beyond what's said** (the same point as Levinson's Rembrandt sketch, and ⚠️ **Searle's hamburger**: listeners share unstated assumptions).
- **Examples**:
  - garage around the corner → it's open
  - *some* students → **not all** (**scalar implicature**)
  - penmanship letter → bad philosopher
  - *Well, I have to grade* → no (dispreferred reply)
  - *South of France* → doesn't know exactly
  - *I speak Portuguese* / ⚠️ *I have a pen* → not Spanish / no pencil
  - $10 tickets, *I have $9* → not $10 (but no such inference with $9 tickets)
- **Implicatures** = ⚠️ **context-dependent, cancelable** (*South of France, oh, Marseille!*), **calculable, reinforceable**. Benefits: efficiency and **plausible deniability** (politeness).
- **Bronston**: a literally true but misleading answer isn't perjury.

### Conversation structure
- **QUD (Roberts 2012)** defines relevance ($9 vs. $10).
- **Adjacency pair** = **conventional pairing of discourse moves** (greeting/greeting, question/answer, invitation/acceptance or refusal); varies cross-culturally (compliments, apologies, thanks).

### Inference test

| | Cancelable? | Survives negation? |
|---|---|---|
| **Entailment** (*ran → exercised*) | ✗ | ✗ |
| **Presupposition** (*the King → a King exists*) | ✗ | ✓ |
| **Implicature** (*late → want to go home*) | ✓ | — |

**Language is efficient** = all of these: we infer beyond what's said, dependencies are short, frequent words are short.

---

## Exam traps
- **Binary/asymmetric/typed** → dependency · **cancelable** → implicature · **projects** → presupposition.
- **Time-stable** → nouns · **change** → verbs · **gradable/subjective** → adjectives.
- **Homonymy** = accidental (*for/four*) · **polysemy** = systematic (*lamb*) · **metaphor** = abstract via concrete (*clear* idea).
- **Ablaut** = vowel · **suppletion** = root swap · **concatenative** = affix.
- **Agglutinating** = 1 meaning/affix ≠ **fusional** = many meanings/affix.
- One-to-many needs the **same left side**; NP→NP PP + PP→P NP is **recursion**.
- *Me eat cookie* = ungrammatical but meaningful (≠ *colorless green ideas*).
- Word-type length peak = **7**.
