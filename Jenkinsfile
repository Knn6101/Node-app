pipeline{
        agent any
        environment {
            EC2_USER = 'ubuntu'
            EC2_HOST = '3.108.53.152'
            SSH_CREDENTIAL_ID = 'ec2-ssh-key'
        }

        stages{
                stage("Build") {
                         steps {
                                echo "Start building"
                                sh "npm install"
                                sh "npm run build"
                                echo "Building Completed"
                        }
                }
            stage("Deploy") {
                steps{
                    echo 'Staring Deployment to EC2...'
                    scp -o stricthostkeyChecking=No -r dist/ ubuntu@3.108.53.152:/var/www/html
                    echo "Restarting web server on EC2"
                    ssh -o stricthostkeyChecking=No ubuntu@3.108.53.152 'sudo system1 restart nginx'
                '''
                }
                echo 'Deployment Completed'    
                    }        
                }                 
            }  
}