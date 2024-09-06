# library_encryption_class ☀️

The goal of this class is to encrypt text using the JavaScript web crypto library. It uses library_to_run_GitHub_Actions.js to automatically save encrypted text to files in GitHub repositories.

## How library_encryption_class works
  - It is a CRUD (CREATE, READ, UPDATE, DELETE) file storage that consistently re-encrypts files every 12 hours, such that all data is continuously encrypted with a new key. [Update keys on Frontend](https://CodeSolutions2.github.io/frontend_backend_message_passing_central_repository_v1/run_html_from_backend_puppeter_index2.html) is run every 12 hours to update encryption keys for encrypting text.
  - A streamlined code with easy-to-use html interface that allows users to: CREATE text data, READ/view text data, UPDATE/add to/append existing text data, and DELETE text data  ***(in progress)***
  - Disadvantages of this workflow architecture: The repository file storage need to be backed-up in another protected repository to avoid complete loss of data. ***(an automated solution is in development)***
  - 
## Frontend library script (library_to_run_GitHub_Actions.js)
The purpose of the frontend library script is to trigger the intermediate repository RepoB to start frontend and/or backend processes for RepoA.
  - The current version of the frontend library script: [library_to_run_GitHub_Actions.js](https://github.com/CodeSolutions2/library_to_run_GitHub_Actions)
