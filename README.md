# Chem 274A - Lab 1

In this lab, you will be using the molecular simulation code we wrote in Chem 280 - Foundations of Molecular Modelling and Software Engineering.

## Exercises

### Section 1 - Makefile (Spend 30 minutes max on this)
1. Use the `makefile` to create an environment for this lab.
    ```
    cd mcsim_python
    make environment
    ```
2. Activate the environment created by the `makefile`
    ```
    conda activate chem274A_lab1
    ```
3. Use the `makefile` to install `mcsim`
    ```
    make install
    ```

4. Review the Makefile in `mcsim_python`. Write a comment above each target explaining what the target does.

### Section 2 - Runnning Simulations
1. Use the notebook `run_mcsim.ipynb` to run Monte Carlo simulations. Follow the instructions in the notebook.

## My Answers

### Section 1:

As software development engineers, Makefile can help us in program writing, development, and demonstration. Instead of telling the customers what is the right environment, we can simply include it in the Makefile, and the customers can install the desired version of the environment and include the needed libraries by simply typing `make <environment>`. We can simply update the modules by typing `make dev-install` as well.

### Section 2:

1. The energy per particle is reduced significantly. From the initial to 10,000 steps, the change was large; the following 10,000-wise changes were not as large as the first 10,000 steps. 
2. Changed the parameters.
3. The energy per particle plot has just one point at 3.8, which is higher than the first point of the first trial, and smaller than 2. In the RDF, a portion of the particles is still at a very close distance, from 0 to 0.5 sigma. The distribution is not wave-like, but close to a straight line. But at 1 sigma distance, more particles are possibly found.
4. When the density is lower, the RDF is less wavy. The highest peaks were both happening at around 1 sigma. At lower density, the RDF would be more similar to the gas phase RDF. Where 0.9 density RDF is close to the liquid phase RDF.
5. At the higher temperature, the shape of the RDF curve is not changed a lot, but just be more flattened. At a higher temperature, the particles randomly move, so that the peaks are not as high as in the low-temperature case.
6. If we generate the particles in a cubic lattice, the energy per particle would be very low at the beginning. Without MC simulation moving, the RDF is a curve with discrete peaks. After the MC simulation moves, the graph of the RDF is the same as before. 
