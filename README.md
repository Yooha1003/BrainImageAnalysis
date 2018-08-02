# BrainImageAnalysis
Brain Extraction and MNI Normalization

#!/bin/bash

function HELP {
    cat <<HELP

------------------------------   BEaN.sh  --------------------------------------------
  (B)rain (E)xtraction (a)nd (N)ormalization script.


  Description:
    This script is using ANTs (http://stnava.github.io/ANTs/) and FSL commands.
    All input images will be normalized with MNI152_T1_1mm space.
    You can select a brain extraction step for saving computation time.
    But, this option could not guarantee a normalization result.
    (I highly suggest to turn this option on)

  Development History:
    Version 0.33:  detecting input extension with 'nii' (2018.8.1)
    Version 0.32:  make sub-directory for 'epi2ana.sh' processing (delay) (2018.8.1)
    Version 0.31:  reconstruction of the native extracted brain image (2018.7.31)
    Version 0.3 :  New brain extraction option was added (2018.7.31)
    Version 0.2 :  added a precise nomalization option (2018.7.30)
    Version 0.1 :  the script release of MNI normalization (2018.7.30)

--------------------------------------------------------------------------------------
  Example Usage:
  BEaN.sh -i input -s 0 -p 1

  (Optional)
  BEaN.sh -version (see the version)

  Compulsory arguments:
      -i:  input image (nifti file)
      -s:  skip brain extraction (1: skip / 0: brain extraction)
      -p:  intermediate file (1: remain / 0: remove)

--------------------------------------------------------------------------------------
  Requirement:
    1. ANTs pre-installation
    2. FSL pre-installation
    3. FreeSurfer pre-installation for converting nifti file to mgz file
--------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------
  This method was created by:

  Uksu, Choi (uschoi@nict.go.jp)
  Center for Information and Neural Networks
  National Institute of Information and Communications Technology
--------------------------------------------------------------------------------------
                      Script writing and modification by Uksu
                      Do not modify without a permission.
--------------------------------------------------------------------------------------
