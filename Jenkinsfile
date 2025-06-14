node('laptop') {
    stage('GetNodeName') {
        def node_name = "${NODE_NAME}"
        echo "The testing the Node Name is : ${node_name}"
    }
}

node('laptop') {
    stage('GetShellName') {
        sh "#!/bin/bash \n" + 
           "echo \"Hello from \$USER\""
    }
}

node('laptop') {
    stage('Git SCM') {
        checkout scm
    }
}

node('laptop') {
    stage('BuildDockerImage') {
        sh "#!/bin/bash \n" + 
           "docker build -t testingtoday:v1 ."
    }
}

node('laptop') {
    stage('ApprovalToPush') {
        input message: 'Do you want to push the Docker image?', ok: 'Yes, Push'
    }
}

node('laptop') {
    stage('PushDockerImage') {
        sh "#!/bin/bash \n" + 
           "docker push vistannextgenhyd/ros1:testjenkinsv1"
    }
}
