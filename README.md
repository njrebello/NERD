# Network Elasticity and Reaction Designer (NERD): A Multiscale Tool to Design Polymer Networks

# Description
Designing reaction schemes that yield a material with quantitative control over properties is one of the largest challenges in polymer science. The Network Elasticity and Reaction Designer (NERD) is an open-source software that enables the prediction and design of mechanical properties of polymer networks, one of the largest categories of materials widely used in engineering, biomedical, and commodity materials.  NERD takes as input from the user a series of BigSMILES or SMILES strings representing polymer and small molecule reactants, aided by a graphical editor for users unfamiliar with the grammar of line notations.  The reaction chemistry is predicted using publicly available small molecule reaction data supplemented with reactions handcrafted by the authors. The network-forming polymers are then coarse-grained using its database of coarse-grained scaling parameters, performing substructure search and similarity calculations tailored to polymers to get the required parameters. NERD then applies reaction simulators to generate the topology of the polymer network, providing all needed input to predict the desired mechanical properties.  While the initial version of NERD focuses on linear elastic modulus and fracture and is restricted to end-linked polymer networks, the computational structure of the platform can easily be expanded to support a broader array of property predictions and to update the accuracy of models as the underlying theory advances.

# Organization
Here are some folders and files that you will encounter in this repository:
- M1 folder contains code for the first module (network design)
- M23 folder contains code for the second and third modules (reaction detection and coarse-graining)
  - The file NERD-Database contains databases of SMARTS reactions and Kuhn segment lengths.
- M45 folder contains code for the fourth and fifth modules (kinetic Monte Carlo simulation and property prediction)

# How to Use
1. Click on the file Draw to launch the drawing tool for network precursors.
2. Draw small molecules and add {Z} for stochastic objects, draw the repeat units and end groups in separate panels, and enter precursor and network information for subsequent modules.
3. Click the button to generate the BigSMILES for each precursor.
4. Click the button Download Data to generate the file Info-Drawing, which includes the generated BigSMILES.
5. Run the file run-23, which inputs information from the file Info-Drawing, to run the reaction detection module.
6. This will generate a list of suggested reactions called Info-Rxn.
7. Choose the appropriate reaction from Info-Rxn.
8. Run the coarse-graining module.
9. This will generate the file Info-CG, which includes the predicted Kuhn parameters.
10. Run the file run-45, which inputs information from the file Info-CG, to run the kinetic Monte Carlo simulation and property prediction modules. Simulations should be run using a supercomputer.

# Creators
- Nathan J. Rebello (https://orcid.org/0000-0002-0178-7701)
- Tzyy-Shyang Lin (https://orcid.org/0000-0002-8265-6702)
- Bradley D. Olsen (https://orcid.org/0000-0002-7272-7140)

# Rights
The software is available under the MIT License (https://opensource.org/licenses/MIT).