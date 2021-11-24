
    pipeline {
        agent any
        parameters {
		string(name: "above", description: '')
            $class: checkboxParameter name: 'Applications', format: 'JSON', protocol: 'FILE_PATH', description: '', uri:'/var/lib/jenkins/workspace/custom-checkbox-plugin/apps.json' 
            string(name: "below", description: '')
        }
        stages {
            stage('Applications') {
                steps {
                    sh '''#!/bin/bash
                    touch appname.txt
                    ls 
                    pwd
                    
                    echo "\${Applications}" > appname.txt
                    cat appname.txt
                    cat appname.txt | tr ',' '\n' > app_name.txt
                    cat app_name.txt
                    '''
                }
            }
        }
    }