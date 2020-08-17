# OneDM Convergence process

One part of OneDM’s mission is to attempt to establish a set of data
models that can be widely used across supported ecosystem. This document
describes the process for creating that set of data models.

(Working document, draft 04.)

# Definitions

*Model*: an IoT data model, defined in SDF.

*Incorporated model*: a model defined in SDF that has been agreed
(through the process described in this document) to be part of the
converged set. \[Adopted, OneDM model]

*Contributed model*: a model from one of the contributing ecosystems
that may be incorporated into the converged set.

*Converged set* (of models): the full set of incorporated models.

*Converged Set Team* (CST): The group within OneDM in charge of
creating and maintaining the converged set.  The CST is composed by
representatives of the contributing ecosystems and other relevant
experts.  Exact setup TBD.

*Ecosystem*: a loose collaboration of parties, centred around the use of
a common data model and other mechanisms needed for interoperability
(e.g., OCF, OMA SpecWorks)

\[Take names from GH repo progress (playground – contributed, accepted –
incorporated).]

\[Incorporate the process]

# Objectives

The objectives of the initiative to establish a converged set are:

1.  Foster interoperability across ecosystems by using common
    vocabularies and same source data models

2.  Allow for developers within an ecosystem to easily reuse best
    practice data models

# Principles

A set of principles behind the creation and construction of the
converged set are defined to guide the process and the decisions of the
CST.

1.  Models should have clear scope

2.  Models in the Converged set should be as simple as possible while remaining useful
    – too complex models are harder to re-use
    
    a.  and the converged set itself should be as simple as possible,
        as well

3.  Models must be defined in SDF – the model may have originated from
    another format but the supplied *model* is already translated.

4.  Model stability is important – developers must be able to trust that
    the models remain consistent and stable. Evolution and versioning
    must be handled gracefully.

5.  Consistent naming and structure of models and their components
    should be used.

6.  Incorporated models should be neutralized from their contributing
    ecosystem legacy – follow

    a.  SDF design patterns

    b.  SDF naming conventions

    c.  using SDF terminology.

    d.  Using OneDM best practices

7.  Domain specific models should be defined by domain experts (if
    possible)

8.  Favor lack of completeness over contention – It is OK to not be
    complete if it avoid contention

Start with models in playground, that have already passed validation and
other tools.

Should there be a principle for preferring more convertible models?

# OneDM best practices

Set of best practices that will be extracted during the 1^st^ phase of
the down selection process. The best practices are:

-   File name convention

-   sdfObject, Thing, etc naming convention

-   reuse of common sdfProperties

    -   This set of common sdfProperties will be gradually built up
        during the initial discussions

# Acceptance process for new Models

1.  A contributed model (CM) is offered for incorporation into the
    converged set. The CM should be expressed in SDF and should follow
    SDF design pattern in terminology and naming of affordances.

    a.  CM in the playground can be considered, being in the playground
        means:

        i.  The CM has valid SDF syntax.

        ii. The CM has been contributed under the BSD-3 license

    b.  If the CM is not in the playground, then a substantial reasoning
        should be supplied why this is the case.

2.  CST reviews CM. If issues are found, the contributing party is
    encouraged to address them and resubmit the CM

    a.  Is CM in the same style as rest of the converged set?

    b.  Does CM described functionality overlap with existing models in
        the converged set?

    c.  Is the source of CM “trusted” to design CM (domain expertise)?

        i.  Translated models from contributing organisations should be
            regarded “designed by domain experts”.

    d.  Is CM complete and can be used as is?

        i.  Preferable atomic CM should be considered

            1.  E.g. a CM should be designed as small as possible

        ii. A set of CMs that complements each other could be supplied

            1.  The separate sets then can be reused in other settings

            2.  This is a judgement call

    e.  Are there improvements to be made to CM to make it have wider
        compatibility with other ecosystems?

        i.  No arbitrary limitations, e.g. no limits on a temperature
            sensor originating in home environment

    f.  Usage of SenML specified units

    g.  Uses the OneDM common properties

        i.  Make sure that the names are correct and have the same
            meaning

3.  When CST finds that issues have been cleared, a Last Call round (two
    weeks) is called for to ask for input from the wider community

4.  If no blocking issues have been found, CM is added to the converged
    set as an incorporated model

# Change Process for *Incorporated model*s

Ensuring backwards compatibility:

-   changing the non-normative text in the object, action, property
    description.

-   adding or removing an optional feature (object, action, property).

-   adding a Resource enumeration value.

-   reusing a Resource enumeration value, which was marked as
    "reserved".

-   changing the non-normative text in a Object description.

-   Any other changes are forbidden (e.g. changing the name of an
    Object, changing the name of a Resource, or reusing a previously
    removed Resource ).

Breaking backward compatibility:

-   changing the "Instances" characteristic of the object, action,
    property.

-   changing the normative text in the object, action, property
    descriptions.

-   adding or removing a mandatory feature (object, action, property)..

-   modifying the list of allowed object/actions.

-   changing the "Instances" characteristic of a Resource.

-   changing the Data Type of a object, action property.

-   modifying the Range of a Resource value.

-   removing a Resource enumeration value.

-   changing the unit of a Resource.

-   changing the normative text in a Resource description.

Breaking changes will result in:

-   New version or a new model (e.g. different file name)

# TBDs

1.  It would be good to be able to associate versioning metadata with
    objects standardized way \[see also discussion document
    [versioning.md](versioning.md)]

2.  License and trademark handling:

    a.  Everything needs to be supplied under BSD-3, if not it should
        not be considered

3.  Atomic models are natural in the converged set, should composite
    models also be allowed?

    a.  Yes, but I do not think we should start out doing that, let’s
        have a set of atomic models first

4.  Evolution process – how to update or refine objects that have been
    incorporated into the converged set already

    a.  Added process with some guidelines above

5.  Name of CST – we used ORB I think in Kista, but I think it should be
    tied to the converged set (or whatever we call the converged set)

6.  FWIW, terminology in this doc is **not** set in stone, feel free to
    suggest better terms

7.  It would be nice if the different states led to different
    abbreviations (converged CM vs. contributed CM)
