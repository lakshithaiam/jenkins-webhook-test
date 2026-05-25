pipeline {
    agent {
        kubernetes {
            yaml '''
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: python
    image: python:3.12-alpine
    command:
    - cat
    tty: true
'''
        }
    }
     
    stages {
        stage('Run Tests') {
            steps {
                container('python') {
                    sh '''
                        pwd
                        ls -a
                        cat Jenkinsfile
                    '''
                }
            }
            
        }
    }
}

