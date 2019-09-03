pipeline {
  agent any
  triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'ref', value: '$.ref']
     ],
     
     causeString: 'Triggered on $ref',
     
     token: 'jfkshfisfsk',
     
     printContributedVariables: true,
     printPostContent: true,
     
     silentResponse: false
    )
  }
  stages {
    stage('Some step') {
      steps {
        echo "Running"
      }
    }
  }
}