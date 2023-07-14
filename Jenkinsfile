pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/yaoit8791/CNA_TestDemo.git'
      }
    }
    //stage('Build') {
      //steps {
        // Add any build steps if necessary
      //}
    //}
    stage('Deploy') {
      steps {
        sh 'docker-compose up -d' // Assuming you're using Docker for WordPress deployment
      }
    }
    //stage('Setup Database') {
      //steps {
        // Execute any database setup commands, e.g., using WP-CLI
      //}
    //}
  }
}
