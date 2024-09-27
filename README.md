# library_encryption_class

The goal of this class is to encrypt text using the JavaScript web crypto library and hexadecimal. 

It uses library_to_run_GitHub_Actions.js to automatically save (ie: REST API GITHUB PUT) text to files in GitHub repositories. library_to_run_GitHub_Actions.js is a jsdelivr/npm library that I created at https://www.jsdelivr.com/package/npm/library_to_run_github_actions.

## How library_encryption_class works
  - It is a CRUD (CREATE, READ, UPDATE, DELETE) file storage that consistently re-encrypts files every 12 hours, such that all data is continuously encrypted with a new key. Keys are updated on the Frontend every 12 hours using the JavaScript web crypto library.
  - When the repository is used to store data, the data will be re-encrypted every 12 hours using the web crypto keys. 

## In progress
- The working version of the CRUD library needs to be improved such that all calls to the library_to_run_GitHub_Actions.js are from npm
- A demonstration html needs to be created to demonstrate the library
