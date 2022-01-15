pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    stages {
        
        stage('install dependencies') {
            when {
                branch 'main'
            }

            steps {
                    sh 'npm install'
            }
        }
        
        // stage("Code Quality Check via SonarQube")
        // {
        //     steps {
            
        //     //def sonarScanner(educap_vitrine) {
        //        script {
        //          def scannerHome = tool 'sonarqube-scanner'
    
        //    withSonarQubeEnv("sonarqube-server") {
        //    sh "${scannerHome}/bin/sonar-scanner \
        //         -Dsonar.projectKey=educap_frontend \
        //         -Dsonar.sources=. \
        //         -Dsonar.host.url=https://sonarqube.educap.io \
        //         -Dsonar.login=educap \
        //         -Dsonar.password=educap"
        //        } 
        //    }
        // }
        // }

        stage('build') {

            steps {
                    sh 'npm run build'
            }
        }
    }
}
