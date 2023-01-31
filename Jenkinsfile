pipeline
    {
        agent any
        stages {
            stage('git checkout') {
                steps {
                    git branch: 'main', url: 'https://github.com/Jufervela/DemoPython.git'
                }
            }

            stage('Checkout') {
                steps {
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Jufervela/DemoPython.git']])
                }
            }
            stage('TEST') {
                steps {
                    sh 'mvn test'
                }
            }
            stage('BUILD') {
                steps {
                    sh 'mvn clean install'
                }
            }
            stage('ANALISIS DE CODIGO ESTATICO') {
                steps {
                    withSonarQubeEnv(credentialsId: 'sonar-api') {
                    sh 'mvn clean packagesonar:sonar'
                    }
                }
            }
        }
    }
