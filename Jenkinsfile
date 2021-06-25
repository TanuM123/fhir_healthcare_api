
    pipeline
{​​​​​​​
    agent any
    stages
    {​​​​​​​
        stage('Build Application')
        {​​​​​​​
            steps
            {​​​​​​​
                bat 'mvn clean install'
            }​​​​​​​
        }​​​​​​​
        stage('SonarQube Quality Check')
        {​​​​​​​
            steps
            {​​​​​​​
                bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=540254bce79d024724070b7c9635860bc306621a'
            }​​​​​​​
        }​​​​​​​
        stage('Deploy Application To Mulesoft Cloudhub')
        {​​​​​​​
            steps
            {​​​​​​​
                bat 'mvn package deploy -DmuleDeploy'
            }​​​​​​​
        }​​​​​​​
        stage('Perform Regression Testing')
        {​​​​​​​
            steps
            {​​​​​​​
                bat 'C:\Users\TMALVIYA\AppData\Roaming\npm\node_modules\newman run C:\\Users\\revishwa\\Documents\\newman\\HealthCare-CloudHub.postman_collection.json --disable-unicode'
            }​​​​​​​
        }​​​​​​​
    }​​​​​​​
}​​​​​​​
