node {
    stage('Git Checkout') { // for display purposes
     echo 'Checout Code and clone it inside jenkins workspace..'
     git 'https://github.com/manee2k6/DeepriRepo.git'
   }
   stage('Build Test & Package') {
      echo 'Build the package'
      sh 'mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent package sonar:sonar -Dsonar.host.url=https://sonarcloud.io -Dsonar.organization=manee2k6 -Dsonar.login=c1c92712de4e9239e36dc6110383da9ff2d88a40'
   }
   stage('Results') {
       echo 'Test Results are reported..'
   
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
