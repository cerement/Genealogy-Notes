# Genealogy Notes

* [Individual](Individual.md)
* [Event](Event.md)
* [Family](Family.md)
* [Samples](Samples.md)

Between looking at my personal timeline and family members showing an interest in genealogy, I got distracted and jumped down that rabbit hole for a while. The main advantage of handling things online is the ability to rely on crowd-sourcing ancestral linkages – once a common point is found between two trees, the trees can be linked and extended, opening up possibilies for future growth.

## Issues

The first shortcoming of the online method is data privacy – the demographic data available in publicly available ancestral trees is as rich as the data offered up by dating websites. This might be mitigated somewhat by a decentralized peer-to-peer ancestral mapping (ie. a set of federated genealogy servers sharing linkages back and forth via some sort of [IRI](https://en.wikipedia.org/wiki/Internationalized_Resource_Identifier) sytem –
ref. [Mastodon](https://en.wikipedia.org/wiki/Mastodon_(software))).

[Network Effect](https://en.wikipedia.org/wiki/Network_effect), [Data Silo](https://en.wikipedia.org/wiki/Information_silo),
and [Lock In](https://en.wikipedia.org/wiki/Vendor_lock-in) – all conditions (or a combination of conditions) which can lead to a situation where your family tree is taken out of your control. If you’ve spent time building up a family tree on any website and the website disappears before you’ve had a chance to download your tree (if it is even possible for that website). If you’ve built your family tree in a program or app and the company goes belly-up before you’ve had a chance to export your family tree out of the program’s proprietary format (if it even allowed exporting) or the app runs afoul of Apple or Google and gets removed from the app store and subsequently deleted from your phone.

The next issue is that there are a multitude of programs and websites that attempt to track and map your family tree, each with their own format for storing the information. Over the years, [GEDCOM](https://en.wikipedia.org/wiki/GEDCOM) has become the de-facto standard, not because it is any better, but simply because it’s the lowest common denominator among the competition. While the standard is open and available, development is very much closed and under the control of the [LDS Church](https://en.wikipedia.org/wiki/The_Church_of_Jesus_Christ_of_Latter-day_Saints) (under the [FamilySearch](https://en.wikipedia.org/wiki/FamilySearch) umbrella) – effectively embedding their whole set of [cultural biases](https://github.com/tmcw/gedcom/blob/main/GEDCOM_BIAS.md) (running right back into the [“Big Data” problem](https://en.wikipedia.org/wiki/Weapons_of_Math_Destruction) again).

Several tries have been made to add extensions to GEDCOM (ie. support for genealogy certification), but without interoperability, each program and site decides which extensions to honor or ignore. There have also been multiple movements over the years, both within the LDS Church ([GEDCOM X](http://www.gedcomx.org/)) and community controlled ([FHISO/BetterGEDCOM](https://fhiso.org/), [Gramps XML](https://www.gramps-project.org/wiki/index.php/Gramps_XML)), but most of them appear to have fallen by the wayside for lack of interest.

## Formats

Available options for file formats when moving forwards:
* [GEDCOM](https://en.wikipedia.org/wiki/GEDCOM)
* [Ahnentafel](https://en.wikipedia.org/wiki/Ahnentafel)
* proprietary
* [XML](https://en.wikipedia.org/wiki/XML)
* [JSON](https://en.wikipedia.org/wiki/JSON)
* [YAML](https://en.wikipedia.org/wiki/YAML)

Most efforts seem to be focusing on either XML or JSON, but I have a personal preference for YAML (both because it is a plaintext format and because it is a human readable format). Since this repository is purely speculation, I’m not too concerned about either development issues I would run into or being overly rigorous with specifications. Keeping that in mind, converting back and forth between YAML and GEDCOM *appears* it should be relatively trivial and, if necessary, could be done by hand.

## GEDCOM

I will be referring to GEDCOM files as a baseline or starting point simply because they are the most prevalent within the genealogy community, the are the format that everyone is familiar with.

GEDCOM files are generally composed of three sections:
* HEAD (header) – metadata
* INDI (individual) – data set for people
* FAM (family) – data set for family mapping
Additionally, two extra categories of data are woven into the above:
* EVEN (event) – events, personal and family
* SOUR (source) – sources and documentation

## Microformats

Of the above, the only component that is somewhat unique is the FAM mapping, the network of connections – a modern alternative to GEDCOM could be split into a whole series of linked discrete components:
* INDI part could be handled by [vCard](https://en.wikipedia.org/wiki/VCard) or its derivatives
* EVEN could be handled by [iCalendar](https://en.wikipedia.org/wiki/ICalendar)
* SOUR by [Dublin Core](https://en.wikipedia.org/wiki/Dublin_Core) or upgraded to a proper [BibTeX](https://en.wikipedia.org/wiki/BibTeX)
  or [CSL](https://en.wikipedia.org/wiki/Citation_Style_Language) (including [CSL YAML](https://pandoc.org/))
* FAM could be handled by something like [XFN](https://en.wikipedia.org/wiki/XHTML_Friends_Network) or use a format that could be cleanly fed into
  [Pajek](http://mrvar.fdv.uni-lj.si/pajek/) or [KrackPlot](https://www.heinz.cmu.edu/faculty-research/profiles/krackhardt-davidm/krackplot)
  or some other network mapping utility – or rely on the capabilities of a statistical language like [R](https://en.wikipedia.org/wiki/R_(programming_language))

ref. [Genealogy Formats](https://microformats.org/wiki/genealogy-formats)
