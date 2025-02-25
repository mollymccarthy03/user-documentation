---
ospool:
  path: overview/account_setup/starting-project.md
---

# Set and View Project Usage

## Background

The OSG team assigns individual user accounts to "projects". These projects 
are a way to track usage hours and capture information about the types of 
research using the OSPool. 

A project typically corresponds to a research group headed by a single PI, but can 
sometimes represent a long-term multi-institutional project or some other grouping. 

You must be a member of a project before you can use OSG Connect to submit jobs. 
The next section of this guide describes the process for joining an OSG Connect project. 

## Default Behavior (one project)

By default, you are added to a project when your OSG account is created. This 
project will be automatically added to your job submissions for tracking usage. 

## Choose a Project (multiple projects)

If you are affiliated with multiple groups using the OSPool and are a member of 
multiple projects, you will want to set the project name in your submit file. 

Run the following command to see a list of projects you belong to:

<pre class="term"><code>grep $USER /etc/condor/UserToProjectMap.txt</code></pre>

You can manually set the project for a set of jobs by putting this option in
the submit file:

<pre class="sub"><code>+ProjectName="ProjectName"</code></pre>

## View Metrics For Your Project

The project's resource usage appears in the OSG accounting system, [GRACC](https://gracc.opensciencegrid.org/d/000000033/osg-project-accounting?orgId=1). 
You can see the main OSG Connect dashboard here: [Link to OSG Connect Dashboard](https://gracc.opensciencegrid.org/d/000000099/osg-connect-summary-osgconnect-net-submit-hosts-only?orgId=1)

At the top of that dashboard, there is a set of filters that you can use to examine 
the number of hours used by your project, or your institution.
