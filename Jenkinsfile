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
    stage('GetDockerImage') {
    sh "#!/bin/bash \n" + 
       "docker build -t testing:testjenkinsv2 ."
    }
}
