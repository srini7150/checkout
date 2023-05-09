pipeline {
    agent any
    
    options {
        skipDefaultCheckout
	//skipDefaultChekout(true)
        buildDiscarder(logRotator(numToKeepStr: '5')) //Decide what builds to discard and what builds to keep
        disableConcurrentBuilds()
        timestamps()
    }

    stages {
        stage('Checkout') {
            steps {
                deleteDir()
                checkout scm
            }
        }
    }
}
