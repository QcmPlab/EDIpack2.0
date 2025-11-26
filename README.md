# `⚠rchived` 
> The development of EDIpack has moved [elsewhere](https://github.com/EDIpack), so this repository is now archived: it will not be updated (you cannot push, we will not sync with the new upstream) nor deleted, to preserve any possible links (git remotes in local clones, git submodules, etc.) to break.
-----


# EDIpack2.0: massively parallel exact diagonalization for generic quantum impurity problems

An extension of [EDIpack](https://arxiv.org/abs/2105.06806): a Lanczos-based method 
for the solution of generic quantum impurity problems, exploiting distributed memory MPI parallelization.
This updated version, aims to solve single-site, multi-orbital models, in either  *normal*, *superconducting* (s-wave) or *spin-non-conserving* (e.g. with spin-orbit coupling or in-plane magnetization) phases, including electron-phonons coupling. The code works at zero and low temperatures.   
 
See [j.cpc.2021.108261](https://doi.org/10.1016/j.cpc.2021.108261) for further information about the original massively parallel algorithm. See [SciPost Phys. Codebases 58](https://scipost.org/10.21468/SciPostPhysCodeb.58) for the newer updates, addressing the superconducting and non-SU(2) extensions.  


### Dependencies

The code is based on:  

* [SciFortran](https://github.com/QcmPlab/SciFortran)  

* MPI 

  


### Installation

Installation is available using CMake. In the current version API are only provided in Fortran. In a future release Python and C/C++ API will be included.  
The software gives acces to the static library `libedipack2.a` and the related modules `EDIPACK2`

Clone the repo:

`git clone https://github.com/QcmPlab/EDIpack2.0 EDIpack2`

And from the repository directory (`cd EDIpack2`) make a standard out-of-source CMake compilation:

`mkdir build`
`cd build`
`cmake ..`     
`make`     
`make install`   
`make post-install`    

Please follow the instructions on the screen to complete installation on your environment.  
The library can be loaded using one of the following, automatically generated, files :  

* pkg-config file in `~/.pkg-config.d/EDIpack2.pc`  
* environment module file `~/.modules.d/EDIpack2/<PLAT>`  
* homebrew `bash` script `<PREFIX>/bin/configvars.sh`


The `CMake` compilation can be controlled using the following additional variables, default values between `< >`:   

* `-DPREFIX=prefix directory <~/opt/EDIpack2/VERSION/PLAT/[GIT_BRANCH]>` 

* `-DUSE_MPI=<yes>/no`  

* `-DVERBOSE=yes/<no> `  

* `-DBUILD_TYPE=<RELEASE>/TESTING/DEBUG`  

--

***LICENSE***  
Copyright 2020- (C) Adriano Amaricci, Lorenzo Crippa, Alberto Scazzola, Gabriele Bellomia, Samuele Giuli, Giacomo Mazza, Francesco Petocchi, Luca de Medici and Massimo Capone

The software is provided with no license, as such it is protected by copyright.
The software is provided as it is and can be read and copied, in agreement with 
the Terms of Service of GITHUB. Use of the code is constrained to author agreement.   


This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.


