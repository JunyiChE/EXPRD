# EXPRD
Source code submitted for anonymous review at **ACL 2024** for the paper **"Grasping the Why: Explainable Graph Learning for Rumor Detection with Lucid Insights"**.

## Core Dependencies
Ensure you have the following core dependencies installed:

- **Python 3.7**
- **PyTorch 1.8.1**
- **PyTorch Geometric 1.7.0**

## Reproduce the Experiments
To reproduce the experiments, follow these commands:

```bash
# Pre-process the Twitter15 dataset
python ./Process/getTwittergraph.py Twitter15

# Pre-process the Twitter16 dataset
python ./Process/getTwittergraph.py Twitter16

# Train the model on Twitter15 for 100 epochs
python ./Model/train.py Twitter15 100

# Train the model on Twitter16 for 100 epochs
python ./Model/train.py Twitter16 100
```
## Rumor Detection Dataset
We utilize the following datasets for our experiments:

- [**Twitter15, Twitter16**](https://github.com/majingCUHK/Rumor_RvNN): These datasets are manually added to the folder.
- [**PHEME**](https://github.com/kochkinaelena/Multitask4Veracity): A significantly larger dataset.

## Prompt Dataset
A sample prompt dataset named `prompt_data.json` is uploaded, containing approximately 10K question and answer pairs for fine-tuning existing LLMs. Each instance in the dataset is structured as follows:

- **Instruction**: Analyze tweet details for conversation examples. One instruction per instance.
- **User**: Asks about rumor detection outcome, model's prediction reasoning, confidence score, and contributions definitions. Multiple user queries per instance.
- **Assistant**: Explains false rumor detection, prediction rationale, confidence score significance, and contributions' impact. The number of assistant responses equals the number of user queries.

## NOTE
The resources are currently not organized very nicely and are built for interested reviewers to quickly reimplement the experiments. Future updates will be made very soon.

