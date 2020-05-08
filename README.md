# RNNs
This github project shows a few examples of what RNNs can do.
Recurrent Neural Networks (RNNs) are networks that can predict the future (not as easy). In these examples, I will use them in different but significant tasks.
## Generate text.
Using some real text, one can train a RNN to generate some artificial text, that in some way, is similar to the real text or follows the same trends. Obviously, the more complex the model, the more difficult is to distinct between the real and the generated text.
In this case, I chosed the famous book Frankenstein or the modern Prometheus by Mary Wollstonecraft. The whole book is preprocessed and then fed to the model, which will learn its style. Once the model is trained, I will use it to generate fake text from a single sentence (seed) from the book.

For comparision, the same model is trained during 5 and 50 epochs, and then used to generate some artificial text.
The results are very clear: the more the model is trained, the better the text is generated. This can be obvious, but given the amount of computational resources (and then time) the training involve, finding a good equilibrium between epochs and results might be a must.

### Future work
There are some ways to improve this project:
- providing more real text: in this case, the lenght of the text is fixed (it's a book), but probably one can use large texts, as many Wikipedia articles, to feed the RNN.
- more complex model: instead of LSTM layers, try to include GRU cells.
- remove the punctuation in the real text.
- train for more epochs (if you can).
- tune hyperparameters (batch_size).
- add dropout layers.

The book used in this project has been adapted from: https://www.gutenberg.org/ebooks/84, keeping only the letters and all the chapters provided.
## Sentimental analysis.
Based on some text (for example, movie reviews) and a sentimental label (positive or negative), a RNN can be trained to distinguish between positive or negative text, infering it from the text passed to the RNN.