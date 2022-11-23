





## run


```
conda create --name=LGN python=3.6
conda activate LGN
pip install -r requirements.txt
cd code
```

The dataset should consist of train/test.txt, in which each row represents a user.

### Gowalla


```
CUDA_VISIBLE_DEVICES=3 python main.py --decay=1e-4 --lr=0.001 --layer=3 --seed=2020 --dataset="gowalla" --topks="[20]" --recdim=64
```

### Yelp18


```
CUDA_VISIBLE_DEVICES=3 python main.py --decay=1e-4 --lr=0.001 --layer=3 --seed=2020 --dataset="yelp2018" --topks="[20]" --recdim=64
```

### Amazon-book


```
CUDA_VISIBLE_DEVICES=3 python main.py --decay=1e-4 --lr=0.001 --layer=3 --seed=2020 --dataset="yelp2018" --topks="[20]" --recdim=64 --bpr_batch=8192
```


## remove

```
conda activate base
conda remove -n LGN --all
```