Implementation of https://arxiv.org/abs/1904.00962 for large batch, large learning rate training.

Bonus: TensorboardX logging (example below).

## Installation
```
git@github.com:Wonderful-Me/pytorch-lamb.gitcd pytorch-lamb
pip install -e .
```

## 
``` shell
python test_lamb.py
tensorboard --logdir=runs
```
``` 
At `--lr=.02`, the Adam optimizer is unable to train.

Red: `python test_lamb.py --batch-size=512 --lr=.02 --wd=.01 --log-interval=30 --optimizer=adam`

Blue: `python test_lamb.py --batch-size=512 --lr=.02 --wd=.01 --log-interval=30 --optimizer=lamb`
```
![](images/loss.png)

![](images/histogram.png)
