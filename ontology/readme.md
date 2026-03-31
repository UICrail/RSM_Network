# Purpose

The purpose of this work is to allow the description and representation of networks.

The representation is grounded in DUL (DOLCE+DnS Ultralite) and adds an intermediate ontology about "views and containers". This intermediate ontology can be used for any technical system such as rolling stock.

# Ontologies

## Parts and Views ontology (PAVO)

Purpose is to distinguish two fundamentally different ways of structuring a system:

* containment relations, grounded in mereology
* view relations, grounded in description

These two structuring principles must remain distinct, even when they happen to concern the same domain objects.

A container is an entity (asset) that may contain other entities (assets). The contained entities may themselves be containers, or they may be mereologically atomic at the granularity relevant to the model. Containers do not contain views. Containment is reserved for entities (assets) only.

A view is a _description object_. A view may have sub-views, and this relation is not necessarily one-to-one: the same view or subview may belong to several broader views. In that sense, views do not necessarily form disjoint trees globally, even if each published or serialized view structure may be organized as a tree.

The key relation on the view side is not containment but denotation. A view, or a sub-view, denotes one or more entities: either containers or individual assets. Denotation is the point at which the descriptive structure reaches the domain structure. It is intended to occur at the leaves of the view tree, and once such a denotation link is followed, it is not followed by further view-to-view traversal.

This distinction is important in order to avoid semantic circularities, and keeps things reasonably simple. In the network case, for example, a network statement is an information object that describes a network. It should not be modeled as part of the network (assets) itself, otherwise the network statement would describe itself. Self-reference should be handled with care, and here it is not necessary.

Containment and view structures also differ in their structural constraints. An entity or entity-container can belong to _only one container at a given time_. By contrast, a view may belong to several broader views at the same time. This asymmetry is essential: compositions are governed by a unique authoritative structure at any given time, whereas views depend on the perspectives from which a system is described.

In this sense, compositions and views are not merely two kinds of grouping. They correspond to two different ontological regimes:

compositions organize entities under a unique containment principle
views organize descriptions under one or more perspective-dependent arrangements
The decision to model a particular view as a tree is a design choice, not a general ontological truth. It is justified here for practical reasons, including easier serialization in JSON or XML and better usability for human users who are more comfortable with clean hierarchies than with general graphs. This choice should therefore be understood as a modeling profile adopted for publication, exchange, and navigation, rather than as a claim that all possible view structures are inherently tree-shaped.

## Networks ontology (NETW)

The network views (e.g. "TEN-T network", "High speed network"...) shall be set up to the viewers' content.

The "authoritative" containment relationships (e.g. to describe some national railway network) are expected to reflect the owners' asset breakdown. The NETW ontology does not prescribe how it should be done, e.g. by region first, then by subsystem, or in reverse order, or by any other convention(s). The only assumption is, there is one owner (or owning consortium) at a time, and views shall ultimately denote assets as leaves in the asset breakdown tree.