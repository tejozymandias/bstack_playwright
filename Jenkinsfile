 pipeline {
    agent any
   tools { nodejs "18.17.0" }
   stages {
       stage('setup') {
         steps {
             browserstack(credentialsId: '9b705e69-e2b3-4081-b933-bfc8e1462cfc') {
                 // add commands to run test
                 // Following are some of the example commands -----
                 git branch: 'main', url: 'https://github.com/tejozymandias/bstack_playwright.git'
                 sh 'npm install'
                 sh 'npm run sample-test'
             }
             //Enable Reporting
             browserStackReportPublisher 'automate'
         }

       }
     }
   }
