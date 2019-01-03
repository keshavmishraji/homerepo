pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                sh 'ls' 
		sh 'git clone https://github.com/keshavmishraji/homerepo.git'
		sh 'docker build -t keshavmishra12345/pipelineimage:${BUILD_NUMBER} -f Dockerfile .'	
		sh 'docker push keshavmishra12345/pipelineimage:${BUILD_NUMBER}'                 
            }
        }
    }
}
