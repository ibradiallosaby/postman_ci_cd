pipeline {
    agent {
        docker{
            image 'postman/newman:latest'
            args '-u root --entrypoint='
        }
    }

    stages {
         stage('Check version nodejs') {
            steps {
                sh 'newman --version'
            }
        }
        stage('Lancer le test') {
            steps {
              
              sh 'newman run Collection/Postman_CI_CD.postman_collection.json -e Environnement/preprod.postman_environment.json'
 
            }
        }
           
         
    }
} 

