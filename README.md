# bacDENOVO-nf
 A genome assemble and annotation pipeline for bacteria

## Quick Start
1. -STEP01:
	-INSTALL NEXTFLOW FOR PIPELINE: 
	```bash
	if [ -d ~/bin ];then
		mkdir -p ~/bin
	fi
	cd ~/bin
	curl -s https://get.nextflow.io | bash  OR INSTALL WITH CONDA : conda install nextflow 
	```
	-ECHO NEXTFLOW TO PATH:
	```bash
	echo 'export PATH=$PATH:~/bin' >> ~/.bashrc
	source  ~/.bashrc
	```
	-This pipeline is based one nextflow DSL2 , so you can run nextflow self-update to update NEXTFLOW to new version

2. -STEP02:
	-DOCKER DEPLOY:
	```bash
	curl -sSL https://get.daocloud.io/docker | sh
	```
	-DOCKER permission:
	```bash
	sudo groupadd -g 999 docker
	sudo gpasswd -a ${USER} docker
	sudo systemctl restart docker
	sudo chmod a+rw /var/run/docker.sock
	```
	-DOCKER TEST
	```bash
	docker ps -a
	```
3. -STEP03:
	-RUN PIPELINE:
	```bash
	nextflow run main.nf --reads 'reads/*.fq.gz'	
	```
	-Tips: When you first install docker and run the process, it will automatically download the required docker image and activate it.

4. -Nextflow is based on java, so please comfirm that java in you PATH