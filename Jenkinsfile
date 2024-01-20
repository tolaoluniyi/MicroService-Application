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
                    sh '''$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=project1 -Dsonar.ProjectName=project1 -Dsonar.java.binaries=.'''
                }
            }
        }
            stage('adservice') {
              steps {
               script {
                 withDockerRegistry(credentialsId: 'dockerhub', toolName: 'docker') {
                    dir('/var/lib/jenkins/workspace/project1/src/adservice/') {
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
                    dir("/var/lib/jenkins/workspace/project1/src/cartservice/src/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/checkoutservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/currencyservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/emailservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/frontend/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/loadgenerator/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/paymentservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/productcatalogservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/recommendationservice/") {
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
                    dir("/var/lib/jenkins/workspace/project1/src/shippingservice/") {
                        sh "docker build -t tkibnyusuf/shippingservice:latest ."
                        sh "docker push tkibnyusuf/shippingservice:latest"
                        sh "docker rmi tkibnyusuf/shippingservice:latest"
                    }
                }
            }
        }
    }

              stage('K8-Deploy') {
            steps {
                withKubeConfig(caCertificate: '', clusterName: 'myAppp-eks-cluster', contextName: '', credentialsId: 'k8s-token', namespace: 'webapps', restrictKubeConfigAccess: false, serverUrl: 'https://75CD60CD64BEAE9AB3CB93894C8FA247.gr7.us-east-1.eks.amazonaws.com') {
                    sh 'kubectl apply -f deployment-service.yml'
                    sh 'kubectl get pods'
                    sh 'kubectl get svc'

                }
                }
            }
        }
   }
   }
