# Genealogy Notes

Between looking at my personal timeline and family members showing an interest in genealogy, I got distracted and jumped down that rabbit hole for a while.

The first issue is that there are a multitude of programs and websites that attempt to track and map your family tree, each with their own format for storing the information. Over the years, [GEDCOM](https://en.wikipedia.org/wiki/GEDCOM) has become the de-facto standard, not because it is any better, but simply because it’s the lowest common denominator among the competition. While the standard is open and available, development is very much closed and under the control of the [LDS Church](https://en.wikipedia.org/wiki/The_Church_of_Jesus_Christ_of_Latter-day_Saints) under the [FamilySearch](https://en.wikipedia.org/wiki/FamilySearch) organization – effectively embedding their whole set of [cultural biases](https://github.com/tmcw/gedcom/blob/main/GEDCOM_BIAS.md) (running right back into the [“Big Data” problem](https://en.wikipedia.org/wiki/Weapons_of_Math_Destruction) again). Several tries have been made to add extensions to GEDCOM (ie. support for genealogy certification), but without interoperability, each program and site decides which extensions to honor or ignore.

There have also been multiple movements over the years, both within the LDS Church ([GEDCOM X](http://www.gedcomx.org/)) and community controlled ([FHISO/BetterGEDCOM](https://fhiso.org/), [Gramps XML](https://www.gramps-project.org/wiki/index.php/Gramps_XML)), but most of them appear to have fallen by the wayside for lack of interest.

Available options for file formats when moving forwards:
* [GEDCOM](https://en.wikipedia.org/wiki/GEDCOM)
* proprietary
* [XML](https://en.wikipedia.org/wiki/XML)
* [JSON](https://en.wikipedia.org/wiki/JSON)
* [YAML](https://en.wikipedia.org/wiki/YAML)

Most efforts seem to be focusing on either XML or JSON, but I have a personal preference for YAML (both because it is a plaintext format and because it is a human readable format). Since this repository is purely speculation, I’m not too concerned about either development issues I would run into or being overly rigorous with specifications.
