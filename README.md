## Installation

Set up and acitvate **Conda Environment** with package requirements:

```shell
conda create --name 2D-ABM --file requirements.txt python=3.10.12
conda activate 2D-ABM
```

Install **Jupyter Notebook** and add the environment as Jupyter kernel:

```shell
conda install jupyter
conda install -c anaconda ipykernel
python -m ipykernel install --user --name=2D-ABM
```

Set up and activate **Environment** in PyCharm:

```shell
python3 -m venv 2D-ABM
```

If venv not active:

```shell
source 2D-ABM/bin/activate
```

Install package requirements and Jupyter kernel:

```shell
pip install -r requirements.txt
pip install jupyter
pip install ipykernel
python -m ipykernel install --user --name=2D-ABM
```

## Describe

The simulator itself is located in the AgentBasedModel module. It contains the simulator objects
that need to be imported and run in a Python script to create the simulation. In the same repository
for the example script main.py is written, it runs a simple simulation with 3 stock exchanges that
trade a single asset, 60 traders and 3 market makers. Unfortunately, I have not been able to
implement the installation of the simulator in pip, so you will have to work in the same folder
where AgentBasedModel is installed via jupiter notebooks or scripts - as it is more convenient.

README contains instructions on how to create an environment in cond and install the necessary
version of python and dependencies for the simulator, as well as creating a kernel in Jupiter. The
commands in it can be simply executed one by one in anaconda prompt (windows) or command line (if
you work on linux/mac). If you don't have Anaconda3 is not installed (as I understand it also
happens), you can create an environment in any suitable way using the specified version of python.
using the specified version of python and dependencies from requirements.txt.

To start comfortably, I advise you to first familiarize yourself with the main.py script, what
objects are initialized there, how to run it, and how to use it. objects are initialized there, how
the simulation itself is started, try to run the script. Unfortunately there are no detailed
instructions on the simulator's features, so I advise you to run through the files of the simulator
to see what there are in it. simulator to see what objects there are and how they are initialized.
The main ones are:

`AgentBasedModel/traders.py` - all traders and their parameters

`AgentBasedModel/simulator.py` - Simulator object and its initialization

`AgentBasedModel/exchange.py` - Exchange objects, assets and their initialization

`AgentBasedModel/extra/events.py` - what events can be triggered on the stock exchange during
trading

`AgentBasedModel/visualization/` - built-in visualization tools
