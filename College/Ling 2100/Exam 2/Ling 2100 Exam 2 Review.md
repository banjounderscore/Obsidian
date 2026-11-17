---
tags: [linguistics, ling2100, exam-prep]
---

# LING 2100 — Exam 2 Review

> [!abstract] Exam at a glance
> **Units:** 5 Morphology · 6 Syntax · 7 Semantics · 8 Pragmatics.
> **Format (practice exam):** multiple choice, heavy on definitions, classifying examples, and "which one is *not*..."
> **⚠️** = on the practice exam but not in the slides.
> Full explanations and diagrams: [[Ling 2100 Exam 2 Notes]].

---

## Unit 5 — Morphology

### Parts of speech
POS is diagnosed by syntactic behavior and determines available morphology. **Automatic POS tagging** (spaCy displaCy) labels every word's POS; it's the first step of NLP.

| POS | Must-know facts |
|---|---|
| Noun | subject/object; inflects for number; takes determiners; **time-stable entities** (exceptions: *explosion, **earthquake***) |
| Pronoun | stands in for a discourse-prominent noun; **only English words with case** (Latin and Russian mark case on all nouns) |
| Verb | tense + subject agreement; describes **changes involving its arguments** (exception: *love*) |
| Adjective | modifies (*red dress*) or predicates with copula *is* (*is red*); gradable; *-er/-est*; can be subjective |
| Adverb | modifies V or Adj; often Adj + *-ly* |
| Determiner | *the/a/this/my/every/five*: new vs. familiar, near vs. far, possession, quantity |
| Preposition | introduces a non-main argument (*at the party*) |
| Modal | *can/would/might*: hypothetical states of affairs |

| Case | Forms |
|---|---|
| Nominative | *I, she, he* |
| Accusative | ***me**, her, him* |
| Genitive | *my, her, his* |

| Transitivity | Arguments | Example |
|---|---|---|
| Intransitive | 1 | *I swam* |
| Transitive | 2 | *I threw the ball* |
| **Ditransitive** | **3** | *I gave her the book* |

| | Content (open class) | Function (closed class) |
|---|---|---|
| Categories | N, V, Adj, Adv | pronouns, determiners, conjunctions, prepositions, modals |
| Paraphrase | easy | hard |
| New ones | coined constantly | rare (*slash*) |
| Frequency | mostly rare | most frequent |

Words that straddle the line: *want, cause, take a bath*.

### Inflection vs. derivation

| | Inflection | Derivation |
|---|---|---|
| Result | same word, new form | **new word** |
| POS change | **never** | often |
| Position | **outermost** | inside |
| Examples | *-s* (plural), *-s* (3sg), *-ed*, *-ing*, *-er/-est*, *she→her* (case = **declension**) | ***-ness***, *-ize*, *-er* (agent), *-able*, *-ly*, *-ity*, *un-*, *re-* |

- POS change with **no affix**: *to **box*** (N→V), *a guitar **pick*** (V→N).
- Root can change shape: *clear→**clar**ify*, *antique→**antiqu**ity*.

| Inflection type | How | Example |
|---|---|---|
| **Concatenative** | add affix (**English plurals**) | *cat→cats* |
| **Ablaut** | change vowel | *man/men, sing/sang* |
| **Suppletion** | replace root | ***good/better/best***, *be/am/was* |

⚠️ **Not suppletion**: *child/children*, *sheep/sheep*, *chair/furniture*.

