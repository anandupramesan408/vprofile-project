pipeline{
    agent any
    tools {
        jdk "JDK17"
        maven "MAVEN3.9"
    }

    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'laKs^2133'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.27.112'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages{
        stage('Build job')
        {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}