node {
   
    stage('Checkout Test 12345') { 
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/trsmca/Test.git']]])
       
    }
      stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+ Test
    def scannerHome = tool 'Sonar Qube';
    withSonarQubeEnv('SonarQube') {
         
           sh "C:/'Program Files (x86)'/Jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/Sonar_Qube/bin/sonar-scanner"
        
      
  } 
}
     stage('Checkout') { 
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/trsmca/slack3.git']]])
       
    }
    stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'Sonar Qube';
    withSonarQubeEnv('SonarQube') {
         
           sh "C:/'Program Files (x86)'/Jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/Sonar_Qube/bin/sonar-scanner"
        
      
  } 
}
}

