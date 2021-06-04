pipeline {
   agent { label "master" }
   stages { 
      stage("build"){
      steps { 
         sh "docker build -t apipeliculas ."
      }
   }
   
   stage("run") { 
      steps { 
         sh "docker run --rm -d  -p 8000:5000/tcp apipeliculas:latest"
      }
   }

   }

}
