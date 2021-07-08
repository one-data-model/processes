# OneDM model adoption process

*Draft for 2021-07-07 meeting*

## Abstract
This document describes the process how data models for IoT devices
are adopted into One Data Model’s Adopted Models repository.

The intent of the repository is to create a place where good and widely re-usable data models can be found. The process has been created to ensure that the adopted models follow good design patterns and have wide applicability and usefulness across multiple ecosystems. A model passes through three main steps on its path to adoption: (1) it is translated into SDF and contributed to the OneDM Playground repository, where it can be found and discussed, (2) a model proponent promotes it to the OneDM Review Board for formal review and alignment to OneDM principles, and (3) by receiving Review Board approval and passing Community Last Call it gets added to One Data Model’s Adopted Models repository.

## 1. Definitions

- Roles:

	- Contributor: The individual or organization contributing the model to the Playground, typically has change control for the model.

	- Model proponent: The individual promoting the model to the Review Board, as well as being the point of contact for all changes that need to be made to the model based on reviews and/or last call

	- Review Board: The group responsible for reviewing incoming promoted models. Board membership based on representation of different ecosystems. The review Board may, under its own discretion, bring in support from external experts for certain review tasks, such as alignment with specific ecosystems that is not currently on the Review Board. The size of the Review Board depends on how many ecosystems are participating, but should be at least 4-5 individuals, including a chair and a secretary

	- Review Board Secretary: The Review Board individual who handles the paperwork for a particular model. Role is selected from Review Board members.
	
	- Review Board Chair: The Review Board individual, selected from Board members, who is task is to facilitate consensus within the group if needed. 

- Consensus: A proposal is approved if no sustained relevant objection has been made in timely fashion.

- Model: An information or data model expressed in SDF, typically for an IoT device

- Ecosystem: a loose collaboration of parties, centered around the use of a common data model and other mechanisms needed for interoperability (e.g., OCF, OMA SpecWorks)

## 2. Process

This picture illustrates the overall process of adopting models, which is further described below.

	              ┌─────────────┐           ┌─────────────┐             ┌──────────────┐
	              │             │           │             │             │              │
	              │             │           │             │             │              │
	─────────────►│ Playground  ├──────────►│Review Board │────────────►│Adopted models│
	              │             │           │             │             │              │
	Contribution  │             │ Promotion │             │ Community   │              │
	              └─────────────┘           └─────────────┘ Last Call   └──────────────┘

The following steps are used:

1.	**Playground**: The model is contributed to the Playground repository by a Contributor

	1.	Pre-requisites:

		1.	The model is in or translated into SDF

		2.	The model license is BSD-3 clause

	2.	Actions:

		1. 	The model is pushed to Playground repo

		2.	Model version is set to PLAYGROUND-VERSION

2.	**Review Board**: A Model proponent promotes the Playground model to the Review Board

	1.	Pre-requisites:

		1.	The model passes SDF validation

	2.	Actions:

		1.	The secretary initiates a process form (see appendix 1) for the model and puts it in the `under-review` folder

		2.	The Review board reviews the model according to review guidelines (see appendix 2) and the secretary updates the process form accordingly. There are two possible outcomes based on Review Board consensus at the end of the review period:

			1.	The model is sent to a two-week Community Last Call for final approval

			2.	The model and its form are sent back to proponent for update

		3.	If a Community Last Call is decided, the secretary handles the process with announcement, comment handling, and communication of outcome. Also, the secretary moves the process form from `under-review` to `in-last-call` folders. 

	3.	Possible outcomes:

		1.	The model is sent back to proponent for handling

		2.	A model that receives objections during Community Last Call goes back to the Review Board for decision on how to progress. This may include sending back to proponent for handling

		3.	The Community Last Call passes and there are no outstanding objections

3.	**Adoption**: The model is added to the Adopted models repository

	1.	Pre-requisites:

		1.	The model passes Community Last Call and has no outstanding objections

	2.	Actions:

		1.	Model namespace is set to ADOPTED-NAMESPACE

		2.	Model version is set to ADOPTED-VERSION

		3.	Secretary adds the model to Adopted Models repository

		4.	Model change control as assigned to Review board

		5.	Secretary archives the process form in the `adopted` folder

