pipeline {
   agent none
   stages {
      stage('Build Code') {
	     when {
             branch 'main'
            }
         agent {
             node {
                  label 'dev-aws'
                  customWorkspace '/home/ubuntu/jenkins/multi-branch/'
                }
            }
         steps {
               sh """
               echo "Building Artifact"
               """
           }
       }
      stage('Deploy Code') {
        when {
             branch 'main'
            }
        agent {
              node {
                  label 'dev-aws'
                  customWorkspace '/home/ubuntu/jenkins/multi-branch/'
                }
            }
        steps {
              sh """
              echo "Deploying Code"
              """
          }
      }
   }
}
