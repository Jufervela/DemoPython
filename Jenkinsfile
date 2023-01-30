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

            stage('BUILD') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                    eho 'python hola_mundo.py'
                }
            }
            stage('TEST') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                    eho 'python hola_mundo.py'
                }
            }
            stage('DEPLOY') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                    eho 'python hola_mundo.py'
                }
            }
        }
    }
