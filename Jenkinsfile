pipeline {
	agent any 
	stages {
stage(‘Build’) {
	steps {
		sh "rm -rf nginx"
        sh "git clone https://github.com/petejades/nginx.git"
	}
	}
	stage (‘Test’) {
	steps {
		sh "cd nginx && ls"
	}
	}
    stage (‘Package’) {
	steps {
		sh "cd nginx && docker build ."

	}
	}
        stage (‘deploy’) {
	steps {
		sh "cd nginx && docker run -d -p 80:80 nginx:latest "

	}
	}
}
}
