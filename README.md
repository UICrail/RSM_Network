# Purpose

RSM Network ontology.

Defines railway infrastructure in a timed relation with topology and with infrastructure management.

The infrastructure management artefacts shall be moved to a specialized module later on.

The present ontology focuses on containment relationships and, in a distinct way, on infrastructure views called "subnetworks".

## Containers

There is no pre-defined containment taxonomy. The implementer are free to choose a railway network breakdown by susbystem, then by area, etc. or the other way round. Any legacy taxonomy can be imported "as is".

The container instances can be set up in such way to optimize the versioning, size, coherence, etc. of data. The present ontology therefore provides maximum freedom in this respect.

## Views

The views, or "subnetworks", do not entail any containment relationships. They can be used to define subnetworks:

* by intension, e.g. "High Speed Network", "Narrow gauge network"... (using a set of pre-defined technical properties), or
* by extension, e.g. "TEN-T Network" (using a pre-defined list of entries), or
* using a combination of other criteria.

The selection criteria can be mapped to external SKOS concept schemes (not provided).
