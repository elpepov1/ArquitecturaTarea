timestamps {


node () {
    
    def exists = fileExists 'README.md'
	
    
    if(exists){
        echo "YES"
    }
    else{
    stage ('Arqui - Checkout') {
        git credentialsId: 'CREDENTIALS', url: 'https://github.com/elpepov1/ArquitecturaTarea.git'
   }} 
   
   
    stage ('Arqui - Build') {
             // Shell build step
        sh 'ls'
        sh 'pwd'
		sh 'git remote set-url origin https://USERNAME:PASSWORD@github.com/elpepov1/ArquitecturaTarea.git'
        sh 'git add . && git commit -m "commit message"'
    }

    stage ('Arqui - Push'){
        sh 'git config --global user.name "USERNAME" && git config --global user.email "EMAIL"'
        
        sh 'git push origin master'
    }
}
}