node (){
  //def app
        stage ('Cloning Git') {
             checkout scm
		}
        stage ('Build-and-Tag') {
        sh "echo build-and-tag"
	   // app = docker.build("jvargass2/snake")  
		}
        stage ('Post-to-Dockerhub') {
             sh "echo post-to-dockerhub"
		//docker.withRegistry('https://registry.hub.docker.com', 'DockerHub'){
               // app.push("latest")
		//}
	    }
        stage ('Pull-image-server') {
             sh "echo Pull-image-server"
             //sh "docker-compose down"
            // sh "docker-compose up -d"
	    }
}
