# Family

“You can choose your friends, but you can’t choose your family.”  
—(proverb)

“The bond that links your true family is not one of blood, but of respect and joy in each other’s life.”  
—Richard Bach

> GEDCOM does not explicitly support data representation of many types of close interpersonal relationships,
> such as same-sex marriages, domestic partnerships, cohabitation, polyamory or polygamy. Such relationships
> can only be represented using the generic ASSO tag used for any type of relationship.

—[Support for varying definitions of families and relationships](https://en.wikipedia.org/wiki/GEDCOM#Support_for_varying_definitions_of_families_and_relationships)

[Ahnentafel](https://en.wikipedia.org/wiki/Ahnentafel)

[Graph Modelling Language](https://en.wikipedia.org/wiki/Graph_Modelling_Language)
```GML
graph [
	node [
		id 1
		label "person 1"
	]
	node [
		id 2
		label "person 2"
	]
	node [
		id 3
		label "person 3"
	]
	edge [
		source 1
		target 2
		label "spouse"
	]
	edge [
		source 2
		target 3
		label "parent"
	]
	edge [
		source 3
		target 1
		label "child"
	]
]
```

[XHTML Friends Network](https://en.wikipedia.org/wiki/XHTML_Friends_Network)
* family
  * child
  * parent
  * sibling
  * spouse
  * kin
```XHTML
<a href="http://jane-blog.example.org/" rel="sweetheart date met">Jane</a>
<a href="http://dave-blog.example.org/" rel="friend met">Dave</a>
<a href="http://darryl-blog.example.org/" rel="friend met">Darryl</a>
<a href="http://www.metafilter.com/">MetaFilter</a>
<a href="http://james-blog.example.com/" rel="met">James Expert</a>
```
