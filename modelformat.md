# Model format requirements for a transformer model
This is a description of an model as an abstruction, without specifying what technology is used to represent it or the architecture of the system that it is a part of. The model has to connect with the world in the ways shown in the diagram and for that it has to follow requirements below.

<img src=modelformat.jpg width="700">

REQUIREMENTS:
* Format support layers
* Format supports data provenance for each layer
* Format supports dependancies between layers
* Format is compatible (with or without conversion) with storage and both runtime environments
* Format supports independent quantisation of layers

