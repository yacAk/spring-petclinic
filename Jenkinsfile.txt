pipeline
{
agent {docker 'maven:3.5-alpine'}
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