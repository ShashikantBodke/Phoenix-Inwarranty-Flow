# Psotman API Automation Integartion with Github Actions #

This repository is a demonstration of POC for integrating postman tests with github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to main branch. You can also execcute the project manually using workflow_dispatch. The project runs on the scheduled time with the helo of cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://shashikantbodke.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team memebrs using GMAIL smtp

## Tech Stack ##
1. Postman
2. Nodejs - 22
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail smtp
7. Github Pages
8. AWS-EC2 instance for self hosted github-runner

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github Page Link: https://shashikantbodke.github.io/Phoenix-Inwarranty-Flow/

## How to run the project ? ##
You can run the project on your local system for that:
1. Clone the project on the local system : https://github.com/ShashikantBodke/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using : npm install -g neman
4. Install Newman-Reporter-Htmlextra using : npm install -g newman-reporter-htmlextra
5. Run the Newman command :
              newman run 'Inwarranty-flow Collection.postman_collection.json' \
              -e 'QA.postman_environment.json' \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
