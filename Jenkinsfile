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
				bat 'mvn sonar:sonar -Dsonar.sources=src/ -Dsonar.host.url=http://localhost:9000 -Dsonar.login=e69ffd5c40989de1af3b150424362dae15360aa3'
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