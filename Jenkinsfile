pipeline {
    agent any
    environment {
        SCANNER_HOME = tool 'sonar-scanner'
        SERVICE_1 = 'adservice'
        SERVICE_2 = 'cartservice'
        SERVICE_3 = 'checkoutservice'
        SERVICE_4 = 'currencyservice'
        SERVICE_5 = 'emailservice'
        SERVICE_6 = 'frontend'
        SERVICE_7 = 'loadgenerator'
        SERVICE_8 = 'paymentservice'
        SERVICE_9 = 'productcatalogservice'
        SERVICE_10 = 'recommendationservice'
        SERVICE_11 = 'shippingservice'
      
   }

    stages {
        stage('SonarQube') {
            steps {
                withSonarQubeEnv('sonar') {
                    sh '''$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=10-Tier -Dsonar.ProjectName=10-Tier -Dsonar.java.binaries=.'''
                }
            }
        }
    
            stage($SERVICE_1) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_1/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_1:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_1:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_1:latest"
                    }
                }
            }
        }
            }
            stage($SERVICE_2) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_2/src") {
                        sh "docker build -t tkibnyusuf/$SERVICE_2:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_2:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_2:latest"
                    }
                }
            }
        }

            }
              
            stage($SERVICE_3) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_3/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_3:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_3:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_3:latest"
                    }
                }
            }
        } 
            }            
            stage($SERVICE_4) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_4/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_4:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_4:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_4:latest"
                    }
                }
            }
        }

            }
            stage($SERVICE_5) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_5/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_5:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_5:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_5:latest"
                    }
                }
            }
        }
            }
              
            stage($SERVICE_6) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_6/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_6:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_6:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_6:latest"
                    }
                }
            }
        }
            }
            stage($SERVICE_7) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_7/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_7:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_7:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_7:latest"
                    }
                }
            }
        }
            }
            stage($SERVICE_8) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_8/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_8:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_8:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_8:latest"
                    }
                }
            }
        }
            stage($SERVICE_9) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_9/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_9:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_9:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_9:latest"
                    }
                }
            }
        }
            stage($SERVICE_10) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_10/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_10:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_10:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_10:latest"
                    }
                }
            }
        }
            stage($SERVICE_11) {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/$SERVICE_11/") {
                        sh "docker build -t tkibnyusuf/$SERVICE_11:latest ."
                        sh "docker push tkibnyusuf/$SERVICE_11:latest"
                        sh "docker rmi tkibnyusuf/$SERVICE_11:latest"
                    }
                }
            }
        }                
    }
   }
   }
    }
  }
}
