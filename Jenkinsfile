pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			steps {
				sh 'echo "Hellow World"'
				withAWS(credentials:'aws-static') {
    				s3Upload(file:'index.html', bucket:'kentsaiawsstatic', path:'/index.html')
				}
			}
		}
	}
}