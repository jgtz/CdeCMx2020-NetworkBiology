# CdeCMx2020-NetworkBiology Challenge

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
  

# The Challenge
  
1. Use NetworkX to calculate network theory measures (degree, distance, betweeness centrality, and others you might find interesting) on each of the three PPI networks (COVID-Human, Human, Drug-Human). What is the distribution of these network measures? What are the nodes or node pairs with the highest value for these measures in each network?
2. Combine these three PPI networks. Do the same as in part 1 but for this combined network.
3. Apply the proximity-based methods "Pipeline P1" and/or "Pipeline P2" from Gysi et al. paper using these the combined PPI network. What are the top drugs you find?
4. Apply the network proximity measure from the Zhou et al. paper using the combined PPI network. What are the top drugs you find?
5. Visualize the results from each this parts.

# Notes and Hints

- Make sure that, when you import the networks, they are of the right type of network (we've only discussed undirected networks). The meaning of distance, centrality, etc. can have a different meaning depending on if the network is undirected, directed, a multigraph, etc.
- Certain network measures can take a long time to calculate in large networks (like the Human and Drug-Human PPI networks). In particular, distance and betweeness centrality can take some time. You can try calculating these measures for a subset of nodes or nodes pairs to get an idea of how long calculating all will take.
- To combine the three PPI networks, you need to know which proteins are shared between them. Make sure the combined network is getting the interactions for each protein from the three PPI networks. 
