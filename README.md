# Installation
Clone this repo and create a conda environment using me508.yml.

# Reproducing our results
The unbiased data used to train the initial committor is found in the unbiased\_sims directory. The biased data generated while iteratively improving the committor is located in mlcolvar\_committor/biased\_sims. Each of the committor models (as well as the committor-derived collective variables) may be found under mlcolvar\_committor/models. 

To reproduce the training of the models, open mlcolvar\_committor/mlcolvar.ipynb and run each cell. To see the results of a particular iteration, change the iter variable in the fourth notebook cell. To train the next iteration of the model, update the filenames in the fifth notebook cell to include biased data at higher iterations (replace the biased data from previous runs; leave the unbiased data as it enforces the desired boundary), and run the cell. Then, run the sixth (final) notebook cell; this will afford the committor model at mlcolvar\_committor/models/model\_{iter}\_q.pt and the committor-derived collective variable at mlcolvar\_committor/models/model\_{iter}\_z.pt.
