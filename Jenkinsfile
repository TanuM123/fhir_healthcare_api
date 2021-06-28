pipeline
{
	agent any
	stages
	{
		stage('Build Application')
		{
			steps
			{
				bat 'mvn clean install'
			}
		}
		stage('SonarQube Quality Check')
		{
			steps
			{
				echo 'hello ,will be implementing on 28 /6/21'
			}
		}
		stage('Deploy Application To Mulesoft Cloudhub')
		{
			steps
			{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		stage('Perform Regression Testing')
		{
			steps
			{
				bat 'C:\\Users\\TMALVIYA\\AppData\\Local\\Postman\\app-8.7.0\\fhir_healthcare_api.postman_collection1.json --disable-unicode'
			}
		}
	}
}