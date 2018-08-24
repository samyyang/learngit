#! /usr/bin/env groovy
pipline{
	agent any
		stages{
		// 代码检出
		stage('get Code') {
			git credentialsId: '', url: 'https://github.com/samyyang/learngit.git'
		}
		stage('compile') { 
			sh 'mvn clean install' 
		}
		stage('package'){
			sh 'chmod -R 755 CI'
			sh './CI/pacakge.sh'
		}	
	}
}
