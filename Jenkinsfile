node('agent1') {
    stage('GetNodeName') {
    def node_name = "${NODE_NAME}"
    echo "The Node Name is: ${node_name}"
    }
}
node('agent1') {
    stage('GetShellName') {
    sh "#!/bin/bash \n" + 
       "echo \"Hello from \$USER\""
    }
}
