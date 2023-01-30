
## Real-time Controllable Denoising for Image and Video

The official pytorch implementation of the paper **[Real-time Controllable Denoising for Image and Video]**


### Installation
This implementation based on [BasicSR] 

```python
python 3.9.5
pytorch 1.11.0
cuda 11.3
```

```
pip install -r requirements.txt
```
### Quick Start 
Data Preparation:
  1. Download Nam dataset (https://shnnam.github.io/research/ccnoise/)
  2. Crop the gt and input images into 512*512 patches and save as gt.lmdb and input.lmdb, respectively.
  3. Edit the dataroot_lq and dataroot_gt in NAFNet-RCD-tiny.yml as the corresponding path: /your_path/gt.lmdb and /your_path/input.lmdb

Test Nam real image noise dataset with NAFNet-RCD-tiny model, which is trained on SIDD training dataset

```
python basicsr/test.py --opt options/test/NAFNet-RCD-tiny.yml
```

