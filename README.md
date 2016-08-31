### SLiM description ###

SLiM is an evolutionary simulation framework that combines a powerful engine for population genetic simulations with the capability of modeling arbitrarily complex evolutionary scenarios. Simulations are configured via the integrated Eidos scripting language that allows interactive control over practically every aspect of the simulated evolutionary scenarios. The underlying individual-based simulation engine is highly optimized to enable modeling of entire chromosomes in large populations

### Import the dockerfile ###

git clone https://github.com/cmonjeau/docker-slim.git

### Build the dockerfile ###

docker build -t cmonjeau/slim .

### Print SLiM programs help ###

docker run -it --rm cmonjeau/slim slim script.txt

### Run SLiM using Godocker (http://www.genouest.org/godocker/)

Create a new job with these parameters:

"Container image" : cmonjeau/slim

"Command" :

```

#!/bin/bash

# command line examples (adapt with your data)

slim $GODOCKER_HOME/data/script.txt


```

"Mount volumes" : home(rw)
