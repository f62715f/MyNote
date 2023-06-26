## Su2 setup for linux----needed when AD_support were used

---

1. download Ubuntu , then open through "WSL" or "Virtual box" 
<br/>
2. Install plugin what you need  :
 
  * sudo apt-get update  
  
  * sudo apt-get upgrade

  * sudo apt-get install gcc 

  * sudo apt-get install g++

  * sudo apt-get install mpich

  * sudo apt-get install pkg-config

  sudo apt-get install python3

  sudo apt-get install python3-numpy 

  sudo apt-get install python3-scipy

  sudo apt install libopenmpi-dev

  sudo apt-get install python3-distutils (linux) 
  
  sudo apt-get install python-distutils-extra 


3. download "SU2 code" through git (git clone ....) 


4. meson build (options are choieable,check SU2 website, --prefix recommanded, enable AD support)


5. set-up environment variable

  Step1.naro ~/.bashrc
 
  Step2.copy content shown below to naro ~/.bashrc

 	 export SU2_RUN=/mnt/c/USERS/User/Desktop/bin
         export SU2_HOME=/mnt/c/USERS/User/Desktop/bin
         export PATH=$PATH:$SU2_RUN
         export PYTHONPATH=$PYTHONPATH:$SU2_RUN



6. sudo ninja install  ------- set environment parameter in windows(SU2_RUN, Path to Bin)


7. reboot PC


8. sudo apt install build-essential  (optional)  

===================================================================================================

Reference

https://www.cfd-online.com/Forums/hardware/179851-trouble-running-su2-parallel-cluster.html

