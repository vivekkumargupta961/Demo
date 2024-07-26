pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git(url: 'https://github.com/vivekkumargupta961/Demo', branch: 'Master', credentialsId: '2f0848f7-8f1c-4452-8cf3-f9618c2115db', poll: true)
      }
    }

    stage('terraform') {
      steps {
        bat(script: 'terraform init', label: 'init')
      }
    }

    stage('deploye') {
      steps {
        bat 'echo "Deploye to prod"'
      }
    }

  }
}