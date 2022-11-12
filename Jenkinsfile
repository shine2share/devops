pipeline {
  parameters {
    choice(
      name: 'Env',
      choices: ['DEV', 'QA', 'UAT', 'PROD'],
      description: 'Passing the Environment'
    )
    booleanParam(
        defaultValue: true, 
        description: '', 
        name: 'BOOLEAN'
    )
    text(
        defaultValue: '''
        this is a multi-line 
        string parameter example
        ''', 
         name: 'MULTI-LINE-STRING'
    )
    string(
        defaultValue: 'scriptcrunch', 
        name: 'STRING-PARAMETER', 
        trim: true
    )
  }
  node("agen1") {
    stages {
      stage('Environment') {
        steps {
          echo " The environment is ${params.Env}"
        }
      }
      stage('Deploy...') {
        steps {
          echo "hello deploy"
        }
      }
    }
  }
}
