pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                echo 'Comple Stage starts...'
				withMaven(maven : Maven_3.5.2)
				 sh 'mvn clean compile'
				echo 'Comple Stage ends...'
            }
        }
        stage('Testing Stage') {
            steps {
                echo 'Testing Stage starts...'
				withMaven(maven : Maven_3.5.2)
				 sh 'mvn test'
				echo 'Testing Stage ends...'
            }
        }
        stage('Deployment Stage') {
            steps {
                echo 'Deploymnet Stage starts...'
				withMaven(maven : Maven_3.5.2)
				 sh 'mvn deploy'
				echo 'Deploymnet Stage ends...'
            }
        }
    }
}