# Entity-Fishing-Tutorial

In this [tutorial]() I'm gonna show you how to use the Entity Fishing tool from a [Client API](https://github.com/issa-project/entity-fishing-client-python) in Python to link your text mentions with the Wikidata knowledge base, as well as how to retreive data that you need and which contains a valid Wikidata link.

You'll find in the next sections, some useful informations about these the three fundemental concepts used in this project.

## Entity Linking
Entity linking [[2]](https://www.cs.jhu.edu/~delip/entity_linking.pdf) is matching a textual entity mention, possibly identified by a named entity recognizer, to a KB entry, such as a Wikipedia page that is a canonical entry for that entity. An entity linking query is a request to link a textual entity mention in a given document to an entry in a KB. The system can either return a matching entry or NIL to indicate there is no matching entry.

And They define in the same article that there are 3 challenges to entity linking:

1. **Name Variations:** An entity often has multiple mention forms, including abbreviations, shortened forms, alternate spellings, and aliases. Entity linking must find an entry despite changes in the mention string.

2. **Entity Ambiguity:** A single mention can match multiple KB entries, as many entity names, like people and organizations, tend to be polysemous.

3. **Absence:** Processing large text collections virtually guarantees that many entities will not appear in the KB (NIL), even for large KBs.

## Entity Fishing

Entity Fishing [[3]](https://nerd.readthedocs.io/en/latest/index.html), is a tool that automate the identification and resolution of specialist entities, and the disambiguisation task in a generic manner, avoiding as much as possible restrictions of domains, limitations to certain classes of entities or to particular usages. Supervised machine learning is used for the disambiguation, based on Random Forest and Gradient Tree Boosting exploiting various features. The main disambiguation techniques include graph distance to measure word and entity relatedness and distributional semantic distance based on word and entity embeddings. The tool currently supports 11 languages, English, French, German, Spanish, Italian, Arabic, Japanese, Chinese (Mandarin), Russian, Portuguese and Farsi

## Wikidata

Wikidata [[4]](https://www.semantic-web-journal.net/system/files/swj1366.pdf) is a project of Wikimedia Deutschland which started on October 30, 2012. The aim of the project is to provide data which can be used by any Wikimedia project, including Wikipedia. Wikidata does not only store facts, but also the corresponding sources, so that the validity of facts can be checked. Labels, aliases, and descriptions of entities in Wikidata are provided in almost 400 languages. Wikidata is a community effort, i.e., users collaboratively add and edit information. Wikidata is currently growing considerably due to the integration of Freebase data, because Freebase shuted down its services completely on August 31, 2016.