pipeline {
    agent any

    environment {
        JAVA_HOME = '/usr/lib/jvm/java-11-openjdk'  // Adjust to your Java version or use default
        PATH = "$JAVA_HOME/bin:$PATH"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository (Jenkins does this automatically for pipeline jobs)
                echo 'Checking out the repository...'
                checkout scm  // This pulls the latest code from your repository
            }
        }

        stage('Compile Java') {
            steps {
                script {
                    // Compile the Java file (assumes a .java file exists in the repo)
                    echo 'Compiling Java file...'
                    bat 'javac ex.java'  // Replace with the actual Java file name
                }
            }
        }

        stage('Run Java') {
            steps {
                script {
                    // Run the Java file and redirect the output to a file (result.txt)
                    echo 'Running the Java program...'
                    bat 'java tab > result.txt'  // Replace with your Java class name
                }
            }
        }

        stage('Archive Result') {
            steps {
                // Archive the result file to be accessible after the build finishes
                echo 'Archiving the result...'
                archiveArtifacts artifacts: 'result.txt', allowEmptyArchive: true
            }
        }
    }

    post {
        always {
            echo 'Build finished!'
        }
    }
}
