node ('master'){
  //def app
        stage ('Cloning Git') {
             checkout scm
		}
        stage ('Build-and-Tag') {
        sh "echo build-and-tag"
		    //app = docker.build("")  
		}
        stage ('Post-to-Dockerhub') {
             sh "echo post-to-dockerhub"
             //app.push("latest")
	    }
        stage ('Pull-image-server') {
             sh "echo Pull-image-server"
             //sh "docker-compose down"
            //sh "docker-compose upd -d"
	    }
}
