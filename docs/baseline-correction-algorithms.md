# Baseline Correction Algorithms

---

## Table of Contents

1.  Introduction
2.  Summary
3.  Manual Algorithms
4.  Semi-Automatic Algorithms
5.  Automatic Algorithms
6.  Reviews

---

## Summary

| Algorithm                                                                    | Application | _a priori_ | Autonomy\* | Hyphenated\*\* | Reference                                                                               | Repository |
| :--------------------------------------------------------------------------- | :---------- | :--------- | :--------- | :------------- | :-------------------------------------------------------------------------------------- | :--------- |
| [Orthogonal Basis (OB)](#orthogonal-basis)                                   | TIC GC-MS   |            |            | Two-Way        |
| [Fuzzy Optimal Associative Memory (FOAM)](#fuzzy-optimal-associative-memory) |             |            |            | Two-Way        |
| [Iterative Polynomial Fitting](#iterative-polynomial-fitting)                |             |            |            | One-Way        |
| airPLS                                                                       |             |            |            |
| Top-Hat Filter                                                               |             |            |            |                | [GitHub](https://github.com/scipy/scipy/blob/v0.14.0/scipy/ndimage/morphology.py#L1631) |

Application: {
Mass Chromatogram: [TIC, EIC, SIM],
Chromatography: [GC, LC],
Spectrometry: [MS, MSMS]
}

---

## Orthogonal Basis

Xu, Zhanfeng, Xiaobo Sun, and Peter de B. Harrington. "**Baseline correction method using an orthogonal basis for gas chromatography/mass spectrometry data.**" Analytical chemistry 83.19 (2011): 7464-7471. [[pdf]](./pdfs/orthogonalbasis.pdf)

---

## Fuzzy Optimal Associative Memory

Wabuyele, Busolo Wa, and Petter de B. Harrington. "**Fuzzy optimal associative memory for background prediction of near-infrared spectra.**" Applied spectroscopy 50.1 (1996): 35-42.

---

## Iterative Polynomial Fitting

Gan, Feng, Guihua Ruan, and Jinyuan Mo. "**Baseline correction by improved iterative polynomial fitting with automatic threshold.**" Chemometrics and Intelligent Laboratory Systems 82.1-2 (2006): 59-65. [[pdf]](./pdfs/gan2006baseline.pdf)

---

## adaptive iteratively reweighted Penalized Least Squares (airPLS)

Zhang, Zhi-Min, Shan Chen, and Yi-Zeng Liang. "**Baseline correction using adaptive iteratively reweighted penalized least squares.**" Analyst 135.5 (2010): 1138-1146. [[pdf]](./pdfs/zhang2010.pdf) [[GitHub]](https://github.com/zmzhang/airPLS)

Baseline drift always blurs or even swamps signals and deteriorates analytical results, particularly in multivariate analysis. It is necessary to correct baseline drift to perform further data analysis. Simple or modified polynomial fitting has been found to be effective in some extent. However, this method requires user intervention and prone to variability especially in low signal-to-noise ratio environments. The proposed adaptive iteratively reweighted Penalized Least Squares (airPLS) algorithm doesn't require any user intervention and prior information, such as detected peaks. It iteratively changes weights of sum squares errors (SSE) between the fitted baseline and original signals, and the weights of SSE are obtained adaptively using between previously fitted baseline and original signals. This baseline estimator is general, fast and flexible in fitting baseline.

---

## Baseline Correction with Assymetrical Least Squares

Eilers, Paul HC, and Hans FM Boelens. "**Baseline correction with asymmetric least squares smoothing.**" Leiden University Medical Centre Report 1.1 (2005): 5. [[pdf]](./pdfs/443199618.pdf)

---

## Friedrichs Model-Free Median Window

Friedrichs, Mark S. "**A model-free algorithm for the removal of baseline artifacts.**" Journal of Biomolecular NMR 5.2 (1995): 147-153. [[pdf]](./pdfs/friedrichs1995.pdf)[[extension]](https://github.com/cran/baseline/blob/master/R/baseline.medianWindow.R)

---

## Modified Polynomial Fit

Lieber, Chad A., and Anita Mahadevan-Jansen. "**Automated method for subtraction of fluorescence from biological Raman spectra.**" Applied spectroscopy 57.11 (2003): 1363-1367. [[pdf]](./pdfs/lieber2003.pdf)

---

## Rolling Ball Non-Linear Digital Filter

Kneen, M. A., and H. J. Annegarn. "**Algorithm for fitting XRF, SEM and PIXE X-ray spectra backgrounds.**" Nuclear Instruments and Methods in Physics Research Section B: Beam Interactions with Materials and Atoms 109 (1996): 209-213. [[pdf]](./pdfs/kneen1996.pdf)

---

## Low-pass Frequency Filter

Atakan, Ahmet K., W. E. Blass, and D. E. Jennings. "**Elimination of baseline variations from a recorded spectrum by ultra-low frequency filtering.**" Applied Spectroscopy 34.3 (1980): 369-372. [[pdf]](./pdfs/atakan1980.pdf)

---

##

Stanford, Tyman E., Christopher J. Bagley, and Patty J. Solomon. "Informed baseline subtraction of proteomic mass spectrometry data aided by a novel sliding window algorithm." Proteome science 14.1 (2016): 19. [[pdf]](./pdfs/12953_2016_Article_107.pdf)

---

## Automated Segment Interpolation Based on Wavelet Feature Points (AWFPSI)

Qian, Fang, Yihui Wu, and Peng Hao. "**A fully automated algorithm of baseline correction based on wavelet feature points and segment interpolation.**" Optics & Laser Technology 96 (2017): 202-207. [[pdf]](./pdfs/qian2017.pdf)

## Selective iteratively reweighted quantile regression

Liu, Xinbo, et al. "**Selective iteratively reweighted quantile regression for baseline correction.**" Analytical and bioanalytical chemistry 406.7 (2014): 1985-1998. [[pdf]](./pdfs/liu2014.pdf)

## Remaining

1.  [R-cran](https://github.com/cran/baseline) - Iterative baseline correction algorithm based on mean suppression
2.  [R-cran](https://github.com/cran/baseline) - Iterative restricted least squares with iteration breaking
3.  [peak-utils](http://peakutils.readthedocs.io/en/latest/tutorial_a.html#estimating-and-removing-the-baseline)- Iteratively performs a polynomial fitting in the data to detect its baseline. At every iteration, the fitting weights on the regions with peaks are reduced to identify the baseline only.
4.  SCiLS Lab software (version 2016a, SCiLS, Bremen, Germany), followed by baseline correction using the convolution method with a width of 20
5.  TopHat algorithm used by OpenMS
6.  Baseline correction by improved iterative polynomial fitting with automatic threshold. Chemom Intell Lab Sys
7.  The iterative convolution algorithm, on the other hand, iteratively fits a polynomial function in such a way that, for each iteration, the values of all the data points that are above the polynomial are replaced with the value of the polynomial itself; the algorithm stops when the change between two consecutive iterations is smaller than a chosen threshold or when the set number of iterations is reached
8.  They were baseline corrected using a spline approximation of the baseline at the 10% quantile of ion intensities and employing window sizes of 500 and 50 and step sizes of 250 and 25 for the protein and lipid-focused spectra, respectively MATLAB
9.  [mzmine2](https://github.com/mzmine/mzmine2/tree/master/src/main/java/net/sf/mzmine/modules/rawdatamethods/filtering/baselinecorrection/correctors) - assymmetry corrector
10. [mzmine2](https://github.com/mzmine/mzmine2/tree/master/src/main/java/net/sf/mzmine/modules/rawdatamethods/filtering/baselinecorrection/correctors) - LocMinLoess Corrector
11. [mzmine2](https://github.com/mzmine/mzmine2/tree/master/src/main/java/net/sf/mzmine/modules/rawdatamethods/filtering/baselinecorrection/correctors) - Peakdetection Corrector
12. [mzmine2](https://github.com/mzmine/mzmine2/tree/master/src/main/java/net/sf/mzmine/modules/rawdatamethods/filtering/baselinecorrection/correctors) - Rolling ball corrector
13. [mzmine2](https://github.com/mzmine/mzmine2/tree/master/src/main/java/net/sf/mzmine/modules/rawdatamethods/filtering/baselinecorrection/correctors) - Rubber Band corrector

---

## Resources

- http://www.onemoonscientific.com/dcsaChunks/ch04s06.html
- http://nemo.cs.umass.edu:54321/baseline

## References

Schulze, Georg, et al. "**Investigation of selected baseline removal techniques as candidates for automated implementation.**" Applied spectroscopy 59.5 (2005): 545-574. [[pdf]](./pdfs/Appl_Spectrosc_2005_Schulze.pdf)

This paper is in a spectroscopy journal; but I think many of the concepts overlap.

Wang, Zhengfang, Mengliang Zhang, and Peter de B. Harrington. "**Comparison of three algorithms for the baseline correction of hyphenated data objects.**" Analytical chemistry 86.18 (2014): 9050-9057. [[pdf]](./pdfs/wang2014.pdf)

Yi, Lunzhao, et al. "**Chemometric methods in data processing of mass spectrometry-based metabolomics: a review.**" Analytica chimica acta 914 (2016): 17-34. [[pdf]](./pdfs/yi2016.pdf)

Schulze, H. Georg, et al. "**A small-window moving average-based fully automated baseline estimation method for Raman spectra.**" Applied Spectroscopy 66.7 (2012): 757-764.

Schulze, H. Georg, et al. "**A model-free, fully automated baseline-removal method for Raman spectra.**" Applied spectroscopy 65.1 (2011): 75-84. [[pdf]](./pdfs/schulze2011.pdf)

Schulze, H. Georg, et al. "**Fully automated high-performance signal-to-noise ratio enhancement based on an iterative three-point zero-order Savitzky–Golay filter.**" Applied spectroscopy 62.10 (2008): 1160-1166.

Prakash, Bhaskaran David, and Yap Chun Wei. "**A fully automated iterative moving averaging (AIMA) technique for baseline correction.**" Analyst 136.15 (2011): 3130-3135.

Gan, Feng, Guihua Ruan, and Jinyuan Mo. "**Baseline correction by improved iterative polynomial fitting with automatic threshold.**" Chemometrics and Intelligent Laboratory Systems 82.1-2 (2006): 59-65.

Schulze, Georg, et al. "**Investigation of selected baseline removal techniques as candidates for automated implementation.**" Applied spectroscopy 59.5 (2005): 545-574.

semiautomated

Li, Gang. "**Removing background of raman spectrum based on wavelet transform.**" Future Computer and Communication, 2009. FCC'09. International Conference on. IEEE, 2009. [[pdf]](./pdfs/li2009.pdf)

Zhang, Zhi-Min, Shan Chen, and Yi-Zeng Liang. "**Baseline correction using adaptive iteratively reweighted penalized least squares.**" Analyst 135.5 (2010): 1138-1146. [[pdf]](./pdfs/zhang2010.pdf)

# concepts

- least squares is fitting technique
- sliding window
- Chemometric methods for baseline correction can be
  subdivided into five categories: full-matrix methods, frequency
  filtering, manual estimation, derivative preprocessing, and
  polynomial fitting.

# Thoughts

1.  samples across a single run should be analyzed together right?

Samples across spectra, metadata, > mzML.

## Notes

- There seem to be a few categories (referencing qian2017)
  - polynomial fitting (A)
  - small window moving average (A)
  - adaptive iteratively reweighted penalized least squares (SA)
  - wavelet (SA)
  - automated vs semi-automated
- What are one way vs two way corrections?

categories:

- orthogonal basis (OB),
- fuzzy optimal associative memory (FOAM),
- polynomial fitting (PF) wang 2014

automated
