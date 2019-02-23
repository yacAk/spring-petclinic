pipeline
{
agent {docker 'maven:latest'}
stages
{
stage('checkout'){
steps{git 'https://github.com/yacAk/spring-petclinic.git'}

}
stage('compile'){
steps{
sh 'mvn clean package'
junit '**/target/surefire-reports/TEST-*.xml'
}
}

}

}