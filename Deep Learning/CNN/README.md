# Deep Learning / CNN

A visual, mathematical CNN revision guide for an M.Tech AI student moving from core ML into deep learning research. Its teaching sequence follows the CS231n ConvNet chapter: architecture, convolution, spatial dimensions, sharing and channels, nonlinearities, pooling, normalization, classifier heads, architecture design, and compute.

## Main guide

**[Download the revised CNN theory, diagrams, PyTorch, and interview guide](CNN-Revision-Notes-and-Interview-Guide.pdf)**

Every core topic includes an explanation, original vector diagram, equations, PyTorch pattern, and an answered interview question. The guide also includes a complete small CNN, a residual-block example, a 20-question interview set, and a research-paper reading order. It contains no D2L implementation.

## Companion PyTorch example

- [cnn_examples.py](cnn_examples.py) includes an original CNN classifier, a residual block, convolution output-size helper, and train/evaluation epoch functions.

Run with Python and PyTorch installed:

```bash
python cnn_examples.py
```

The model expects floating-point RGB images shaped `(N, 3, H, W)` and returns raw logits. Use `CrossEntropyLoss` directly on those logits.

## Further reading

- [CS231n: Convolutional Neural Networks](https://cs231n.github.io/convolutional-networks/) - conceptual organization used for the guide.
- [D2L: why convolution](https://d2l.ai/chapter_convolutional-neural-networks/why-conv.html), [convolution layer](https://d2l.ai/chapter_convolutional-neural-networks/conv-layer.html), [padding and strides](https://d2l.ai/chapter_convolutional-neural-networks/padding-and-strides.html), [channels](https://d2l.ai/chapter_convolutional-neural-networks/channels.html), and [pooling](https://d2l.ai/chapter_convolutional-neural-networks/pooling.html) are optional theory references only.
- The PDF links primary papers on AlexNet, VGG, Batch Normalization, ResNet, U-Net, nnU-Net, and Vision Transformer.

## Sources and license

The PDF contains original explanations, examples, and vector diagrams linked to primary and educational references; no source figures or D2L implementation are reproduced. Companion code is MIT-licensed; see [LICENSE-CODE.txt](LICENSE-CODE.txt) and [ATTRIBUTION.md](ATTRIBUTION.md).
# Deep Learning - CNN

**[Read or download the 27-page revision PDF](CNN-Revision-Notes-and-Interview-Guide.pdf)**

Based on D2L sections 7.1-7.6, with original diagrams, worked examples, two PyTorch architectures and **30 interview questions with solutions**.

## Contents

| Topic | PDF pages |
|---|---|
| Coverage and notation | 1-2 |
| Why convolution; cross-correlation; edges and activations | 3-5 |
| Parameter sharing; padding, stride and dilation | 6-8 |
| Channels, 1x1 and grouped/depthwise convolution | 9-10 |
| Pooling, gradients and receptive fields | 11-13 |
| LeNet architecture and parameter accounting | 14 |
| PyTorch models, data, training and evaluation | 15-18 |
| Debugging, formulas and references | 19-21 |
| Interview questions and solutions | 22-27 |

## Code

- [cnn_models.py](cnn_models.py): LeNet, SmallCNN and educational cross-correlation.
- [train.py](train.py): Fashion-MNIST train/validation/test workflow.
- [test_cnn.py](test_cnn.py): eight offline correctness checks.

```bash
python -m pip install torch torchvision
python -m unittest -v test_cnn.py
python cnn_models.py
python train.py --model lenet --epochs 10 --output runs/lenet
python train.py --model small --epochs 10 --output runs/small
```

Eight checks passed on Python 3.12, PyTorch 2.14.1+cpu and torchvision 0.29.1+cpu. LeNet has 61,706 parameters; grayscale SmallCNN has 23,946. Full Fashion-MNIST training was not run; no benchmark accuracy is claimed. The trainer uses Adam rather than the D2L SGD recipe.

## Sources and license

See [ATTRIBUTION.md](ATTRIBUTION.md) for the D2L sources and changes. The adapted PDF is CC BY-SA 4.0; companion code is MIT under [LICENSE-CODE.txt](LICENSE-CODE.txt). This guide is not endorsed by the D2L authors.
