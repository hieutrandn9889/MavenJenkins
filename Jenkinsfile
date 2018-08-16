node {
        stage('---check out---') {
            sh "sudo rm -rf MavenJenkins"
            git 'https://github.com/hieutrandn9889/MavenJenkins'
        }
        stage('--test--') {
            def mvnHome = tool name: 'maven 3.5.4', type: 'maven'
            sh "$mvnHome/bin/mvn clean"
            sh "$mvnHome/bin/mvn test" 
            sh "$mvnHome/bin/mvn package"
        }              
}
