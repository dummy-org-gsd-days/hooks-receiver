pipeline {
  agent any
  triggers {
    GenericTrigger(
     genericVariables: [
      [key: 'action', value: '$.action'],
      [key: 'merged', value: '$.pull_request.merged'],
      [key: 'created_at', value: '$.pull_request.created_at'],
      [key: 'merged_at', value: '$.pull_request.merged_at']
     ],

     causeString: 'Triggered on $action',

     token: 'SECRET',
     printContributedVariables: true,
     
     regexpFilterText: '$action',
     regexpFilterExpression: 'closed',

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