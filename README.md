## 1. Introduction
This is a branch of [DDSP_SVC](https://github.com/yxlllc/DDSP-SVC) that adds a Makefile to more easily allow it to run on machines like Paperspace. Mainly this provides various conveniencies for running in that environment. 

## 2. Usage

1. Open a terminal and "git clone https://github.com/Mojobones/DDSP-SVC-Paperspace"
2. Run "make install" to install the python depencies. You will need to run this every time the Paperspace machine runs
3. Run "make files" to download the required files. You will only need to run this one, as the files will persist across Paperspace runs
4. Run "make folders name=<model_name>" to create the folder structure
5. In the base-level directory, upload a .zip of all your audio files, and then run "make unzip-source zip=<zip_name> name=<model_name>"
   * **NOTE:** The zip should be the files themselves, not a folder containing the files
7. Run "make preprocess name=<model_name>" to pre-process the audio
8. Open a second terminal and run "make tensorboard" to run the Tensorboard
9. Run "make train-ddps name=<model_name>" to train the DDSP model
10. Run "make train-diffusion name=<model_name>" to train the Diffusion model

## 3. Acknowledgements
* [DDSP-SVC](https://github.com/yxlllc/DDSP-SVC)
* [ddsp](https://github.com/magenta/ddsp)
* [pc-ddsp](https://github.com/yxlllc/pc-ddsp)
* [soft-vc](https://github.com/bshall/soft-vc)
* [ContentVec](https://github.com/auspicious3000/contentvec)
* [DiffSinger (OpenVPI version)](https://github.com/openvpi/DiffSinger)
* [Diff-SVC](https://github.com/prophesier/diff-svc)

