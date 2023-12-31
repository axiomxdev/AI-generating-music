## AI generating music

I created an AI generator based on a script developed by [Andrej Karpathy](https://github.com/karpathy) on [this code](https://colab.research.google.com/drive/1JMLa53HDuA-i7ZBmqV7ZnA3c_fvtXnx-?usp=sharing).

## How does it work?
- 1 Installing a folder

Execute this command in cmd.
```bash
git clone https://github.com/axiomxdev/AI-generating-music.git
```

- 2 Installing a text database

for starters, if you want to make an AI that generates something other than text, you should paste the text here,
```bash
IA\data set\all_artist_data_artist.txt
```

Otherwise, go to
```bash
IA\data set\get data set.py
```

changed the name of artist at the launch of function line 69.
```python
GetTiny("Ed-sheeran")
```

The best is to add a dozen artist, for this copied paste the function and mixing a new artist.
Before launching this script, make sure that his is the right artist by checking on [genius](https://genius.com)
```json
https://genius.com/{artist}
```

now, you can execute the file,
ps : don't debug and execute, juste execute.

- 3 You have these hyperparameters,
 
 | hyperparameter | value | explanation
 | --- | --- | --- |
 | batch_size | 16 | Batch size (number of examples) used when training the AI at each iteration.
 | block_size | 32 | The size of the block used to split data into sequences or batches. | 
 | max_iters | 1000000 | The maximum number of training iterations (steps) to be performed. | 
 | eval_interval | 1000 | How often AI performance evaluation is performed (in number of iterations). | 
 | learning_rate | 0.001 | Learning rate, which determines the size of adjustments made to model weights with each update. | 
 | eval_iters | 200 | Number of iterations between each performance assessment (e.g. loss calculation) of the AI. | 
 | n_embd | 64 | Number of units in embedding. | 
 | n_head | 4 | Number of heads in multi-head attention mechanisms. | 
 | n_layer | 4 | Total number of layers in the AI model. | 
 | dropout | 0.0 | Probability of deactivation of neurons during training, where 0 means no dropout. | 

You can change these hyperparameters in the IA\IA script\hyperparameters.json file.

Once all the hyperparamis put to your liking, you can simply execute the file and wait for the end of the training.

- 4 text generation

Once the script is finished, you have a new file called `IA_training.pth` which is the whole AI training.
You can now run the script
```bash
IA\IA script\generator txt.py
```
You have 2 parameter entered the console for each generation:

1e the text that the generator will take to start and have a consistency with (you can leave blank).

2nd entered the number of characters you want in the text.
