### To build from source	

***As a general rule, Do not lose your password and keystore file. In any case, recovery is impossible.***
***And it doesn't collect any personally identifiable information.***

**Prerequisite**

* [Go lang](https://golang.org/dl/)   
Ubuntu, for instance    
`sudo apt-get install -y build-essential libgmp3-dev golang git curl`		
`curl -O https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz`  
`sudo tar -C /usr/local -xzf go1.6.2.linux-amd64.tar.gz`  
`mkdir -p ~/go; echo "export GOPATH=$HOME/go" >> ~/.bashrc`   
`echo "export PATH=$PATH:$HOME/go/bin:/usr/local/go/bin" >> ~/.bashrc`  
`source ~/.bashrc`  

* [Docker](https://www.docker.com/products/docker#/servers)   
Ubuntu, for instance    
`sudo curl -fsSL https://get.docker.com/ | sh`    
`sudo usermod -aG docker $(whoami)` (might require reboot)  
`docker pull ubuntu:16.04` (16.04 ubuntu version. if 15.04 `docker pull ubuntu:15.04`) 

**build** 
```
cd go-elementrem    
make gele
    //(or, to build the other OS suite of utilities:
make gele-windows
make gele-linux
```

**Run Gele**		
- Windows		
1.Run `gele.exe`    
2.Automatically connects to the Elementrem node : Default directory will be created in the C:\Users\<User Account>\AppData\Roaming\Elementrem	
3.Run `gele attach` from command prompt window(cmd.exe) will be automatically connected to the Elementrem console.	
		<br>
- Linux		
1.Run `gele` from Terminal - If do not copy gele to /usr/bin it must be run ./gele    
2.Automatically connects to the Elementrem node : Default directory will be created in the /home/<User Account>/.elementrem		
3.Run `gele attach` from Terminal will be automatically connected to the Elementrem console.		
		<br>
- Mac OSX	
1.Run `gele` from Terminal - If do not copy gele to /usr/bin it must be run ./gele    
2.Automatically connects to the Elementrem node : Default directory will be created in the /Library/Elementrem		
3.Run `gele attach` from Terminal(launchpad -> Terminal) will be automatically connected to the Elementrem console.	    
		<br>
*Elementrem Network listening port = 30707

