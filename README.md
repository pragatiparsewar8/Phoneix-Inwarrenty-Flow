# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in postman and executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project using workflow_dispatch.The project runs on a scheduled time with the help of cron job.

The html reports are archieved and kept in the artifact section for the team to download it.Along with that they can view the reports directly from the github page from the github page: https://pragatiparsewar8.github.io/Phoneix-Inwarrenty-Flow/
The latest report is mailed to the team members using gmail smtp.

## Tech stack ##
1.Postman
2.Nodejs
3.Newman
4.Newman-reporter-htmlextra
5.Github Actions
6.Gmail smtp
7.Github Pages
8.CSV for data driven testing
9.AWS EC2 instance for self hosted github runner

## Testing Scope ##
1.Happy flow testing
2.Negative testing and edge case testing
3.Token testing
4.Data driven testing with csv 
5.schema validation
6.Secrets management with github secrets

## Github Pages ##
You can directly view the latest test report of the postman test at the github page : https://pragatiparsewar8.github.io/Phoneix-Inwarrenty-Flow/

## HTML Report ##
 The report will be created in the newman folder
 ![Postman Test Results Report]( https://github.com/pragatiparsewar8/Phoneix-Inwarrenty-Flow/blob/static-content/newman-htmlextra-report.png)


## Project Structure ##

```
Phoneix Inwarrenty Flow
├─ Inwarrenty flow.postman_collection.json
├─ QA.postman_environment.json
└─ testdata.csv

```

## How to run the project? ##
You can run the project on the local system
1.Clone the project on the local system : https://github.com/pragatiparsewar8/Phoneix-Inwarrenty-Flow.git
2. Install Nodejs and NPM
3. Install newman using   ``` npm install -g neman ```
4. Install reported using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command:

          newman run "Inwarrenty flow.postman_collection.json" \
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export newman/index.html
    

## About Me ##
Hi My name is Pragati Parsewar. I have 6 years of experience in automation testing.My skillset includes UI automation with selenium,cypress,karate and for API testing use RestAssured,Karate,postman
You can connect with me : ! [Linkedin Profile] (https://www.linkedin.com/in/pragati-parsewar-198481331/)
