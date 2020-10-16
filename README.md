## Weighted Tensor Completion for Time-Series Causal Inference
-
* Terminology
  * We have two kinds of worlds -- thin and fat. They respectively refer to the worlds narrow and wide in the paper.
  * For the experiment, the values of $N$ and $T$ are set as $N=500$ and $T=10$ for thin world, and $N=10$ and $T=500$ for fat world, but they can be adjusted in the code.
  * We have two kinds of policies -- I and II. They respectively refer to simple and complex policies in the paper.


* Description of the code
  * Folder [./GEN_DATA] contains the script to generate the datasets.
  * The main file is gendata.py. It takes as input three variables -- an iteration count (it), type of world, and type of policy. For example, suppose you want to generate 11-th example for world thin   2and policy II, then run the following command: python gendata.py --it=11 --world=thin --policy=II
  * This generates treatments A, outcomes Y, and covariates XX. In particular the script saves three files Aobs_thin_II_11.npy, Yobs_thin_II_11.npy, and XX_thin_II_11.npy in the folder ./GEN_DATA/data/  2thin/
  * Folder [./ESTIMATION] contains python files to run the tensor completion algorithms. In particular, this folder contains three main files.

