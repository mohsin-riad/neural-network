# Custom Neural Network  

## Predicting Texual Emotions 
### Dataset Contents
<img width=“964” alt=“Table1” src=images/dset.png>

---

> Samples Total : **Training** 4700, **Testing** 940 

> Dimensionality : **Dynamic** [200, 220, 240, 260, 280, 300, 350, 800]
> * Experimental dimensions: *average words per line* `x` *Embedding dim. Per word*

---

### Experiment Contents

> Activations :  **relu**, **softmax**, **tanh**

> Optimizers : **Adam**

> Loss : **MSE**, **Binary Crossentropy**, **categorical_crossentropy** 

> Dataset Constraints:
> * VOCUB_SIZE: **17577**, **17261**, **15397**
> * MAX_LENGTH: Average words per line [**train**: 17, **Test**:10]

*[`***`Best Accuracy from Best Model highlighted]*

<img width=“964” alt=“Table1” src=images/table.png>

---

## Other

> **Reference link :** 
* [*wikipedia*](https://en.wikipedia.org/wiki/Multi-label_classification)
* [*Bangla NLP*](https://bnlp.readthedocs.io/en/latest)