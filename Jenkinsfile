pipeline {
  agent {
    label 'maven-jdk8'
  }
  stages {
    stage('Compile Stage') {
      steps {
        echo 'yo me building'
        withMaven(maven: 'maven_3_5_4') {
          sh 'mvn clean compile'
        }

      }
    }
    stage('Testing Stage') {
      steps {
        withMaven(maven: 'maven_3_5_4') {
          sh 'mvn test'
        }

      }
    }
    stage('Packaging Stage') {
      steps {
        withMaven(maven: 'maven_3_5_4') {
          sh 'mvn package'
        }

      }
    }
  }
}