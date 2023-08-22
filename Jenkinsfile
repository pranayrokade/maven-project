pipeline
{
agent any
stages
{
    stage('scm checkout')
    { steps { git branch: 'master', url: 'https://github.com/pranayrokade/maven-project' }}

    stage('execute unit test freamework')
    {steps {withMaven(globalMavenSettingsConfig: 'd7f5a893-fff6-46f6-9e1a-697c44df13e9', jdk: 'LocalJDK', maven: 'LOCALMVN', mavenSettingsConfig: '0e325b8e-c4eb-4728-928d-9730b7a366ef', traceability: true) 
    {  sh 'mvn test'        //maven test goal 
    }
     }}

     stage ('build the code')
     {steps {withMaven(globalMavenSettingsConfig: 'd7f5a893-fff6-46f6-9e1a-697c44df13e9', jdk: 'LocalJDK', maven: 'LOCALMVN', mavenSettingsConfig: '0e325b8e-c4eb-4728-928d-9730b7a366ef', traceability: true) 
     { sh 'mvn package'
     }
     }}

}

}