pipeline {
    
    agent { label 'master' }


    tools {
    jdk 'Java'
    maven 'Maven3.3.9'

  }

    stages {
        
        stage('Git Clone') {
            steps {
                // Get some code from a GitHub repositor
                git branch: 'main',
               url: 'https://github.com/Saranyadenuva/Apache.git'
            }

        }
        stage('aws') {
            steps {
                // Get some code from a GitHub repository
                sh  '''
                  cd $WORKSPACE
                  aws s3 sync . s3://saranya198755
                  '''

            }
        }
      }
     }
