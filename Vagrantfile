Vagrant.configure("2") do |config|
  config.vm.box = "dummy"
  
  config.vm.provider :aws do |aws, override|"
    aws.access_key_id = "[acces_key]"
	  aws.secret_access_key = "[secret_key]"
	  
    aws.keypair_name = "[key_pair]"
    aws.region = "ap-southeast-1"
    aws.ami = "ami-6f198a0c"
	aws.instance_type = "t2.micro"

    override.vm.synced_folder '.', '/var', disabled: true
    override.ssh.username = "ubuntu"
    override.ssh.private_key_path = "[path/key_pair.pem]"
	aws.security_groups = [ 'default' ]
  end
 end
