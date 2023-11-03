pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('Get role') {
            steps {
                dir('vector-role') {
                    git branch: 'main', credentialsId: '26fdc1b8-3068-45bd-80a1-e663e5df084a', url: 'https://github.com/michail-77/vector-role.git'
                }
            }
        }
        stage('Molecule test') {
            steps {
                dir('vector-role') {
                sh 'molecule test'
                }
            }
        }
    }
}
