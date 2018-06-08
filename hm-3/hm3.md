# Problem solving
There is always a point in life when you are ready to solve a problem by inventing a magical data structure (s). Use your problem-solving skills and all other tricks to address the following.


Problem: given a prefix or a suffix find all matching words in a given list of words.

For example, consider following list:

```
abactor
abaculi
abaculus
abacus
abacuses
abada
```

Prefix `abacul` should return `abaculi, abaculus` while suffix `s` should return `abaculus, abacus, abacuses`.

Now, write a program that takes an option, an argument, and reads the list of words from standard input as shown in the example bellow:
```
python fix_search.py -p "test" < word_list.txt
```

Following commands need to be implemented:

1. `python fix_search.py -h`  should return usage instructions of the application. You can run `python -h` for inspiration.
2. `python fix_search.py -p "abacul" < word_list.txt`, option `-p` or `prefix` should return a list of words with the prefix "abacul" as in example before.
3. `python fix_search.py -s "abacul" < word_list.txt`, option `-s` or `suffix` should return a list of words with the suffix "abacul" as in example before.


Constraints:
* only one option at the time should be supported
* Suffix and prefix have two conditions:
  * it must contain at least one character,
  * it can only include letters from English ASCII character set in the range from DEC 65 to DEC 122
* if the option, argument, or input is incorrect, usage instructions should be printed
* it was to have clearly separate part for: input reading, parsing, control, and the algorithm
* you have to implement a class `AmazingAutoComplete` that given a list of words creates an appropriate data structure(s) (one or more)
* solution has to be in one file
* your code should run in `O(n)` for `n` symbols.


Yes, there are many options providing plenty of opportunities to shine and use all your knowledge. For your convenience implement testing first.

# Deliverables
1) File fix_search.py with the implementation of problem 1.
2) A brief explanation why your code follows `O(n)` for `n` symbols and your data structure.

# How to submit

Use the invitation link below to create the repo:
https://classroom.github.com/a/dSM_WctA
