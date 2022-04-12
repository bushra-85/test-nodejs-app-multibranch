pipeline { 
  
   agent any

   stages {
     
     stage('Fetch Code') {
            steps {
            
                script
                {

              git branch: '$BRANCH_NAME', credentialsId: 'f3a343d0-9b37-46f0-a08d-cf8b47300d13', url: 'https://bitbucket.org/siliconstack/gestaltra_fe.git'
              echo '$BRANCH_NAME'
                }
                 
            }
   
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
        }
     }
     
     stage('Test') { 
        steps { 
           sh 'echo "testing application..."'
        }
      }

         stage("Deploy nodejs application") { 
         steps { 
           sh 'echo "deploying application..."'
         }

     }
  
   	}

   }
