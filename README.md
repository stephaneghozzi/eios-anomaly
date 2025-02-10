# Towards Anomaly Detection in EIOS

Using natural language processing and machine learning, epidemiologically relevant text are identified from streams of online articles for [Epidemic Intelligence from Open Sources (EIOS)](https://www.who.int/initiatives/eios/) of the [World Health Organization](https://www.who.int).

“Anomaly detection” is defined as applying algorithms trained to predict which EIOS articles would be identified as “signals” by experts at WHO. The texts of the articles are vectorized following both a bag-of-words and a word-embeddings approach. Overall 78 combinations of data preparation and classification algorithms are evaluated using a series of scores. Focusing on high recall, the logistic regression applied to a bag-of-words approach reaches a specificity of 0.83 for a recall of 0.92, among other good performances. However it has a very low precision of 0.021. Nevertheless, it could already be useful in sorting articles.

Two Jupyter notebooks (Python 3) were used:
- [exploration_signals_events.ipynb](exploration_signals_events.ipynb) to gather, clean, pre-process and describe raw labels.
- [exploration_eios_articles.ipynb](exploration_eios_articles.ipynb) to get articles, pre-process texts, analyse sentiment and topics, train and test classifiers, compute scores and generate the results (tables and interactive plots); progress is written in a log and intermediate results are saved on disk to avoid overloading memory.

The template [nbconvert_template_altair.tpl](nbconvert_template_altair.tpl) allows the displaying of interactive plots produced with Altair in the notebooks.

Approach, results and perspectives are presented in [eios_anomaly-seoul-20191113.pdf](eios_anomaly-seoul-20191113.pdf), the slides of a talk held at the [2019 EOIS Global Technical Meeting](https://www.who.int/initiatives/eios/global-technical-meeting-2019).

## Data

The article data were provided by the [Joint Research Centre (JRC)](https://ec.europa.eu/jrc/en) for EIOS. The labels (signals) were compiled by the DVA team of the [World Health Organization (WHO)](https://www.who.int). No data are shared here because they are not public.

## Contributions

Author: Stéphane Ghozzi

Funding: [INIG](https://www.rki.de/EN/Content/Institute/DepartmentsUnits/ZIG/INIG/INIG_node.html) of the [Robert Koch Institute](https://www.rki.de) and DVA of WHO.

## Licence

The code is made available under a [CC0](https://creativecommons.org/share-your-work/public-domain/cc0/) licence, i.e. others may freely build upon, enhance and reuse the works for any purposes without restriction under copyright or database law.