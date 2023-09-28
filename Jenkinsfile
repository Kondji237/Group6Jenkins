pipeline{
	agent any 
	stages{
		stage('clonecode'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team7-git-id', url: 'https://github.com/DivineNN/Group6Jenkins.git']])
			}
		}
		stage('Divine-Disc-Management'){
			steps{
				sh 'lsblk'
			}
		}
		stage('Steeve-System-Analysis'){
			steps{
				sh 'ps -ef'
				sh 'sudo systemctl status Jenkins'
			}
		}
		}
	}