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
        // stage('Deploy') {
        //     steps {
        //         input {
        //             message "Do you want to continue ?"
        //             ok 'Do it!'
        //         }
        //     }   
        // }

        stage('Example') {
            steps{
                input {
                    message "Should we continue?"
                    ok "Yes, we should."
                    submitter "alice,bob"
                    parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                     }
                }
            }
        }
    }
}

