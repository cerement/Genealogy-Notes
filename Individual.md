# Individual

[Personal names around the world](https://www.w3.org/International/questions/qa-personal-names)
* Do name fields need to be split? [full name]
* Make fields long enough (and don’t limit database field size)
* UTF-8
* If splitting, keep simple [family name] [other/given names]
* alternatively [full name] [preferred name]
* Japanese names need a field for pronunciation [ruby]
* Don’t assume a single letter is an initial
* Don’t require a family name
* Allow use of punctuation (hyphens, apostrophes, spaces)
* Don’t require all uppercase (and don’t normalize casing ex. McAdams)
* Don’t use title as an alternative to trying to find out gender

## Name

    name:         &id
      fullname:   !!str     # full name in order
      sortname:   !!str     # sorting, data entry
      ruby:       !!str     # pronunciation guides
      preferred:  !!str     # name to be addressed by
      pseudonym:  !!str     # stage name, pen name, username
      deadname:   !!str     # bureaucratic, legal alternates

### `name`
* Parent key with `&id` to be referenced with `*id` later on (ie. in Family mappings)

### `fullname`
* Individual’s full name with appropriate punctuation in appropriate encoding

### `sortname`
* Name as it is expected to be sorted in individual’s locale
* ex. Iceland and Thailand, sort by given name
* ex. Japan sort by pronunciation (ruby) of kanji, not by kanji directly
* ref. [A note on sorting](https://www.w3.org/International/questions/qa-personal-names#sorting)

### `ruby`
* [Ruby text](https://en.wikipedia.org/wiki/Ruby_character) – pronunciation guidelines where appropriate
* ref: [Ambiguity in written forms](https://www.w3.org/International/questions/qa-personal-names#japanese)

### `preferred`
* “How may I call you?” vs. “What is your name?”
* “How would you like to be addressed?”

### `pseudonym`
* Pseudonyms, usernames, pen names, stage names, aliases

### `deadname`
* \**Needs a better descriptor*\*
* Bureaucratic or legalese name
  * ie. form filled out on paperwork because of or in spite of name change
* Should *only* be used when back-mapping or external linking is wanted
  * Serious data privacy issues
* Considering Kafka-esque situation people get shuffled into when doing an expected name change (ex. wife in traditional American marriage)
* Situation is significantly worse for “non expected” name changes (ie. paperwork is filed but “superiors” refuse to acknowledge)
