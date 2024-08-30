DATA AND CODE AVAILABILITY RELATED TO:
"Some effects of limited wall-sensor availability on flow estimation with 3D-GANs"
by Antonio Cuéllar, Andrea Ianiro, and Stefano Discetti
published in Theoretical and Computational Fluid Dynamics

----------------------------------------------------------------------------------------------------------------

GitHub: https://github.com/erc-nextflow/3D-GAN-limited-sensors

-> FOLDER 'python codes' contains:
	-> codes for each case to train the network using tensorflow   ->   run_training*.py
	-> codes for each case to estimate the flow using a trained model   ->   run_predictions*.py
	-> codes to introduce noise in the estimation process over a trained model   ->   run_predicions*noise.py
	-> code 'matfileconverter.py' to conver the estimation output (.npy) into matlab files (.mat)
   Set the variable 'root_folder' in the last lines of the codes accordingly with the location of the folders 'models' and/or 'tfrecords'.
   In codes for estimation, select the architecture and the checkpoint according to the files in folder 'models'.

-> FOLDER 'channel coordinates' contains:
	-> files 'coordX.npy', 'coordY.npy' an 'coordZ.npy'. These files may be useful to reconstruct the geometry of the channel.

----------------------------------------------------------------------------------------------------------------

ZENODO REPOSITORY 3D-GAN-limited-sensors : https://doi.org/10.5281/zenodo.13587745

-> FOLDER 'models' with the trained models of the network, contain the weights of each layer.
	CASES TRAINED WITH ALL THREE WALL INPUTS
	-> CASE 64x64: case *E01-1
	-> CASE 32x32: case *E02-1
	-> CASE 16x16: case *E03-1
	-> CASE 8x8  : case *E04-1
	-> CASE 16x64: case *E05-1
	-> CASE 8x32 : case *E06-1

	CASES TRAINED WITH ONE WALL INPUT
	-> CASE 64x64: case *H-64-1 [p_w]
		       case *H-64-2 [tau_x]
		       case *H-64-3 [tau_z]
	-> CASE 32x32: case *H-32-1 [p_w]
		       case *H-32-2 [tau_x]
		       case *H-32-3 [tau_z]
	-> CASE 16x16: case *H-16-1 [p_w]
		       case *H-16-2 [tau_x]
		       case *H-16-3 [tau_z]
	-> CASE 8x8  : case *H-8-1  [p_w]
		       case *H-8-2  [tau_x]
		       case *H-8-3  [tau_z]

----------------------------------------------------------------------------------------------------------------

The data set used can be openly found in the repository of "Three-dimensional generative adversarial networks for turbulent flow estimation from wall measurements":
https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/threedimensional-generative-adversarial-networks-for-turbulent-flow-estimation-from-wall-measurements/6BD96A003A1D53325D8AC04341DC1713

ZENODO REPOSITORY 3D-GAN: https://doi.org/10.5281/zenodo.11090713

-> FOLDER 'tfrecords' contains: (THE CODES ARE PREPARED TO READ THE DATASETS IN THIS FORMAT)
	-> 'scaling.npz' file, needed for training and testing
	-> 'train' folder with training/validation dataset. 10 files are included in this repository due to storage restrictions. If more samples were needed, data can be shared upon request.
	-> 'test' folder with testing dataset. 4000 samples.



	