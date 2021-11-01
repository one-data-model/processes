# Adoption process (draft)

1. Promotor EITHER: 
	1. Create branch named BRANCH_NAME on main, add proposed model to the right folder
	2. Forks main to private repo, creates branch named `BRANCH_NAME` there and adds model to the right folder. Promotor may create an issue named `ISSUE_NAME` that links to the private repo for heads-up to community. 
2. Community is invited to discuss and comment on proposed models, Promoter may update 
2. Promotor creates PR named PR_NAME to pull in the branch signs CLA when PR is submitted
	1. Automatically added to Proposed for Review
	2. CI runs SDF linter
	3. Assignees should be Secretary and Promotor
3. The Secretary prepares Review Board meeting at least 11 days before meeting. This includes
	1. For each PR ready for review
		1.  Assigns three reviewers per PR
		2. Moves PR to Under Review
	2. Sending meeting agenda on mail to onedm@iotliaison.org
4. Review board members review PRs and provides comments in PR comments section
5. At the review board meeting the PRs are discussed according to the agenda. For each PR there are two possible outcomes:
	1. PR is ready for adoption
		1.	PR is moved to In Last Call
		2. Last Call is announced on mailing list onedm@iotliaison.org by the Secretary
	2. PR has objections and is not ready for adoption
		1. PR is moved to Proposed For Review
		2. Promotor is made aware of status change by the Secretary
6. For each Last Call that receives no objections, the Secretary
	1. PR is moved to Adopted
	2. CI merges the PR
 
 

    BRANCH_NAME = onedm-pa-MODELNAME

    PR_NAME 
	
	ISSUE_NAME

