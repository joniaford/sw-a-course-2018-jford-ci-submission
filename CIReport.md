# CI System Recommendation for AllIn Technologies
### Employee: Joni Ford
### Date: August 9th, 2018

## Introduction
Continuous integration is a critical component for AllIn Technologies. Therefore, it is important to review our CI system options and select the best CI system that will be easy to work with and meet our company's needs. In this report, I will review two CI systems, Travis CI and Skynet. My recommendation for a CI system will be based on these reviews.

## Travis CI Overview
Travis CI is a web based system that supports Linux and MacOS systems. TravisCI monthly subscriptions start at $69, with the most basic recommended for Hobby Projects. Allin Technologies will need at least the small business option, which is $249 a month, to fit our needs.

The biggest benefit of TravisCI is it is easy to set up with GitHub. Once TravisCI is authorized on the GitHub account, repos are selected on the TravisCI website. A .travis.yml file is created on the repo and defines the build configuration. The configuration can be very simple, but the TravisCI site also includes examples of more complex builds. Furthermore, a separate shell script can be included in the .travis.yml file. Once the .travis.yml file is added to the repo, a push to the repo will automatically trigger a build. The build status page is found on the TravisCI website. The TravisCI website has a simple user interface that is easy to navigate and allows you to view current builds, build history, branches, and pull requests.

TravisCI also provides build servers. While this can decrease our expenses, there are risks with shared servers such as security and overall less oversight and control. Our company could host our own build servers with TravisCI, however, the company would need to purchase a more premium plan, which can cost hundreds of dollars a month, outweighing the benefit of not needing to provide our own servers.

TravisCI also include a build matrix function. This allows us to split test builds and run in parallel, speeding up the build. Also more specific functions include including and excluding jobs, skipping builds by simply using a specific commit message, and building only specific branches.

## Skynet Overview
Skynet is a CI system that interfaces to Jenkins. One benefit of utilizing Jenkins is it is compatible with all operating systems. It also requires no subscription fee, but will require us to host our own servers. However, hosting our own servers gives us better control over security and fixing any unexpected errors.

Skynet utlizies a Job-DSL Plugin to create jobs. The DSL allows us to describe jobs and the plugin manages and maintains scripts. Jobs are configured with Lua files. Whereas with TravisCI the dependencies are defined the .travis.yml file, the dependencies when using Skynet are installed directly on machines. This may create a longer initial setup, but will keep configuration files well maintained. The Skynet interface is a little difficult to navigate if you are not familiar with it and may take time to adjust. Including and excluding jobs, skipping builds, and building only specific branches can be acheived through Skynet, but requires some work-arounds and additional time and effort. With Skynet, we would also be able to run builds in parallel.

## Comparison Overview
### Skynet   

Pros:
 + Compatible with all OS  
 + Free   
 + Requires only maintenance cost longterm, room for growth  
 
 Cons:
 + Longer setup time    
 + Below average UI     
 + Larger setup costs for servers 
 + PRs built on the same script  
 
Neutral:
  - Must host our own servers

 
### TravisCI 

Pros:
 + Quick and easy setup   
 + Easy and sleek UI
 + Can reconfigure for different PRs  
 
 Cons:
 + Not compatible with Windows    
 + Will require monthly subscription     
 + Large costs incurred for growth  
 
Neutral:
  - Servers provided
 
## Recommendation
Based on these findings, I recommend Skynet as the CI system for AllIn Technologies. While Skynet requires higher initial cost and more setup time, I believe it gives our company more room for growth. TravisCI restricts our OS usage and the power of the build servers. Currently there do not seem to be any plans to expand TravisCI compatibilties with Windows and controlling our own servers will cost us much more in the long run rather than starting with our own initially. Although it will require more work and effort, the UI for Skynet can also be upgraded by our team to include an easier UI with functions the team deems necessary and nice to have. Our company is on the brink of major growth and I believe TravisCI may hinder that growth and incur more cost.
