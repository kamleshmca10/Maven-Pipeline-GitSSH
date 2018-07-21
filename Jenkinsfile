pipeline { 
    agent any 
    tools {
        maven 'Maven 3.1.1'
        
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
        
        stage('Build') { 
            steps {
              //  withMaven(maven : 'maven-3.1.1'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
              //  withMaven(maven : 'maven-3.1.1'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
             //  withMaven(maven : 'maven-3.1.1'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
