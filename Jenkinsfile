pipeline {
    agent any
    stages {
	
	stage('Non-Parallel Stage') {
	    
        steps {
                echo 'This stage will be executed first'
                }
        }

	
        stage('Run Tests') {
            parallel {
                stage('Test On Windows') {
                    
                    steps {
                        echo "Task1 on Agent"
                    }
                    
                }
                stage('Test On Master') {
                   
                    steps {
						echo "Task1 on Master"
					}
                }
            }
        }
    }
}
