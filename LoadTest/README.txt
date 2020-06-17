Calibrated Load Creator in Python 3
===========================================================================================================

This python script allows to generate a fixed CPU load(in %) for a finite or indefinite time period, on one or more CPU cores.

The script takes in the input the desired CPU load(in %) and the CPU core on which the load has to be generated.
The controller and the CPU monitor are implemented in two different threads.
-----------------------------------------------------------------------------------------------------------

Dependencies and required modules:

This script uses Python 3.6 and requires the following additional libraries:

- matplotlib
- psutil
- click

You can install them by giving the following commands in the cmd shell.
$ pip install matplotlib
$ pip install psutil
$ pip install click
-----------------------------------------------------------------------------------------------------------

Examples

1) Generate 80% of load on core 0 for 30 seconds: 

python .\CPULoadGenerator.py -l 0.80 -d 30 -c 0

2) Generate 55% load on cores 0, 1 and 3, until the program is interrupted through Ctrl-C:

python .\CPULoadGenerator.py -l 0.55 -c 0 -c 1 -c 3

3) Generate 35% load on core 0, 70% on core 3, until the program is interrupted through Ctrl-C: 

python .\CPULoadGenerator.py -c 0 -c 3 -l 0.35 -l 0.70

4) Generate 52% load on cores 0 and 1, for 20 seconds, and then plot the load for each of the cores:

python .\CPULoadGenerator.py -l 0.52 -c 0 -c 1 -d 20 --plot

(To plot the graph give the parameter '--plot')

-----------------------------------------------------------------------------------------------------------
THANK YOU!
-----------------------------------------------------------------------------------------------------------