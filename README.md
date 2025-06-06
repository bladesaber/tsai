# tsai


<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->

<div align="center">

<img src="https://github.com/timeseriesAI/tsai/blob/main/nbs/multimedia/tsai_logo.svg?raw=true" width="50%">

</div>

<br /> <br />

![CI](https://github.com/timeseriesai/tsai/workflows/CI/badge.svg)
[![PyPI](https://img.shields.io/pypi/v/tsai?color=blue&label=pypi%20version.png)](https://pypi.org/project/tsai/#description)
[![Conda (channel
only)](https://img.shields.io/conda/vn/timeseriesai/tsai?color=brightgreen&label=conda%20version.png)](https://anaconda.org/timeseriesai/tsai)
[![DOI](https://zenodo.org/badge/211822289.svg)](https://zenodo.org/badge/latestdoi/211822289)
![PRs](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

## Description

> State-of-the-art Deep Learning library for Time Series and Sequences.

`tsai` is an open-source deep learning package built on top of Pytorch &
fastai focused on state-of-the-art techniques for time series tasks like
classification, regression, forecasting, imputation…

`tsai` is currently under active development by timeseriesAI.

## What’s new:

During the last few releases, here are some of the most significant
additions to `tsai`:

- **New models**: PatchTST (Accepted by ICLR 2023), RNN with Attention
  (RNNAttention, LSTMAttention, GRUAttention), TabFusionTransformer, …
- **New datasets**: we have increased the number of datasets you can
  download using `tsai`:
  - 128 univariate classification datasets
  - 30 multivariate classification datasets
  - 15 regression datasets
  - 62 forecasting datasets
  - 9 long term forecasting datasets
- **New tutorials**:
  [PatchTST](https://github.com/timeseriesAI/tsai/blob/main/tutorial_nbs/15_PatchTST_a_new_transformer_for_LTSF.ipynb).
  Based on some of your requests, we are planning to release additional
  tutorials on data preparation and forecasting.
- **New functionality**: sklearn-type pipeline transforms, walk-foward
  cross validation, reduced RAM requirements, and a lot of new
  functionality to perform more accurate time series forecasts.
- Pytorch 2.0 support.

## Installation

### Pip install

You can install the **latest stable** version from pip using:

``` python
pip install tsai
```

If you plan to develop tsai yourself, or want to be on the cutting edge,
you can use an editable install. First install PyTorch, and then:

``` python
git clone https://github.com/timeseriesAI/tsai
pip install -e "tsai[dev]"
```

Note: starting with tsai 0.3.0 tsai will only install hard dependencies.
Other soft dependencies (which are only required for selected tasks)
will not be installed by default (this is the recommended approach. If
you require any of the dependencies that is not installed, tsai will ask
you to install it when necessary). If you still want to install tsai
with all its dependencies you can do it by running:

``` python
pip install tsai[extras]
```

### Conda install

You can also install tsai using conda (note that if you replace conda
with mamba the install process will be much faster and more reliable):

``` python
conda install -c timeseriesai tsai
```

## Documentation

Here’s the link to the
[documentation](https://timeseriesai.github.io/tsai/).

## Available models:

Here’s a list with some of the state-of-the-art models available in
`tsai`:

- [LSTM](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/RNN.py)
  (Hochreiter, 1997)
  ([paper](https://ieeexplore.ieee.org/abstract/document/6795963/))
- [GRU](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/RNN.py)
  (Cho, 2014) ([paper](https://arxiv.org/abs/1412.3555))
- [MLP](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/MLP.py) -
  Multilayer Perceptron (Wang, 2016)
  ([paper](https://arxiv.org/abs/1611.06455))
- [FCN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/FCN.py) -
  Fully Convolutional Network (Wang, 2016)
  ([paper](https://arxiv.org/abs/1611.06455))
- [ResNet](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/ResNet.py) -
  Residual Network (Wang, 2016)
  ([paper](https://arxiv.org/abs/1611.06455))
- [LSTM-FCN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/RNN_FCN.py)
  (Karim, 2017) ([paper](https://arxiv.org/abs/1709.05206))
- [GRU-FCN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/RNN_FCN.py)
  (Elsayed, 2018) ([paper](https://arxiv.org/abs/1812.07683))
- [mWDN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/mWDN.py) -
  Multilevel wavelet decomposition network (Wang, 2018)
  ([paper](https://dl.acm.org/doi/abs/10.1145/3219819.3220060))
- [TCN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TCN.py) -
  Temporal Convolutional Network (Bai, 2018)
  ([paper](https://arxiv.org/abs/1803.01271))
- [MLSTM-FCN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/RNN_FCN.py) -
  Multivariate LSTM-FCN (Karim, 2019)
  ([paper](https://www.sciencedirect.com/science/article/abs/pii/S0893608019301200))
- [InceptionTime](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/InceptionTime.py)
  (Fawaz, 2019) ([paper](https://arxiv.org/abs/1909.04939))
- [Rocket](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/ROCKET.py)
  (Dempster, 2019) ([paper](https://arxiv.org/abs/1910.13051))
- [XceptionTime](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/XceptionTime.py)
  (Rahimian, 2019) ([paper](https://arxiv.org/abs/1911.03803))
- [ResCNN](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/ResCNN.py) -
  1D-ResCNN (Zou , 2019)
  ([paper](https://www.sciencedirect.com/science/article/pii/S0925231219311506))
- [TabModel](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TabModel.py) -
  modified from fastai’s
  [TabularModel](https://docs.fast.ai/tabular.model.html#TabularModel)
- [OmniScale](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/OmniScaleCNN.py) -
  Omni-Scale 1D-CNN (Tang, 2020)
  ([paper](https://arxiv.org/abs/2002.10061))
- [TST](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TST.py) -
  Time Series Transformer (Zerveas, 2020)
  ([paper](https://dl.acm.org/doi/abs/10.1145/3447548.3467401))
- [TabTransformer](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TabTransformer.py)
  (Huang, 2020) ([paper](https://arxiv.org/pdf/2012.06678))
- [TSiT](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TSiTPlus.py)
  Adapted from ViT (Dosovitskiy, 2020)
  ([paper](https://arxiv.org/abs/2010.11929))
- [MiniRocket](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/MINIROCKET.py)
  (Dempster, 2021) ([paper](https://arxiv.org/abs/2102.00457))
- [XCM](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/XCM.py) -
  An Explainable Convolutional Neural Network (Fauvel, 2021)
  ([paper](https://hal.inria.fr/hal-03469487/document))
- [gMLP](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/gMLP.py) -
  Gated Multilayer Perceptron (Liu, 2021)
  ([paper](https://arxiv.org/abs/2105.08050))
- [TSPerceiver](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TSPerceiver.py) -
  Adapted from Perceiver IO (Jaegle, 2021)
  ([paper](https://arxiv.org/abs/2107.14795))
- [GatedTabTransformer](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/GatedTabTransformer.py)
  (Cholakov, 2022) ([paper](https://arxiv.org/abs/2201.00199))
- [TSSequencerPlus](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/TSSequencerPlus.py) -
  Adapted from Sequencer (Tatsunami, 2022)
  ([paper](https://arxiv.org/abs/2205.01972))
- [PatchTST](https://github.com/timeseriesAI/tsai/blob/main/tsai/models/PatchTST.py) -
  (Nie, 2022) ([paper](https://arxiv.org/abs/2211.14730))

plus other custom models like: TransformerModel, LSTMAttention,
GRUAttention, …

## How to start using tsai?

To get to know the tsai package, we’d suggest you start with this
notebook in Google Colab:
**[01_Intro_to_Time_Series_Classification](https://colab.research.google.com/github/timeseriesAI/tsai/blob/master/tutorial_nbs/01_Intro_to_Time_Series_Classification.ipynb)**
It provides an overview of a time series classification task.

We have also develop many other [tutorial
notebooks](https://github.com/timeseriesAI/tsai/tree/main/tutorial_nbs).

To use tsai in your own notebooks, the only thing you need to do after
you have installed the package is to run this:

``` python
from tsai.all import *
```

## Examples

These are just a few examples of how you can use `tsai`:

### Binary, univariate classification

**Training:**

``` python
from tsai.basics import *

X, y, splits = get_classification_data('ECG200', split_data=False)
tfms = [None, TSClassification()]
batch_tfms = TSStandardize()
clf = TSClassifier(X, y, splits=splits, path='models', arch="InceptionTimePlus", tfms=tfms, batch_tfms=batch_tfms, metrics=accuracy, cbs=ShowGraph())
clf.fit_one_cycle(100, 3e-4)
clf.export("clf.pkl") 
```

**Inference:**

``` python
from tsai.inference import load_learner

clf = load_learner("models/clf.pkl")
probas, target, preds = clf.get_X_preds(X[splits[1]], y[splits[1]])
```

### Multi-class, multivariate classification

**Training:**

``` python
from tsai.basics import *

X, y, splits = get_classification_data('LSST', split_data=False)
tfms = [None, TSClassification()]
batch_tfms = TSStandardize(by_sample=True)
mv_clf = TSClassifier(X, y, splits=splits, path='models', arch="InceptionTimePlus", tfms=tfms, batch_tfms=batch_tfms, metrics=accuracy, cbs=ShowGraph())
mv_clf.fit_one_cycle(10, 1e-2)
mv_clf.export("mv_clf.pkl")
```

**Inference:**

``` python
from tsai.inference import load_learner

mv_clf = load_learner("models/mv_clf.pkl")
probas, target, preds = mv_clf.get_X_preds(X[splits[1]], y[splits[1]])
```

### Multivariate Regression

**Training:**

``` python
from tsai.basics import *

X, y, splits = get_regression_data('AppliancesEnergy', split_data=False)
tfms = [None, TSRegression()]
batch_tfms = TSStandardize(by_sample=True)
reg = TSRegressor(X, y, splits=splits, path='models', arch="TSTPlus", tfms=tfms, batch_tfms=batch_tfms, metrics=rmse, cbs=ShowGraph(), verbose=True)
reg.fit_one_cycle(100, 3e-4)
reg.export("reg.pkl")
```

**Inference:**

``` python
from tsai.inference import load_learner

reg = load_learner("models/reg.pkl")
raw_preds, target, preds = reg.get_X_preds(X[splits[1]], y[splits[1]])
```

The ROCKETs (RocketClassifier, RocketRegressor, MiniRocketClassifier,
MiniRocketRegressor, MiniRocketVotingClassifier or
MiniRocketVotingRegressor) are somewhat different models. They are not
actually deep learning models (although they use convolutions) and are
used in a different way.

⚠️ You’ll also need to install sktime to be able to use them. You can
install it separately:

``` python
pip install sktime
```

or use:

``` python
pip install tsai[extras]
```

**Training:**

``` python
from sklearn.metrics import mean_squared_error, make_scorer
from tsai.data.external import get_Monash_regression_data
from tsai.models.MINIROCKET import MiniRocketRegressor

X_train, y_train, *_ = get_Monash_regression_data('AppliancesEnergy')
rmse_scorer = make_scorer(mean_squared_error, greater_is_better=False)
reg = MiniRocketRegressor(scoring=rmse_scorer)
reg.fit(X_train, y_train)
reg.save('MiniRocketRegressor')
```

**Inference:**

``` python
from sklearn.metrics import mean_squared_error
from tsai.data.external import get_Monash_regression_data
from tsai.models.MINIROCKET import load_minirocket

*_, X_test, y_test = get_Monash_regression_data('AppliancesEnergy')
reg = load_minirocket('MiniRocketRegressor')
y_pred = reg.predict(X_test)
mean_squared_error(y_test, y_pred, squared=False)
```

### Forecasting

You can use tsai for forecast in the following scenarios:

- univariate or multivariate time series input
- univariate or multivariate time series output
- single or multi-step ahead

You’ll need to: \* prepare X (time series input) and the target y (see
[documentation](https://timeseriesai.github.io/tsai/data.preparation.html))
\* select PatchTST or one of tsai’s models ending in Plus (TSTPlus,
InceptionTimePlus, TSiTPlus, etc). The model will auto-configure a head
to yield an output with the same shape as the target input y.

#### Single step

**Training:**

``` python
from tsai.basics import *

ts = get_forecasting_time_series("Sunspots").values
X, y = SlidingWindow(60, horizon=1)(ts)
splits = TimeSplitter(235)(y) 
tfms = [None, TSForecasting()]
batch_tfms = TSStandardize()
fcst = TSForecaster(X, y, splits=splits, path='models', tfms=tfms, batch_tfms=batch_tfms, bs=512, arch="TSTPlus", metrics=mae, cbs=ShowGraph())
fcst.fit_one_cycle(50, 1e-3)
fcst.export("fcst.pkl")
```

**Inference:**

``` python
from tsai.inference import load_learner

fcst = load_learner("models/fcst.pkl", cpu=False)
raw_preds, target, preds = fcst.get_X_preds(X[splits[1]], y[splits[1]])
raw_preds.shape
# torch.Size([235, 1])
```

#### Multi-step

This example show how to build a 3-step ahead univariate forecast.

**Training:**

``` python
from tsai.basics import *

ts = get_forecasting_time_series("Sunspots").values
X, y = SlidingWindow(60, horizon=3)(ts)
splits = TimeSplitter(235, fcst_horizon=3)(y) 
tfms = [None, TSForecasting()]
batch_tfms = TSStandardize()
fcst = TSForecaster(X, y, splits=splits, path='models', tfms=tfms, batch_tfms=batch_tfms, bs=512, arch="TSTPlus", metrics=mae, cbs=ShowGraph())
fcst.fit_one_cycle(50, 1e-3)
fcst.export("fcst.pkl")
```

**Inference:**

``` python
from tsai.inference import load_learner
fcst = load_learner("models/fcst.pkl", cpu=False)
raw_preds, target, preds = fcst.get_X_preds(X[splits[1]], y[splits[1]])
raw_preds.shape
# torch.Size([235, 3])
```

## Input data format

The input format for all time series models and image models in tsai is
the same. An np.ndarray (or array-like object like zarr, etc) with 3
dimensions:

**\[# samples x \# variables x sequence length\]**

The input format for tabular models in tsai (like TabModel,
TabTransformer and TabFusionTransformer) is a pandas dataframe. See
[example](https://timeseriesai.github.io/tsai/models.TabModel.html).

## How to contribute to tsai?

We welcome contributions of all kinds. Development of enhancements, bug
fixes, documentation, tutorial notebooks, …

We have created a guide to help you start contributing to tsai. You can
read it
[here](https://github.com/timeseriesAI/tsai/blob/main/CONTRIBUTING.md).

## Enterprise support and consulting services:

Want to make the most out of timeseriesAI/tsai in a professional
setting? Let us help. Send us an email to learn more:
info@timeseriesai.co

## Citing tsai

If you use tsai in your research please use the following BibTeX entry:

``` text
@Misc{tsai,
    author =       {Ignacio Oguiza},
    title =        {tsai - A state-of-the-art deep learning library for time series and sequential data},
    howpublished = {Github},
    year =         {2023},
    url =          {https://github.com/timeseriesAI/tsai}
}
```
