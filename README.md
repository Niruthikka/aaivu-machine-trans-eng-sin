# English to Sinhala Neural Machine Translation

![project] ![research]



- <b>Project Mentor</b>
    1. Dr Uthayasanker Thayasivam
- <b>Contributors</b>
    1. Thilakshi Fonseka
    2. Rashmini Naranpanawa
    3. Ravinga Perera

---

## Summary

This research is about developing a NMT system using Transformer architecture for the under-resourced, domain-specific English to Sinhala translation task. The translation quality is improved by exploring effective ways of incorporating Part-of-Speech (POS) information and subword techniques.

## Description

This project consists of the following.

- Transformer baseline 
- Transformer with subword segmentation 
    - Byte Pair Encoding
    - Unigram based subword regularization
- Transformer with Part-of-Speech (POS) 
    - Input embedding
    - Positional encoding
    
### Architecture Diagrams

Following are the architecture diagrams for the POS integration with the input embedding and positional encoding respectively.

<p align="center">
<img src="https://github.com/aaivu/aaivu-machine-trans-eng-sin/blob/master/docs/images/Architecture-diagram-pos-integration-input-embedding.jpg" width="600">
<img src="https://github.com/aaivu/aaivu-machine-trans-eng-sin/blob/master/docs/images/Architecture-diagram-pos-integration-positional-encoding.jpg" width="600">
</p>

The following instructions will guide to produce our results. 

### Requirements

We use [fairseq](https://github.com/pytorch/fairseq) for training, [sentencepiece](https://github.com/google/sentencepiece) for preprocessing & [sacrebleu](https://github.com/mjpost/sacrebleu) to produce BLEU scores.

**Transformer Baseline**

```
pip install fairseq sacrebleu 
```

**Transformer with subword segmentation**

```
pip install fairseq sacrebleu sentencepiece
```

**Transformer with POS**

```
pip install sacrebleu sentencepiece
```
Since POS is implemented withing the fairseq-transformer, navigate to the project directory and install fairseq as following

```
pip install --editable ./
```

### Train the baseline transformer model 

- Navigate to `src/Transformer-baseline`. Follow the instructions given in the `README.md`.

### Train the subword segmented transformer models 

- To train the Transformer BPE model, navigate to `src/Subword-segmentation/Transformer-BPE`. Follow the instructions given in the `README.md`.
- To train the Transformer subword regularization model, navigate to `src/Subword-segmentation/Transformer-subword-regularization`. Follow the instructions given in the `README.md`.

### Train the POS integrated transformer models

- To train the Transformer model with POS integrated to the input embedding, navigate to `src/POS-implementation/Fairseq-POS-integration-input-embedding/`. Follow the instructions given in the `README.md`.
- To train the Transformer model with POS integrated to the positional encoding unit, navigate to `src/POS-implementation/fairseq/`. Follow the instructions given in the `README.md`.
---

### License

Apache License 2.0

### Code of Conduct

Please read our [code of conduct document here](https://github.com/aaivu/aaivu-introduction/blob/master/docs/code_of_conduct.md).

[project]: https://img.shields.io/badge/-Project-blue
[research]: https://img.shields.io/badge/-Research-yellowgreen
