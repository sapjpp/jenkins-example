pipeline {
  agent {
    label 'maven-jdk8'
  }
  stages {
    stage('Compile Stage') {
      steps {
        echo 'yo me building yo yo yo'
        withMaven(maven: 'maven_3_5_0') {
          sh 'mvn clean compile'
        }

      }
    }
    stage('Testing Stage') {
      steps {
        withMaven(maven: 'maven_3_5_0') {
          sh 'mvn test'
        }

      }
    }
    stage('Packaging Stage') {
      steps {
        withMaven(maven: 'maven_3_5_0') {
          sh 'mvn package'
        }

      }
    }
  }
}
