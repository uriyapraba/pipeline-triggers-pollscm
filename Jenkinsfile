pipeline
{
    agent any
    triggers
    {
        pollSCM('* * * * *')
    }
    stages
    {
        stage('Build')
        {
            steps
            {
                checkout scmGit(branches: [[name: 'origin/master']],
                userRemoteConfigs: [
                    [ url: 'https://github.com/uriyapraba/pipeline-triggers-pollscm.git' ]
                ])
            }
        }
    }
}