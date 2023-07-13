pipeline {
    //   agent{ 
    //     label 'build'
        
    // }
agent any


    stages {

        stage('scm') {
            steps {
                cleanWs()
                 echo 'a'
                determineOS()
                echo 'b'
                // sh 'echo "[Version 1.0.0]" | tee -a changelog.txt'
                sayHello()
                //getServiceVersion('.', 'changelog.txt', 'myservice')
                // cat service.properties
                // sendEmail('failed', 'test@test.com')
                script {
                    def utils = new Utils()
                    if (utils.isWindows()) {
                        echo '<-- Is windwos -->'
                    }
                    else {
                        echo '<-- Is linux -->'
                    }
                }

                 
                //checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                //    userRemoteConfigs: [[url: 'https://github.com/how2coding/react-nodejs-nginx.git']]])


                // checkout([$class: 'GitSCM', 
                // branches: [[name: '*/main']],
                // doGenerateSubmoduleConfigurations: false,
                // extensions: [[$class: 'CleanCheckout']],
                // submoduleCfg: [], 
                // userRemoteConfigs: [[url: 'https://github.com/how2coding/react-nodejs-nginx.git']]])

                // git url: 'https://github.com/how2coding/react-nodejs-nginx.git', branch: 'main'
                // Change file permisson
                //sh "chmod +x -R ./jenkins"
                // Run shell script
                //sh "./jenkins/script/scripted_pipeline_ex_2.sh"

                //sh "cd react-nodejs-nginx"

            }
        }


        stage('build') {
            steps {
             
               sh "echo build"
            }
            
        }
        
        stage('deploy') {
          
            steps {
               sh "echo deploy"
               
            }
            
        }
    }
}
