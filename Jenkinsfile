node (){
  def app
        stage ('Cloning Git') {
             checkout scm
		}
        stage ('Build-and-Tag') {
        //sh "echo build-and-tag"
	   app = docker.build("jvargass2/snake")  
		}
        stage ('Post-to-Dockerhub') {
             //sh "echo post-to-dockerhub"
		docker.withRegistry('https://registry.hub.docker.com', 'DockerHub'){
                app.push("latest")
		}
	    }
        stage ('Pull-image-server') {
             //sh "echo Pull-image-server"
             sh "/usr/local/bin/docker-compose down"
             sh "/usr/local/bin/docker-compose up -d"
	    }
}
