pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
   pipeline {
       agent any

       stages {
           stage('Build') {
               steps {
                   // TODO: Build
                   sh './gradlew assemble'
               }
           }
           stage('Test') {
               steps {
                   // TODO: Test
                   sh './gradlew test'
               }
           }
       }

       post {
           always {
               junit '**/build/test-results/test/*.xml'
               archiveArtifacts artifacts: '**/build/libs/*.jar', allowEmptyArchive: true
           }
       }
   }
}
