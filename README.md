# Monocular depth prediction using unsupervised deep learning
* Designed neural network suited for edge devices
* Chosen pyramidal bases network instead of deep layers to reduce model size
* Train deep learning model using stereo images with left-right image consistency but post-training, monocular images are used for inference.


# Training
* The model's dataloader expects a data folder path as well as a list of filenames (relative to the root data folder):

* python monodepth_main.py --mode train --model_name my_model --data_path ~/data/KITTI/ --filenames_file ~/filenames/kitti_train_files.txt --log_directory ~/tmp/

# Evaluation
* python utils/evaluate_kitti.py --split kitti --predicted_disp_path ~/my_model/disparities.npy --gt_path ~/data/KITTI/
