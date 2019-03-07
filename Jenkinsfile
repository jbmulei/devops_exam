node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t 4193:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'jbmulei' -p 'Academy@2019' "
sh "docker tag 4193:latest jbmulei/4193:latest"
sh "docker push jbmulei/4193:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}