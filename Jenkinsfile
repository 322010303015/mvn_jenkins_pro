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
                bat '''
                    mvn validate
                '''
                
            }
        }
        stage('build')
        {
            steps
            {
                bat '''
                    echo "createting jar"
                    mvn package
                '''
            }
        }
        stage('running')
        {
            steps
            {
                bat '''
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
