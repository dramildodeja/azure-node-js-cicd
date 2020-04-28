# Sample NodeJS application for Azure CI CD

For pipeline yml

- script: |
  npm install
  npm run build
  npm test
 displayName: 'npm install and build'
settings:
- task: PublishTestResults@2
  inputs: 
    testResultsFormat: 'JUnit'
    testResultsFile: '**/TEST.*.xml'
