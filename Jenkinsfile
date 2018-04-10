pipeline {
  agent {
    node {
      label 'win10'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
      }
    }
    stage('Test') {
      steps {
        echo 'Trying to test this thing'
      }
    }
    stage('anystep') {
      agent any
      steps {
        mail(subject: 'Test', body: 'from any slave', to: 'florian.lobmaier@ams.com')
      }
    }
  }
}