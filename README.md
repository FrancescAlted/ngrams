ngrams
======

Example of how to find substrings in large datasets new 'contains' in numexpr
-----------------------------------------------------------------------------

The code is exercising the recently introduced 'contains' function in
numexpr so it is shown how fast these queries can be.

The data is based in Google Books Ngrams, whose description can be
found [here](http://aws.amazon.com/datasets/8172056142375670) and the
files can be downloaded from
[here](http://storage.googleapis.com/books/ngrams/books/datasetsv2.html).

In particular, the dataset used is the "English One Million", and you
can download it from a bash shell with a command like:

```
for i in `seq 0 199`; do wget http://storage.googleapis.com/books/ngrams/books/googlebooks-eng-1M-3gram-20090715-$i.csv.zip; done
```

However, in order to keep the time for running the script reasonable, only the 2 first files will be downloaded, so the next command has been used here:

```
for i in `seq 0 1`; do wget http://storage.googleapis.com/books/ngrams/books/googlebooks-eng-1M-3gram-20090715-$i.csv.zip; done
```

which will be stored in the 'eng-1M-3gram' directory.
