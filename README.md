# Pattern Recognition in Spiking Neural Networks and Synaptic Delays
A standardized and containerized environment for building and analyzing Spiking Neural Network (SNN) models. This template uses Docker Compose to launch a NEST Simulator instance inside a Jupyter Notebook environment, providing a reproducible and consistent setup for research on neural network dynamics.

## Getting Started
To get the project up and running, you'll need Docker and Docker Compose installed on your system.

1. Clone the repository:

``` bash
git clone https://github.com/SaeedTaghavi/pattern-recognition-synaptic-delay
cd pattern-recognition-synaptic-delay
```
2. Start the Docker container:

``` bash
bash start-docker-container.sh
```
This command builds the Docker image (if not already built) and starts a container named nest-pattern-recognition-synaptic-delay in the background.

3. Access the Jupyter Notebook:
Open your web browser and navigate to `http://localhost:81`.

4. Log in:
Use the password or token configured in the `docker-compose.yml` file. By default, you can use the token: `easy`.

## Project Structure
```
.
├── notebooks/
│   └── (all jupyter notebooks go here)
├── references/
│   └── (contains all source materials, papers, books, etc.)
├── scripts/
│   └── helper.py
│   └── __init__.py
├── .gitignore
├── start-docker-container.sh
├── stop-docker-container.sh
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md
```
`notebooks/`: This directory is where you store your Jupyter notebooks for developing, running, and analyzing simulations.

`references/`: This directory contains all the source materials used for this project, including research papers, books, and BibTeX files for citations.

`scripts/`: This directory contains reusable Python modules, such as helper.py, which centralizes functions for your simulations. The __init__.py file turns this folder into a Python package, allowing you to import functions from it cleanly.

`.gitignore`: This file tells Git which files and directories to ignore, such as the __pycache__ directories created by Python and the checkpoint files created by Jupyter.

`start-docker-container.sh`: A shell script that automates the process of building your Docker image and running the container.

`stop-docker-container.sh`: A shell script that makes it easy to stop and remove the running Docker containers defined in docker-compose.yml. This provides a clean way to shut down your simulation environment.

`docker-compose.yml`: The main configuration file for Docker, defining the services, volumes, and ports for your project.

`Dockerfile`: A script that contains instructions for Docker to build a custom image on top of the NEST simulator image, including the installation of your project's dependencies from requirements.txt.

`requirements.txt`: A file listing all the Python libraries and their versions required for your project.

`README.md`: The main documentation file for your repository, providing instructions on how to set up and run the project.
