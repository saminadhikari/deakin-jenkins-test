pipeline {
  agent any
  stages {
    stage("Build" ){
      steps {
        echo "Building ..."
      }
      post {
        success {
          mail to: "saminadhikari20@gmail.com",
          subject: "Build Status Email",
          body: "Build was successful!"
        }
      }
    }
  }
}
