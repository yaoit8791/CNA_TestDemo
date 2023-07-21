pipeline {
  agent any
  environment {
    GITHUB_TOKEN = credentials('GHToken')
  }
  stages {
    stage('Checkout') {
      steps {
        sh "git config --global credential.helper '!f() { echo username=$GITHUB_TOKEN; echo password=x-oauth-basic; }; f'"
        sh "git https://github.com/yaoit8791/CNA_TestDemo.git"
      }
    }
    stage('Build') {
      steps {
        //Add any build steps if necessary
        sh "docker-compose -f build_working.yaml build"           
      }
    }
    //stage('Deploy') {
      //steps {
        //sh 'docker-compose up -d' // Assuming you're using Docker for WordPress deployment
      //}
    //}
    //stage('Setup Database') {
      //steps {
        // 12Execute any database setup commands, e.g., using WP-CLI
      //}
    //}
  }
}
