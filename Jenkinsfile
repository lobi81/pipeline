pipeline {
  agent {
    node {
      label 'win10'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build_Win10') {
          steps {
            node(label: 'win10') {
              echo 'Building on Win10'
            }
            
          }
        }
        stage('Build_Win7') {
          steps {
            node(label: 'win7_pic') {
              echo 'Building on Win7'
            }
            
          }
        }
      }
    }
    stage('Test') {
      parallel {
        stage('Test_Win10') {
          steps {
            node(label: 'win10') {
              echo 'Testing on Win10'
            }
            
          }
        }
        stage('Test_Win7') {
          steps {
            node(label: 'win7_pic') {
              echo 'Testing on Win7'
            }
            
          }
        }
      }
    }
  }
}