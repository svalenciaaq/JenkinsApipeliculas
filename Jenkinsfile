node {
   stage('Get Source') {
      // copy source code from local file system and test
      // for a Dockerfile to build the Docker image
      git ('https://github.com/svalenciaaq/JenkinsApipeliculas')
      if (!fileExists("Dockerfile")) {
         error('Dockerfile missing.')
      }
   }
   stage('Build Docker') {
       // build the docker image from the source code using the BUILD_ID parameter in image name
         sh "sudo docker build -t apipeliculas ."
   }
   stage("run docker container"){
        sh "docker run --rm -d  -p 8080:5000/tcp apipeliculas"
    }
}
