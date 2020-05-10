node {
  stage('SCM') {
    git 'https://github.com/Carlos-cv/maven-hello-world.git'
  }
  stage('Maven Build') {
    sh """
      cd my-app
      mvn compile
    """
  }
  stage('Maven Test') {
    sh """
      cd my-app
      mvn test
    """
  }
  stage('Maven Deploy') {
    sh """
      cd my-app
      java -cp target/classes com.mycompany.app.App
    """
  }
}
