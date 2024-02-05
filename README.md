# Toxic Comment Classification Project
### Overview

This project addresses the critical issue of toxic comments on online platforms. Our solution aims to effectively identify toxic comments and reduce biases associated with specific demographic identities.
Here is the link to this [Kaggle competition](https://www.kaggle.com/competitions/toxic-comment-classification-dsba-2023-2)

### Objectives
Accurate Identification of Toxicity: Build models to accurately determine toxicity levels in comments. <br>
Demographic Fairness: Ensure models are unbiased against specific demographic identities, maintaining uniform accuracy in toxicity detection across different groups. <br>

### Evaluation Critera 

Worst-Group Accuracy. 

- For every identity group two accuracies are calculated - Accuracy when the group is present, Accuracy when the group is not present.
- So, for 8 identity groups, we have 16 accuracies reported and the least of these is selected as the final metric for evaluation
- The idea behind this is to make sure that the model performs well in all cases and thus ensuring fairness

### Models Used
**BiDirectional LSTM with Attention Mechanism**: For capturing long-term dependencies within sequences. <br>
**BERT (RoBERTa)**: Utilized for its advanced language representation capabilities.

### Key Challenges
- Addressing class imbalance in the dataset.
- Ensuring model accuracy and fairness across different demographic groups.

### Loss Functions
- Weighted Binary Cross Entropy.
- Custom Loss Function, emphasizing subgroup fairness.
- Focal Loss, focusing on hard-to-classify examples.

### Results
Our project achieved outstanding success in the competition, securing the 1st place finish. Our models demonstrated remarkable performance in identifying toxic comments across various demographics, as reflected in our Worst-group Accuracy (WGA) scores:
- WGA - 83.9 (RoBERTa)
- WGA (after deadline) - 84.5 (BiLSTM + Attention)

