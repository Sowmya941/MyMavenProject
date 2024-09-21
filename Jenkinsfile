pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
            }
        }

        stage('update my this part') 
        {
            steps 
            {
                echo 'Test App'
            }
        }

        stage('Github-webhook-Jenkins') 
        {
            steps 
            {
                echo 'Deploy App'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'sowmyasrisunkara519@gmail.com'
    	}

    }
}
