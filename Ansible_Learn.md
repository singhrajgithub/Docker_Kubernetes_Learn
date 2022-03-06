
# Adhoc Commands 

1) free -m
2) uptime 
3) ansible web_group[group of Inventory] -m ping[ module name]
4) ansible web_group -m shell -a 'free -m'
5) ansible web_group -m shell -a 'uptime'
6) ansible web_group -m shell -a 'yum list installed | grep nginx'
7) ansible webgroup -m sheel -a 'yum list installed | grep perl'
8) ansible-doc -l [list modules] 
9) ansible [group] -m copy -a [src=source_path dest=destination_path]  --> copy file on ansible clients from ansible controller
10) ansible [group] -m copy -a [content=" File content Here" dest="destination_path"] --> complete filename , path has to be defined.
11) ansible 
12) ansible [group] -m yum/apt -a "name=<package name> state=<State>"  --> install package  , Linux= yum module name and apt for unix/debian"
13) ansible web_app -m yum  -a "name=nginx state=present"
14) ansible web_app -m yum -a "name=git state=present" -b [ pass root permission or change the user , it will append sudo by default]
15) ansible web_app -m yum -a "name=git state=latest" -b [ latest package]
  

# Ansible creates .py file that eventually runs on the client machine. 

# User can create Files or Directories on Ansible clients from Ansible Controller using File Module.
1) ansible [group] -m file -a "path=file/dir destination location state=<State>"
2) ansible [group] -m file -a "dest=tmp/test state=touch"
3) ansible [group] -m file -a "dest=tmp/test state=absent mod='0775'"
4) ansible [group] -m file -a "path=destination directory state=directory"  --> create Directory
5) ansible [group] -m file -a "path=destination directory state=absent"

  

  
  
  
  