## A1. Appendix 1 OneDM Model adoption process form

A process form is created for each model that is promoted to the review board, and is intended to record the dicsussions and decisions during model review. 

A process form can be in one of four states, which correspond to the subdirectories of the [`adopted`](https://github.com/one-data-model/adoption) repo:

- `under-review` The model has been submitted and is under review by the review board.

- `in-last-call` The review board has completed its processing and is asking for community comments.

- `adopted` The model is adopted as a OneDM model; the process form is maintained to document the process leading to this state.

- `retired` The submission has been retired (possibly after submitting related models, which should be mentioned on the retired process form).

The process form: 

	# Basic info (filled in by contributor)

	Model: <url>
	Model-name: <human readable form>
	Proposed-name: <Proposed name in adopted repo>
	Description: <high level model description>
	Ecosystem: <origin ecosystem, if any>
	Model-responsible: <name of promotor >
	email: <of promotor>
	submit-date: <date>

	# Model metadata (filled in by contributor)

	namespace: <namespace>
	version: <commit-hash>

	# ----------------
	# Pre-review analysis (done by review board secretary)

	SDF-verification-passed: <true/false>
	OneDM-terminology-review-passed: <true/false>
	# Return-to-contributor if any of the above is checked


	# ----------------
	# Review board section

	Reviewers: list of (assigned) reviewers

	## Reviewer_1:     # One per reviewer

	date: date
	GitHub_issues: link to GH issues if filed
	opinion: No_objections, Objection
	comments: comment

	Review_board_decision: <back to contributor w comments/spin up \
		convergence activity/to community for last call>
	Review_board_date: <date>

	# ----------------
	# Last call

	LC_Start_date: <date>
	LC_End_date: <date + 2 weeks>
	LC_objections_raised: <list>
	LC_Comments: <need some way to feedback comments>

	# ----------------
	# Adoption decision

	Review_board_adoption_decision: <tbd>
	Review_board_adoption_decision_date: <date>

	# ----------------
	# Adoption

	Link_to_adopted_model_in_OneDM_repo: <url>
	Check_here_when_done: <X>

	# Secretary archives this file in adopted models repo to maintain bit trail

## A2. Appendix 2 Review board review guidelines

### A2.1. Review guidelines

1. Is the model in the same style as rest of the adopted models?

2. Does the model's described functionality overlap with existing adopted models

3.  Is the source of the model “trusted” to design the model (domain expertise)?

	1. Translated models from contributing organisations should be regarded as “designed by domain experts”.

4.  Is the model complete and can be used as is?

    1.  Preferable atomic the model should be considered

        1.  E.g. a the model should be designed as small as possible

    2. A set of the models that complements each other could be supplied

        1.  The separate sets then can be reused in other settings

        2.  This is a judgement call

5.  Are there improvements to be made to the model to make it have wider
    compatibility with other ecosystems?

    1.  No arbitrary limitations, e.g. no limits on a temperature
        sensor originating in home environment

6.  Usage of SenML specified units

7.  Uses the OneDM common properties

    1.  Make sure that the names are correct and have the same
        meaning

### A2.2. Review board principles

In addition to the review guidelines, there are a number of principles that should be followed  guide the process and the decisions of theReview board.

1.  Models should have clear scope

2. Models in the Adopted repository should be as simple as possible while remaining useful – too complex models are harder to re-use. The adopted repository itself should be as simple as possible as well.

3.  Models must be defined in SDF – the model may have originated from another format but the supplied *model* is already translated.

4. Model stability is important – developers must be able to trust that the models remain consistent and stable. Evolution and versioning must be handled gracefully.

5.  Consistent naming and structure of models and their components should be used.

6.  Adopted models should be neutralized from their contributing
    ecosystem legacy, this means they should follow

    a.  SDF design patterns

    b.  SDF naming conventions

    c.  using SDF terminology.

    d.  Using OneDM best practices

7.  Domain specific models should be defined by domain experts (if
    possible)

8.  Favor incompleteness over contention – It is OK to not be
    complete if it is to avoid contention

### A.3. (TBD) OneDM best practices

-   File name convention

-   sdfObject, Thing, etc naming convention

-   reuse of common sdfProperties

    -   This set of common sdfProperties will be gradually built up
        during the initial discussions
