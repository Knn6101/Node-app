pipeline{
    agent any
        stages{
            stage("Build") {
                steps {
                    echo "Start building"
                    sh "npm install"
                    sh "npm run build"
                    echo "Building Completed"
                }
            }
        
        }                 
    }           
