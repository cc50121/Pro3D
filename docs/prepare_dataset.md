# DAIR-V2X-I 
Download DAIR-V2X-I dataset from official [website](https://thudair.baai.ac.cn/index).

## Symlink the dataset root to `./data/`.
```
ln -s [single-infrastructure-side root] ./data/dair-v2x
```

## Convert DAIR-V2X-I to KITTI format.
```
python scripts/data_converter/dair2kitti.py --source-root data/dair-v2x-i --target-root data/dair-v2x-i-kitti
```

The directory will be as follows.
```
Pro3D
├── data
│   ├── dair-v2x-i
│   │   ├── velodyne
│   │   ├── image
│   │   ├── calib
|   |   └── label
|   └── dair-v2x-i-kitti
|   |   ├── label_2
|   |   └── ImageSets
|   |        ├── trainval.txt
|   |        ├── train.txt
|   |        └── val.txt     
└── ...
```

## Prepare DAIR-V2X-I infos.
```
python scripts/gen_info_dair.py
python scripts/gen_info_dair_prompt.py
```
