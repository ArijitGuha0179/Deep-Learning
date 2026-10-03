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
