# CdeCMx2020-NetworkBiology

This repository contains the Jupyter notebooks, networks, and other files for the CdeCMx 2020 Network Biology Challenge.

Current content is:

- Jupyter notebook used in the "Network Biology and the Interactome" talk. Uses NetworkX (https://networkx.github.io/) to import a network, visualize it, and calculate some basic network measures.

- Some protein-protein interaction (PPI) networks that we can use to try to infer drug repurposing targets for COVID-19. In particular  
  * SARS-CoV-2 - Human PPI network. Gordon et al., Nature 2020. (https://www.nature.com/articles/s41586-020-2286-9).
  * Human PPI network. Luck et al., Nature 2020. (https://www.nature.com/articles/s41586-020-2188-x).
  * Drug - Human protein target network. DrugBank (https://www.drugbank.ca/).
Note: These networks were obtained from NDEx (http://ndexbio.org/). You need to register to copy these networks and export them in the GraphML format (which can be read by NetworkX and most network libraries and software.
  
- Can we do a similar approach (as in the papers below) to infer drug repurposing targets for COVID-19 based on the proximity of a drug's protein targets to the SARS-CoV-2 - Human protein interactions?
  * Zhou et al., Cell Discovery 2020 (https://www.nature.com/articles/s41421-020-0153-3).
  * Gysi et al., arXiv:2004.07229v1 (https://arxiv.org/abs/2004.07229).
  
