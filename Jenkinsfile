node {
    stage('Git Checkout') { // for display purposes
     echo 'Checout Code and clone it inside jenkins workspace..'
     git 'https://github.com/manee2k6/DeepriRepo.git'
   }
   stage('Build Test & Package') {
      echo 'Build the package'
      sh 'mvn clean compile'
   }
   stage('Sonarqube analysis') {
       steps {
    script {
             scannerHome = tool 'SonarScanner';
        }
     withSonarQubeEnv('SonarQube') {
         sh "${scannerHome}/bin/sonar-scanner.bat" 
    }

    }
   
   }
   stage('Deploy to Dev'){
       echo 'Deploy to Dev environment'
   }
   stage('Deploy to Test'){
       echo 'Deploy to Test environment'
   }
      stage('Test Automation'){
       echo 'Deploy to Dev environment'
   }
   
}
