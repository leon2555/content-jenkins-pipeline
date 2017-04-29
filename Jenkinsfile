pipeline {
  agent any
  stages {
  stage('build') {
    steps {
      sh 'javac -d . src/Rectangulator.java'
      sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
      sh 'jar -cvmf MANIFEST.MF rectangle.jar Rectangulator.class'
    }
  }
  stage('run') {
    steps {
      sh 'java -jar rectangle.jar 7 9'
    }
  }
 }
}
