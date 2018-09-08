---
title: "EuroSciPy 2018 in Trento, Italy"
data: 2018-08-10
tags: [conferences, data science, python]
header:
exerpt: "Python, Science, and beautiful scenery"
---
[![N|scipy](https://www.euroscipy.org/theme/images/euroscipy_logo.png)](https://euroscipy.org)

Last week I attended my first Python conference ever, and I must say I am impressed. I'm used to big neuroscience conferences where people are usually quite secretive about their exact methods or present outdated results so as not to give the competition any advantage. At the EuroSciPy everyone was so eager to share the source code of their work and offer support to anyone who wants to use their tools.

Also, Trento is a very interesting, underrated location. A beautiful old town with historical architecture surrounded by impressive mountains. The EuroSciPy 2019 will be held in Trento again, so if you missed the first installment, I highly recommend giving it a try next year.

Here are some of the highlights in no particular order:

- **Scikit learn 0.20** will get some new features to more easily support tabular data directly from pandas. For example, the one-hot-encoder currently does not support string inputs. Also feature names should be read in directly from the pandas column names in the future.
- On a related note, **numpy** is also planning to add more support for categorical data.

A few interesting libraries related to machine learning have been presented. I have yet to check them out:
- **[modAL](https://github.com/cosmic-cortex/modAL)** is fully compatible with scikit learn but allows *active learning*. It samples the learning data in more intelligent ways than the standard random sampling of scikit.
- **[Imbalanced-learn](https://github.com/scikit-learn-contrib/imbalanced-learn)** addresses the issues with datasets where one class has a much smaller number of samples, such as rare diseases.
- **[CatBoost](https://github.com/catboost/catboost)** is a gradient boosting tool that apparently outperforms all its competition such as XGBoost or LightGBM. Definitely worth trying out.

Then there have been a couple of promising plotting libraries. An area, where I'm still not quite happy with python. For really polished plots I've been using plot.ly, but 20+ lines of code for a simple plot is really a pain and inefficient.
- **[Altair](https://github.com/altair-viz/altair)** was presented as an alternative to Bokeh, which can create interactive java visualizations with relatively few lines of python code. As I understood it is a higher-level wrapper for another tool called Vega.
- Then there is **[pixiedust](https://github.com/pixiedust/pixiedust)** a very user-friendly wrapper to quickly visualize data using many other python libraries. Not sure how much customization it allows, but it may be very useful for deciding which plotting library to choose for a given data problem.

One talk about dimensionality reduction in neuroscience presented some interesting alternatives to Principal Component Analysis (PCA) for cases in which you would like to keep one of the original data dimensions such as the time or trial number, in order to make the results more interpretable. Examples were *Tensor Component analysis (TCA)* on github under **[tensortools](https://github.com/ahwillia/tensortools)**, and *Demixed PCA* on github under **[dPCA](https://github.com/machenslab/dPCA)**.

For people interested in Jupyter, there were several presentations.
- [Jupyterhub](https://github.com/jupyterhub/jupyterhub) is a great tool to easily set up a server to allow multi-user access to notebooks. It seems to become very popular in education e.g. to distribute notebooks according to a schedule and automatically correct the exercises.
- A must-see talk for notebook users was the one by [Antonino Ingargiola](https://www.youtube.com/watch?v=J32Guga4mtM) about reproducibility with Jupyter. Explaining some pitfalls and best practices. He is also the author of [nbrun](https://github.com/tritemio/nbrun) a nice little tool to run notebooks like a script with input arguments from another notebook. As I learned there is also a tool made by Netflix with the same purpose and more advanced features called [papermill](https://github.com/nteract/papermill).

I noticed that there is quite a big controversy about the usefulness of notebooks. Its users like the clean interface, the ability to quickly experiment with snippets of code, and having the code and output in one place. Critics interject that it is neither optimized for coding nor for presenting/publishing, and that it prevents users from improving their coding skills. I think I will dedicate a whole blog entry about the pros and cons of Jupyter.
To hear a more critical talk, and an alternative tool for reproducible publishing by combining the advantages of python and LaTex, I highly recommend the presentation of my colleague [Christian Horea](https://www.youtube.com/watch?v=J32Guga4mtM).


Then there were a bunch of presentations specific to various scientific fields, providing more insights into the python workflows of researchers, best practices, recommended libraries etc. As always the videos of all talks are freely accessible [online](https://www.euroscipy.org/2018/)
