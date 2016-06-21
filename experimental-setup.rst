Proper experimental setup is THE MOST
IMPORTANT requirement for a machine learning project.

There are two common ways of designing learning experiment. They both
are based on having a separate test set.

Setup 1
-------

You take a sample of your data (typically around 20%) as a test
set. You set this data aside and do not do anything with it until the
final stages of your project.

The rest of your data you divide into training set and validation set (also
called development). Typically training will be around 60%, and
validation around 20% of the total data.

You train your models with different settings (including different
preprocessing and feature extraction) on the training set, and check
the scores on *validation set*. If there is any interesting effect of
settings you want to discuss, you should use these results on
validation data to illustrate it.

At the end of your project, you want to report on your main research
question. For this, you typically have two or three models (with
properly tuned settings), already trained on training set, which you
want to compare. For example a baseline (M0), a model used in previous
work (M1), and your own improved model (M2).

At point, you test each of the three models on the *test set*, and
report the results.

Setup 2
-------

This is also a common setup, and is similar to Setup 1. You reserve a
separate test set for the final stages of the project. 

But instead of having a fixed training set and a fixed validation set, you use
cross-validation to tune your setting, which means that you split the
data (excluding test set) in several ways into training and validation.

Cross validation data *does not* include the final test set. Like in
setup 1, the test set is only used at the end, *after* you have tuned
the models you want to compare.


There are also some other ways of setting up your experiments, but
they require that you know exactly what you're doing and are not
recommended for beginners.

