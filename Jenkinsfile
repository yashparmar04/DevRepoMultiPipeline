pipeline {

    agent any
 
    stages {

        stage('Checkout') {

            steps {

                git url: 'https://github.com/yashparmar04/DevRepoMultiPipeline', branch: env.BRANCH_NAME

            }

        }
 
        stage('Build') {

            steps {

                script {

                    echo "Building development branch: ${env.BRANCH_NAME}"

                    sh 'javac Sample.java'

                    sh 'java Sample'

                }

            }

        }
 
        stage('Deploy') {

            steps {

                script {

                    echo "Running Deployment on development branch: ${env.BRANCH_NAME}"

                    sh 'javac Sample.java'

                    sh 'java Sample'

                }

            }

        }

    }
 
    post {

        always {

            echo 'Pipeline finished.'

        }

        success {

            echo 'Pipeline succeeded.'

        }

        failure {

            echo 'Pipeline failed.'

        }

    }

}
 
