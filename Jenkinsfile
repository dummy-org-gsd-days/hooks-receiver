pipeline {
  agent any
  triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'ref', value: '$.ref']
     ],
     
     causeString: 'Triggered on $ref',
     
     token: 'aaabbb',
     
     printContributedVariables: true,
     printPostContent: true,
     
     silentResponse: false,
    
     regexpFilterText: '$ref'
    )
  }
  stages {
    stage('Some step') {
      steps {
        sh "echo $ref"
        echo "Success!"
      }
    }
  }
}