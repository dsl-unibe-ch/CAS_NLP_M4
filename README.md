# First Time Steps

1. Log into [Ondemand](https://ondemand.hpc.unibe.ch/) on Ubelix.
2. Create a new session with 
    1. GPU-Type - RTX 4090
    2. Time - 2 hours
    3. Instance - small or medium.
    4. Cuda - 12.1
    5. Mode - VS Code or Jupyter Lab.
    6. Set `QOS` to `job_reservation`.
    6. Select the Advanced mode checkbox
        1. Reservation = CAS_NLP_4
    7. Select the email on start and give your email.
    8. Submit.
    9. Once the session has started, open it. 
    10. On the terminal, fork the github repository with `git clone https://github.com/dsl-unibe-ch/CAS_NLP_M4.git`
3. Change into the directory with `cd CAS_NLP_M4`
4. Load the python module with `module load Python/3.12.3-GCCcore-13.3.0`.
4. Create a virtual environment with `python -m venv .venv`
5. Activate the virtual environment with `source .venv/bin/activate`
6. Install the requirements wit `pip install -r requirements.txt`
7. Set the kernel to this new python environment on the notebook. If kernel is not found
    1. Go to home directory with `cd ..` 
    1. Upgrade ipykernel with `pip install --upgrade pip ipykernel` 
    1. Install a kernel with `CAS_NLP_M4/.venv/bin/python -m ipykernel install --user --name cas-nlp --display-name "Python(cas-nlp)"`
    2. Activate the jupyter lab with `jupyter lab --no-browser --port 8891` 
    3. Copy the path "http://localhost:8891/lab?token=YOUR_TOKEN" under the notebook "select kernel -> Existing Jupyter Server -> Path" and press enter. 

# Before each session
1. Create a new session with 
    1. GPU-Type - RTX 4090
    2. Time - 2 hours
    3. Instance - small or medium
    4. Cuda - 12.1
    5. Mode - VS Code or Jupyter Lab
    6. Select the Advanced mode checkbox
        1. Reservation = CAS_NLP_4
    7. Select the email on start and give your email.
    8. Submit.
    9. Once the session has started, open it. 
2. Change into the directory with `cd CAS_NLP_M4`
3. Pull latest github repo updates with `git pull`
4. Set the kernel to this new python environment on the notebook. If kernel is not found, repeat the steps mentioned in **First Time Steps**


## Conda steps
1. load anaconda `module load Anaconda3`
2. Initialise conda `eval "$(conda shell.bash hook)"`
3. Add conda source
    1. `conda config --add channels conda-forge`
    2. `conda config --set channel_priority strict`
3. Create venv `conda create --name myenv`
4. Conda create `conda activate myenv`
5. Install pip requirements with `pip install -r requirements.txt`
6. Create kernel `python -m ipykernel install --user --name conda_kernel`

CAS_NLP_M4/.venv/bin/python -m pip install -U ipykernel

# Useful Links
1. [Ubelix HPC guide](https://hpc-unibe-ch.github.io/)