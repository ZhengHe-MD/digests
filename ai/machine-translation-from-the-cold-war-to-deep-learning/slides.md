# 1993: Troyanskii's Translation Machine

![translation-machine](https://i.vas3k.ru/7c8.png)

1. direction word-translation by card + morphological characteristics as the "intermediate language"
2. further translated by linguists

---

# 1954: Georgetown - IBM experiment

Said to automatically translate 60 Russian sentences into English for the first time in history,
without details being revealed.

---

# A Brief History

1. Rule-based (1950 - 1980)
2. Example-based (1980 - 1990)
3. Statistical (1990 - 2015)
4. Neural Network (2015 - Now)

---

# RBMT (Rule-based machine translation)

Examples: PROMPT, Systran

- Bilingual dictionary (RU -> EN)
- A set of linguistic rules for each language

Suffered from irregularities of all natural languages

---

## RBMT variant 1: Direct Machine Translation

![dmt](https://i.vas3k.ru/7cb.png)

* Divides the text into words
* Translate each word with a dictionary
* slightly correct the morphology and harmonize syntax

---

## RBMT variant 2: Transfer-based Machine Translation

```
~~~graph-easy --as=boxart
[ source language text ] -> [ source grammatical structure ] -> [ target grammatical structure ] -> [ target language text ]
~~~
```

---

## RBMT variant 3: Interlingual Machine Translation

```
~~~graph-easy --as=boxart
[ Source language text ] -> [ unified intermediate representation ] -> [ Target language text ]
~~~
```

In real life, it was extremely hard to create such universal interlingua.

---

# EBMT (Example-based Machine Translation)

Using ready-made phrases instead of repeated translation.

1. Maintain a bunch of examples
2. Find the example closest to the target
3. Figure out the difference and translate the missing parts


- Closest: I'm going to the **cinema** -> 我想去**电影院**
- Translated: I'm going to the **theater** -> 我想去**剧院**

Shed a light on today's translation techniques.

---

# SMT (Statistical Machine Translation)

* Know nothing about the rules and linguistics
* Analyze similar texts in two languages and find patterns

The more texts we use, the better translation we get.
Google still use SMT today to get possible translations of a word or phrase.

---

## SMT variant 1: Word-based SMT

- Model 1: the bag of words - only consider word frequency stats
- Model 2: considering word order in the sentences
- Model 3: extra fertility
- Model 4: word alignment - relative order
- Model 5: bugfixes

Because every single word was translated in a single-true way,
word-based systems failed to deal with cases, gender and homonymy.

---

## SMT variant 2: Phrase-based SMT

Similar to word-based translation, 
except that it splits the text not only to words but also **phrases**,
the so-called n-grams.

Example: "not enough examples about translation"

* unigrams: not, enough, examples, about, translation
* bigrams: not enough, enough examples, examples about, about translation
* trigrams: not enough examples, enough examples about, examples about translation

> Every time I fire a linguist, the performance of the speech recognizer goes up. --- Frederick Jelinek

Word-based solution needs exact match of words from different languages, phrase-based solution don't need that.
Texts with the same meaning are enough, which is a more natural way intuitively.

Phrase-based solution kills until 2016.

---

## SMT variant 3: Syntax-based SMT

Many years before the emergence of the neural networks,
the syntax-based translation was considered as "the future of translation".
But the idea did not take off.

Similar to word-based and phrase-based solution, syntax-based splits the text in a syntactic way.

Why failed? The syntactic parsing works like shit.

---

# Neural Machine Translation (NMT)

Encoder-decoder model powered by neural network, starts with this [announcement](https://ai.googleblog.com/2016/09/a-neural-network-for-machine.html). The return of **Interlingua**.

---

# Future

- idea of "Babel fish" - the instant speech translation
- people can learn a language by exposing them to materials in that language, but machine needs parallel text blocks now

