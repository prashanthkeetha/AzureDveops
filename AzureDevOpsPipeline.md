# Continous Integration:
1. Building the code.
2. Packing the application 
3. Running basic automated tests which well the health of the application.

# Agile ways of working:
------------------------
1. There is a need to release application frequently fixing the bugs and the changes based on the requirement.
2. The need for automating releses increased.
3. In Agile, we list out all the {USER STORIES} needed to be done as Product Backlog.

# Azure DevOps Pipeline:
------------------------
1. Tool for managing continous integrations as well as deployments (releases) to the customer.
2. A tool where developers can submit the code
3. A tool for managing the project

# Steps that happens in the CI

Devloper writes the code
       |
Pushes the code into vcs
       |
Build the code  ----------------------------------                                  |
       |                                          |
Test the code                                     |
       |                                          | This all steps are come into the Build and packaging the application 
Code analysis                                     |
       |                                          |
Package tha application (Into jar or war files)---   |
       |
we have artifacts after packaging the application
       |
Push artifactory to repository
       |
Release Activities.


# Things we need
* GitHub account
* From my understanding we will create the Azure DevOps account using GitHub
* In azure devops we create the project 
    * In the projects we have Public and Private Projects.
      # To create Project the process is
         i) Click on "New Project"
                        |
        Fill in "(Project Name)"
                        |
        Create the Project(Public and Private Projects)
                        |
                  click create
                        |

                         
        Where Public Project can see by everyone
        And Private project is seen bu 
    -> In side the project you are able to see the 
         a) Boards: This is used Plan, Manage and projects tracking not part of the pipeline itself, but it complements your CI/CD Process
             i) WorkItems:
             ii) Boards:
             iii) Baqcklogs:
             iv) sprints:
             v) Queries:
             vi) Delivery Plans:
        b) Repos: This is where developers commit code(that means where devlopers push the code to the repository)
             * Azure Repos support (Git)
                     |
             * To creata repository inside the project we use REPOS click on the repos and files(Inside that add
                   New repository,
                       | 
                   Import Repository and
                       | 
                   Manage Repository.
                    * Adding a new repository: just adds a new source code repository to that project.(It doesn't mean adding new project)
                    * Importing New repository: It allows us to bring existing repository from an external source like GitHub into 
                      current Azure DevOps Project as a new Repository.
                        * If you're moving a project from GitHub to Azure DevOps, you can use the "Import Repository" option to bring in      
                        the repository, including its entire commit history, into your Azure DevOps project without needing to manually clone and push the data.
               * After creating Repository we can see the clone which have (SSH AND HTTPS) login 
                     
            i) Files:
            ii) Commits:
            iii) Pushes:
            iv) Branches:
            v) Tags:
            vi) Pull Requests:
        c) Pipelines: This is service where CI/CD Pipelines are managed
             * In these are two types of Pipelines
                a) Build Pipeline:
                b) Release Pipeline:
             * Inside the Pipeline we have
                 i) Pipelines:
                 ii) Environments:
                 iii) Releases:
                 iv) Library:
                 v) Task group:
                 vi) Deployment groups:
        d) Test Plans: This service manage test cases and test executions
             i) Test plans:
             ii) Progress report:
             iii) Runs:
        e) Artifacts: This service manage build artifacts


# Connections:
--------------

# This process is for classic editor without using the Yaml file.

* Azure DevOps to connect with the external service or external cloud services like (GitHub, AWS and Azure) need {CONNECTIONS}
                                                                                                                 -------------
* After completing the connection we have {added the required details of the project regarding the (Docker container, packaging 
  application from there save and queue and run the PIPELINE hosted agent)}

# WE HAVE A PRALLEL JOBS THERE MULTIPLE TYPES.
1. PRIVATE PROJECTS {THIS IS WE USED IN THE ORGANIZATIONS}
   * Microsoft Hosted there is (0) Prallel Jobs are allowed 
   * Self Hosted there is (1) Prallel Jobs are allowed
2. PUBLIC PROJECTS
   * Microsoft Hosted there is (0) Prallel Jobs are allowed
   * Self Hosted there is (unlimited) Prallel Jobs are allowed

           

        