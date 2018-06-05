# Analysis of 2018 Olympic Figure Skating Scores

This repository contains the data and code that BuzzFeed News used [to analyze figure skating scores at the 2018 Olympic Winter Games](https://www.buzzfeed.com/johntemplon/by-voting-for-their-own-figure-skating-judges-may-have). The data and analyses are adapted from BuzzFeed News' [original figure skating analyses](https://github.com/BuzzFeedNews/2018-02-figure-skating-analysis), published February 8, 2018. At that link, you can find a longer explanation of the terminology, data, data-processing, and analyses presented below.

## Data

Whereas the original analyses used data from 17 high-level competitions between October 2016 and December 2017, this repository uses data only from the 2018 Olympic Winter Games. The following files contain data extracted from [the official Olympic score sheets](http://www.isuresults.com/results/season1718/owg2018/):

- `performances.csv`
- `judged-aspects.csv`
- `judge-scores.csv`

You can find definitions of each column [here](https://github.com/BuzzFeedNews/figure-skating-scores).

The [`data`](./data) directory also includes the following files:

- `judge-goe.csv` - The "translated Grade of Execution" for judgment of each performed technical element. See [this notebook](https://github.com/BuzzFeedNews/2018-02-figure-skating-analysis/blob/master/notebooks/translate-goe.ipynb) for more information on the translation process.
- `judges.csv` - A list of each judge at the 2018 Winter Olympic Games and each judge's home-country (as indicated on [the International Skating Union's roster of officials](https://www.isu.org/communications/12127-isu-communication-2111/file)).

## Analyses

The [`notebooks` directory](./notebooks) contains two sets of analyses:

- [`points-versus-average`](notebooks/points-versus-average.ipynb) calculates the difference between each individual judge's total scores (for a given performance) and the average of the remaining judges on the panel. This notebook calculates the overall home-country preference in the 2018 Olympic Winter Games, and identifies the largest disparities between a judge's scores and the average.

- [`alternative-scenarios`](notebooks/alternative-scenarios.ipynb) calculates the total points and final standings of the ice dance and men's competitions under two alternative scenarios: (1) If the scores from certain countries' judges were replaced by scores from an "average" judge, and (2) if those judges' scores were removed entirely.

## Technical Notes

All of the analyses above are coded in Python 3, using the libraries listed in [`requirements.txt`](./requirements.txt).

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). All data files are available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license.

## Questions / Feedback

Contact John Templon at [john.templon@buzzfeed.com](mailto:john.templon@buzzfeed.com).

Looking for more from BuzzFeed News? [Click here for a list of our open-sourced projects, data, and code.](https://github.com/BuzzFeedNews/everything)
