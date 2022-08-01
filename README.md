# Human-Video-Motion-Transfer
Lecture project for "Computer Vision and Deep Learning: Visual Synthesis"

## Pipeline of our method
* Process the source pictures
  * Put source video `mv.mp4` in `./data/source/` 
  * Then run `make_source.py`, the label images and coordinate of head will save in `./data/source/test_label_ori/` and `./data/source/pose_souce.npy`
* Process the target pictures
  * Rename your own target video as `mv.mp4` and put it in `./data/target/`.
  * Then run `make_target.py`, `pose.npy` will save in `./data/target/`, which contain the coordinate of faces.
* Train and use pose2vid network
  * Run `train_pose2vid.py` and check loss and full training process in `./checkpoints/`
  * Run `normalization.py` rescale the label images, you can use two sample images from `./data/target/train/train_label/` and `./data/source/test_label_ori/` to complete normalization between two skeleton size
  * Run `transfer.py` and get results in `./results`
* Gain results
  * Run `make_gif.py` to create a gif out  of the resulting images.
![](/result/output_zheyu.gif)

![](/result/output_jinhe.gif)
