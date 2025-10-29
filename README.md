# SpinSolve2TopSpin
NMR data converter from SpinSolve (Magritek) to TopSpin (Bruker)

Converts 2D data from SpinSolve Expert to TopSpin.
Tested for 1H-13C and 1H-1H spectra from 43 MHz and 80 MHz Magritek spectrometers and TopSpin 4.5.

To run, open SpinSolveExpert_to_Bruker.ipynb in the jupyter-lab:

```
jupyter-lab SpinSolveExpert_to_Bruker.ipynb
```

Then, set up the input and output paths and the quadrature mode in the second cell.

``` 
magritek_data_path='example/HSQC_MC/'
file_path_fid = magritek_data_path+'HSQC_FID.pt2'
destination_folder = 'example/1002'
quad=1 #1 for MC, 2 for States, 3 for Echo-Antiecho
```

After converting, run **xfb** and **sref** in TopSpin to obtain the spectrum with proper referencing.

Currently, apodzation is **NOT** transferred from the Magritek proc.par file.



