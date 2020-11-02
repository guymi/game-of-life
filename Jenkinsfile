pipeline {
   agent any


   stages {
      stage('Build') {
         steps {
             
            //sshagent(['git-ssh-key']) {
                // Get some code from a GitHub repository
                git 'https://github.com/guymi/game-of-life.git'
            //}
            

            // Run Maven on a Unix agent.
            sh "echo testing jira"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

         post {
            // If Maven was able to run the tests, even if some of the test
            // failed, record the test results and archive the jar file.
            success {
                echo 'finish success'
                //jiraComment body: "jenkins build #$BUILD_NUMBER", issueKey: 'DOPA-58'
            }
         }
      }
   }
}
