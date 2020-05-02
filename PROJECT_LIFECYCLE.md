# Project lifecycle

This document details how to handle a project lifecycle at MIC'S.  

## Requirements
Each project will include a Readme.md describing:
- The language's version.  
- How to install and set-up a development environment. This includes how to use any additional file you might have provided (Dockeriles, Vagrantfiles, etc...).  
- A file describing the requirements/dependencies of your code with specific versions and in which Operating system it works (if relevant).  
- How to run the test suite, how to build/compile and run the project.  

Issues templates will have to be prepared on each project to help users report bugs and issues.  
Contributors should be registered in the project with the appropriated rights by the repository's owner which should be the person in charge of the project. Admin rights should be also delegated to another contributor of trust (if possible).   

### Documentation
You should also pick how you want to write your documentation, the choice is yours as long as it is there and contains the following requirements:  
- The project's goal, why is it being developed.
- Architecture details, this could be under any form: schemas, paragraphs, videos...
- An index on your different chapters.  
- Any callable function or API route should be described with the required parameters and the returned value, including the format.  
- If the documentation is more like a user's guide, it should present how to do specific tasks with detailed step-by-step paragraphs.  

## Production
The ultimate goal of your project/code is to be set up in production and be used, so let's talk about that first. You should have a production branch in your repository, it must be the main branch (like master, but feel free to rename it however you want) and must be protected from any push directly to it. All changes to this branch must be done from Pull-Requests with one person reviewing the code and a different one merging it if possible.  
We also encourage you to set up CI/CD pipelines or at least CI on this branch, with the trigger on PR activated. You can use the integrated solution if you're hosting your code on platforms like Github or Gitlab, or use third-party systems like Travis, Jenkins or Bamboo.  

### About security
Absolutely NO credentials should be pushed in the repository, or be present in a file defining the CI/CD pipeline. Every sensitive file should be added into the __.gitignore__. If you do need to push them, they **must** be encrypted and the encryption key must be kept safe in a passwords/secrets manager and never be pushed in the repository, on any branch. If you do push one sensitive information by mistake, you must correct it ASAP and squash your commits so it doesn't appear in the history anymore.  
If you notice something that should not be there or any security issue, please contact the repository's administrators.  


## Releases
Each major feature should be marked with a release from the production/master branch. This will help to track the modifications inside the repository and be easier to rollback if needed. 
A release cycle could also be set-up at the beginning of the project which can include all the features and bug fixes developed during the meantime between two releases. Example: Every 3 month, a new release is created.  
Release v1.0 should be reached only when the software is mature and stable enough to be in production, more information can be found here: [https://semver.org/spec/v1.0.0.html](https://semver.org/spec/v1.0.0.html).  
Each release should come with a documentation update.


## Developing features
While having a development branch is nice, having a branch per feature is better. We encourage you to create your branches based on the production ones with your name inside the branch and the feature you're developing. Example: dev/john.smith/myawesome_feature.  
For details about commits and reviews, we believe in "Eat Your Own Food" so you should apply the same guidelines we apply to our open source project in [the CONTRIBUTING documentation](CONTRIBUTING.md).


## Issues
An issue template has to be created to make it easier to report bugs or issues.  
The template must include:  
- Write a description about the problem.  
- Specify the software's version.  
- Describe which aspect of it it impacts.  
- Explain how to reproduce the bug/issue.  
- You might attach a Pull Request to it if you would like to fix it yourself.  
