node ('Slave1') {
    stage('Checkout') {  
        cleanWs()
        git 'https://github.com/shankrish77/Softmax_Springboot_JenkinsPipeline_MasterSlaves.git'   
    }
    stage('Compile') {
	sh 'mvn compile'
    }
}
node ('Slave2') {
    stage('Checkout') {  
        cleanWs()
        git 'https://github.com/shankrish77/Softmax_Springboot_JenkinsPipeline_MasterSlaves.git'   
    }
    stage('Test') {
	sh 'mvn test'
        junit 'target/surefire-reports/*.xml'
    }
}
