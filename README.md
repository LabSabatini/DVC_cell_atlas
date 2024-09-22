## A unified rodent atlas reveals the cellular complexity and evolutionary divergence of the dorsal vagal complex
#### Cecilia Hes, Abigail J. Tomlinson, Lieke Michielsen, Hunter J. Murdoch, Fatemeh Soltani, Maia Kokoeva, Paul V. Sabatini

This repository has the code used for constructing the murine and rodent dorsal vagal complex (DVC) cell hierarchies in our publication and for predicting cell identity labels using treeArches.

The versions of the relevant libraries and dependencies we used are:
- pip==23.3.1
- pandas==1.5.0
- scvi-tools==0.17.1
- torch==2.0.1
- torch_geometric==2.4.0
- scanpy==1.9.8
- numpy==1.24.4
- matplotlib==3.8.2
- seaborn==0.13.2
- leidenalg==0.10.2
- scarches==0.5.3
- scipy==1.8.1
- scHPL==v1.0.5

Notebook: datasets_DVC_preparation.ipynb \
It has code to find and add genes in the original 2,500 most variable genes which are NOT present in a new given dataset. If any, we generated a function to add these with values 0 to the dataset.
This makes possible to subset the same 2,500 (even with 0 counts for the added genes) on each new dataset to match the original 2,500 most variable genes from our murine dataset, which was used to initially construct the cell hierarchy.
We have used these functions with each new DVC dataset/database to either expand the initial hierarchy or to predict cell labels (See **Materials and methods** in our publication).

Notebooks: 01_treearches_murine_hierarchy_2500.ipynb \
           02_treearches_prediction_HesLudwig_2500.ipynb \
           03_treearches_prediction_Dowsett_2500.ipynb \
           04_treearches_mouse_rat_hierarchy_2500.ipynb \
They have code for reproducibility of our murine and rodent (mouse and rat) hierarchies and for the conducted verification in mouse data using the predict_labels function from scHPL.

The bioRxiv publication can be found here: https://doi.org/10.1101/2024.09.19.613879

Sabatini Lab/ McGill University, 2024
