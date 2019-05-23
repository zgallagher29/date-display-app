pipeline{

    stages {
        stage('Build') {
            steps {
                sh '''
                    #!/bin/bash -e

                    # Install dependencies:
                    npm install

                    # Run lint and unit tests:
                    npm run lint
                    npm run test -- --watch false --code-coverage

                    # Run end-to-end tests:
                    npm run e2e
                    # Build artifact
                    npm run build -- --prod
                '''
        
            }
        }
}