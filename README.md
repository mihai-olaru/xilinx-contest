# xilinx-contest
## Plan of record
 * Download a model 
 * Quantization of the model 
 * Compilation of the model
 * Update a defaul app to use this model

## Quantization

### Install ###

#### Running vai_q_pytorch ####
Install all the python modules needed. Some of the modules needs some extra installation tools to be installed.

This command line is creating the "pytorch_nndct" python module.

<code>cd ./pytorch_binding; python setup.py install </code>

The "pytorch_nndct" needs xir(Xilinx Intermediate Representation) module which is a graph representation of the AI algorithms from Vitis-AI-Runtime.

Install xir

Cmake command </br>
<code>./cmake.sh --build-python --user </code> </br>

Install steps
 * install boost library from https://www.boost.org/
 * install unilog which is another tool from Vitis-AI Runtime.
 * install protobuf (google project for data serialisation, similar with XML, https://github.com/protocolbuffers/protobuf)
 * if the protobuf shared library is not found. Run:</br>
 <code>sudo ldconfig</code>
 * install pybind11 using the following conda command. The pip install one doesn't include the cmake file needed.</br>
 <code>conda install pybind11 -c conda-forge</code>
 * segfault when importing setuptools.command.develop, import ctypes manually, not sure if this is the problem

