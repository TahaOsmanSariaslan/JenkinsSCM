pipeline {
    agent any

    stages {
        stage('Build step') {
            steps {
                echo 'Build success'
            }
        }
        stage('Test step') {
            steps {
                echo 'Test success'
            }
        }    
        stage('Deploy step') {
            steps {
                retry(2){
                    echo 'Deploy success'
                }
            }
        }        
        stage('Timeout') {
            steps {
                timeout(time:3, unit:'SECONDS'){
                    echo 'Deploy success'
                }                  
                
            }
        } 
    }
}
