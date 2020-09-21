pipeline{
agents any
stages{
stage('Maven Compile'){
steps{ 
echo 'Project Compile stage'
bat label: 'compilation running', script:""mvn compile""
}}

stage('Unit Test'){
steps{ 
echo 'Project Training stage'
bat label: 'Test running', script:""mvn test""
}} 

stage('Maven Package'){
steps{ 
echo 'Project Packaging stage'
bat label: 'project packaging', script:""mvn package""
}}