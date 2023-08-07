# LSCDF-VIAOD
Learning Semantic-aligned Cross-modal Discriminative Fusion Features for Aerial Object Detection

## Datasets
DroneVehicle: https://github.com/SunYM2020/UA-CMDet

## Environments
- Ubuntu 18.04
- CUDA 10.0
- NCCL 2+
- GCC 4.9+
- PyTorch 1.1
- Python 3.7
- torch-vision 0.3
- mmcv 0.4.3

## Getting Started
### Train
```shell
python tools/train.py configs/DroneVehicle/LSCDF.py
```
### Test
```shell
python tools/test.py configs/DroneVehicle/LSCDF.py work_dirs/LSCDF/latest.pth --out work_dirs/LSCDF/results.pkl
```
### Parse the results.pkl
```
python tools/parse_results.py --config configs/DroneVehicle/LSCDF.py --type OBB
```
### Evaluation
```
python eval/DroneVehicleEval.py LSCDF
```

