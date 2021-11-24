
    pipeline {
        agent any
        parameters {
            $class: checkboxParameter name: 'Applications', format: 'JSON', protocol: 'FILE_PATH', description: '', uri:'//var/lib/jenkins/workspace/custom-checkbox-plugin/public/apps.json' 
            
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