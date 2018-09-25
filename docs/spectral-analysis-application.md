# The Application

So what I want to do is build an application that takes an algorithm, and evaluates it quantitatively against a test dataset. This application will automate this process, and allow us to rapidly test out new algorithms and find suitable implementation for them.

The logic behind this effort is to automate the way we evaluate algorithms. Most often I find algorithms that are used simply because they are the default algorithm used in a particular programming package. This makes users blind to Artifacts which may profoundly impact the analysis. Current application trusts users to possess training and knowledge to interrogate parameters and models, and this is dangerous.

This will form the basis of the data science core modules development, as well as the public database. These will require extensive thought and planning which will not be described here.

From a product standpoint, this is not very useful as the ROI is poor for exploring additional algorithms. Most novel algorithms are garbage, and the 'tried and tested'- albeit stupid- methods perform better than new ones. If 80% of usecases will only be using the latter, this platform would be dedicated towards the 20%. The argument can be made here that most analysis in biology is rather primative, and there remains quite the opportunity to explore. The caveat here is _not_ that all untested algorithms are equally valued, but certain techniques implement variables to probe additional dimensions in the model, that ultimately generates insight.

## Questions

1.  What will the general workflow look like?
2.  What exactly will we be evaluating?
3.  What will the testing look like?
4.  What does the labeled test dataset look like?
5.  What will be the big data workflow?
6.  How will we version everything?
7.  What about CI/CD considerations?

## Performance

- We want to use raw data that represent the proper categories (automation, object-number, etc.)
- We want to also simulate data.
- compare to other classifiers? ie PLS-DA, FuRES
- Latin bootstrap partition to evaluate classification accuracy
