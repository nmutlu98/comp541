# Explanations of the files:

- _last_baseline.ipynb_: Includes the baseline model which uses the following rule to segment the file:
  It extracts left and right contexts of each word in the given file. Left context size and right context size are taken as 1 as they will not make any difference in the execution of the model. If the left context has an ending punctuation and right context does not start with a number, the word is marked as candidate site. The baseline model adds a newline after each candidate site. The baseline only works for English now.
- _test.en_ : This is the not segmented test data for the model.
- _wsj.03-03.en_ : This includes the original segmented file.
- _always_split_result2.en_ : This includes the segmented text by the baseline model in my last trial. I run the score.py file to calculate the score of my baseline model.
- _results.out_: Includes the scores of my trial run with baseline model.
- _score.py_: The scoring file provided by the authors. It is not part of the model. It just takes two text files and compares them. You can calculate the scores by running this file from terminal python score.py I didn't run it from PyCall package because it is too long and takes time to compile.

P.S.: It takes some time to calculate the scores.
