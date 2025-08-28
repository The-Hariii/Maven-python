pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                echo"file compiling"
                sh 'python3 -m py_compile app.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python tets/ || echo "no test found "'
            }
        }
          stage('package') {
            steps {
                sh 'zip -r app-package.zip app.py'
            }
        }
        stage('deploy') {
            steps {
                echo "Running HelloWorld Java Program"
                sh 'python3 app.py'
            }
        }
    }
}
