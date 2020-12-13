# fdh_austrian_cadaster_extraction
Repository for the deliverables of the Foundation of Digital Humanities project : Austrian Cadastral Map Extraction

The description of the project can be found on http://fdh.epfl.ch/index.php/Austrian_cadastral_map

## Description of contents
The cadaster_1848_train folder contains all necessary files for model training using DHSegment-torch. 

* config_classes.json, config_edges_2.json, config_edges_2_long.json, config_classes_nowater.json : the configuration files used during training of the models. nowater indicates the training done when putting street and water in the same class to see if it worked better. long indicates a higher patience.
* train_classes.csv, train_edges_2.csv, val_classes.csv, val_edges_2.csv, train_classes_nowater.csv and val_classes_nowater.csv contain the path to the training images and the corresponding masks. 
* classes.txt and classes_edges.txt contain the color values associated with the classes explicitaded in the config files.
* the folder Masks contains all the masks and corresponding images used for the different trainings.

The Probabilities_to_geometries-Austrian.ipynb is the notebook used for getting the probabilities map from the models and extract the corresponding geometries. It was adapted from the notebook used in the 1808 cadaster extraction pipeline.
