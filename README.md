# name-gen

This is a small module intended for use within procedural games (eg. RPGs, Roguelikes) to generate names or other words.

It works by analyzing a sample text for a set of representative syllables, and then generating tables of co-occurrences. A simple call to one function generates a word "inspired" by the sample.

By working at the syllable level, the output is usually much more believable than conventional approaches, without specific tweaking of rules.

Possible applications include generation of names for characters, places, etc; and generating text in fictional languages.

Examples from some of the languages:

Names for deities | Celtic myth | Roman names | Characters from Beowulf | Norse myth
------------------|-------------|-------------|-------------------------|------------
Nehemel | Brigaus | Colautius | Heorga | Beylass
Jehddad | Bria | Tuberius | Eormeneca | Thunaerul
Jerahmah | Aranis | Nasicus | Halg | Herfjvi
Beremiiel | Gwydioen | Aquiliuius | Sceand | Frea
Uzzieah | Mapomna | Laena | Eoforgar | Skegbil
Haniasaah | Camulgus | Baculius | Heorld | Odandgrnd
Jahdie | Arnerus | Tuberius | Frankaf | Ssonna
Azariah | Aufagusus | Galeriuslus | Weohstgas | Forsetgg
Gedaliah | Damarona | Hostivus | Eanmundlaf | Orgerthuyn
Eliadael | Blodelad | Claudius | Wiglaf | Sigmundist 



## Demonstration
Just run `namegen_example.py`.


## Using in your game / program
* Copy `namegen.py` to the source folder.
* `from namegen import NameGen`
* Initialize with path to language file: `gen = NameGen('language.txt')`
* Call `gen.gen_word()` method, returns generated string.
There are some languages available in the Languages folder, but you can create your own too.


## Optional
* Change `gen.min_syl` and `gen.max_syl` to control number of syllables.
* Pass the sample file as 2nd parameter at initialization to set it as the list of forbidden words. No words from the sample will be replicated.
* Pass `True` as the 1st parameter to `gen_word()` to add the generated word to the list of forbidden words. The word will not occur again.


## Creating new languages (also optional)
Run `namegen_train.py [filename]` to create a new language from the file `Samples/[filename].txt`.
See command line help `namegen_train.py -?` for more.
