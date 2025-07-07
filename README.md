# Julia set-up

First Download Julia
https://julialang.org/downloads/

If you are using Mac convenient way to install julia is by using 

```bash
brew install julia
```

Once you install julia open it through the terminal by typing
```bash
julia
```
Then type the following commands to install Julia for Jupyter notebook.
```bash
julia
using Pkg
Pkg.update()
] add IJulia
```
The last line will open a package manager called JuliaREPL. Exit it via Ctrl+C, and in Julia terminal type:
```
using IJulia
IJulia.installkernel("Julia")
```
After this installation is complete you should be able to use Julia kernel in jupyter notebook! Just select Jupyter kernels -> Julia and you should be ready to go.

# SLMTools set-up


Our current solution to the problem of phase retrieval is open-source and can be found at:
https://github.com/hoganphysics/SLMTools

I will guide you through the installation process. Open your terminal and clone the repo:
```bash
cd OT
git clone https://github.com/hoganphysics/SLMTools
```
Next we need to install the package through Julia. In your terminal
```bash
julia
] add ./SLMTools
```
To verify the installation open the `playground.ipynb`, select the Julia kernel and execute the first cell. First import of the package could be a bit slow, but hopefully it works :)


# More packages

if there is a package that is missing -- julia will suggest how to install it. For example, if you don't have Plots installed, you can just run a cell with the following julia code
```Julia
import Pkg; Pkg.add("Plots")
```