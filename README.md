# SIDA

### 1. Dataset Construction

The dataset needs to be divided into two folders for training and testing. The training and testing data should be in the format of the "data" folder.

### 2. Train

`code/train.py` is the implementation of our method on the Prostate, Fundus, and BUSI dataset.

Modify the paths in the code.

```python
if args.dataset == 'fundus':
    train_data_path='../../data/Fundus' # the folder of fundus dataset
elif args.dataset == 'prostate':
    train_data_path="../../data/ProstateSlice" # the folder of prostate dataset
```

then simply run:

```python
python sh_train.py --dataset ... --lb_domain ... --lb_num ... --save_name ... --gpu 0
```

### 3. Test

To run the evaluation code, please update the path of the dataset in `test.py`:

Modify the paths in lines 249 to 254 of the code.

then simply run:

```
python test.py --dataset ... --save_name ... --gpu 0
```

### 4. Acknowledgement

This project is based on the code from the [SSL4MIS](https://github.com/HiLab-git/SSL4MIS) and [UST-RUN](https://github.com/MQinghe/UST-RUN) project.

Thanks a lot for their great works.
