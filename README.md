# Crucible Review Hook for Bitbucket (Stash)
Issue manager and Documentation for Crucible Review Hook for Bitbucket.

# Getting Started
For the plugin to work correctly, the following must be setup:  
1. Setup the Crucible Application link with Bitbucket. Instructions can be found [here](https://confluence.atlassian.com/fisheye/linking-to-another-application-385321667.html).  
2. Add the repository to FIshEye/Crucible for indexing. Instructions can be found [here](https://confluence.atlassian.com/crucible/setting-up-a-git-repository-in-crucible-298977505.html).  
3. Enable the hook in the plugin settings for the desired repository settings.  

You're now ready to get started!

#Configuration
The plugin has the following settings which must be configured per **repository**.

| Option | Description |
| ------------- | ------------- |
| Review Project | The Crucible Review project to be created under. | 
| Automatically Create Reviews | Whether to automatically create reviews in Crucible. The review project specified here will be used. |
| Merge Hook Branch Regex | All branches that match this regex will have a review created when another tries to merge any changes to them through a PullRequest. | 

# Adding/Editing Reviews
Crucible reviews can be created one of two ways:  
1. Automatically through the plugin.  
2. By hand through the Pull Request dropdown.  
![enter image description here](https://raw.githubusercontent.com/mohamicorp/crucible-review-hook/master/images/crucible-review-edit-review.png)

Automatically creating the reviews will fail if the pull-request author does not have the correct permissions in Crucible. Make sure to have the Crucible administrator check the following permissions:
* The user is listed as a Allowed review participant in the project settings.
![enter image description here](https://raw.githubusercontent.com/mohamicorp/crucible-review-hook/master/images/Screenshot%20from%202016-09-14%2017-03-57.png)
* Authors have permission to Edit Review Details in the permission schemes.
* ![enter image description here](https://raw.githubusercontent.com/mohamicorp/crucible-review-hook/master/images/Screenshot%20from%202016-09-14%2017-00-11.png)


