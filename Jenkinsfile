pipeline {
agent any

stages {
stage ('Compile Stage'){
steps{
echo 'Building'
withMaven(maven : 'maven_3.5.3'){
sh 'maven clean compile'
      }
   }
}
stage ('Testing Stage'){
steps{
withMaven(maven : 'maven_3.5.3'){
sh 'maven test'
    }
 }
}
stage ('Deplotment Stage'){
steps{

withMaven(maven : 'maven_3.5.3'){
sh 'maven deploy'
    }
 }
}


}
}
