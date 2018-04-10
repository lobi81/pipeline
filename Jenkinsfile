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
        stage('Build_Linux') {
          steps {
            node(label: 'linux') {
              echo 'Building on Linux'
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
        stage('Test_Linux') {
          steps {
            node(label: 'linux') {
              echo 'Testing on Linux'
            }
            
          }
        }
      }
    }
  }
}