# RotationNet

## Make virtualenv for Python 2.7 and install packages
```
virtualenv --python=/usr/bin/python2.7 --no-site-packages env
source env/bin/activate

pip install -r requirements.txt 
```

## Train network
```
python controller.py <dataset path>
```

## Test network
```
python controller.py <dataset path> -e -r <checkpoint file>
```

## Important hyperparameters
```
--pretrained          # Use pretrained model
--arch                # Architecture (f.ex resnet18, densenet121, alexnet)
--views               # Number of views (supports 2, 3, 12, 20)
--lr                  # Learning rate
-b                    # Batch size (must be divisible by number of views)
-r  <checkpoint path> # Resume from checkpoint
-e                    # Evaluatation mode, only use test set (use together with -r to test model)
```
