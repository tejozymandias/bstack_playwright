 pipeline {
   agent { label 'master' }
   tools { nodejs "18.17.0" }
   stages {
       stage('setup') {
         steps {
             browserstack(credentialsId: '9b705e69-e2b3-4081-b933-bfc8e1462cfc') {
                 // add commands to run test
                 // Following are some of the example commands -----
                 sh 'npm install'
                 sh 'npx playwright test --config=./playwright.config.js'
             }
             //Enable Reporting
             browserStackReportPublisher 'automate'
         }

       }
     }
   }
