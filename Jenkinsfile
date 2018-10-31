pipeline {
agent any

stages {
stage ('Compile Stage'){
steps{
echo 'Building'
withMaven(maven : 'maven'){
sh 'mvn clean compile'
      }
   }
}
stage ('Test Stage'){
steps{
withMaven(maven : 'maven'){
sh 'mvn test'
    }
 }
}
stage ('Deplyotment Stage'){
steps{

withMaven(maven : 'maven'){
sh 'mvn deploy'
    }
 }
}


}
}
