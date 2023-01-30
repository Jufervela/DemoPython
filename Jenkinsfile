pipeline
    {
        agent any
        stages {
            stage('git checkout') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                }
            }

            stage('UNIT testing') {
                steps {
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Jufervela/DemoPython.git']])
                }
            }

            stage('Build') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                    bat 'python hola_mundo.py'
                }
            }
        }
    }
