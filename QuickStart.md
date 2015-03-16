
---


### Demonstration ###
Just run `namegen_example.py`.


### Using in your game / program ###
  1. Copy `namegen.py` to the source folder.
  1. `from namegen import NameGen`
  1. Initialize with path to language file: `gen = NameGen('language.txt')`
  1. Call `gen.gen_word()` method, returns generated string.
There are some languages available in the Languages folder, but you can create your own too.


### Optional ###
  * Change `gen.min_syl` and `gen.max_syl` to control number of syllables.
  * Pass the sample file as 2nd parameter at initialization to set it as the list of forbidden words. No words from the sample will be replicated.
  * Pass `True` as the 1st parameter to `gen_word()` to add the generated word to the list of forbidden words. The word will not occur again.


### Creating new languages (also optional) ###
Run `namegen_train.py [filename]` to create a new language from the file `Samples/[filename].txt`.
See command line help `namegen_train.py -?` for more.