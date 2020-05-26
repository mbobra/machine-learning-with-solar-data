# machine-learning-with-solar-data
predicting solar eruptions using machine-learning methods

Of all the activity observed on the Sun, two of the most energetic events are flares and
Coronal Mass Ejections (CMEs). Coronal Mass Ejections (CMEs) are large blasts of energy that eject plasma from the Sun into interplanetary space; flares are more localized blasts that don't eject as much plasma into space. Usually, solar active regions that produce large flares will also produce a CME, but this is not always true.

We use machine-learning algorithms from [scikit-learn](http://scikit-learn.org/stable/) to [1] determine which features distinguish flares associated with CMEs from flares that are not, and [2] forecast whether an active region that produces a flare will also produce a CME. To do so, we use features derived from the photospheric vector magnetic field data taken by the Helioseismic and Magnetic Imager instrument aboard the Solar Dynamics Observatory, which takes the most data of any NASA satellite in history. We find that [1] we only need about 6 features to distinguish between the two populations, and [2] our True Skill Statistic, a forecast verification metric, is a relatively high value of approximately 0.8 plus or minus 0.2. To read more about the research, see [Bobra & Ilonidis (2016)](http://arxiv.org/abs/1603.03775).

### What is in this repository?

* The Jupyter notebook `cme_svm.ipynb` contains the original code we used to conduct this study. Since this study was published in 2016, the notebook uses now outdated packages running on Python 2.7. In the spirit of academic preservation and reproducibility, we have not touched this code since publication. To reinstate the exact environment used to conduct the original analysis, use the `environment.yml` file included in this repository. This notebook, additional data files, and the environment file are also permanently available in the [Stanford Digital Repository](https://purl.stanford.edu/wt605kh4712). 

* The Jupyter notebook `cme_svm_updated_for_pyastro.ipynb` contains updated code, using Python 3.7 and the most recent versions of the imported packages. 

### Citation

If you make use of any of this code or examples in a scientific publication, please consider citing our paper.

Here is the bibtex entry for the paper:

```
@ARTICLE{2016ApJ...821..127B,
   author = {{Bobra}, M.~G. and {Ilonidis}, S.},
    title = "{Predicting Coronal Mass Ejections Using Machine Learning Methods}",
  journal = {\apj},
archivePrefix = "arXiv",
   eprint = {1603.03775},
 primaryClass = "astro-ph.SR",
 keywords = {Sun: activity, Sun: flares},
     year = 2016,
    month = apr,
   volume = 821,
      eid = {127},
    pages = {127},
      doi = {10.3847/0004-637X/821/2/127},
   adsurl = {http://adsabs.harvard.edu/abs/2016ApJ...821..127B},
  adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```