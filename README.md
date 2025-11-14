# First Time Steps

1. Log into [Ondemand](https://ondemand.hpc.unibe.ch/) on Ubelix.
2. Create a new session with 
    1. GPU-Type - RTX 4090
    2. Time - 2 hours
    3. Instance - small or medium.
    4. Cuda - 12.8
    5. Mode - Jupyter Lab.
    6. Account : `teaching`
    7. wckey: Leave it blank
    8. Partition: `teaching (GPU)`
    9. Select the Advanced mode checkbox
        1. Reservation = `CAS_NLP_4`
    10. Select the email on start and give your email.
    11. Submit.
    12. Once the session has started, open it. 
3. On the terminal, fork the github repository with `git clone https://github.com/dsl-unibe-ch/CAS_NLP_M4.git`
4. Change into the directory with `cd CAS_NLP_M4`
5. Load Anaconda `module load Anaconda3`
6. Create a virtual environment with `python -m venv .venv`
7. Initialise conda `eval "$(conda shell.bash hook)"`
8. Add conda source
    1. `conda config --add channels conda-forge`
    2. `conda config --set channel_priority strict`
9. Create venv `conda create --name myenv`
10. Conda activate environment `conda activate myenv`
11. Install pip requirements with `pip install -r requirements.txt`
12. Create kernel `python -m ipykernel install --user --name conda_kernel`
13. Set the kernel to this new conda environment `conda_kernel` on the notebook. 

# Before each session
1. Perform the steps 1, 2, 4, 5, 10 from [First Time Steps](#first-time-steps).
2. Pull latest github repo updates with `git pull`. In case of conflicts, resolve them. 
4. Perform the steps 13 from [First Time Steps](#first-time-steps).


# Useful Links
1. [Ubelix HPC guide](https://hpc-unibe-ch.github.io/)