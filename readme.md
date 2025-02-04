# Interslavic wordlist for games

This wordlist was made with the game of Codenames in mind. I imagine it might serve as a resource for other word-based games and puzzles, such as Wordle, Hangman, Letter Soup etc.

What it contains:
- nouns in their dictionary form (nominative singular)
- mostly common nouns
- some proper names (with casing preserved)
- synonyms (see below for explanation)

What it DOESN'T contain:
- words with whitespace in them (equivalent examples in English would be: 'New York', 'ice cream')

## How was it made and how to recreate it?

This was made by intersecting two things:
- [the new Interslavic wordlist](https://docs.google.com/spreadsheets/d/1N79e_yVHDo-d026HljueuKJlAAdeELAiPzdFzdBuKbY/edit?gid=1987833874#gid=1987833874)
- the English, Polish, Czech and Russian wordlists from [this repo](https://github.com/sagelga/codenames)

Download all the resources used to create this, put them in an `input` directory, rename them as they are called in the script and run it.

## Variations of the wordlist

|               | standard spelling | etymological spelling |
| ---           | --- | --- |
| with synonyms | nouns_standard_spelling_with_synonyms.txt | nouns_etymological_spelling_with_synonyms.txt |
| no synonyms   | nouns_standard_spelling_no_synonyms.txt | nouns_etymological_spelling_no_synonyms.txt |

## Standard vs. etymological spelling

Latin alphabet is used.

The difference between standard vs. scientific/etymological can be found in resources about Interslavic (such as here: https://interslavic.fun/learn/orthography/).

In short, the standard one has less diacritics. The choice of spelling is largely a matter of preference.

## Synonyms

A feature of Interslavic is that it has many synonyms. For example, `aerodrom`, `aeroport`, `letišče` are all valid words for "airport".

The wordlist with synonyms contains them separated by slashes:
`aerodrom / aeroport / letišče`

The one without synonyms will contain the first element only:
`aerodrom`

### Why include synonyms?

Interslavic is a language meant to be understood by speakers of many Slavic languages without prior learning. This means that you can play a game in it with people who have never even heard of the language. Exposing them to synonyms will facilitate understanding. (Although in a game like Codenames, it also has some disadvantages.)

## TODOs

- verify if the synonyms are grouped correctly
- for pairs of gendered nouns (`kuhar`, `kuharka`), leave only one of them

When I first runned the script, I included English in the `langs_to_merge_by`. This led to an incorrect grouping: `čas / raz / vrěme` ('raz' means 'time' as in 'how many times?', the other two mean 'time' as in 'time is passing').

It also grouped gendered nouns together: `kuhar / kuharka` (male and female cook, respectively). Now they are separate.