pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat '''
                python --version
                python -m venv venv
                . venv/bin/activate
                "C://Users//manur//AppData//Local//Programs//Python//Python313//Scripts//pip.exe" install --upgrade pip
                "C://Users//manur//AppData//Local//Programs//Python//Python313//Scripts//pip.exe" install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                venv\\Scripts\\pytest
                pytest
                '''
            }
        }
    }
}
