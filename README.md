# frontend_backend_message_passing_central_repository_v1 ☀️

The goal of this repository is to practice writing BackEnd yaml workflows that process FrontEnd user input. User input is obtained from any repository, called RepoA. RepoA is a GitHub Page that only has access to REST API calls using JavaScript and HTML, thus there needs to be some other numerical infrastructure that collects information that user inputs such that their information can be processed at an endpoint or on a virtual machine via a model and/or script.

RepoB, this repository, is an intermediate processing area where information from RepoA can be sent to backend processes (GitHub Actions). To send information to backend processes, the repository must risk exposing the repository resources to cyber-attack by using a key to contact the backend processes. Thus, to minimize this risk, RepoB an intermediate repository, is used. RepoB contains a key with the lowest-level permissions (file/content modification) to contact backend processes, and no valuable long-term information except for it's basic functioning are stored in RepoB. This is the second version of RepoB, it will be more secure than the first version because it will store only its key in GitHub secrets.

## Frontend library script (library_to_run_GitHub_Actions.js)
The purpose of the frontend library script is to trigger the intermediate repository RepoB to start frontend and/or backend processes for RepoA.
- The current version of the frontend library script ***(to be published on jsdelivr.com)***: [library_to_run_GitHub_Actions.js](https://github.com/CodeSolutions2/library_to_run_GitHub_Actions)


## Version 0 of RepoB
The [frontend_backend_message_passing_central_repository_v0](https://github.com/CodeSolutions2/frontend_backend_message_passing_central_repository_v0) repository is the first version of RepoB, it is an intermediate repository that is triggered by RepoA (ie: a button push on a GitHub Page deployed application called my_chatbot). The frontend library script is called by a user pushing a button on the deployed my_chatbot application. The frontend library saves the user input_text in a file in RepoB, RepoB listens for changes/creation of the input_text file whereupon it triggers backend processes for RepoA using a repository dispatch event. Thus, RepoA does not have to expose their resources to cyber-attack while processing the user input_text.

  - Disadvantages of RepoB_V0 workflow architecture: RepoB needs RepoA's key on the backend via GitHub Secrets, to create the repository dispatch event. If the backend of RepoB is compromised, it could expose RepoA. Thus, a second version of RepoB, this repository (frontend_backend_message_passing_central_repository_v1), was created.

## Version 1 of RepoB
  - [Update keys on Frontend] https://CodeSolutions2.github.io/frontend_backend_message_passing_central_repository_v1/index_reset.html
  - Disadvantages of this workflow architecture: RepoB file contents need to be backed-up in another protected repository to avoid complete loss of data. ***(an automated solution is in development)***
