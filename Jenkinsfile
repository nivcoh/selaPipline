pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Publish') {
      steps {
        archiveArtifacts(artifacts: '*.zip', allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true)
      }
    }
  }
}