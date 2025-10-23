# First Steps

1. Log into [Ondemand](https://ondemand.hpc.unibe.ch/) on Ubelix.
2. Create a new session with 
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
    10. On the terminal, fork the github repository with `git clone https://github.com/dsl-unibe-ch/CAS_NLP_M4.git`
4. Change into the directory with `cd CAS_NLP_M4`
5. Create a virtual environment with `python -m venv .venv`
6. Install the requirements wit `pip install -r requirements.txt`
7. Set the kernel to this new python environment on the notebook.