# Pro3D
![Framework and benchmarking-results of Pro3D](./assets/intro.png)

**Pro3D** is a new vision-based roadside monocular 3D object detector. Pro3D surpasses BEVSpread by a obvious margin of **6.4%**, **9.8** and **9.3%** in vehicle, cyclist, pedestrian classes respectively on **DAIR-V2X-I**.



<br>

<!-- TABLE OF CONTENTS -->
<details open="open" style='padding: 10px; border-radius:5px 30px 30px 5px; border-style: solid; border-width: 1px;'>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#Getting Started">Getting Started</a>
    </li>
    <li>
      <a href="#Acknowledgment">Acknowledgment</a>
    </li>
  </ol>
</details>

<br/>

# Getting Started

- [Installation](docs/install.md)
- [Prepare Dataset](docs/prepare_dataset.md)

Generate the scene priors
```
python scripts/gen_scene_prior.py
```

Train Pro3D
```
python [EXP_PATH] --gpus 8 -b 32
```
Eval Pro3D
```
python [EXP_PATH] --ckpt_path [CKPT_PATH] --gpus 1 -e
```

# Acknowledgment
This project is not possible without the following codebases.
* [BEVSpread](https://github.com/DaTongjie/BEVSpread)
* [BEVHeight](https://github.com/ADLab-AutoDrive/BEVHeight)
* [BEVDepth](https://github.com/Megvii-BaseDetection/BEVDepth)
* [DAIR-V2X](https://github.com/AIR-THU/DAIR-V2X)
* [Rope3D](https://github.com/liyingying0113/rope3d-dataset-tools)

