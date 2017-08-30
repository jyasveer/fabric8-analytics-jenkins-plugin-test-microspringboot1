#!groovy

node {
    git url: 'git@github.com:jyasveer/microspringboot1.git'

    sh 'mvn io.github.stackinfo:stackinfo-maven-plugin:0.2:prepare'
    
    def response = bayesianAnalysis url: 'https://recommender.api.openshift.io'
    if (response.success) {
        echo "Results here: ${response.getAnalysisUrl()}"
    }
    echo "${response.content}"
}

