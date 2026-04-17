Install Miniconda on Windows

Download from https://docs.conda.io/en/latest/miniconda.html

Run installer

Select “Just Me”

Keep default settings

Open Miniconda Prompt or Anaconda Prompt

Run conda --version to verify installation

Enable Conda in PowerShell

Run conda init powershell

Close terminal

Open PowerShell

Run conda activate base

Create a clean environment

Run conda create -n pypims python=3.10 -y

Run conda activate pypims

Verify Python

Run python --version

Upgrade pip

Run python -m pip install --upgrade pip

Install compatible setuptools

Run python -m pip install "setuptools<82"

Verify pkg_resources works

Run python -c "import pkg_resources; print('OK')"

Install SynxFlow

Run python -m pip install synxflow

Test installation

Run python -c "from synxflow import flood; print('synxflow OK')"

Check GPU and CUDA

Run nvidia-smi

Daily usage

Run conda activate pypims before using SynxFlow

Optional cleanup

Run conda remove -n pypims --all
