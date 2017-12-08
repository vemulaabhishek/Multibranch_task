properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/vemulaabhishek/Multibranch_task.git'],
            pipelineTriggers([upstream('master')])])
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
                    echo 'Building..ss........'
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
