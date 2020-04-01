pipeline{
agent any 
stages{
stage('1'){
steps{
checkout([$class: 'GitSCM', 
    branches: [[name: '*/master']], 
    userRemoteConfigs: [[credentialsId: '4c01db90-8e7d-4781-8bc9-1037b2ca887c', url: 'https://github.com/gokugoha/mavenrepo.git']]
])

}
}
stage('build'){
steps{
sh 'mvn package'
}
}
}
}
