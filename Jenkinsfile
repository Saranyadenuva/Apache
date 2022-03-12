pipeline {
    
    agent { label 'main' }


    tools {
    jdk 'Java'
    maven 'Maven3.3.9'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repository
               git 'https://github.com/chinni4321/apache2.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://prashanth41234154
                  '''

            }
        }
      }
     }
