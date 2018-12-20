# fastai

### PyTorch fastai - Practical Deep Learning
* Official website: https://www.fast.ai/
* Github: https://github.com/fastai/fastai

### Versions
For fastai courses, use fastai 0.7.0
* Google Colab set up: https://colab.research.google.com/drive/1pYYddH90hdOKPdhVeC69xoz8AszrpYbz
* Google Cobad setup 2: https://colab.research.google.com/github/corykendrick/fastai_in_colab/blob/master/Using_Google_Colab_for_Fastai.ipynb
* Windows 10 set up: https://forums.fast.ai/t/howto-installation-on-windows/10439
* Fix "Error: No module named 'bcolz'": https://forums.fast.ai/t/error-no-module-named-bcolz-but-bcolz-is-already-installed/9504/11
```
cd ~/fastai
source activate fastai (conda activate fastai)
conda install jupyter
conda env update
source deactivate (conda deactivate)
source activate fastai (condata activate fastai)
jupyter notebook
```
* Fix "Found GPU0 GeForce GTX 950M which is of cuda capability 5.0. PyTorch no longer supports this GPU because it is too old. warnings.warn(old_gpu_warn % (d, name, major, capability[1]))" error: https://forums.fast.ai/t/unable-install-pytorch-from-source-for-older-gpu-card/15436/14 (The key is to update PyTorch version to later than 0.4.0.)
```
conda activate fastai
conda uninstall pytorch
git clone --recursive https://github.com/pytorch/pytorch
cd pytorch
conda install -c pytorch pytorch
```

### Check Versions
Use the following code to check versions
```
import torch
print("PyTorch version: ", torch.__version__)
print("CUDA Version: ", torch.version.cuda)
print("cuDNN version is: ", torch.backends.cudnn.version())
print('Device:', torch.device('cuda:0'))
```
### Open Issues
* Colab setup https://gist.github.com/gilrosenthal/58e9b4f9d562d000d07d7cf0e5dbd840

<br><br><br>
### P.S.

* After seting up fastai for Windows 10, two "Jupyter Notebook" options can be found in the Start Menu.

<img width="400" src="https://github.com/Nov05/fastai/blob/master/images/001.jpg">

* To start the non-fastai environment, you can choose "Jupyter Notebook" in the Windows Start Menu, or simply type `jupyter notebook` in Anaconda. e.g. I got the following version information.

<img width="600" src="https://github.com/Nov05/fastai/blob/master/images/002.jpg">

* To start the fastai environment, you can choose "Jupyter Notebook (fastai)" in the Start Menu, or run the following code in Anaconda.
```
conda activate fastai
jupyter notebook
```

e.g. I got the following version information.

<img width="600" src="https://github.com/Nov05/fastai/blob/master/images/003.jpg">

* If you ran into error similar to "Found GPU0 GeForce GTX 950M which is of cuda capability 5.0.", update PyTorch version to later than 0.4.0 in the fastai environment with the method mentioned before.

<img width="600" src="https://github.com/Nov05/fastai/blob/master/images/004.jpg">

e.g. I got the following version information after updating.

<img width="600" src="https://github.com/Nov05/fastai/blob/master/images/005.jpg">

