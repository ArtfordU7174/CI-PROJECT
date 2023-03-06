pipeline{
    agent any
    tools {
        maven "mvn3.9"
        jdk "jdk8"
    }
    environment {
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'nexus'
        RELEASE_REPO = 'release-ciproject'
        SNAP_REPO = 'ciproject-snapshot'
        CENTRAL_REPO = 'maven-central-ciproject'
        NEXUS_IP = '172.31.7.203'
        NEXUS_PORT = '8081'
        NEXUS_GROUP_REPO = 'ciproject-group'
        NEXUS_LOGIN = 'nexuslogin'
    }
    stages{
        stage("Build"){
            steps{
                sh 'mvn -s settings.xml install -DskipTests'
            }
        }

    }
}
