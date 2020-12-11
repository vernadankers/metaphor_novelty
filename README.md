# neural_metaphor_discourse

A code base for performing metaphor detection using neural models that incorporate discourse-level information.<br/>
The two sequence labelling models implemented are:
1.   Concatenated ELMo and GloVe embeddings fed to a one-layer LSTM model, followed by a linear classification layer and softmax;
2.   BERT-base-cased followed by a linear classification layer and softmax.

Discourse-level information is included through a discourse vector concatenated to the input of the linear classification layer.
We define discourse through a window of size <i>2k+1</i>, with <i>k=0</i> including only the immediate sentential context.

## Installation

## Usage

```
python main.py --model "elmo" | "bert" --attention "general" | "hierarchical"
               --seed <int> --k <int> --lr <float> --epochs <int> --batch_size <int>
               --meta_train <filename> --meta_dev <filename> --meta_test <filename> --output <filename> 
```

## Credits

Credits to my co-authors:<br/>
[@kmalhotra30](https://github.com/kmalhotra30)<br/>
[@gkudva96](https://github.com/gkudva96)<br/>
[@vovamedentsiy](https://github.com/vovamedentsiy)<br/> 
[@eshutova](https://github.com/eshutova)<br/>

## License

[MIT](https://choosealicense.com/licenses/mit/)