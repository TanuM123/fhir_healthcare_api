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
        }​​​​​​​​​​​​​​
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
                bat 'C:\\Users\\TMALVIYA\\AppData\\Roaming\\npm\\node_modules\\newman run newman run C:\\Users\\TMALVIYA\\AppData\\Local\\Postman\\app-8.7.0\\fhir_healthcare_api.postman_collection.json --disable-unicode'
            }​​​​​​​
        }​​​​​​​
    }​​​​​​​
}
​​​​​​​
