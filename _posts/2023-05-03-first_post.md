# Getting started

1. TOC
{:toc}

## What is fast.ai

fastai is a deep learning library based on Pytorch.

## Dataloader

Pytorch iterates through to grap a bunch of data at a time.

A Dataloader will feed the training algorithm with a `batch` of images at once.

```python
# Show me an example of a batch of data
dls.showbatch()
```

## Learner

Learner is something that combines a model - the actual neural network function we'll be training.

Have to pass in two things: data and a model.
### .fine_tune()

Takes those pre-trained weights and adjust them in a carefully controlled way. To teach model the differences between your dataset and what it originally trained for. 