# DVD-GAN
This repo is an implementation of [*Efficient Video Generation on Complex Datasets*](https://arxiv.org/abs/1907.06571)

Process UCF-101
- Step 1 (Done): Download dataset
- Step 2 (Done): Convert from avi to jpg files using:
python utils/video_jpg_ucf101_hmdb51.py avi_video_directory jpg_video_directory
- Step 3 (Done): Generate n_frames files using:
python utils/n_frames_ucf101_hmdb51.py jpg_video_directory
- Step 4 (Done): Generate annotation file in json format similar to ActivityNet using:
python utils/ucf101_json.py annotation_dir_path 
**Note: To change the number of class:
- Modify classInd.txt to contain the expected class(es). For example:
1 ApplyEyeMakeup
2 ApplyLipstick
3 Archery
- Run step 4 only
- The code in dataloader automatically skips the unsed videos.
