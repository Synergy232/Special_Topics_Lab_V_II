//
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/Synergy232/Special_Topics_Lab_V_II.git'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
    echo "Hello"

    withMaven (maven: 'maven3') {
              sh "mvn package"
            }
  }
  //archiveArtifacts artifacts: '**/*.jar', fingerprint: true
  junit 'target/surefire-reports/*.xml'
      }