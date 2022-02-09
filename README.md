# NLP Gutenberg Punctuation
(NLP course project) <br>
This repository contains the code for creating/using a model to punctuate,capitalize and reconstruct paragraphs for a dataset of books from the Gutenberg project. 
The code can be ran from a CLI using the following:<br>
 python src/main.py [-h] [-Action {train,evaluate,inference}] [-config CONFIG] [-download_data {y,yes,n,no}] [-book_data_path BOOK_DATA_PATH] [-train_config TRAIN_CONFIG]
 [-model_path MODEL_PATH] [-text TEXT] [-output OUTPUT] <br>
optional arguments: <br>
  -h, --help:            show this help message and exit <br>
  -Action {train,evaluate,inference}, -a {train,evaluate,inference}:
                        Desired action. Note that train will run evaluation as well <br>
  -config CONFIG:        configuration file *.y(a)ml <br>
  -download_data {y,yes,n,no}, -d {y,yes,n,no}:
                        Whether to download the dataset from gutenberg. Will default to yes if book_data_path is
                        not provided and previous data not found <br>
  -book_data_path BOOK_DATA_PATH, -b BOOK_DATA_PATH:
                        Path to location for saving/loading book data csv file. <br>
  -train_config TRAIN_CONFIG, -tc TRAIN_CONFIG:
                        Dictionary in the format {'batch_size':int,'num_epochs':int,'seq_len':int'}, only relevant
                        if train selected. Default: 30,25,150 <br>
  -model_path MODEL_PATH, -m MODEL_PATH:
                        Path to model. Must be provided if evaluate or inference selected <br>
  -text TEXT, -t TEXT:   Path to a text file for inference or evaluation. Note that evaluation will be meaningless
                        for text that is not fully punctuated. Must be provided if inference selected <br>
  -output OUTPUT, -o OUTPUT:
                        Path to output annotated text, if not provided will use stdout <br>
 
