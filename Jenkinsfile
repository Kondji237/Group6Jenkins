pipeline{
	agent {
		label 'slave1'
	}
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
		stage('parallel-test'){
		parallel{
		stage('unitest'){
			steps{
				sh 'lscpu'
				sh 'df -h'
			}
		}
		stage('deploy'){
			agent{
				label 'slave2'
			}
			steps{
				echo "we are on pipeline as code module"
			}
		}
			}
		}
		stage('Steeve-System-Analysis'){
			agent{
				label 'slave1'
			}
			steps{
				sh 'ps -ef'
				echo "Happy birthday Sielyma"
			}
		}
	}
}
