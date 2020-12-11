# Metaphor & novelty

A code base for jointly predicting binary metaphor labels and numerical metaphor novelty scores using BERT.<br/>

## Installation

Confirmed to run with:
```
transformers==2.8.0
torch==1.5.1
```
## Usage
```
python main.py --seed <int> --lr <float> --train_steps <int> --batch_size <int>
               --alpha <float> --beta <float> --metaphor_weight <float> 
```

- alpha & beta regulate the contributions to the loss for the metaphor detection and novelty prediction tasks, respectively.
- metaphor_weights regulates the weight of the positive class for the metaphor detection task. Set it >> 0.5, since metaphors are pretty rare.
