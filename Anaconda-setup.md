# Anaconda (python) - setup

1. What are the prerequisites?
2. Which OS?
3. What are the steps?

## Windows OS - Steps

* Check if python is already installed. If yes, remove it and restart the system
* Download and install  Anaconda distribution <https://www.anaconda.com/products/distribution>
* Install only for the current user
* Install pywin32 <https://github.com/mhammond/pywin32/releases>
* Open `anaconda prompt`
* Check the conda configuration file - `cat .condarc`
* `conda config --set show_channel_urls true`
* `conda config --set report_errors false`
* `conda update conda`

