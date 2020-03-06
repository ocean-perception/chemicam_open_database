# chemicam_open_database
Please cite the following paper if using the database:

Tomoko Takahashi, Soichi Yoshino, Yutaro Takaya, Tatuo Nozaki, Koichi Ohki, Toshihiko Ohki, Tetsuo Sakka, and Blair Thornton, 
Quantitative in situ mapping of elements in deep-sea hydrothermal vents using laser-induced breakdown spectroscopy and multivariate analysis, 
Deep Sea Research Part I: Oceanographic Research Papers (2020): 103232, in press:　https://doi.org/10.1016/j.dsr.2020.103232

This database contains in situ LIBS spectra of deep-sea rocks at 1000 m water depth obtained using ChemiCam, a 3000 m depth rated in situ deep-sea long-pulse LIBS analyser, developed in Institute of Industrial Science, the University of Tokyo, Japan. 
LIBS spectra of underwater targets taken using the same system in laboratory, system calibration data, and composition information of measured targets are also included in this database.

The detail information of the setup and conditions can be obtained from the paper. 

## calibrationDB

Wavelength calibration file showing corresponding wavelength of each pixel
ChemiCamF_wavelength_20151212.txt

Sensitivity calibration files showing intensity of each pixel with a standard calibration lamp
chemicamF_calib_250-570_150805.txt

## sampleDB

Each sample has its own separate text file “XXXXX.txt” where XXXXX should be replaced by the sample name

eg. 31XB23.txt

The file contains a list of elements (denoted as in the periodic table) followed by its corresponding abundance in %. The elements should be separated by “;” and the element and its concentration should be separated by a “,”. The order of the elements, or the number of elements contained in each file does not matter. There should be no spaces and no carriage return at the end of the file.

eg. Cu,89.57;Fe,0.06;Pb,0.046;Zn,9.97

but 

eg. Fe,0.06;Cu,89.57;Zn,9.97;Pb,0.046

is also fine.

If the sample is georeferenced the coordinates should be included as an additional field labelled Lat,Deg.deg;Lon,Deg.deg;Depth,m; where Lat is +ve N and Lon is +ve E


## spectraDB

The folder "Laboratory" contains spectra of underwater solids (metal alloys, sheets and pelletised powder samples of rocks and sediments) taken in laboratory. The metal samples were submerged in DI water and polletised powder samples were submerged in seawater. 
The folder "In-situ" contains in situ spectra taken at deep-sea, where are stored in folders with a name of a cruise number. 

The file format is csv, and each column indicate as follows:
| 1 | 2 | 3 | 4-10 | 11-1034 |  
|--------|--------|--------|--------|--------|
| Date; yyyymmdd | Time; hhmmss | Time (ms) | Intarnal condition | Spectral information |



