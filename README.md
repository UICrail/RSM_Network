# Purpose

RSM Network ontology.

Defines railway infrastructure in a timed relation with topology and with infrasrtructure management.

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

# Ontology-template

Template for ontologies. Structured in view of using shared **continuous integration** and **documentation** workflows.

Currently, the following workflows are pre-defined:

* continuous integration (CI) (.github/workflows/ci.yml): the usual formal checks, using ROBOT, reasoners...
* WIDOCO generation (.github/workflows/widoco.yml), triggered by successful CI
* Wiki extraction (.github/workflows/wiki-extract.yml), triggered by successful CI

The shared workflows are in GitHub repository Airy59/OntoQA.

Replace this file with a proper readme.md describing your project.

Replace the default EUPL 1.2 license (that applies to the present template) by the license suitable for your project.
