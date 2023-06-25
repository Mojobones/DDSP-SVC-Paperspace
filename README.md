## 1. Introduction
This is a branch of [DDSP_SVC](https://github.com/yxlllc/DDSP-SVC) that adds a Makefile to more easily allow it to run on machines like Paperspace. Mainly this provides various conveniencies for running in that environment. 

## 2. Usage

1. Open a terminal and "git clone https://github.com/Mojobones/DDSP-SVC-Paperspace"
2. Run "make install" to install the python depencies. You will need to run this every time the Paperspace machine runs.
3. Run "make files" to download the required files. You will only need to run this one, as the files will persist across Paperspace runs.
4. Run "make folders name=<model_name>" to create the folder structure
5. Upload your audio files into the 'datasets/<model_name>/train/audio' directory, and upload your config files into the 'configs/<model_name>' directory
6. Run "make preprocess name=<model_name>" to pre-process the audio
7. Open a second terminal and run "make tensorboard" to run the Tensorboard
8. Run "make train-ddps name=<model_name>" to train the DDSP model
9. Run "make train-diffusion name=<model_name>" to train the Diffusion model

## 3. Acknowledgements
* [DDSP-SVC](https://github.com/yxlllc/DDSP-SVC)
* [ddsp](https://github.com/magenta/ddsp)
* [pc-ddsp](https://github.com/yxlllc/pc-ddsp)
* [soft-vc](https://github.com/bshall/soft-vc)
* [ContentVec](https://github.com/auspicious3000/contentvec)
* [DiffSinger (OpenVPI version)](https://github.com/openvpi/DiffSinger)
* [Diff-SVC](https://github.com/prophesier/diff-svc)

