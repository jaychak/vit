# Vision Transformer and Vision Transformer - Masked Autoencoder Playground

In this repo, I have several ipython notebooks for playing with ViT and ViT-MAE models.
I have both training, fine-tuning and linear probing code in stand-alone notebooks.

## Notebooks
- [`vit_train_test.ipynb`] Trains a ViT from scratch and tests it. Dataloaders tested for the CIFAR10 dataset and the UCMerced dataset.
- [`vit_mae_train_scratch.ipynb`] Trains a ViT-MAE from scratch.
- [`vit_mae_test.ipynb`] Tests a ViT-MAE on data by reconstructing input images after 75% of them have been randomly masked out.
- [`vit_mae_finetune.ipynb`] Fine-tunes a pre-trained ViT-MAE on new data.
- [`vit_mae_linprobe_train.ipynb`] Trains an MLP head on top of the encoder of a pre-trained ViT-MAE for an image classification task.
- [`vit_mae_linprobe_test.ipynb`] Tests above model.
- [`resnet_train_test.ipynb`] Trains and tests a Resnet (for comparison with ViT/ViT-MAE).

Note that the Resnet beats the ViT/MAE on small datasets like CIFAR-10. 
The ViT supposedly excels in bigger datasets.  

The ViT is from the paper
- [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)

![Local Image](images/vit.png)

The ViT-MAE is from the paper
- [Masked Autoencoders Are Scalable Vision Learners](https://arxiv.org/abs/2111.06377)

![Local Image](images/vitmae.png)


## Disclaimers

This repo has borrowed from 
https://uvadlc-notebooks.readthedocs.io/en/latest/tutorial_notebooks/tutorial15/Vision_Transformer.html for the ViT
and https://github.com/facebookresearch/mae for the ViT-MAE



## Bibtex

```
@article{dosovitskiy2020vit,
  title={An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale},
  author={Dosovitskiy, Alexey and Beyer, Lucas and Kolesnikov, Alexander and Weissenborn, Dirk and Zhai, Xiaohua and Unterthiner, Thomas and  Dehghani, Mostafa and Minderer, Matthias and Heigold, Georg and Gelly, Sylvain and Uszkoreit, Jakob and Houlsby, Neil},
  journal={ICLR},
  year={2021}
}

@Article{MaskedAutoencoders2021,
  author  = {Kaiming He and Xinlei Chen and Saining Xie and Yanghao Li and Piotr Doll{\'a}r and Ross Girshick},
  journal = {arXiv:2111.06377},
  title   = {Masked Autoencoders Are Scalable Vision Learners},
  year    = {2021},
}
```