pipeline {
    agent any
    
    stages {
        stage('Test') {
            parallel {
                stage('Unit Test') {
                                steps {
                                        echo 'Running the unit test . . .'
                                }
                }
            
                stage('Integration test') {
                                agent {
                                    docker {
                                        reuseNode true
                                        image 'ubuntu'
                                    }
                                }
                                steps {
                                    echo 'Running the integration test . . .'
                                }
            
                }
            }
        }
        
        stage('Functional Test') {
            steps {
                echo 'Functional Test . . .'
            }
        }
    }
    
    
}        
