---
layout: post
title: "simple-statistics"
date: 2017-02-03 05:02:48 +0000
comments: true
categories: math
---

#[simple-statistics](https://www.npmjs.com/package/simple-statistics)
> Descriptive, regression, and inference statistics.

`simple-statistics` module is a neat pack of most commonly used functional for statistical analysis. 

It contains about `62` helper methods bundled with it : 

```js
[ 'linearRegression',
  'linearRegressionLine',
  'standardDeviation',
  'rSquared',
  'mode',
  'modeSorted',
  'min',
  'max',
  'minSorted',
  'maxSorted',
  'sum',
  'sumSimple',
  'product',
  'quantile',
  'quantileSorted',
  'interquartileRange',
  'iqr',
  'mad',
  'medianAbsoluteDeviation',
  'chunk',
  'shuffle',
  'shuffleInPlace',
  'sample',
  'ckmeans',
  'uniqueCountSorted',
  'sumNthPowerDeviations',
  'equalIntervalBreaks',
  'sampleCovariance',
  'sampleCorrelation',
  'sampleVariance',
  'sampleStandardDeviation',
  'sampleSkewness',
  'permutationsHeap',
  'combinations',
  'combinationsReplacement',
  'geometricMean',
  'harmonicMean',
  'average',
  'mean',
  'median',
  'medianSorted',
  'rms',
  'rootMeanSquare',
  'variance',
  'tTest',
  'tTestTwoSample',
  'bayesian',
  'perceptron',
  'epsilon',
  'factorial',
  'bernoulliDistribution',
  'binomialDistribution',
  'poissonDistribution',
  'chiSquaredGoodnessOfFit',
  'zScore',
  'cumulativeStdNormalProbability',
  'standardNormalTable',
  'erf',
  'errorFunction',
  'inverseErrorFunction',
  'probit',
  'mixin',
  'bisect' ]
```

__Get it:__ `npm install --save simple-statistics`

__Sample usage:__


```js
const ss = require('simple-statistics');

ss.mad([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]);
// ^ 3; median absolute deviation.

ss.combinations([1, 2, 3], 2);

/*

[
    [1, 2],
    [1, 3],
    [2, 3]
]
*/
```

__GIF FTW!__

![](/images/simple-statistics/simple-statistics.gif)