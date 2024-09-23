pipeline
{
    agent any
    stages
    {
        stage('validate')
        {
            steps
            {
                echo "check pom file!"
                sh '''
                    mvn validate
                '''
                
            }
        }
        stage('build')
        {
            steps
            {
                sh '''
                    echo "createting jar"
                    mvn package
                '''
            }
        }
        stage('running')
        {
            steps
            {
                sh '''
                    java -jar target/MavenProject-0.0.3-SNAPSHOT.jar
                '''
            }
        }
        stage('completed')
        {
            steps
            {
                echo "sucess"
            }
        }
    }
}
