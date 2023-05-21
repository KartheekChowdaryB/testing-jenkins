node('agent1') {
    stage('GetNodeName') {
    def node_name = "${NODE_NAME}"
    echo "The testing Node Name is : ${node_name}"
    }
}
node('agent1') {
    stage('GetShellName') {
    sh "#!/bin/bash \n" + 
       "echo \"Hello from \$USER\""
    }
}
node('agent1') {
    stage('git scm') {
    checkout scm
    }
}
node('agent1') {
    stage('BuildDockerImage') {
    sh "#!/bin/bash \n" + 
       "docker build -t vistannextgenhyd/ros1:testjenkinsv1 ."
    }
}
node('agent1') {
    stage('PushDockerImage') {
    sh "#!/bin/bash \n" + 
       "docker push vistannextgenhyd/ros1:testjenkinsv1"
    }
}
