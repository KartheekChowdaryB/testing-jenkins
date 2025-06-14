node('kartheek') {
    stage('GetNodeName') {
    def node_name = "${NODE_NAME}"
    echo "The testing the Node Name is : ${node_name}"
    }
}
node('kartheek') {
    stage('GetShellName') {
    sh "#!/bin/bash \n" + 
       "echo \"Hello from \$USER\""
    }
}
node('kaartheek') {
    stage('git scm') {
    checkout scm
    }
}
node('kartheek') {
    stage('BuildDockerImage') {
    sh "#!/bin/bash \n" + 
       "docker build -t vistannextgenhyd/ros1:testjenkinsv1 ."
    }
}
node('kartheek') {
    stage('PushDockerImage') {
    sh "#!/bin/bash \n" + 
       "docker push vistannextgenhyd/ros1:testjenkinsv1"
    }
}
