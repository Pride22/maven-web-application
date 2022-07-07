def call(string stageName) {
    if ("${stageName}" == '2test&build') {
        sh "mvn clean"
        sh "mvn install"
    }    
    else if ("${stageName}" == '3codequalityandanalysis') {
        sh "mvn clean"
        sh "mvn sonar:sonar"
    }    
    else if ("${stageName}" == '4backupartifacts') {
         sh "mvn clean"
         sh "mvn deploy" 
    }   
    else if ("${stageName}" == '5authorisation') {
       timeout(time: 48, unit: 'HOURS') {
                  // some block
                  input message:"approve or decline"
                  } 
    }    
}    
