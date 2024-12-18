pipeline {
    agent any 
tools {
        python 'Python 3.x' // Name of the Python tool configured in Global Tool Configuration
    }
    stages {
        stage('Build') { 
            steps {
                bat 'python3 -m py_compile sources/add2vals.py sources/calc.py' 
                stash(name: 'compiled-results', includes: 'sources/*.py*') 
            }
        }
    }
}