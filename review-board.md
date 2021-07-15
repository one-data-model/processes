# OneDM model adoption: review board

*Carsten Bormann, 2021-07-15 Draft for 2021-07-19 meeting*

One Data Model (OneDM) has an [adoption process](adoption.md) for
accepting common data models into OneDM’s *Adopted Models* repository.
This process relies on a review board as the gating function for
moving the process forward.

The present memo describes the review board, its principles of
operation, and the way it is set up.

## Review board

The review board makes the day-to-day decisions in the OneDM model
adoption process.
The decisions are made on a consensus basis as detailed below.
The review board does not vote, and its decisions are based on
technical considerations and their merit in moving the goals of the
OneDM liaison organization forward.

The review board is composed of individuals that act as experts, not
as representatives of companies or other organizations.
That said, the review board is intended to operate based on a good
overall coverage of knowledge about:

1. IoT data/interaction modelling and specifically the SDF data
   modeling language as standardized by IETF's ASDF WG; with a goal
   that the adopted models are a good fit for the overall objectives
   of OneDM.
2. Specific characteristics of the *ecosystems* that come together in
   the OneDM activity, in order to ensure not only a high quality of
   adopted models but also their usefulness in the ecosystem specific
   processes and applications.

The review board members should be chosen with the intention for them
to act in unison toward harmonizing the use of data/interaction models
in the greater IoT industry.  They should always feel empowered to *Do
the Right Thing*.

## Principles of operation

The review board meets regularly, each meeting being conditional on
whether models to be adopted have been submitted and/or general
business of the review board needs to be taken care of.

The review board elects a chair (running the meetings) and a secretary
(ensuring that input is prepared and decisions are recorded), which
may be the same or different individuals.

The review board runs a mailing list for which submission is enabled
both for the review board members and for active model submitters
(e.g., by simply giving them an account).

Eleven days before a decision meeting, the secretary makes the agenda of
that meeting known, which mainly consists of references to models in
one of the OneDM repositories, assisted by the process form as held in
the adoption repository.

The secretary solicits one of the review board members to act as the
*champion* for the agenda item (the champion can, but usually will
not, change during the process steps for one model); the champion
should not be a member that will need to recuse itself (see below).
If no champion can be found, this is a process failure.

The time between the agenda setting and the decision meeting can be
used for informal communication between board members and the
submitter, possibly facilitated by the champion and usually including
the rest of the review board.
This informal communication can lead to some short-notice revisions in
the model under review in order to resolve technical issues.

Revision numbers are used to minimize the confusion by this informal
process; it is considered more important to be able to exercise this
informal channel than to have perfect consistency at all times, but
the informal alignment process should not be abused for sweeping
changes.

Before a decision meeting, each individual in the review board reviews
the models under review, taking one of the following positions.  Minor
comments can be attached to each of these positions to raise some
potential for elective improvements; a Discuss position also comes
with an explanation of the problem.

1. Yes -- the board member has reviewed the model in detail and
   considers it a good addition to the repository of adopted models.
2. No objection -- the model has been reviewed at a potentially less
   detailed level and there is no problem.
3. Discuss -- the board member has a problem with the submission that
   needs to be resolved before the process can go forward.
4. Abstain -- the board member does not want a position to be
   recorded.
5. Recuse -- the board member is involved in the submission or has
   some other conflict of interest.

For a model to go forward, it needs at least two Yes positions and no
outstanding Discuss positions.

As a special case for resolving difficult Discuss cases (*rough
consensus*), a single Discuss position can be overruled in the next
meeting by the other review board members, if none of the other review
board members has expressed their support for the single Discuss position.

The review board can give the champion license to process Discuss
positions between meetings with the board member(s) that raised the
Discuss and the submitter; if the Discuss can be resolved by a change
and the champion has reason to assume no further discussion will be
needed, no further formal meeting is necessary to complete the
processing step.

## Review board constituency and evolution

The initial review board is set up by the OneDM liaison group members
based on the principles outlined above.
The review board can decide by consensus to co-opt additional
individuals.
Ultimate control over the membership resides with the OneDM liaison
group members, with a tendency to a hands-off approach.
