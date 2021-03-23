# Development Process

The application is developed using modified Feature model. Developers cannot commit to **master** branch.  All features are developed in feature branches. A feature can then be merged into master using Pull/merge request.

All branches must be named using the following conventions :
 - `feature/issue-{number}` : use for application new features 
 - `bugfix/issue-{number}` : use for fixing application bugs / issues 

 examples :
 - feature/issue-15469
 - bugfix/issue-15469

 Developers should follow the following steps :
  - Updated the `master` : `git pull origin master`
  - create feature branch : `git chekout -b feature/issue-15469`
  - Develop the specified requirements
  - commit and Push the code
  - Raise a Pull request when the code meets **[Checklist]((#pr-checklist))**
  - Ask one of the pears for the review
  - Address the required review comments
  - After the review squash-merge the PR

###  PR Checklist :
- code done as per the requirements. It should meet the acceptance criteria.
- unit tests done for all business components
- Integration test done the specified REST APIs
- Build is passing  

