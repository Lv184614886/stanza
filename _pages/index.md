---
title: Stanza Python Library
keywords: Stanza, Python, NLP, Natural Language Processing, Deep Learning, PyTorch
type: first_page
permalink: '/index.html'
homepage: true
---

## About

Stanza is a Python natural language analysis package. It contains tools, which can be used in a pipeline, to convert a string containing human language text into lists of sentences and words, to generate base forms of those words, their parts of speech and morphological features, to give a syntactic structure dependency parse, and to recognize named entities. The toolkit is designed to be parallel among more than 70 languages, using the [Universal Dependencies formalism](https://universaldependencies.org).

Stanza is built with highly accurate neural network components that also enable efficient training and evaluation with your own annotated data. The modules are built on top of the [PyTorch](https://pytorch.org/) library. You will get much faster performance if you run this system on a GPU-enabled machine.

In addition, Stanza includes a Python interface to the [CoreNLP Java package](https://stanfordnlp.github.io/CoreNLP) and inherits additonal functionality from there, such as constituency parsing, coreference resolution, and linguistic pattern matching.

<br />
To summarize, Stanza features:

* Native Python implementation requiring minimal efforts to set up;
* Full neural network pipeline for robust text analytics, including tokenization, multi-word token (MWT) expansion, lemmatization, part-of-speech (POS) and morphological features tagging, dependency parsing, and named entity recognition;
* Pretrained neural models supporting [66 (human) languages](models.md#human-languages-supported-by-stanza);
* A stable, officially maintained Python interface to CoreNLP.

<br />
Below is an overview of Stanza's neural network NLP pipeline:

<p align="center">
   <img src="images/pipeline.png" style="width:60%">
</p>

## Getting Started

We strongly recommend installing Stanza with `pip`, which is as simple as:

```bash
pip install stanza
```

To see Stanza's neural pipeline in action, you can launch the Python interactive interpreter, and try the following commands:

```python
>>> import stanza
>>> stanza.download('en') # download English model
>>> nlp = stanza.Pipeline('en') # initialize English neural pipeline
>>> doc = nlp("Barack Obama was born in Hawaii.") # run annotation over a sentence
```

You should be able to see all the annotations in the example by running the following commands:

```python
>>> print(doc)
>>> print(doc.entities)
```

For more details on how to use the neural network pipeline, please see our [Getting Started Guide](installation_usage.md) and [Tutorials](tutorials.md).

Aside from the neural pipeline, Stanza also provides the official Python wrapper for accessing the Java Stanford CoreNLP package. For more details, please see [Stanford CoreNLP Client](corenlp_client.md).

{% include alerts.html %}
{{ note }}
{{ "If you run into issues during installation or when you run the example scripts, please check out [this FAQ page](faq.md). If you cannot find your issue there, please report it to us via [GitHub Issues](https://github.com/stanfordnlp/stanza/issues)." | markdownify }}
{{ end }}

## License

Stanza is licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0) (the "License"), you may not use the software package except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Main Contributors

The PyTorch implementation of Stanza's neural pipeline is due to [Peng Qi](http://qipeng.me), [Yuhao Zhang](http://yuhao.im), and [Yuhui Zhang](https://cs.stanford.edu/~yuhuiz/), with help from [Jason Bolton](mailto:jebolton@stanford.edu) and [Tim Dozat](https://web.stanford.edu/~tdozat/).

The CoreNLP client is mostly written by [Arun Chaganty](http://arun.chagantys.org/), and [Jason Bolton](mailto:jebolton@stanford.edu) spearheaded merging the two projects together.

We are also grateful to community contributors for their help in improving Stanza.

## Citing Stanza in papers

If you use Stanza in your work, please cite this paper:

> Peng Qi, Yuhao Zhang, Yuhui Zhang, Jason Bolton and Christopher D. Manning. 2020. [Stanza: A Python Natural Language Processing Toolkit for Many Human Languages.](https://arxiv.org/abs/2003.07082) arXiv preprint arXiv:2003.07082. \[[pdf](https://arxiv.org/pdf/2003.07082.pdf)\]

If you use Stanford CoreNLP through the Stanza python client, please also follow the instructions [here](https://stanfordnlp.github.io/CoreNLP/#citing-stanford-corenlp-in-papers) to cite the proper publications.

## Links

* [GitHub](https://github.com/stanfordnlp/stanza)
* [PyPI](https://pypi.org/project/stanza/)
* [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/)