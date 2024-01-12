# LLM-Basics

## Pre-training phase - Decoder from scratch (Andrej Karpathy)
1. Implemented video code (Andrej Karpathy)

    video Link: [https://www.youtube.com/watch?v=kCc8FmEb1nY](https://www.youtube.com/watch?v=kCc8FmEb1nY)

2. Tried with Harry potter dataset (1 book)
3. Tried with all 7 books- decent results
4. increased batch-size (context length) and used frequency encoding (character based) - better loss (1.8)
5. Increased epochs - better results (final loss - 1.4 )
6. Tried bert based encoding and decoding 

    After 1 epoch loss = 10.47

    After 100 epochs loss = 6.31

    After 300 epochs loss = 5.59

colab link: [https://colab.research.google.com/drive/1w2xrCzgQ7PejGULuiaOY_mQfZKdtH8UW](https://colab.research.google.com/drive/1w2xrCzgQ7PejGULuiaOY_mQfZKdtH8UW)
## Important terms
* [Torch LR finder](https://pytorch-lightning.readthedocs.io/en/1.4.9/advanced/lr_finder.html): the learning rate is increased after each processed batch and the corresponding loss is logged. The result of this is a lr vs. loss plot that can be used as guidance for choosing a optimal initial lr.
* [One cycle policy](https://medium.com/dsnet/the-1-cycle-policy-an-experiment-that-vanished-the-struggle-in-training-neural-nets-184417de23b9): start with a lower learning rate, gradually increase it to a maximum value (the peak of the cycle), and then gradually decrease it again. Additionally, during the cycle, the momentum is typically increased and then decreased. The intuition is that starting with a lower learning rate helps the model converge, and using a higher learning rate during the middle of training allows the model to escape sharp minima and explore the loss landscape more efficiently. Towards the end of training, reducing the learning rate helps the model converge to a more refined solution.
  
## Supervised Fine-tuning phase - Phi2 with qlora
Will update soon xD
