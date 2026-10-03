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
