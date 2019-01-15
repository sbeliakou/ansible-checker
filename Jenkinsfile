node('host') {
    checkout scm

    stage('SonarQube analysis') {
      // requires SonarQube Scanner 2.8+
      def scannerHome = tool 'SonarQube Scanner v3.3';
      withSonarQubeEnv('sonar.playpit.net') {
        sh "${scannerHome}/bin/sonar-scanner"
      }
    }
}
