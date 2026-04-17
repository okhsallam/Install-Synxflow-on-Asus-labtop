⚙️ 3 Enable Conda in PowerShell
Run this once inside the Conda prompt

PowerShell
conda init powershell
Then

Close terminal

Open PowerShell

Activate Conda

PowerShell
conda activate base
🧪 4 Create Clean Environment
PowerShell
conda create -n pypims python=3.10 -y
conda activate pypims
Verify Python

PowerShell
python --version
📦 5 Upgrade pip
PowerShell
python -m pip install --upgrade pip
⚠️ 6 Install Compatible setuptools
SynxFlow depends on pkg_resources which is removed in newer versions

PowerShell
python -m pip install "setuptools<82"
Verify

PowerShell
python -c "import pkg_resources; print('pkg_resources OK')"
📥 7 Install SynxFlow
PowerShell
python -m pip install synxflow
✅ 8 Test Installation
PowerShell
python -c "from synxflow import flood; print('synxflow import OK')"
Expected output

synxflow import OK

A warning about pkg_resources being deprecated may appear this is normal

🎮 9 Check GPU and CUDA
PowerShell
nvidia-smi
You should see

GPU name

Driver version

CUDA version

💡 Useful Commands
PowerShell
clear
ls
conda env list
conda activate pypims
python --version
🧹 Remove Environment Optional
PowerShell
conda remove -n pypims --all
📌 Quick Summary
PowerShell
conda init powershell
conda activate base
conda create -n pypims python=3.10 -y
conda activate pypims
python -m pip install --upgrade pip
python -m pip install "setuptools<82"
python -m pip install synxflow
python -c "from synxflow import flood; print('synxflow import OK')"
nvidia-smi
🔥 Notes
Always activate your environment before using SynxFlow

Avoid upgrading setuptools above version 81 in this environment

For heavy simulations use Linux WSL HPC or cloud GPUs
"""

with open("README.md", "w", encoding="utf-8") as f:
f.write(readme_content)

Your README.md file is ready.

[file-tag: code-generated-file-0-1776387355873685726]
