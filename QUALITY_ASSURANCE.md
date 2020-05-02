# Quality assurance

This document presents how, at MIC, we intend to ensure the quality of what we are producing.

## Software

### Pull Requests
For a feature to be included in an internal project (in a main branch), it has to check the following list:  
    - Changes need to be presented in a Pull Request.  
    - The PR has to be validated from the automated CI if there is one, this includes the validation of every unit tests. Which implies that all the changes are including tests. If the pipeline fails, PR will be refused.  
    - It must follow the guidelines described in our [DEVELOPER_GUIDE](DEVELOPER_GUIDE.md).  
    - Commits need to follow the guidelines described in [CONTRIBUTING](CONTRIBUTING.md).  
    - It must include a small description of the features developed, where the changes are made and *why*.  
    - Pull Requests have to be reviewed and merged by two distinct contributors if possible.

Once the pull request has been merged, the contributors can start to write the necessary documentation that will be required in the next release.  

### Issues
Issues have to be created with the right template. Once the issue created, the contributors are free to discuss the problem inside the issue and/or to assign it to someone.  
Issues can be labeled to make it easier to order them. Assigning labels to issues has to be made by one of the contributors.  
To fix an issue, a Pull Request must be created referencing the issue it is fixing and won't contain anything else than the very specific code fixing the problem.


## Hardware
For hardware proof of concepts, or new features, a video demonstrating how it works is expected and will be communicated to the whole team using our discord server, the team will then approve or not any modification in a meeting then will make a report of the decision in a specific channel.  
Any new big feature will be marked by a release with its specific version just like we defined it in our [DEVELOPER_GUIDE](DEVELOPER_GUIDE.md). 
