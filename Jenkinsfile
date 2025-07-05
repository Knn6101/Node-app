pipeline{
    agent any
        stages{
            stage("Build"){
                step{
                    echo "Start building"
                    sh "npm install"
                    sh "npm run build"
                    echo "Building Completed"
                }
            }
        
        }                 
    }           
}