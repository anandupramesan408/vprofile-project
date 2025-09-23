pipeline{
    agent any
    tools {
        jdk "JDK17"
        maven "MAVEN3.9"
    }

    environment{
        SNAP-REPO = 'vprofile-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'laKs^2133'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.27.112'
        NEXUSPORT = '8081'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUS-LOGIN = 'nexuslogin'
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