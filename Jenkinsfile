pipeline { 
    agent { 
        kubernetes {
           //image 'maven:3.6.3-jdk-11' 
           namespace 'jenkins'
        }
    }
    tools {
//        maven 'Maven 3.3.9' jdk 'jdk8'
        
        jdk 'jdk-11' maven 'maven-3.6.3'
    }
    node {
        checkout scm 
	stage('Clone sources') {
             git url: 'https://github.com/davidmachacek/infomer.git'
        }

        stage('Build Maven') {
            sh "mvn clean package"
        }
        /* .. snip .. */
    }
    stages { stage ('Build') { steps {
            //git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                //withMaven {
                sh "mvn clean package"
                //}
            }// withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and 
            }// FindBugs reports
        }
    }
}
