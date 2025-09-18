# CausalTalk: A Multi-Level Dataset for Causal Reasoning in COVID-19 Public Health Discussions

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.7+-blue.svg)

## Overview

CausalTalk is a comprehensive multi-level dataset comprising five years of Reddit posts (2020–2024) discussing public health topics related to the COVID-19 pandemic. The dataset focuses on causal reasoning in natural language, with 10,120 posts annotated across four distinct causal tasks by domain experts.

## Dataset Description

### Key Statistics
- **Time Period**: 2020-2024 (5 years)
- **Platform**: Reddit
- **Domain**: COVID-19 public health discussions
- **Annotated Posts**: 10,120
- **Annotation Source**: Gold-standard labels created by domain experts

### Causal Tasks

The dataset includes annotations for four complementary causal reasoning tasks:

1. **Binary Causal Classification**: Determining whether a post contains causal relationships
2. **Explicit vs. Implicit Causality**: Distinguishing between explicitly stated and implicitly implied causal relationships
3. **Cause–Effect Span Extraction**: Identifying and extracting specific text spans that represent causes and effects
4. **Causal Gist Generation**: Generating concise summaries that capture the essential causal relationships

## Dataset Structure

```
CausalTalk/
├── data/
│   ├── binary_classification/
│   ├── explicit_implicit/
│   ├── span_extraction/
│   └── gist_generation/
├── annotations/
│   └── expert_labels/
├── scripts/
│   ├── data_loading.py
│   ├── evaluation.py
│   └── baseline_models.py
└── README.md
```

## Data Format

Each annotation includes:
- **Post ID**: Unique identifier for the Reddit post
- **Text**: Original post content
- **Timestamp**: Post creation date
- **Causal Labels**: Task-specific annotations
- **Expert Annotations**: Gold-standard labels from domain experts

## Applications

This dataset enables research in:
- Causal reasoning in natural language processing
- Public health communication analysis
- Social media discourse understanding
- Multi-task learning for causal inference
- Domain-specific language understanding

## Usage

### Loading the Dataset

```python
import pandas as pd

# Load binary classification data
binary_data = pd.read_csv('data/binary_classification/train.csv')

# Load span extraction annotations
span_data = pd.read_csv('data/span_extraction/annotations.csv')
```

### Evaluation Metrics

- **Binary Classification**: Accuracy, Precision, Recall, F1-score
- **Span Extraction**: Exact Match, Partial Match, F1-score
- **Gist Generation**: BLEU, ROUGE, BERTScore

## Citation

If you use CausalTalk in your research, please cite our paper:

```bibtex
@article{causal_talk_2024,
  title={CausalTalk: A Multi-Level Dataset for Causal Reasoning in COVID-19 Public Health Discussions},
  author={[Authors]},
  journal={[Journal]},
  year={2024}
}
```

## License

This dataset is released under the MIT License. See [LICENSE](LICENSE) for details.

## Contributing

We welcome contributions to improve the dataset and associated tools. Please see our contribution guidelines for more information.

## Contact

For questions about the dataset or to report issues, please contact:
- Email: [contact_email]
- GitHub Issues: [Repository Issues Page]

## Acknowledgments

We thank the domain experts who contributed to the annotation process and the Reddit community for the valuable discussions that form the basis of this dataset.