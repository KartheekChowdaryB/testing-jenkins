node('poorna') {
    stage('GetNodeName') {
        def node_name = "${NODE_NAME}"
        echo "The testing the Node Name is : ${node_name}"
    }
}

node('poorna') {
    stage('GetShellName') {
        sh "#!/bin/bash \n" + 
           "echo \"Hello from \$USER\""
    }
}

node('poorna') {
    stage('Git SCM') {
        checkout scm
    }
}

node('poorna') {
    stage('BuildDockerImage') {
        sh "#!/bin/bash \n" + 
           "docker build -t testingtoday:v1 ."
    }
}

node('poorna') {
    stage('ApprovalToPush') {
        input message: 'Do you want to push the Docker image?', ok: 'Yes, Push'
    }
}

node('poorna') {
    stage('PushDockerImage') {
        sh "#!/bin/bash \n" + 
           "docker push vistannextgenhyd/ros1:testjenkinsv1"
    }
}
