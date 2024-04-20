https://llama-cpp-python.readthedocs.io/en/latest/install/macos/
Installing llama-cpp-python with metal support


pip
CMAKE_ARGS="-DCMAKE_OSX_ARCHITECTURES=arm64 -DCMAKE_APPLE_SILICON_PROCESSOR=arm64 -DLLAMA_METAL=on"
pip install --upgrade --verbose --force-reinstall --no-cache-dir llama-cpp-python



conda

wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh
bash Miniforge3-MacOSX-arm64.sh

conda create -n llama python=3.9.6
conda activate llama

pip uninstall llama-cpp-python -y
CMAKE_ARGS="-DLLAMA_METAL=on" pip install -U llama-cpp-python --no-cache-dir
pip install 'llama-cpp-python[server]'

# you should now have llama-cpp-python v0.1.62 or higher installed
llama-cpp-python         0.1.68
