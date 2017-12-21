---
published: true
layout: post
tags:
  - javascript
---
## Kubernetes - #2 on Holiday Techie Fun Project List

So yesterday I posted on this blog for the first time since 6/16 (is that 18 months?!).  In that post I shared my [Holiday Techie Fun Project List](http://davidmcd.com/2017/12/20/Holiday-Projects-List/) in which I have listed my candidate geeky projects for the holiday season.  Project #1 was getting this blog back to the point where I could easily manage it again - this time on Windows using Bash Shell.  

Today's project, which I started last night, is to stand up a sample app running in Azure's new Kubernetes Service (AKS).  I'm happy to report that I finished that one early this afternoon.  There were two primary articles that helped guide me through.  
- [Scott Hanselman's Blog - Setting up AKS in Minutes](https://www.hanselman.com/blog/SettingUpAManagedContainerClusterWithAKSAndKubernetesInTheAzureCloudRunningNETCoreInMinutes.aspx)
- [Azure Docs - AKS Walkthrough](https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough)

These are both similar.  The Hanselman's post had some extra coolness at the end to launch the Kubernetes Dashboard.  Also his article included the parameter to create a single node cluster (the default is three node).  I worked on this both in the portal CLI and the local CLI.  The local CLI has the extra step of requiring a login (az login).  

There were a number of issues that I ran into getting this running.  The biggest was that I kept getting bad request for missing registrations on Microsoft.Network and Microsoft.Compute.  I'm still not clear on why, but the following seemed to fix the issue.  
- az provider register -n Microsoft.Compute
- az provider register -n Microsoft.Network

Also note that I created a three node cluster.  I'm not sure about the cost etc. so I was sure to tear it down at the end.  
- az group delete -n davidmcdAKSrg --yes

This was super fun and I learned lots.  I can't wait to get started on tomorrow's project.  
