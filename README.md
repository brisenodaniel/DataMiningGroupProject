# Final Project #
**Authors:**

	**Lucas Jeay-Bizot**

	**Jeremy Wayland**

	**Daniel Briseno**

This Git Repo contains the code, paper and presentation for our CS 530 final project.

## Description of Directories: ##

- `Data/`
	- This directory should contain the data used in our analysis. The directory is currently empty due to the large size of the data files, but the needed data can be downloaded from [here](https://drive.google.com/drive/folders/1RLKVqrd7dmyu7oeTLaVNLNHCbL5rcHaN). The relevant files are the subject two data: [data_cube_s2.mat](https://drive.google.com/file/d/1ZTKHc1-FN9ApRAEsPEbOTWhgtJE0gKKr/view?usp=sharing), and the subject one data: [data_cube_s1_ica.mat](https://drive.google.com/file/d/1-NG2LTa2dOwXzO1qo8yCBcuSuQwGtppz/view?usp=sharing)
- `FinalPaper/`
	- This directory contains the pdf file for our final paper writeup.
- `FinalPresentation/`
	- This directory contains the pdf file for our final presentation.
- `Plots/`
	- This directory contains the plots generated by our code, and all plots used in the Final Paper and Final Presentation.
- `src/`
	- This directory contains .ipynb files and zipped binary files used to generate results. More specifically:
		- `HyperparameterTuningModelSelection.ipynb`: ipynb used to hyperparameter tune models and generate plots of model classification accuracy on the entire dataset (before taking sliding windows on sample time). 
		- **Jeremy fill in here**
		- `bin/`
			- This directory contains pickled dictionary objects resulting from running `HyperparameterTuningModelSelection.ipynb`. Due to large file sizes, all pickles are currently zipped.	

## Instructions on running code and re-generating plots ##

- Before running any scripts, experiment data must be downloaded to `./Data/`. Two data-matrices need to be downloaded, data from [subject 1](https://drive.google.com/file/d/1-NG2LTa2dOwXzO1qo8yCBcuSuQwGtppz/view?usp=sharing) and data from [subject 2](https://drive.google.com/file/d/1ZTKHc1-FN9ApRAEsPEbOTWhgtJE0gKKr/view?usp=sharing).
- To tune hyperparameters for all models and generate plots for model classification accuracy on entire dataset (before taking sliding windows), run all code blocks in [./src/HyperparameterTuningModelSelection.ipynb](./src/HyperparameterTuningModelSelection.ipynb).
	- After running this python notebook two files named `clfs_s1_NoFilt.p` and `clfs_s2_NoFilt.p` will be written to [./src/bin/](./src/bin). These files will contain a list of pickled objects corresponding to hyperparameter tuned and cross-validated models. For a full description of the contents of these pickled files, see [./src/HyperparameterTuningModelSelection.ipynb](./src/HyperparameterTuningModelSelection.ipynb). Additionally, after running this notebook all generated plots will be saved to [./Plots](./Plots).
	- **WARNING**: This notebook takes approximatley 24hrs to run on 7 cores.
- To generate plots on sliding windows **Jeremy fill in here**
	- Note, in order for this python notebook to run, the pickle files created by [./src/HyperparameterTuningModelSelection.ipynb](./src/HyperparameterTuningModelSelection.ipynb) must be present in [./src/bin/](./src/bin/). In order to run this file without waiting for the lengthy runtimes needed for Hyperparameter tuning, [S2_nofilt.tar.gz](./src/bin/S2_nofilt.tar.gz) and [S1_noFilt.tar.gz](./src/bin/S1_noFilt.tar.gz) located in [./src/bin](./src/bin).  
