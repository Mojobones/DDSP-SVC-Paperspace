## 1. Introduction
This is a branch of [DDSP_SVC](https://github.com/yxlllc/DDSP-SVC) that adds a Makefile to more easily allow it to run on machines like Paperspace. Mainly this provides various conveniencies for running in that environment. 

## 2. Usage

1. Open a terminal and "git clone https://github.com/Mojobones/DDSP-SVC-Paperspace"
2. Click on Makefile and change the value on line 4 for "MODEL_NAME" to be the name of your model (avoid spaces)
3. Run "make install" to install the Python depencies. You will need to run this every time the Paperspace machine runs
4. Run "make files" to download the required files. You will only need to run this once as the files will persist across Paperspace runs
    * This will also create the folder structure, but "make folders" can be run independently if need be
5. Upload your config files into 'configs/<model_name>'
6. In the base-level directory upload a .zip of all your audio files, and then run "make extract zip=\<zip\>" (ex. "make extract zip=source.zip") 
   * **NOTE:** The zip should be the files themselves, not a folder containing the files
7. Run "make process" to pre-process the audio
8. Open a second terminal and run "make tensorboard" to run the Tensorboard
9. Run "make train-ddps" to train the DDSP model
10. Run "make train-diffusion" to train the Diffusion model

## 3. Acknowledgements
* [DDSP-SVC](https://github.com/yxlllc/DDSP-SVC)
* [ddsp](https://github.com/magenta/ddsp)
* [pc-ddsp](https://github.com/yxlllc/pc-ddsp)
* [soft-vc](https://github.com/bshall/soft-vc)
* [ContentVec](https://github.com/auspicious3000/contentvec)
* [DiffSinger (OpenVPI version)](https://github.com/openvpi/DiffSinger)
* [Diff-SVC](https://github.com/prophesier/diff-svc)

