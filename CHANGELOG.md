# Changes

Most recent releases are shown at the top. Each release shows:

- **New**: New classes, methods, functions, etc
- **Changed**: Additional parameters, changes to inputs or outputs, etc
- **Fixed**: Bug fixes that don't change documented behaviour

## 0.2.0 (2019-08-12)

### New:
- Support for pretrained BERT Text Classification 

### Changed:
- For ```Learner.lr_find```, added optional ```max_epochs``` argument. 
- Changed ```Learner.confusion_matrix``` to ```Learner.validate``` and added optional ```val_data``` argument.

### Fixed:
- Further cleanup of  ```utils.is_iter``` function to use type check.





## 0.1.10 (2019-08-02)

### New:
- N/A

### Changed:
- For ```Learner.lr_find```, removed epochs and max_lr arguments and added lr_mult argument
  Default lr_mult is 1.01, but can be changed to control size of sample being used
  to estimate learning rate.
- Changed structure of examples folder

### Fixed:
- Resolved issue with ```utils.y_from_data``` not working correctly with DataFrameIterator objects.


## 0.1.9 (2019-08-01)

### New:
- N/A

### Changed:
- Use class check in utils.is_iter as temporary fix
- revert to epochs=5 for ```Learner.lr_find```

### Fixed:
- N/A

## 0.1.8 (2019-06-04)

### New:
- N/A

### Changed:
- N/A

### Fixed:
- ```Learner.set_weight_decay``` now works correctly


## 0.1.7 (2019-05-24)

### New:
- BIGRU text classifier: Bidirectional GRU using pretrained word embeddings

### Changed:
- Epochs are calculated automatically in ```LRFinder```

### Fixed:
- Number of epochs that ```Learner.lr_find``` runs can be explicitly set again


## 0.1.6 (2019-05-03)

### New:

### Changed:
- relocated calls to tensorflow 
- installation instructions and reformatted examples

### Fixed:



## 0.1.5 (2019-05-01)

### New:
- **cycle\_momentum** argument for both```autofit``` and ```fit_onecycle``` method that will cycle momentum between 0.95 and 0.85 as described in [this paper](https://arxiv.org/abs/1803.09820)
- ```Learner.plot``` method that will plot training-validation loss, LR schedule, or momentum schedule
- added ```set_weight_decay``` and ```get_weight_decay``` methods to get/set "global" weight decay in Keras

### Changed:
- ```vision.data.preview_data_aug``` now displays images in rows by default
- added multigpu flag to ```core.get_learner``` with comment that it is only supported by```vision.model.image_classifier```
- added ```he_normal``` initialization to FastText model

### Fixed:

- Bug in ```vision.data.images_from_fname``` that prevented relative paths for directory argument
- Bug in ```utils.y_from_data``` that returned incorrect information for array-based training/validation data
- Bug in ```core.autofit``` with callback failure when validation data is not set
- Bug in ```core.autofit``` and ```core.fit_onecycle``` with learning rate setting at end of cycle


## 0.1.4 (2019-04-10)

- Last release without CHANGELOG updates


