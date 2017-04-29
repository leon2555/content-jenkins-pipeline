pipeline {
  agent any
  stages {
  stage('build') {
    steps {
      sh 'javac -d . src/Rectangle.java'
      sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
      sh 'jar -cvmf MANIFEST.MF rectangle.jar Rectangle.class'
    }
  }
  stage('run') {
    steps {
      sh 'java -jar rectangle.jar 7 9'
    }
  }
 }
}
