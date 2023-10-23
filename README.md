
## <u>`flairR`</u>: An R Wrapper for Accessing Flair NLP Library <img src="man/figures/logo.png" align="right" width="180"/>

[![R](https://github.com/davidycliao/flaiR/actions/workflows/r_macos.yml/badge.svg)](https://github.com/davidycliao/flaiR/actions/workflows/r_macos.yml)
[![R-CMD-check](https://github.com/davidycliao/flaiR/actions/workflows/r.yml/badge.svg)](https://github.com/davidycliao/flaiR/actions/workflows/r.yml)
[![coverage](https://github.com/davidycliao/flaiR/actions/workflows/test-coverage.yaml/badge.svg)](https://github.com/davidycliao/flaiR/actions/workflows/test-coverage.yaml)
[![codecov](https://codecov.io/gh/davidycliao/flaiR/graph/badge.svg?token=CPIBIB6L78)](https://codecov.io/gh/davidycliao/flaiR)
[![CodeFactor](https://www.codefactor.io/repository/github/davidycliao/flair/badge)](https://www.codefactor.io/repository/github/davidycliao/flair)
[![Codespaces
Prebuilds](https://github.com/davidycliao/flaiR/actions/workflows/codespaces/create_codespaces_prebuilds/badge.svg)](https://github.com/davidycliao/flaiR/actions/workflows/codespaces/create_codespaces_prebuilds)

<!-- README.md is generated from README.Rmd. Please edit that file -->

<div style="text-align: justify">

`{flaiR}` is an R wrapper for the
[{flairNLP/flair}](https://github.com/flairnlp/flair) library in Python,
designed specifically for R users, especially those in the social
sciences. It provides easy access to the main functionalities of
`{flairNLP}`. Developed by [Zalando
Research](https://engineering.zalando.com/posts/2018/11/zalando-research-releases-flair.html)
in Berlin, Flair provides intuitive interfaces with exceptional
multilingual support, especially for various embedding frameworks, and
is compatible with the HuggingFace API. It also comes equipped with
state-of-the-art natural language processing models to analyze your
text, such as named entity recognition, sentiment analysis,
part-of-speech tagging, biomedical data, sense disambiguation, and
classification, with support for a rapidly growing number of languages
in the community. For a comprehensive understanding of the
`{flairNLP/flair}` architecture, you can refer to the research article
‘[Contextual String Embeddings for Sequence
Labeling](https://aclanthology.org/C18-1139.pdf)’ and the official
[manual](https://flairnlp.github.io) written for its Python
implementation.

`{flaiR}` enables R users to leverage Flair’s capabilities without the
need to interact directly with Python. For R users, {`flairR`} primarily
consists of two main components. The first is a wrapper function in
{`flaiR`} built on top of {`reticulate`}, which enables you to interact
directly with Python modules in R and provides seamless support for
documents and [tutorial (in
progress)](https://davidycliao.github.io/flaiR/articles/tutorial.html)
in the R community. Secondly, to facilitate more efficient use for
social science research, {`flairR`} extend {`flairNLP/flair`}’s core
functionality for working with three major functions to extract features
in a tidy and fast format–
[data.table](https://cran.r-project.org/web/packages/data.table/index.html)
in R.

The core features (and example usage) can be found:

- [**part-of-speech
  tagging**](https://davidycliao.github.io/flaiR/articles/get_pos.html)
- [**named entity
  recognition**](https://davidycliao.github.io/flaiR/articles/get_entities.html)
- [**transformer-based sentiment
  analysis**](https://davidycliao.github.io/flaiR/articles/get_sentiments.html)

In addition, to handle the load on RAM when dealing with larger corpus,
{`flairR`} supports batch processing to handle texts in batches, which
is especially useful when dealing with large datasets, to optimize
memory usage and performance.

</div>

<br>

### Installation via <u>**`GitHub`**</u>

<div style="text-align: justify">

The installation consists of two parts: First, install [Python
3.7](https://www.python.org/downloads/) or higher, and [R
3.6.3](https://www.r-project.org) or higher. Although we have tested it
on Github Action with R 3.6.2, we strongly recommend installing [R 4.0.0
or above](https://github.com/davidycliao/flaiR/actions/runs/6416611291)
to ensure compatibility between the R environment and {`reticulate`}. If
there are any issues with the installation, feel free to ask in the
<u>[Discussion](https://github.com/davidycliao/flaiR/discussions) </u>.

</div>

``` r
install.packages("remotes")
remotes::install_github("davidycliao/flaiR", force = TRUE)
```

``` r
library(flaiR)
#> flaiR: An R Wrapper for Accessing Flair NLP Tagging Features      
#> Python: 3.11                                           
#> Flair: 0.12.2  
```

<br>

## Contribution and Open Source Support

<div style="text-align: justify">

`{flaiR}` is maintained and developed by [David
Liao](https://davidycliao.github.io) and friends. R developers who want
to contribute to {`flaiR`} are welcome – {`flaiR`} is an open source
project. I warmly invite R users who share similar interests to join in
contributing to this package. Please feel free to shoot me an email to
collaborate on the task. Contributions – whether they be comments, code
suggestions, tutorial examples, or forking the repository – are greatly
appreciated. Please note that the `flaiR` is released with the
[Contributor Code of
Conduct](https://github.com/davidycliao/flaiR/blob/master/CONDUCT.md).
By contributing to this project, you agree to abide by its terms.

The primary communication channel for R users can be found
[here](https://github.com/davidycliao/flaiR/discussions). Please feel
free to share your insights on the
[Discussion](https://github.com/davidycliao/flaiR/discussions) page and
report any issues related to the R interface in the
[Issue](https://github.com/davidycliao/flaiR/issues) section. If the
issue pertains to the actual implementation of Flair in Python, please
submit a pull request to the offical [flair
NLP](https://github.com/flairnlp/flair).

</div>

<br>

## Citing the Contributions of `Flair NLP`

<div style="text-align: justify">

If you use this tool in academic research, we recommend citing the
research article, [Contextual String Embeddings for Sequence
Labeling](https://aclanthology.org/C18-1139.pdf) from
[Flair](https://flairnlp.github.io) and [Zalando
Research](https://engineering.zalando.com/posts/2018/11/zalando-research-releases-flair.html).

</div>

    @inproceedings{akbik2018coling,
      title={Contextual String Embeddings for Sequence Labeling},
      author={Akbik, Alan and Blythe, Duncan and Vollgraf, Roland},
      booktitle = {{COLING} 2018, 27th International Conference on Computational Linguistics},
      pages     = {1638--1649},
      year      = {2018}
    }
