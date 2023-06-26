## Su2 setup for linux----needed when AD_support were used

---

1. download Ubuntu , then open through "WSL" or "Virtual box" 
<br/>
2. Install plugin what you need  :
  * sudo apt-get update  
 <br/>
  * sudo apt-get upgrade
<br/>
  * sudo apt-get install gcc 
<br/>
  * sudo apt-get install g++
<br/>
  * sudo apt-get install mpich
<br/>
  * sudo apt-get install pkg-config
<br/>
  * sudo apt-get install python3
<br/>
  * sudo apt-get install python3-numpy 
<br/>
 *  sudo apt-get install python3-scipy
<br/>
  * sudo apt install libopenmpi-dev
<br/>
  * sudo apt-get install python3-distutils (linux) 
<br/>
  * sudo apt-get install python-distutils-extra 
<br/>
3. download "SU2 code" through git (git clone ....) 
<br/>
4. meson build (options are choieable,check SU2 website, --prefix recommanded, enable AD support)
<br/>

5. set-up environment variable
<br/>
  * naro ~/.bashrc
 <br/>
  * copy content shown below to naro ~/.bashrc :
  ```
         export SU2_RUN=/mnt/c/USERS/User/Desktop/bin
         export SU2_HOME=/mnt/c/USERS/User/Desktop/bin
         export PATH=$PATH:$SU2_RUN
         export PYTHONPATH=$PYTHONPATH:$SU2_RUN
```
<br/>

6. sudo ninja install  ------- set environment parameter in windows(SU2_RUN, Path to Bin)
<br/><br/>
7. reboot PC  
<br/><br/>
8. sudo apt install build-essential  (optional) 

---

### Reference

https://www.cfd-online.com/Forums/hardware/179851-trouble-running-su2-parallel-cluster.html

