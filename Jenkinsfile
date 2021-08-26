pipeline {
    agent any
    environment{
        project_name = "Pipeline_Practice"
    }

    stages {
        stage('Build') {
            steps {
                sh "echo 'This is build no. ${build_number} for project: ${project_name}'"
            }
        }
        stage('Deploy') {
                input {
                    message "Do you want to continue ?"
                    // ok 'Do it!'
                }
                steps{
                    echo "Checking Input."
                }
               
        }

    }
     post{
            always{
                echo "Print if build is success or not!"
            }
        }
}

