properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/vemulaabhishek/Multibranch_task.git'],
            pipelineTriggers([githubPush()])])
pipeline {
    agent any
        stages {
            stage('Build') {
                when {
                    expression {
                        "foo" == "bar"
                    }
                }
                steps {
                    echo 'Building......sk....'
                }
            }
        stage('Test') {
            when {
                environment name: 'JOB_NAME', value: 'foo'
            }
            steps {
                echo 'Testing.......'
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying........'
            }
        }
      }
}
