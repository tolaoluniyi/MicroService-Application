pipeline {
    agent any
    environment {
        SCANNER_HOME = tool 'sonar-scanner'
        SERVICE_1='adservice'
        SERVICE_2='cartservice'
        SERVICE_3='checkoutservice'
        SERVICE_4='currencyservice'
        SERVICE_5='emailservice'
        SERVICE_6='frontend'
        SERVICE_7='loadgenerator'
        SERVICE_8='paymentservice'
        SERVICE_9='productcatalogservice'
        SERVICE_10='recommendationservice'
        SERVICE_11='shippingservice'
   }

    stages {
            stage('SonarQube') {
             steps {
                withSonarQubeEnv('sonar') {
                    sh '''$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=10-Tier -Dsonar.ProjectName=10-Tier -Dsonar.java.binaries=.'''
                }
            }
        }
            stage('adservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir('/var/lib/jenkins/workspace/10-Tier/src/adservice/') {
                        sh "docker build -t tkibnyusuf/adservice:latest ."
                        sh "docker push tkibnyusuf/adservice:latest"
                        sh "docker rmi tkibnyusuf/adservice:latest"
                    }
                }
            }
        }
            }
            stage('cartservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/cartservice/src/") {
                        sh "docker build -t tkibnyusuf/cartservice:latest ."
                        sh "docker push tkibnyusuf/cartservice:latest"
                        sh "docker rmi tkibnyusuf/cartservice:latest"
                    }
                }
            }
        }
       }
            stage('checkoutservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/checkoutservice/") {
                        sh "docker build -t tkibnyusuf/checkoutservice:latest ."
                        sh "docker push tkibnyusuf/checkoutservice:latest"
                        sh "docker rmi tkibnyusuf/checkoutservice:latest"
                    }
                }
            }
        }
            }
            stage('currencyservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/currencyservice/") {
                        sh "docker build -t tkibnyusuf/currencyservice:latest ."
                        sh "docker push tkibnyusuf/currencyservice:latest"
                        sh "docker rmi tkibnyusuf/currencyservice:latest"
                    }
                }
            }
        }

            }
            stage('emailservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/emailservice/") {
                        sh "docker build -t tkibnyusuf/emailservice:latest ."
                        sh "docker push tkibnyusuf/emailservice:latest"
                        sh "docker rmi tkibnyusuf/emailservice:latest"
                    }
                }
            }
        }
            }
            stage('frontend') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/frontend/") {
                        sh "docker build -t tkibnyusuf/frontend:latest ."
                        sh "docker push tkibnyusuf/frontend:latest"
                        sh "docker rmi tkibnyusuf/frontend:latest"
                    }
                }
            }
        }
            }
            stage('loadgenerator') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/loadgenerator/") {
                        sh "docker build -t tkibnyusuf/loadgenerator:latest ."
                        sh "docker push tkibnyusuf/loadgenerator:latest"
                        sh "docker rmi tkibnyusuf/loadgenerator:latest"
                    }
                }
            }
        }
            }
             stage('paymentservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/paymentservice/") {
                        sh "docker build -t tkibnyusuf/paymentservice:latest ."
                        sh "docker push tkibnyusuf/paymentservice:latest"
                        sh "docker rmi tkibnyusuf/paymentservice:latest"
                    }
                }
            }
        }
             }
             stage('productcatalogservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/productcatalogservice/") {
                        sh "docker build -t tkibnyusuf/productcatalogservice:latest ."
                        sh "docker push tkibnyusuf/productcatalogservice:latest"
                        sh "docker rmi tkibnyusuf/productcatalogservice:latest"
                    }
                }
            }
        }
             }
             stage('recommendationservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/recommendationservice/") {
                        sh "docker build -t tkibnyusuf/recommendationservice:latest ."
                        sh "docker push tkibnyusuf/recommendationservice:latest"
                        sh "docker rmi tkibnyusuf/recommendationservice:latest"
                    }
                }
            }
        }
             }
             stage('shippingservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir("/var/lib/jenkins/workspace/10-Tier/src/shippingservice/") {
                        sh "docker build -t tkibnyusuf/shippingservice:latest ."
                        sh "docker push tkibnyusuf/shippingservice:latest"
                        sh "docker rmi tkibnyusuf/shippingservice:latest"
                    }
                }
            }
        }
    }
   }
   }
