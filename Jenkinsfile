pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # Initialize conda in a non-interactive shell
                ls
                # sudo source /home/team10/miniconda3/bin/activate mlip-lab

                # Activate the conda environment
                conda activate mlip-lab

                # Run pytest
                pytest

                echo 'pytest run completed'
                exit 1 #comment this line after implementing Jenkinsfile
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
