pipeline {
    agent any

    stages {
                stage('git') {
            git url: 'https://github.com/rupinenisreehari/java-project.git',
        }
        stage('build') {
            sh '''
                echo "PATH=${PATH}"
                echo "M2_HOME=${M2_HOME}"

            '''
            sh '/usr/local/apache-maven-3.8.4/bin/mvn package'
        }
        stage('archive') {
            archiveArtifacts artifacts: 'target/*.jar',
        }

        }
    }
}

