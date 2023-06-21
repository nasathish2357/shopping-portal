pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs'
    }
    

    stages{
        stage('build'){
            steps{
                echo 'this is the build-the-app job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is the second job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the third job'
                sh 'npm run package'
            }
        }
	stage('archive'){
            steps{
                archiveArtifacts '**/distribution/*.zip'
            }
        }
    }
    
    post{
        always{
            echo 'shopping portal pipeline has completed...'
        }
        
    }
    
}
