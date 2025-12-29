
### Required packages

```
sudo apt install -y python3 python3-opencv
```

### Runtime on raspberry pi zero w

| Script           | Real Time | User Time | Sys Time | Detections  |
| ---------------- | --------- | --------- | -------- | ----------- |
| run_v1_ssd.py    | 0m55.688s | 0m54.414s | 0m1.049s | Person, Dog |
| run_v1ppn_ssd.py | 0m54.121s | 0m52.541s | 0m0.766s | Person, Dog |
| run_v2_ssd.py    | 1m22.792s | 1m17.149s | 0m2.226s | Person, Dog |
| run_v3_ssd.py    | 0m41.905s | 0m39.208s | 0m1.159s | Person (x3) |

The v3 ssd failed to detect the dog.

### Try it

``` Bash
git clone https://github.com/Ab-Tx/ExploreOpencvDnn.git

cd ExploreOpencvDnn
```
- Download the weights and configs from [OpenCV](https://github.com/opencv/opencv/wiki/TensorFlow-Object-Detection-API).

``` 
time python3 run_v1_ssd.py; time python3 run_v1ppn_ssd.py; time python3 run_v2_ssd.py; time python3 run_v3_ssd.py 
```

### Sources

[OpenCV](https://github.com/opencv/opencv/wiki/TensorFlow-Object-Detection-API)

[Comet](https://www.comet.com/site/blog/real-time-object-detection-on-raspberry-pi-using-opencv-dnn/)