- Irregulars survive on **frequent** words; *holp* → *helped*; *dived/dove* still varies.
- French inflects more: determiners, adjectives, verbs (*la belle maison*; *J'aimerais* = like.1SG.COND).

### Morphemes and word structure

| Term | Meaning | Example |
|---|---|---|
| **Morpheme** | smallest meaningful unit | *walk + -ing* |
| **Free** morpheme | can stand alone | *car, I* |
| **Bound** morpheme | can't stand alone | *-ing, un-, -s* |
| **Cranberry morpheme** | bound, occurs in only one word | *cran-, rasp-* |
| **Unpaired word** (Jack Winter, *New Yorker*) | base never exists alone | *chalant, gruntled, kempt, shevelled* |

- *-es* in *cranberries* = **bound, inflectional**; ***-ness*** = **bound, derivational**.
- Forms without clear meaning: *-ceive* (*re/de/perceive*); *Under+stand* isn't compositional; *pulver-* = bound root.
- **Word structure** = root + derivational + inflectional (outermost): *nation+al+ize+s*.

| Affix | Position | Example |
|---|---|---|
| Prefix | before | *repay* |
| Suffix | after | *paying* |
| **Circumfix** | both sides | ***en**light**en*** |
| Infix | inside | English only *abso-effing-lutely* |

WALS maps case (51A), prefixing vs. suffixing (26A), and reduplication (27A).

**Words are hierarchical** (trees), not beads on a string: *-al* needs a N, *-ize* an Adj/N, *-ation* a V → \**nationation*, \**nationizeal*; ?*nationize*.

| Ambiguous form | Structure 1 | Structure 2 |
|---|---|---|
| *unlockable* | `[[un-lock]V -able]` "can be unlocked" | `[un- [lock-able]Adj]` "can't be locked" |
| ***inflammable*** | `[[in-flame]V -able]` **"can become inflamed"** (real meaning; pick the tree with *inflame* as a Verb) | `[in- [flammable]Adj]` "not flammable" → hence *flammable* |
| *American art teacher* | `[[American art] teacher]` | `[American [art teacher]]` |

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
| ⚠️ **POS change, no affix** | | *clock* (N→V) |
| ⚠️ **Phrases, not word formation** | | *hold space, locked in, 6-7* |

The dictionary follows usage; it isn't the authority.

### Zipf and corpora

| Law | Statement |
|---|---|
| **Frequency Law** | a few very frequent (function) words, very many rare (content) words → **power law**, not normal |
| **Brevity Law** | **frequent words are shorter** (language is efficient) |
| **Word-type length** | ≈ bell curve, **peak = 7 characters** |

- Counting tokens gives shorter lengths, since frequent words are short.
- Log axis because frequencies span orders of magnitude.
- *The* is #1 (Brown 7%, Reddit 3%); Reddit ranks *i/my/you* high.

### Typology

| Type | Key | Language |
|---|---|---|
| **Isolating** | ~1 morpheme/word | Yoruba |
| **Agglutinating** | many affixes, **1 meaning each**: *ev-imiz-de* = house + our + in | Turkish |
| **Polysynthetic** | sentence = one word | Yupik |
| **Fusional** | one affix = **several meanings**: *-ait* in *était* = 3rd person + singular + imperfective | French |
| **Analytic** | between isolating & agglutinating | English |

### Appendix bits
- **Reduplication**: *salad salad*; iconic ("more is more"); Sapir 1921.
- **Compounds**: artifact heads → use relations (*water jug*); natural-kind heads → appearance/habitat (*water spinach*).
- **Pumpkin spice**: spice *for* vs. *of* pumpkin is ambiguous (the Food Babe missed this).
- **"The old"**: plural = old people / mass = oldness.

---

## Unit 6 — Syntax

- **Syntax** = word order; grammatical vs. \*ungrammatical; finite rules → infinite sentences.
- Syntax and semantics are independent (Chomsky): *Colorless green ideas sleep furiously* = **grammatical, meaningless**; ***Me eat cookie*** = **ungrammatical, somewhat meaningful**. The line is fuzzy (*?The toothbrush is pregnant*).
- Watch for gender stereotypes in constructed example sentences.

| English fact | Example |
|---|---|
| SVO | *The student read the book* |
| Object fronting (contrastive only) | *The book, the student read* |
| Adj before N | *the clever student* |
| Polar question = **do-support + inversion** | *Did the student read it?* |
| Subject–auxiliary inversion | *Will the student read it?* |
| Negation uses do-support | *did not read* |
| Relative clauses / wh-questions | subject and object relatives; subject, object, multiple wh-questions |
| **Long-distance dependency** | *What did you eat ___?* (*what* = object of *eat*) |

More long-distance dependencies:
- *The book that I read ___ is on the table* (*the book* = object of *read*)
- ⚠️ Agreement: *The **key** to the cabinets **is** on the table* (*key* ↔ *is*, skipping *cabinets*)

### Constituents
Language is **produced linearly but mentally organized hierarchically**. Constituent = **subtree**.

Tests (any yes = constituent):
1. can answer a question
2. sticks together when reordered
3. can be conjoined

| Sentence | ✓ Constituents | ✗ Not |
|---|---|---|
| *The history of linguistics begins with the Indian grammarian Panini* | *the history of linguistics, of linguistics, the Indian grammarian Panini, begins with...Panini* | *linguistics begins with the, begins with the Indian* |
| *The athlete tossed the ball* | *the athlete, the ball, tossed the ball* | *athlete tossed the, tossed the* |

| Lexical categories | Phrasal categories |
|---|---|
| Det, N, TransV... | NP, VP, AdjP |
| swap word for word ("Mad Libs") | swap phrase for phrase |

### Phrase Structure Grammar (Chomsky, 1950s)

| Expands | Rules |
|---|---|
| S | `S -> NP VP` |
| NP | `NP -> (Det)(Adj*) N` · `NP -> NP (PP)` · `NP -> Pronoun` |
| VP | `VP -> TransV NP` · `VP -> IntransV` · `VP -> VP PP` |
| PP | `PP -> Prep NP` |

- Rules = **non-terminals**; **lexicon** = terminals (words). `()` optional, `*` = 0 or more.
- Correct tree for *The author wrote the book*: **[S [NP the author] [VP wrote [NP the book]]]**; a flat tree, or *the / book* split, is wrong.
- Drawing tools: mshang.ca/syntree, LaTeX/Overleaf, by hand.
- **Transformations/movement** = extra rules for long-distance dependencies (a metaphor): *what* moves from object position to the front, into a CP layer above S.

| PS rules are | PS rules are not |
|---|---|
| **generative**, **recursive** (NP→NP PP, PP→P NP), **one-to-many** (**VP→V NP; VP→V**), **language-specific** | language-general · binary/asymmetric/typed (that's dependency) · cancelable (implicature) · inflectional |

### Dependency grammar
- **Tesnière**; inspired by free-word-order **Latin/Slavic** (*Puella canem amat* in any order; case marks roles; given before new).
- **Binary, asymmetric, typed** head→dependent relations between **POS-tagged** words (DET, NSUBJ, OBJ, AUX); **verb = root**.
- **Pros**: works for any word order → **NLP**, **Universal Dependencies** (100+ languages); word-based, fewer abstractions; long-distance dependency = just a longer arc; corpora (37 languages) favor **short dependencies** (efficient).
- **Cons**: doesn't capture a language's word order, grammaticality judgments, or rules.
- **NLP uses dependency parsing** (not PS trees, not Grice).

### Ambiguity types

| Headline | Type | The two readings |
|---|---|---|
| *Pope's Baby Steps on Gays* | structural | baby **steps on** / **baby steps** on |
| *MBA Studies Mushroom* | structural | studies **grow** / MBA **studies** a mushroom |
| *Hospital sued by 7 foot doctors* | structural | **7-foot** doctors / 7 **foot doctors** |
| *Lawyers give poor free legal advice* | structural | to **poor people** / **low-quality** advice |
| *Complaints about referees growing ugly* | structural | **complaints** grow ugly / **referees** grow ugly |
| *Time for football and meatball stew* | structural | football, and meatball stew / football-and-meatball stew |
| *Iraqi Head Seeks Arms* | lexical | leader seeks weapons / head seeks limbs |
| *Kids make nutritious snacks* | event participation | kids **prepare** / kids **are** snacks |
| *Include your children when baking cookies* | event participation | as helpers / as **ingredients** |
| *Pillars replaced by alumni* | event participation | alumni **paid** / alumni **are** pillars |
| *Stolen painting found by tree* | event participation | **near** a tree / a tree **found** it |

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

- **Methods**: how many examples? speaker's role? spoken/written/glossed? language of elicitation? did the speaker understand the question?
- **Ethics**: give back to minoritized communities (books, archives, dictionaries, writing systems, documentaries like *Talking Black in America*, MIT Indigenous Language program), not just paywalled papers.

---

## Unit 7 — Semantics

| Term | Meaning |
|---|---|
| **Semantics** | meaning of words and sentences |
| **Pragmatics** | inferences from utterances in context |
| **Truth conditions** | what the world must be like for a sentence to be true |
| **Entailment** | if A is true, B must be (*cat → pet*) |
| **Contradiction** | A and B can't both be true (*has a cat* vs. *has no pets*) |
| **Lexical semantics** | meaning of content words |
| **Compositional semantics** | meaning of function words; combining meanings |

- Lewis: ask what meaning *does*.
- Word meaning = referent (if any; *unicorn* has none but is still meaningful) + relations (*cat* ⊂ *animal*) + use in sentences.

### Word relations

| Relation | Key |
|---|---|
| Synonym / antonym | *couch/sofa*; *tall/short* (antonyms are mostly adjectives because of gradable scales) |
| Marked / unmarked | *How tall* (neutral) vs. *How short* (assumes short); *?5 ft short* |
| **Homonymy** | unrelated, **accidental**, won't recur cross-linguistically: *bank*, ***for/four*** |
| **Polysemy** | related, **systematic**, may recur: *dinner* (food / event), *book* (object / content), ⚠️ ***lamb*** (animal / meat) |

- Languages differ in categories: French *J'ai faim* (noun for "hungry"); Persian light verbs ("do a run").
- ⚠️ **Most astonishing**: a language with **no nouns** (lacking tense, "the," or "purple" is common).

### Who decides meaning?

| Who | Examples |
|---|---|
| **Experts** | ***carbohydrate***, *quark*, *whale*; ⚠️ *polygon* (spirals aren't polygons = **True**) |
| **Everyone** | *sandwich* (burrito case: Panera v. Qdoba), *soup*, *woman*, *person*, *champagne* |
| Changed over time | *planet* (with astrophysics) |

- **Wittgenstein's *game*** = **family resemblance**, no strict boundaries; a problem for law (is a borderline tumor "cancer"? Jessica Rett).
- **Labov's cups**: fuzzy, gradient category boundaries.

### Nouns, verbs, adjectives

| Term | Meaning / example |
|---|---|
| **Relational** vs. **sortal** | *sister* vs. *sheep*: *?the sheep of my friend* |
| **Mass** vs. **count** | *water, mail, **furniture*** vs. *books, letters*; "more furniture" is judged by **number of pieces** |
| **Artifact** vs. **natural kind** | purpose (*stapler*, *start a book*) vs. essence (*bear*). ***Finish a sandwich* = make/eat it, because a sandwich is an artifact** |
| **Dynamic** vs. **stative** | *threw* vs. *loved*; stative sentences overlap in time, events follow in sequence |
| **Agentive** vs. **non-agentive** | *ran* vs. *fell* |
| **Telic** vs. **atelic** | endpoint, *in an hour* (*ate the pizza*) vs. *for an hour* (*ate pizza*, ***watched TV***) |
| **Argument structure** | *the ship sank* (patient as subject) vs. *the athlete lifted* (agent, object dropped) |
| **Causative** | *broke → the fence broke* ✓; *hit → ?the fence hit* |
| **Gradable** | *taller* vs. *?deader* |
| **Vague** | depends on comparison class |
| **Subjective** | **faultless disagreement**: ***"Roller coasters are fun."*** |
| **Intersective** · **subsective** · **privative** | ***American**, Swedish* · *skillful, important* · *former, fake*; *plastic* depends on the noun |

- **Scontras et al. 2017**: **more subjective adjectives sit further from the noun** (*cute red dress*).
- Glass 2025: subjective adjectives prefer predicate position.

### Other word types

| Type | Key |
|---|---|
| **Deixis** (context-pointing) | *I, me, you, here, now, today, tomorrow*. **Not** *beautiful* |
| **Expressives** (*damn*) and **slurs** | add attitude without changing truth conditions |
| ⚠️ **Metaphor** vs. **simile** vs. **allegory** | *a heavy topic* (no "like") vs. *a topic like a heavy rock* (uses *like/as*) vs. a whole story standing for ideas (*Animal Farm* = the Russian Revolution) |

### Metaphor (Lakoff & Johnson 1980)
- **Fundamental to thought**, not decoration: abstract via concrete.
- Time is money · Time is space · Good is up · Understanding is vision · Arguments are wars · Projects are meals / buildings.
- History runs concrete → abstract (*stands*); see the Database of Semantic Shifts (datsemshift.ru).
- ⚠️ *Morale is **low**... **wasting** time **battling**...* = **all of these**.

### Composition

| Term | Meaning |
|---|---|
| **Lambda calculus** | types *e* (individuals), *t* (truth values); *swim* = λx[swim(x)] : ⟨e,t⟩, applied to **Lelia** : e → swim(Lelia) : t |
| *a* (Heim) | add a new referent |
| *the* (Heim) | find a familiar referent |
| **Bridging** | *the* for something implied by context: *a car... the seat* |

---

## Unit 8 — Pragmatics

Linguists **have tried to identify general rules** of conversation.

| Term | Meaning |
|---|---|
| **Performative** (Austin) | an utterance that makes itself true when said by the right person in the right context; marked by ***hereby*** (*I now pronounce you...*, *You're fired*) |
| **Common Ground** | info **mutually taken for granted** (Stalnaker, Grice), e.g. we're at Georgia Tech, speaking English; requires Theory of Mind |
| **Assertion** | a **proposal** to update the CG: *I'm from Maryland* is accepted and added; *No, it's due Wednesday* rejects one |
| **Presupposition** | assumed to be in the CG; if false, the sentence is **nonsensical** (Strawson's *King of France*: you have to "rewind"). **Projects through negation**, modals, and questions |

| Presupposition trigger | Example → presupposition |
|---|---|
| *the* | *The King of France is bald* → there is one |
| *stop* | *Phil stopped smoking* → he used to smoke |
| ⚠️ **factive *know*** | *Sam knows it's raining* → it's raining |

### Grice

| Maxim | Rule |
|---|---|
| **Quality** | truth |
| **Quantity** | as informative as needed |
| **Manner** | clarity |
| **Relevance** | stay on topic |
| ⚠️ ~~Politeness~~ | **not a maxim** |

- The maxims are phrased as commands but are descriptive (the assumptions listeners use); critique: they may be Eurocentric.
- By assuming cooperation, we **infer beyond what's said**. Same point as Levinson's Rembrandt sketch, and ⚠️ **Searle's hamburger** (listeners share unstated assumptions).

| Utterance | Inference |
|---|---|
| garage around the corner | it's open |
| *some* students | **not all** (**scalar implicature**) |
| penmanship letter | bad philosopher |
| *Well, I have to grade* | no (dispreferred reply) |
| *South of France* | doesn't know exactly |
| *I speak Portuguese* / ⚠️ *I have a pen* | not Spanish / no pencil |
| $10 tickets, *I have $9* | not $10 (no such inference with $9 tickets) |

- **Implicatures** are ⚠️ **context-dependent, cancelable** (*South of France, oh, Marseille!*), **calculable, reinforceable**.
- Benefits: efficiency and **plausible deniability** (politeness).
- **Bronston**: a literally true but misleading answer isn't perjury.

### Conversation structure

| Term | Meaning |
|---|---|
| **QUD** (Roberts 2012) | the implicit question a conversation addresses; defines relevance ($9 vs. $10) |
| **Adjacency pair** | **conventional pairing of discourse moves** (greeting/greeting, question/answer, invitation/acceptance or refusal); varies cross-culturally (compliments, apologies, thanks) |

### Inference test

| | Cancelable? | Survives negation? |
|---|---|---|
| **Entailment** (*ran → exercised*) | ✗ | ✗ |
| **Presupposition** (*the King → a King exists*) | ✗ | ✓ |
| **Implicature** (*late → want to go home*) | ✓ | — |

**Language is efficient** = all of these: we infer beyond what's said, dependencies are short, frequent words are short.

---

## Exam traps

| If the option says... | It's about |
|---|---|
| binary / asymmetric / typed | dependency grammar |
| cancelable | implicature |
| projects | presupposition |
| time-stable | nouns |
| change | verbs |
| gradable / subjective | adjectives |
| accidental (*for/four*) | homonymy |
| systematic (*lamb*) | polysemy |
| abstract via concrete (*clear* idea) | metaphor |
| vowel · root swap · affix | ablaut · suppletion · concatenative |
| 1 meaning/affix vs. many meanings/affix | agglutinating vs. fusional |
| NP→NP PP + PP→P NP | **recursion** (one-to-many needs the same left side) |
| *Me eat cookie* | ungrammatical but meaningful (≠ *colorless green ideas*) |
| word-type length peak | **7** |
