# Contribution Guidelines

We build Open Source software and we invite everyone to join us and contribute. So if you are interested into participate, please refer to the guidelines below.

## Developer Guide

[Developer Guide](DEVELOPER_GUIDE.md).

## GIT Repositories

All code changes and submissions happen on [Github](http://github.com), that means that to start contributing you should clone the target repository, perform local changes and then do a Pull Request. For more details about the workflow we suggest you check the following documents:

 - https://help.github.com/articles/using-pull-requests
 - https://help.github.com/articles/creating-a-pull-request


## General requirements

### Commit Changes

When you commit your local changes in your repository (before to push to Github), we need you take care of the following:

 - Your principal commit message (one line subject) **must be** prefixed with the modified module name in lower case plus a colon. If you are fixing a bug in the core module your message should look like:

   ```
   core: fix handling of abc
   ```

   Expanding a bit the example feature message we could use the following command:

   > $ git commit -a -s
   >
   > engine: fix handling of abc
   >
   > This patch fixes a problem when the device shuts down while applying the configuration.
   > If the configuration is in a unstable state, it will reset itself so the code can function again.
   >
   > the patch have been tested using tools A & B.
   >
   > Signed-off-by: Your Name <your@email.com>

   Your patches should be fully documented. That will make the review process faster for us and a faster merge for you.  
   You can give as much details as you would like inside your pull requests comments, as long as they are relevant and will help the reviewers to understand your modifications.


- One single commit **must not** include changes to files that are different from the component specified in the subject.

- One single commit **must not** include multiple prefixes to specify different areas being touched. Don't commit modifications to two modules in one single commit, even if they are part of the same feature.

- The subject of the commit **must not** be longer than 80 characters.

- On the commit body, each line **must not** be longer than 80 characters.

- On most of cases we want full description about what your patch is doing, the patch description should be self descriptive.. like for dummies. Do not assume everybody knows what you are doing and on each line do not exceed 80 characters.

- When running the __git commit__ command, make sure you are using the __-s__ flag, that will add a Signed-off comment in the patch description.


### Code reviews

When we review your code submission, the code should follow our [Developer Guide](DEVELOPER_GUIDE.md), be documented and the patch Subject and Description well formed (within others).

If your code needs some improvement, someone of the reviewers or core developers will write a comment in your Pull Request, so please take in count the suggestion there, otherwise your request could never be merged.

Despite the effort that took for you to create the contribution, that is not an indication that the code has to be merged into upstream, everything will be reviewed and must be aligned as the code base.
