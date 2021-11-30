pipeline {
  agent any
  stages {
    stage('Git CheckOut') {
      parallel {
        stage('Git CheckOut') {
          steps {
            git(url: 'https://github.com/iomegak12/BlueOcean_Pipeline', branch: 'main')
            echo 'Successfully Checkout from GitHub!!'
          }
        }

        stage('Print Message') {
          steps {
            echo 'Simple Messaging Printing Completed'
          }
        }

      }
    }

    stage('Compile') {
      steps {
        sh 'bash Compile.sh'
        echo 'Compiled Successfully!!'
      }
    }

    stage('Package') {
      steps {
        sh 'bash Package.sh'
        echo 'Packaged Successfully!!'
      }
    }

    stage('Deploy') {
      steps {
        sh 'bash Deploy.sh'
        echo 'Deployed!!'
      }
    }

  }
}
