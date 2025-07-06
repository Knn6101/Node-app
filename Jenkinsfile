pipeline{
        stages{
            stage("Build"){
                steps{
                    echo "Start building"
                    sh "npm install"
                    sh "npm run build"
                    echo "Building Completed"
                }
            }
            stage("deploy"){
                steps{
                    echo "Staring deployment on EC2"
                    sh "scp -r -o strictCheckingOfKey=No ./dist/* /home/ubuntu/node-app/"
                    sh "npm start"
                    echo "Deployment done"         
                }                 
            }  
        }