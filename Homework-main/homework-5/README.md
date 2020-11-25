# Homework-5

Homework 5 is due by 11:59 pm on Tuesday, 24 November, 2020.  It has two components to be submitted (both via GitHub pull requests):

1. A short coding example where you calculate species mass fluxes between two locations for several given state vectors.

2. Project: Derive and implement conservation of charge to model charge transfer for at least one electrode/electrolyte interface in your system (if you want to do both, that is certainly fine with me :) )

## 1. Transport Modeling
Your task here is to write a sofware functions that calculate the mass and/or molar flux between two nodes for the following conditions:
- Ideal gas flowing through a porous cathode.
- Ions flowing in an incompressible liquid electrolyte flowing through a porous polymer separator.
- Ions moving in a triple conducting oxide through a composite anode.

In all cases, you will be provided the necessary transport parameters (diffusion coefficients, mobilities, or somesuch), as well as microstructuure and geometry parameters.  You will then write a function to calculate flux as a function of species concentrations/mole fractions, electric potential, and distance beteen the two nodes.

Subsequent code cells in the notebook will then call your functions for a range of conditions, comparing your output to validation data to judge for accuracy.


## 2. Project Progress: Conservation of Charge and Charge Transfer

At a minimum, you must submit a pull request to your project repo that includes (i) a Jupyter notebook showing the derivation of your conservation of charge equation(s), and a model file (edit and rename the `_model.py` template) that implements this into a model code that I can run.

You (or your partner, if applicable), should fork a copy of the repo I have created for your project.  It probably makes sense to just fork this to one teammate's repo, and then have both team members push to this repo.  Or, create a GitHub team for your project, and fork a copy to this repo.

Details:
- Describe the model domain and state variables, then derive the conservation equations in a Jupyter notebook.  Implement the conservation equations to calculate a steady-state voltage difference, for a fixed external current (i_ext), and assuming that all species concentrations and all other state variables remain fixed.  
- Take your implementation from the Jupyter notebook and implement it as a python module that can be run independently.
- See my `Code-Examples` repo for [Battery SPM](https://github.com/Echem-Systems-Engineering-Fall2020/Code-Examples/tree/main/BatterySPM) and [PEMFC](https://github.com/Echem-Systems-Engineering-Fall2020/Code-Examples/tree/main/pemfc) examples, to get you started. You will eventually need to justify any parameter values (ideally via literature citations), but for now you are fine to stick with "this number worked" as your justification.  Note that while "steady state" may not be the eventual goal for your project, it is still okay to start here.
- Note that I have a particular way that I like to modularize my models (main `_model.py` file, with separate `_init.py`, `_function.py` files, etc.).  While there are obviously reasons I like this approach, you are by no means bound by it.  The only requirement is that the main file that is run ends with `_model.py`.  If you want to cram every line of code into this file, and think you can do so in a sensible way that your instructor can understand, then by all means, be my guest :).
- Both the Jupyter file and your python implementation will be submitted as a pull request to your project repo on the Echem [Projects page](https://github.com/Echem-Systems-Engineering-Fall2020/Projects).

