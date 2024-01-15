pipeline {
    agent any
    
    environment {
        ANT_HOME = 'C:/Users/2273434/Documents/ApacheANT/apache-ant-1.10.14'
    }
 
    stages {
        stage('Run Ant Build') {
            steps {
                script {
                    withEnv(["PATH+ANT=${env.ANT_HOME}/bin"]) {
                        dir('C:\Users\2273434\Documents\SavvasProjectWithGit\project1\gitTesting\ANT') {
                            sh 'cat unpackaged/package.xml'
                            sh 'ant -f retrieveUnpackaged'
                            sh 'ant -f deployUnpackaged'
                        }
                        // Add additional processing or actions based on the Ant build output
                    }
                }
            }
        }
        // Add more stages as needed
    }
    // Add post-build actions or other configurations
}